# Introduction #

Add your content here.


# Details #
Getting Started

Install developer tools, either from the OS X Install DVD or from Apple's website symlink include folder of OpenGL framework to /usr/local/include/GL (Unix programs have an easier time finding it this way)

> % sudo ln -s /System/Library/Frameworks?/OpenGL.framework/Versions/A/Headers/ /usr/local/include/GL

(you might need to create /usr/local/include/ first if you never built and installed anything from source! sudo mkdir -p /usr/local/include/)

Environment Add /usr/local/bin to your PATH, **before** /usr/bin so that the new versions of stuff you install are picked over the older ones installed by default (this might not be necessary if you don't install autotools below) In a terminal : sudo nano /etc/profile (enter your password as prompted) add the line export PATH=/usr/local/bin:$PATH at the bottom of the file Hit Ctrl+O then press enter to save changes. Hit Ctrl-X to exit. Download pkg-config sources from  http://pkgconfig.freedesktop.org/releases/ and build it:

> % cd /path/to/pkg-config-0.22 % ./configure % make % sudo make install

All the following programs can be built and installed with the following commands on the terminal :

> % cd /path/to/source\_file % ./configure % make % sudo make install

get M4 from  http://ftp.gnu.org/gnu/m4/ and install it symlink m4 to gm4 since that's how some programs refer to it.

> % sudo ln -s /usr/local/bin/m4 /usr/local/bin/gm4

Then, build and install autoconf and automake from GNU the same way as described above  http://www.gnu.org/software/autoconf/  http://www.gnu.org/software/automake/

DYLIBBUNDLER  http://macdylibbundler.sourceforge.net/

LIBXML2

./configure && make && sudo make install

SDL

./configure CC=/usr/bin/gcc CXX=/usr/bin/g++ && make && sudo make install

LIBOGG

./configure && make && sudo make install

LIBVORBIS

./configure && make && sudo make install

LIBMAD

./configure x86\_64-apple-darwin10.6.0 CC=/usr/bin/gcc CXX=/usr/bin/g++ && make && sudo make install

FLAC

./configure x86\_64-apple-darwin10.6.0 && make && sudo make install

MIKMOD #We must us a patched version of libmikmod

cd ~; curl -o libmikmod.tbz dl.dropbox.com/u/3252883/Libs/libmikmod-3.2.0-beta2.tbz -#; tar -xjf libmikmod.tbz; cd ~/libmikmod-3.2.0-beta2; ./configure; make; sudo make install

SDL\_MIXER

./configure -enable-music-mp3-shared=false --enable-music-ogg-shared=false --enable-music-flac-shared=false --enable-music-mod-shared=false --enable-music-mp3-mad-gpl && make && sudo make install

LIB\_PNG

./configure x86\_64-apple-darwin10.6.0 && make && sudo make install

LIB\_JPEG

./configure x86\_64-apple-darwin10.6.0 && make && sudo make install

LIB\_TIFF

./configure x86\_64-apple-darwin10.6.0 --with-apple-opengl-framework && make && sudo make install

SDL\_IMAGE

./configure -enable-jpg-shared=false --enable-png-shared=false --enable-tif-shared=false && make && sudo make install

FREETYPE2

./configure && make && sudo make install

SDL\_TTF

./configure && make && sudo make install

SDL\_GFX

./configure x86\_64-apple-darwin10.6.0 && make && sudo make install

WX\_WIDGETS

../configure --disable-shared --with-cocoa --with-macosx-sdk=/Developer/SDKs/MacOSX10.5.sdk --with-macosx-version-min=10.5 && make && sudo make install

PHYSFS

mkdir cmake-build && cd cmake-build && cmake -DPHYSFS\_BUILD\_WX\_TEST=False .. && make && sudo make install

LINCITY-NG

cd lincity-ng, curl -o make\_mac.tgz dl.dropbox.com/u/3252883/Games/make\_mac.tgz -#; tar zxvf ./make\_mac.tgz; cd make\_mac/; ./build.sh