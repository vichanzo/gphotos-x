# gphotos-x
Backup photos from goolg photos and sync/export to your OneDrive (or other cloud storage)

This are my personal notes on how to backup photos and sync them to my OneDrive the goal is to take those photos from Gphotos and export to any cloud storage compatible with rclone/ rsync.

## Copy the id_rsa file and load this to your github
In pwd console:
```bash
cp ~/.ssh/id_rsa ~
```
Click Editor and open the file.  Copy and paste into git hub.

## Clone this repo
```bash
git clone git@github.com:vichanzo/
```


# gphotos-x
Backup photos from goolg photos and sync/export to your OneDrive (or other cloud storage)

This are my personal notes on how to backup photos and sync them to my OneDrive the goal is to take those photos from Gphotos and export to any cloud storage compatible with rclone/ rsync.

## Generate a new id_rsa file and load this to your github
In pwd console:
```bash
ssh-keygen
# If asked to overwrite existing keys say "yes"
cp ~/.ssh/id_rsa.pub ~
```
Click Editor and open the file.  Copy and paste into git hub.

## Clone this repo
```bash
git clone git@github.com:vichanzo/gphotos-x.git
cd gphotos-x
```

## Set your global commit name and email address, run the git config command with the --global option
```
git config --global user.name "Vichanzo"
git config --global user.email "vichanzo@protonmail.ch"
```

```
python3 -m pip install pipenv
pipenv install gphotos-sync
pipenv run gphotos-sync
```

```
ERROR: Please supply root_folder in which to save photos
[node2] (local) root@192.168.0.7 ~/gphotos-x
$ pipenv run gphotos-sync .
05-05 11:17:36 WARNING  gphotos-sync 3.2.1 2024-05-05 11:17:36.290979
missing or bad secrets file: /root/.config/gphotos-sync/client_secret.json
05-05 11:17:36 ERROR
Process failed.
Traceback (most recent call last):
  File "/root/.local/share/virtualenvs/gphotos-x-a0SaG_Rw/lib/python3.11/site-packages/gphotos_sync/authorize.py", line 50, in __init__
    with secrets_file.open("r") as stream:
         ^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/lib/python3.11/pathlib.py", line 1044, in open
    return io.open(self, mode, buffering, encoding, errors, newline)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
FileNotFoundError: [Errno 2] No such file or directory: '/root/.config/gphotos-sync/client_secret.json'

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "/root/.local/share/virtualenvs/gphotos-x-a0SaG_Rw/lib/python3.11/site-packages/gphotos_sync/__main__.py", line 509, in main
    self.setup(args, db_path)
  File "/root/.local/share/virtualenvs/gphotos-x-a0SaG_Rw/lib/python3.11/site-packages/gphotos_sync/__main__.py", line 346, in setup
    self.auth = Authorize(
                ^^^^^^^^^^
  File "/root/.local/share/virtualenvs/gphotos-x-a0SaG_Rw/lib/python3.11/site-packages/gphotos_sync/authorize.py", line 64, in __init__
    exit(1)
  File "<frozen _sitebuiltins>", line 26, in __call__
SystemExit: 1
05-05 11:17:36 WARNING  Done.
```
