# rosen-ergada-watcher

Some code taken from rosen-bridge/operation watcher module.

This is still WIP, I tested it so far and running a watcher with it, but use at own risk and report any issues.

Copy env var template before editing:

```console
cp env.example .env
```

Same for all the files under config folder copy and remove .example

```console
sudo chown 3000:3000 logs/ada_watcher
sudo chown 3000:3000 logs/erg_watcher
sudo chown 9052:9052 db/erg_node
mkdir db/adapg16
mkdir db/ergpg16
```
