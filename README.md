# My backup startegy
This set of scripts run regulary and backup a predefined files and directories written in the `backup` and save them to a local directory then upload them to multiple cloud services.
## Requirements
1. GNU/Linux
2. systemd
3. [borg](https://github.com/borgbackup/borg)
4. [rclone](https://github.com/ncw/rclone)

## Notes
* To start/enable a service with a user privilages and
an user enviroment you should run `systemctl` with the `--user` argument.

* To make a systemd service available as a user service it should be located at `/usr/lib/systemd/user/`

## Motivation
Anything that can go wrong will go wrong.