# Running htpdate as a daemon on MacOS
Launchd Configuration file to run htpdate as a daemon on MacOS.

If your Mac computer is behind a firewall and you cannot update your time using the default ntpdate you can use htpdate.

Make sure you have [Brew](https://brew.sh) installed.

1. Install htpdate using brew:
```
brew install htpdate
```
2. Put the file ```com.clevervest.htp.htpdate.plist``` into the ```/Library/LaunchDaemons``` directory.
3. Change the ownership of the file to root:wheel
```
chown root:wheel /Library/LaunchDaemons/com.clevervest.htp.htpdate.plist
```
4. Load it with Launchctl
```
launchctl load -w /Library/LaunchDaemons/com.clevervest.htp.htpdate.plist
```

More information on how to use launchctl from [here](http://www.launchd.info/).

This has been tested on MacOS 10.13.15 (High Sierra).
