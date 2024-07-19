# pys
Repository used to pre-build Python enabled images for popular operating systems

These images are not intended for production, instead they are aimed on
testing Python libraries on multiple platforms.

Inclusions
==========

* pip
* SELinux Python bindings (Red Hat systems)
* GCC
* Git
* Python headers
* OpenSSL headers
* sudo

Use cases
=========

* Testing if your builded wheel can be installed on a specific platform

Customizations
==============

* `/usr/bin/python` symlink is created to point to `python3` where needed. Keep in
mind to use module calling convention for pip, virtualenv and other tools as
this symlink is the only exception made. The idea way to avoid having to detect
python executable when you implement testing.
