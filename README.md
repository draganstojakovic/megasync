# megasync

I made this script to help me sync files to my personal MEGA cloud storage, but I *think* you can use any remote location. Purpose of this script is to as the name implies - to sync files and to prevent syncing files to MEGA if nothing's changed with the file structure or the files itself. This script is using [rclone](https://rclone.org/) to sync files and [checksumdir](https://pypi.org/project/checksumdir/) for checksum.


## Dependencies

- rclone v1.64.2
- checksumdir 1.2.0

## Usage

```
Usage: megasync <REMOTE_NAME> <LOCAL_DIRECTORY> <REMOTE_DIRECTORY>

REMOTE_NAME: Name of the configured remote.
LOCAL_DIRECTORY: The directory to verify against the MD5 hash.
REMOTE_DIRECTORY: The designated folder name within your MEGA account.
```

## Note

You might be asking why would you want this overhead if you can simply be aware when you change the files and sync as needed? Because the main point is to automate the process. I setup a cron job to run this script every 30 minutes on my machine, here it is if anyone's interesed:

`*/30 * * * * /home/user/.programs/path/to/megasync <REMOTE_NAME> /home/user/path/to/dir path/to/remote/folder`
