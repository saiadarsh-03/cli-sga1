whoami
- I checked the active user account, and the output showed the current user is codespace.

groups
- I listed the groups for the user and confirmed membership in development and runtime groups.

echo "$SHELL"
- I printed the active login shell to verify the shell environment is Bash.

pwd
- I verified the current working directory and confirmed it is /workspaces/cli-sgal.

ls -ls
- I listed workspace files to confirm the repository contents and file permissions.

curl -s --max-time 10 https://youtube.com > /dev/null && echo "Network: youtube.com reachable"
- I checked network connectivity by testing access to youtube.com and saw that it is reachable.
