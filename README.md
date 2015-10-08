Archlinux-DummyJohn
===================

Updated 2015-10-08 to use version 0.1.3, "dummyjohn-0.1.3.tar.gz"
Various fixes and fix messages from a napcap test.


A dummy package for learning the Package Build, Install and Service features of Arch/Manjaro Linux.

The dummy package to install is dummyjohn from https://github.com/jradxl/dummyjohn
This install package is from https://github.com/jradxl/archlinux-dummyjohn

Usage:

Download this package and unpack the tar.gz to some convenient directory in home. 

You can get get the tar.gz from the Release page of github.

cd your directory

execute makepkg

(if you are repeating, then use makepkg -c or makepkg -fc beforehand to clean up)

makepkg may complain about integrity checks.

To update md5 execute updpkgsums, (previously makepkg -g >> PKGBUILD)

makepkg will generate dummyjohn-0.1.3-3-any.pkg.tar.xz

where 0.1.3 is the version, the 3 is the release and the any is the architecture


October 2015
March 2014
