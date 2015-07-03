# Dokku Events Logger

Event logger for [dokku](https://github.com/progrium/dokku)

**The development of this plugin is discontinued as it has been merged into Dokku since v0.3.21**

Record events (i.e. [pluginhook](https://github.com/progrium/pluginhook)'s  calls) as syslog entries and provides a shortcut command to display the last ones.

## Installation

On the Dokku server, install the plugin in the plugins directory and run `dokku plugins-install`:

```
cd /var/lib/dokku/plugins
git clone https://github.com/alessio/dokku-events events
dokku plugins-install
```

## Usage

```
Options:
    events [-t]               Show the last events (-t follows)
    events:list               List the logged events
    events:on                 Enable events logger
    events:off                Disable events logger
```

## Notes

After the installation the plugin needs to be enabled by typing:
```
dokku events:on
```

The plugin outputs the messages to a separate log file too, which is located at `/var/log/dokku.log`.
