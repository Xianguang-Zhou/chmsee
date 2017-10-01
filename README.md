ChmSee is an HTML Help(CHM) viewer for Unix/Linux. It is based on CHMLIB
and use GTK+ as frontend toolkit. Because of using WebKit as HTML
rendering engine, ChmSee can support rich features of modern HTML
page, such as CSS and JavaScript.

Homepage: https://github.com/Xianguang-Zhou/chmsee


Dependencies
============

To compile ChmSee from source you need following packages:
 * g++ >= 5.4.0
 * cmake >= 2.6
 * intltool
 * libgtk2.0-dev >= 2.8
 * libglade2-dev >= 2.4
 * libwebkitgtk-dev >= 1.8.1
 * libchm-dev
 * libgcrypt-dev
 * libxml2-dev
 * libxapian-dev >= 1.2.12
 * libboost-filesystem-dev >= 1.49.0

Installation
============

```shell
git clone https://github.com/Xianguang-Zhou/chmsee.git
cd chmsee
mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE=Release ..
make
sudo make install
```

Dependencies installation for Ubuntu 16.04
==========================================

```shell
sudo apt-get install g++-5 cmake intltool libgtk2.0-dev libglade2-dev \
    libwebkitgtk-dev libchm-dev libgcrypt20-dev libxml2-dev libxapian-dev \
    libboost-filesystem-dev
```

Installation for Ubuntu 16.04
=============================

```shell
git clone https://github.com/Xianguang-Zhou/chmsee.git
mkdir chmsee_release_build
cd chmsee_release_build
CC=gcc-5 CXX=g++-5 cmake -DCMAKE_BUILD_TYPE=Release ../chmsee
make
sudo make install
```

Development for Eclipse 3.7 and Ubuntu 16.04
============================================

```shell
git clone https://github.com/Xianguang-Zhou/chmsee.git
mkdir chmsee_eclipse_build
cd chmsee_eclipse_build
CC=gcc-5 CXX=g++-5 cmake -G "Eclipse CDT4 - Unix Makefiles" \
    -DCMAKE_ECLIPSE_GENERATE_SOURCE_PROJECT=TRUE -DCMAKE_BUILD_TYPE=Debug \
    -DCMAKE_ECLIPSE_VERSION=3.7 ../chmsee
make
```

Report bug
==========

If you find any problem, please file this bug in
https://github.com/Xianguang-Zhou/chmsee/issues, thanks.
