# htpdate
Launchd Configuration file to run htpdate as a daemon

If your Mac computer is behind a firewall and you cannot update your time using the default ntpdate you can use htpdate.

Make sure you have [Brew](https://brew.sh) installed.

1. Install htpdate using brew:
```
brew install htpdate
```
2. Put the file ```com.clevervest.htp.htpdate.plist``` into the ```/Library/LaunchDaemons``` directory.
