RSS-Bridge supports whitelists in order to limit the available bridges on your web server.

A default whitelist file (`whitelist.default.txt`) is shipped with RSS-Bridge. Please do not edit this file, as it gets replaced when upgrading RSS-Bridge!

You should, however, use this file as template to create your own whitelist (or leave it as is, to keep the default bridges). In order to create your own whitelist perform following actions:

* Copy the file `whitelist.default.txt` in the RSS-Bridge root folder
* Rename the new file to `whitelist.txt`
* Change the lines to satisfy your requirements

RSS-Bridge will automatically detect the `whitelist.txt` and use it. If the file doesn't exist it will default to `whitelist.default.txt` automatically.

# Specific whitelisting

In order to specifically whitelist bridges, open `whitelist.txt` and add one line for each bridge you want to show. Make sure you use normal [line-feeds](https://en.wikipedia.org/wiki/Newline "Line-feed") at the end of a line (LF not [CRLF](https://en.wikipedia.org/wiki/Carriage_return "Carriage-return line-feed")). The bridge name must match the filename of the bridge in the bridges folder (see [folder structure](../04_For_Developers/03_Folder_structure.md)). The name may or may not include the 'Bridge' part.

**Examples**:
```TEXT
FacebookBridge
WikipediaBridge
TwitterBridge
```

or

```TEXT
Facebook
Wikipedia
Twitter
```

# Global whitelisting

In order to globally whitelist all bridges, open the `whitelist.txt` file, remove all contents and just write an asterisk `*` into the file (only this one character).

```TEXT
*
```