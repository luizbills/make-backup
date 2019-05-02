# make-backup

Simple tool to backup a folder to a destination and delete the oldest generated backup files (by default its keep the 10 more recent files).

## Requeriments

I don't know exactly. I tested with `Bash 4.4.19` in a Lubuntu 18.10 (a Ubuntu-based distro).

## Install

```
MAKE_BACKUP=https://raw.githubusercontent.com/luizbills/make-backup/master/make-backup \
&& sudo wget "$MAKE_BACKUP" -O /usr/bin/make-backup \
&& sudo chmod +x /usr/bin/make-backup
```

## Usage

Create a cronjob or just execute this command:

```
make-backup origin-folder destination-folder
```

Notes:

- You can pass a *3rd argument* to indicates the max number of backup files inside of `dest-folder` (default is 10).
- Errors are written in `~/make-backup.log`.
- If you need ignore files, create a file named `.backup-ignore`. This file will be passed in `tar` command as `--exclude-from=.backup-ignore`.

## LICENSE

MIT
