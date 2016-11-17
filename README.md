This repository contains a tftpboot menu file: default.

This file has entries for the following operating systems:

Kali Linux, running in "Live" mode.
CentOS 7 installation, no kickstart entry.
CentOS 6 installation, no kickstart entry.
Linux Mint 18 (XFCE), running in "Live" mode.
Fedora 24 Workstation, running in "Live" mode and using a local installation source.  You will see the default "Try or Install" screen.
Fedora 24 Workstation, running in "Live" mode and using the default Fedora 'mirror' installation list.  You will see the default "Try or Install" screen.
Fedora 24 Server Installation, no kickstart entry.
ESET Resuce CD running in "Live" mode.
CentOS 6 running in "resuce" mode.
CentOS 7 running in "resuce" mode.
SuperGRUB -- mainly to show that I've learned how to boot a floppy based disk image.
Memtest -- because who doesn't have this?



Notes:

The http entries are using port 20000, which I set up on my QNAP server.  This allows me to separate kickstart paths from the default NAS http path.  In a produciton environment, I'd perfer to use a separate VLAN that is only used to create machines.  In a "cloud" enviornment, I'd build a defulat image and use a tool like Ansible to customize the instance.

To add kickstart entries, include a "ks=http://<path>" in the CentOS "append" entries, or an "inst.ks=http://<path>" in the Fedora "append" entries.
