# megasync

I made this script to help me sync files to my personal MEGA cloud storage, but I *think* you can use any remote location. Purpose of this script is to prevent syncing files to MEGA if nothing's changed. This script is using [rclone](https://rclone.org/) to sync files and [checksumdir](https://pypi.org/project/checksumdir/) for checksum.


## Dependencies

- rclone v1.64.2
- checksumdir 1.2.0
