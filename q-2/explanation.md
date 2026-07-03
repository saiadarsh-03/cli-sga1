mkdir -p secure_workspace/{docs,src,logs}
- I created the secure workspace directory structure with folders for documentation, source, and logs.

touch secure_workspace/docs/plan.txt
- I created the project plan file inside the docs folder.

touch secure_workspace/src/app.txt
- I created the application source placeholder file inside the src folder.

touch secure_workspace/logs/activity.log
- I created the log file placeholder inside the logs folder.

ls -ld secure_workspace secure_workspace/*
- I listed the directory structure and confirmed the folders exist with initial permissions.

chmod 750 secure_workspace
chmod 750 secure_workspace/src
chmod 640 secure_workspace/docs/plan.txt
chmod 640 secure_workspace/src/app.txt
chmod 640 secure_workspace/logs/activity.log
- I applied restrictive permissions to protect the workspace and files from unauthorized access.

ls -ld secure_workspace secure_workspace/*
- I verified the updated permissions on the workspace and child directories.

ls -l secure_workspace/*
- I listed the files to confirm the final file permissions and ownership.

umask
- I checked the default umask value to document how new file permissions are created.
