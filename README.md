# Tmux 3.2a as a snap package

Use this if you want to install an updated tmux via snap on Ubuntu, as the current tmux release (3.2a), is only available in the 
upcoming LTS [Jammy Jellyfish](https://packages.ubuntu.com/search?keywords=tmux&searchon=names&suite=jammy&section=all)

## Install:

To build and install locally:

```shell
   git clone https://github.com/tactinix/tmux-snap
   cd tmux-snap
   snapcraft
   sudo snap install tmux_[version].snap --dangerous --classic
```

## Requirements:

This builds against Ubuntu 20.04 (core20)
- snapcraft snap installed (sudo snap install snapcraft)
- a working multipass environment (core20) is needed
- disable any virtualization services, not related to multipass, like VirtualBox

VirtualBox have been known to cause issues with multipass. 
On Ubuntu with VirtualBox installed do,

```shell
sudo systemctl stop virtualbox
```

## Resources:
* [Snapcraft Docs](https://snapcraft.io/docs)  
* [Official tmux development on OpenBSD CVS](https://cvsweb.openbsd.org/cgi-bin/cvsweb/src/usr.bin/tmux/) this is the primary source repository. This snap pulls
  from the [GitHub](https://github.com/tmux/tmux/releases) repository  
* [tmux mailing list](tmux-users@googlegroups.com)  
* [tmux on GitHub](https://github.com/tmux/tmux/wiki)