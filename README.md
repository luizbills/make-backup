# make-backup
Simple tool to copy folder and move to destination

## Requeriments

I don't know exactly. I tested with `Bash 4.4.19` in a Lubuntu 18.10 (a Ubuntu-based distro).

## Install

```
sudo wget https://raw.githubusercontent.com/luizbills/make-backup/master/make-backup -O /usr/bin/make-backup
sudo chmod +x /usr/bin/make-backup
```

## Usage

Create a cronjob with this command:

```
make-backup ~/your-origin-folder ~/your-dest-folder
```

Notes:

- You can pass a 3rd argument to indicates the max number of backup files inside of `dest-folder` (default is 10).
- Errors are written in `~/make-backup.log`.

## LICENSE

MIT
