# electrumx-installer
A script to automate the installation of electrumx 🤖

Installing electrumx isn't really straight-forward (yet). You have to install the latest version of Python and various dependencies for
one of the database engines. Then you have to integrate electrumx into your init system.

`electrumx-installer` simplifies this process to running a single command. All that's left to do for you
is to customise the configuration and to start electrumx.

## Usage
This installs electrumx using the default options:

    wget https://raw.githubusercontent.com/malikankit/electrumx-installer/master/bootstrap.sh -O - | bash

You can also set some options if you want more control:

| -d --dbdir | Set database directory (default: /db/)               |
|------------|------------------------------------------------------|
| --update   | Update previously installed version                  |
| --abelian      | Install from HEAD of abelian branch of malikankit/electrumx     |
| --leveldb  | Use LevelDB instead of RocksDB                       |


For example:

    wget https://raw.githubusercontent.com/malikankit/electrumx-installer/master/bootstrap.sh -O - | bash -s - -d /media/ssd/electrum-db

For example: to update existing installation with 'abelian' branch
```
  wget https://raw.githubusercontent.com/malikankit/electrumx-installer/master/bootstrap.sh -O - | bash -s - -d /media/data/electrum-abelian-db --update --abelian
```

Optional : Might need to ```rm -rf ~/.electrumx-installer/``` if it already exists

     
## Credits

Forked from https://github.com/bauerj/electrumx-installer
