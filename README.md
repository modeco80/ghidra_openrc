## Ghidra Server OpenRC Support

This repository provides working modern (supervise-daemon) OpenRC init/conf scripts to run the Ghidra server entirely without incurring YAJSW.


## Installing

Clone this repository, then run `# ./install`. (as root, or use sudo)

Edit `/etc/conf.d/ghidra` to favor your configuration, and then.. you're ready!

## Running

```
# rc-service ghidra start
```
