+++
title = "Open man page at switch section"
date = 2022-11-21
[taxonomies]
tags = ["Open man page switch jump to option shell bash"]
authors = ["Sapi", "The sh crew"] 
+++

The shell is my fave pick for automation scripts that maximize compatibility and interoperability. By that I 
mean that the first person to make a toaster run Linux was likely motivated by the ability to interface with it through 
a shell (probably `bash`). You get IEEE Std 1003.1-2008-compliant commands (AKA Unix), software and libraries from all the free-as-in-speech-is-better groups is readily available, and it can run on hardware as old as the 80s (Intel 80486 family). Security amounts to handling 
ssh keys (the only encryption algorithm used by the NSA on the "Top Secret" layer is AES). Yes, Heartbleed was bad but 
the fact that it was discovered independently by Google and Codenomicon (yes, at the same time) tells me 
there are eyes actively scrutinizing the specs/code.

I'm using the `man` command a lot lately (and plan on continuing doing so forever and for the reasons above). So I tried to find an inline way to jump to specific sections when opening a man page. There's a `--pager` but you'll need to pass an argument that looks like this every time: "less -p \"    --switch\" ". So I made a (practically one-liner) script for it. Type manj $NAME_OF_COMMAND -$SWITCH and you're taken to the SWITCH-relevant section of the man page.

### Instructions:

- Download manj file: https://github.com/sapiensmalti/manj/blob/main/manj
- Save it in system's bin folder: `sudo cp ./manj /usr/local/bin`
- Then make it executable: `chmod +x manj`
- Finally, use by appending the command/utility's name to manj (e.g. `manj tcpdump -H`).

You'll find the [source code here](https://github.com/sapiensmalti/manj).
