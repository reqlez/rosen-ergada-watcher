# rosen-ergada-watcher

Some code taken from rosen-bridge/operation watcher module.

This is still WIP, I tested it so far and running a watcher with it, but use at own risk and report any issues.

WARNING: While I added nginx basic auth support that was not present in original ops repo, note that if you are accessing over http credentails are clear text and if you are on some hotel WIFI accessing your watcher, you are going to get REKT. SSL cert implementation coming, otherwise, just keep it bound to 127.0.0.1 and don't open to world, or make a tunnel.

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
