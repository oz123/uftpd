INSTALLATION
============

uftpd can be built using autotools, using:

$ ./configure
$ make
$ make install


Initial support for meson build system is available if you have meson installed:

 $ meson builddir
 $ cd builddir
 $ ninja

This results in uftpd built in `builddir`.
