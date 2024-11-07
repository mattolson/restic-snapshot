# restic-snapshot

Command line utility to send a snapshot of `$HOME` to offsite storage using [restic](https://restic.net) on an hourly basis.

## Installation

* Copy [./bin/restic-snapshot](./bin/restic-snapshot) to `$HOME/.local/bin`
* Copy [./etc/restic-snapshot.excludes](./etc/restic-snapshot.excludes) to `$HOME/.local/etc`
* Copy [./LaunchAgents/com.mattolson.restic-snapshot.plist](./LaunchAgents/com.mattolson.restic-snapshot.plist) to `$HOME/Library/LaunchAgents` and update values as appropriate for your environment (all the placeholders that start with `$`)
* Run `launchctl load -w ~/Library/LaunchAgents/com.mattolson.restic-snapshot.plist` to install the LaunchAgent
