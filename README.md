# Tmux 3.2a as a snap package

Use this if you want to install an updated tmux via snap as the current release (3.2a) is only available in the 
upcoming LTS [Jammy Jellyfish](https://packages.ubuntu.com/search?keywords=tmux&searchon=names&suite=jammy&section=all)

## Install this snap

To create a snap and install the locally built snap: git clone this repo and run:

```shell
   cd tmux-snap
   snapcraft
   sudo snap install tmux_[version].snap --dangerous --classic
```

## This builds against Ubuntu 20.04 (core20)

If initial build fails, check the following:

- a working multipass environment (core20) is needed
- disable any virtualization services, not related to multipass, like VirtualBox

VirtualBox have been known to cause issues. 
On Ubuntu with VirtualBox installed do,

```shell
sudo systemctl stop virtualbox
```

## Resources
* [Snapcraft Docs](https://snapcraft.io/docs)  
* [Official tmux development on OpenBSD CVS](https://cvsweb.openbsd.org/cgi-bin/cvsweb/src/usr.bin/tmux/) this is the primary source repository. This snap pulls
  from the [GitHub](https://github.com/tmux/tmux/releases) repository  
* [tmux mailing list](tmux-users@googlegroups.com)  
* [tmux on GitHub](https://github.com/tmux/tmux/wiki)