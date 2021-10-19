## Ghidra Server OpenRC Support

This repository provides working modern (supervise-daemon) OpenRC init/conf scripts to run the Ghidra server entirely without incurring YAJSW.

The alternatives, being:
- Still letting YAJSW run (sucky)
- using a whole Docker container just for Ghidra 

are all not too great. Therefore, I initially wrote a pretty hacky shell script that would start the Ghidra server without YAJSW, and then refined it until turning it into the OpenRC initscripts seen here.

## Installing

Clone this repository, then run `# ./install`. (as root, or use sudo)

Edit `/etc/conf.d/ghidra` to favor your configuration, and then.. you're ready!

## Running

```
# rc-service ghidra start
```

## Notes

To use `./svrAdmin`, you will need to update the YAJSW config file to provide the right path to your Ghidra repositories. After that, it should work just like the YAJSW-laden server.
