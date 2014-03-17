Archlinux-DummyJohn
===================

A dummy package for learning the Package Build, Install and Service features of Arch/Manjaro Linux.

The dummy package to install is dummyjohn from https://github.com/jradxl/dummyjohn
This install package is from https://github.com/jradxl/archlinux-dummyjohn

My /etc/pacman.conf
I have a custom repository entered before any other repositories, thus

[custom]
SigLevel = Never
Server = https://github.com/jradxl/archlinux-dummyjohn/releases/download/v0.1.1/archlinux-dummyjohn-0.1.1.tar.gz

When I run 
    $ sudo pacman -S archlinux-dummyjohn
it will install the package

March 2014
