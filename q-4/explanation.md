echo "sample log line" > app.log
- I created a sample log file for the I/O investigation.

lsof | head -n 20
- I listed open files system-wide to see active file handles.

exec 3<app.log
- I opened app.log on file descriptor 3 to inspect shell open-file behavior.

lsof -p $$ | grep app.log
- I verified the current shell process had app.log open on descriptor 3.

ls -l /proc/$$/fd
- I examined the shell process file descriptor directory to map descriptors to actual files.

ls -l /proc/$$/fd | grep app.log
- I confirmed the file descriptor for app.log in the /proc filesystem.

ls -l > stdout.txt
- I redirected normal command output to stdout.txt.

ls /not_a_real_path 2> stderr.txt
- I redirected error output to stderr.txt for the missing path command.

(ls -l && ls /not_a_real_path) > combined.txt 2>&1
- I captured both standard output and standard error in a single file.

ulimit -a
- I recorded shell resource limits to understand available I/O and process limits.

exec 3<&-
- I closed file descriptor 3 to clean up the open file handle.
