# My backup scripts
This collection of scripts install and run regular backup of predefined files and directories and save them to a local directory then upload them to multiple cloud services.

Contributions and suggestions are always welcomed.
## Requirements
1. GNU/Linux
2. systemd
3. [borg](https://github.com/borgbackup/borg)
4. [rclone](https://github.com/ncw/rclone)
## Usage
```bash
$ git clone https://github.com/nemoload/backup
$ cd backup
$ bash install
```

Add the files and directories names you want to backup  in the `backuprc`, which is located at `$XDG_CONFIG_HOME/.backup`.

By default the backup script uploads the backup files to all the remote backends defined in the current `rclone` configuration. You can specify your own preferred remote backend by editing the `$RCLONE_BACKENDS` in `backup`.
```bash
# RCLONE_BACKENDS="$(rclone config show | grep -E "^\[.+\]" | tr -d '[]')"
RCLONE_BACKENDS=(googledrive dropbox)
```
## Motivation
> Anything that can go wrong will go wrong.
