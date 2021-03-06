UEFI Support
============

Introduction
------------

The Unified Extensible Firmware Interface (UEFI) is a specification that
defines the software interface between an OS and platform firmware.
With the UpdateCapsule boot service it can be used to update system firmware.

Build Requirements
------------------

For UEFI capsule support, you need to install fwupdate 0.5 or later.
* source:		https://github.com/rhinstaller/fwupdate
* rpms:			https://pjones.fedorapeople.org/fwupdate/
* debs (Debian):	https://tracker.debian.org/pkg/fwupdate
* debs (Ubuntu):	https://launchpad.net/ubuntu/+source/fwupdate

If you don't want or need this functionality you can use the
`--disable-uefi` option.

UEFI Unlock Support
-------------------

On some Dell systems it is possible to turn on and off UEFI capsule
support from within the BIOS.  This functionality can also be adjusted
from within the OS by fwupd. This requires using fwupdate 5 or later
and compiling it with libsmbios support.

When fwupd and fwupdate have been compiled with this support you will
be able to enable UEFI support on the device by using the `unlock` command.
