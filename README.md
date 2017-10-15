ChmSee is an HTML Help(CHM) viewer for Unix/Linux. It is based on CHMLIB
and use GTK+ as frontend toolkit. Because of using WebKit as HTML
rendering engine, ChmSee can support rich features of modern HTML
page, such as CSS and JavaScript.

Homepage: https://github.com/Xianguang-Zhou/chmsee


# Dependencies

To compile ChmSee from source you need following packages:
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

Note: If you are using Ubuntu 16.04, then you need to install g++ compiler 
with a version equal to or higher than "5.0.0".

For Ubuntu 16.04, install dependencies by this command:

```sh
sudo apt-get install g++-5 cmake intltool libgtk2.0-dev libglade2-dev \
    libwebkitgtk-dev libchm-dev libgcrypt20-dev libxml2-dev libxapian-dev \
    libboost-filesystem-dev
```

# Getting source code

```sh
wget -c https://github.com/Xianguang-Zhou/chmsee/archive/master.zip
unzip master.zip
mv chmsee-master chmsee
```

or

```sh
git clone --depth=1 https://github.com/Xianguang-Zhou/chmsee.git
```

or

```sh
git clone https://github.com/Xianguang-Zhou/chmsee.git
```

# Building

## Creating a separate directory for building

```sh
mkdir chmsee_build
cd chmsee_build
```

## Generating Makefile by CMake

```sh
cmake -DCMAKE_BUILD_TYPE=Release ../chmsee
```

For Ubuntu 16.04, generate Makefile by this command:

```sh
CC=gcc-5 CXX=g++-5 cmake -DCMAKE_BUILD_TYPE=Release ../chmsee
```

For Ubuntu 16.04, generate Makefile and Eclipse project files by this command:

```sh
CC=gcc-5 CXX=g++-5 cmake -G "Eclipse CDT4 - Unix Makefiles" \
    -DCMAKE_ECLIPSE_GENERATE_SOURCE_PROJECT=TRUE -DCMAKE_BUILD_TYPE=Debug \
    -DCMAKE_ECLIPSE_VERSION=3.7 ../chmsee
```

## Compiling and Linking

```sh
make
```

# Installation

```sh
sudo make install
```

# Report bug

If you find any problem, please file this bug in
https://github.com/Xianguang-Zhou/chmsee/issues, thanks.
