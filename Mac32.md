#This process is old and unmaintained

# Introduction #

Add your content here.


# Details #

How to build lincity-ng on Mac Os X - 27/9/2007

By Thierry Maillard] with the help of Hiroyuki Nakamura. It has ben edited by jpenguin

This is the older method of compiling, for the currently supported method; see Mac64Compiling

==References== **Source Package?**lincity-ng-1.1.1/README

==Adresses for softwares and packages to download== **Mac OS 10.4.10 Build 8R2232 on Intel or Mac OS 10.3.9 on Power PC Mac**gcc : i686-apple-darwin8-gcc-4.0.1 (GCC) 4.0.1 (Apple Computer, Inc. build 5367) **perforce jam 2.5 : ftp.perforce.com/pub/jam (Mac Developer Kit provide Jam but the version is too low : /Developer/Private?/jam -v -> Jam/MR Version 2.2.1.)**pkg-config-0.22 : pkgconfig.freedesktop.org/wiki/ **libxml2-sources-2.6.30 : xmlsoft.org/**SDL-1.2.12 : www.libsdl.org/ **SDL\_mixer-1.2.8 : www.libsdl.org/projects/SDL\_mixer/**libogg-1.1.3 : www.xiph.org/downloads/ **libvorbis-1.2.0 : www.xiph.org/downloads/**SDL\_image-1.2.6 : www.libsdl.org/projects/SDL\_image/ **libpng-1.2.20 : www.libpng.org/pub/png/libpng.html**jpegsrc.v6b : www.ijg.org/files/ **SDL\_ttf-2.0.9 : www.libsdl.org/projects/SDL\_ttf/**freetype-2.3.5 : www.freetype.org/ : download.savannah.gnu.org/releases/freetype/ **SDL\_gfx-2.0.16 : www.ferzkopp.net/~aschiffler/Software/SDL\_gfx-2.0**cmake-2.4.7-Darwin-universal.dmg : www.cmake.org/ **physfs-1.1.1 : www.icculus.org/physfs/downloads/**wxMac-2.8.5 : www.wxwidgets.org/downloads/ (Avalaible in MacOs? X.4 but to old version) **mac\_bundle from Hiroyuki Nakamura : www.maloninc.com/archive/mac\_bundle.tar.gz**

==Compiling instructions== **It will take you a lot of time to compile all the pachages.**All commands are typed in a Terminal window. **you need root (su) privileges on your Mac for make install operations. This command send built library in /usr/local directory.**To become root in a Terminal window opened in an admin account, type su command. The prompt for root user is #. Be carefull you have all rights and permission on your computer and you can dammage the Operating System. **Root access is locked for common users by Apple, unlock it with utility NetInfo? in /Applications/Utilies?, in menu Security/ Allow root user.**

===X11 libraries installation=== You must have it intalled on Mac : **Insert your Mac OS X Install disc 1**Enter in the /Volumes/Mac? OS X Install Disc 1/System/Installation/Packages folder of your installation disk : (It is hidden in the bottom of the window. Use scrollbar to see the system folder In the Finder Windows). **double-clic on X11User.pkg and follow the instructions.**

===perforce jam 2.5=== <pre> cd jam-2.5 make -> bin.macosxx86/jam or bin.macosxppc/jam according to your machine. </pre>

===pkg-config=== <pre> cd pkg-config-0.22 ./configure make (su) make install make clean </pre>

===libxml=== idem pkg-config

===SDL=== idem pkg-config except for : ./configure --x-includes=/Developer/SDKs/MacOSX10.4u.sdk/usr/X11R6/include --x-libraries=/Developer/SDKs/MacOSX10.4u.sdk/usr/X11R6/lib

===libogg=== idem pkg-config

===libvorbis=== idem pkg-config

===SDL\_mixer=== idem pkg-config except for : ./configure --prefix=/usr/local -enable-music-mp3-shared=false --enable-music-ogg-shared=false --enable-music-mp3-mad-gpl

===libpng=== idem pkg-config

===jpeg=== <pre> cd jpeg-6b ln -s which glibtool ./libtool export MACOSX_DEPLOYMENT_TARGET=10.4 cp /usr/share/libtool/config.sub . cp /usr/share/libtool/config.guess . ./configure --enable-shared --enable-static --x-includes=/Developer/SDKs/MacOSX10.4u.sdk/usr/X11R6/include --x-libraries=/Developer/SDKs/MacOSX10.4u.sdk/usr/X11R6/lib make (su) make install make clean </pre>

===tiff=== idem pkg-config

===SDL\_image=== idem pkg-config except for : ./configure --prefix=/usr/local --enable-jpg-shared=false --enable-png-shared=false --enable-tif-shared=false

===freetype2=== idem pkg-config

===SDL\_ttf=== idem pkg-config except for : ./configure --prefix=/usr/local --with-freetype-exec-prefix=/usr/local/ --x-includes=/Developer/SDKs/MacOSX10.4u.sdk/usr/X11R6/include --x-libraries=/Developer/SDKs/MacOSX10.4u.sdk/usr/X11R6/lib

===SDL\_gfx=== idem pkg-config except for : ./configure --prefix=/usr/local --with-sdl-prefix=/usr/local --x-includes=/Developer/SDKs/MacOSX10.4u.sdk/usr/X11R6/include --x-libraries=/Developer/SDKs/MacOSX10.4u.sdk/usr/X11R6/lib --disable-mmx

===cmake=== double-clic on cmake-2.4.7-Darwin-universal.dmg and follow instructions, don't modify predefined options.

===wxMac=== idem pkg-config

===physfs=== <pre> cd physfs-1.1.1 ccmake . Modify key wxWidgets_CONFIG_EXECUTABLE with the value /usr/local/bin/wx-config in ccmake utility. make (su) make install </pre>

Note: on linux and windows, lincit-ng uses physfs 1.0 because 1.1 causes trouble. :PhysicsFS 1.1 is the unstable developement branch. Don't expect it to be perfect and don't use it for anything but testing.

===lincity-ng=== <pre> cd lincity-ng curl -o mac_bundle.tar.gz www.maloninc.com/archive/mac_bundle.tar.gz -# tar zxvf ./mac_bundle.tar.gz cd mac_bundle/ ./make_for_mac The bundle is available in mac_bundle/lincity-ng.app and can be copied anywhere. </pre>

==Application Packaging== You will now put the application in a disk image .DMG (reference www.wikihow.com/Make-a-DMG-File-on-a-Mac) : # Create a New Folder and place lincity-ng.app, readme, GNU licence files into this new folder # Open Disk Utility (Applications > Utilities > Disk Utility) # Press Command+Shift+N (tthis should open a dialog asking you to select a folder to image) # Choose the new folder you created in the first step # Select compressed from the format pop-up menu # Put the archive on a Web server (www.mediafire.com is good if you don't have a server already) and (Optional) write a page like perso.orange.fr/thierry.maillard/software/lincity-ng/lincity-ng.html to explain your work # Make it known on Lincity Wiki : Download/Installation?.

Congratulation, it was very hard, but you have done it ;-)

Please let me know your remarks and problems on the discussion page