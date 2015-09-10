# Introduction #

To download source code for any release, pleas click the 'source' link above, select a tag and click tar.gz or zip


# Details #
Lincity might be already available for your system/distribution.
If you know about a [[Download/Installation#Packages | package]] that is not listed here please add it.
[[wikipedia:Md5sum|Md5sums]] of the official downloads are listed on [[Download/Checksums]] which also contains links to the official files on a protected page.

# Can't open the download? #
Many of our binaries will use 7zor xz compression.  To open these on OSX, use [The Unarchiver](http://wakaba.c3.cx/s/apps/unarchiver); to open these on MS Windows, use [PeaZIP](http://peazip.sourceforge.net/)/[7-ZIP](http://www.7-zip.org/)

# Release 2.0 #

This release introduces water as a new resource. Also it is possible to build bridges across rivers. The file format used to save games changed, data is written to ~/.lincity-ng/ now, but you can still continue old games.

'''Note''': To use the Japanese translation you have to copy or symlink
a font with Japanese characters to fonts/sans-ja\_JP.ttf.

'''Note''':
**If you are using kde or artsd and the game crashs at startup, start the game like this from a console:
> SDL\_AUDIODRIVER=dsp lincity-ng**

# Release 1.1.2 #

Coal reserves below buildings are now visible on mini map. The
range of windmills and coal mines is shown while placing the building.
This release fixes a bug in the solar power plant. It also includes
some updated translations.

# Contributed Packages #

These packages are not provided by the Lincity NG team. So if you have a problem with them, contact the package's maintainer first. Packages/Information about other systems are always appreciated. Please send proposals to lincity-ng-devel@lists.berlios.de or edit this page. '''Not all distributions always ship the latest version.'''

If you build a package for your distribution and discover a problem or even fix something in the process, '''please tell us about it'''. Other people might want that fixed, too and we can only fix stuff we know about. Same goes for bug reports you get via your distribution's bug tracker. Report them to upstream so we know about the problems our users have. Nothing more frustrating than a mail complaining about a problem they filed with their distro months ago but we hear about it the first time.

## Arch Linux ##

lincity-ng is available in the Arch Linux community repository.
  1. pacman -S lincity-ng
Make sure you have enabled the community repository in /etc/pacman.conf.

## Ark Linux ##

Ark Linux packages of lincity-ng 2.0 are available in the normal Ark Linux software repository. Users can simply go to Mission Control -> Install Software, or use
> apt-get update; apt-get install lincity-ng

## Debian Linux ##

Lincity-ng is [officially supported by Debian](http://packages.debian.org/lincity-ng):

> aptitude install lincity-ng

## Fedora Linux ##

For Fedora Core 5 lincity-ng is available in the extras repository

> yum install lincity-ng

## FreeBSD ##

FreeBSD package by Andrej Zverev

> http://www.freshports.org/games/lincity-ng

## Gentoo Linux ##

Gentoo includes a lincity-ng ebuild. Just do the usual

> emerge lincity-ng

## Mac OS ##

### Mac Intel ###

#### 1.1.2 ####

A build of 1.1.2 for Intel Macs has been created by 

&lt;jpenguin&gt;


> http://www.mediafire.com/download.php?tk3mwtyyt5y

#### 1.1.0 ####
You can test this compiled version for Mac OS 10.4.9 Intel
Download it from my web page with the link '''lincity-ng Mac''' in
the left frame :

> http://perso.wanadoo.fr/thierry.maillard

or directly with this link :

> http://perso.orange.fr/thierry.maillard/software/lincity-ng/lincity-ng-1.1.0-macos-10.4.9-i386.dmg.zip

Read installation instruction for X11 on Mac contained in the disk
image.
Send comments to thierry dot maillard50 at wanadoo dot fr.

A SVN build has been compile by 

&lt;jpenguin&gt;



http://www.mediafire.com/?jntyymcttad1.93 SVN [r1461](https://code.google.com/p/lincity-ng/source/detail?r=1461)

### 10.3.9 PPC ###
You can test this compiled version for Mac OS 10.3.9 PPC
Download it from my web page with the link '''Download''':

> http://www.maloninc.com/cgi-bin/fswiki/wiki.cgi?page=Lincity%2DNG+for+MacOS10%2E3%2E9+PPC

or directly with this link:

> http://www.maloninc.com/archive/Lincity-NG-MacOS10.3.9-PPC.dmg.zip

## Mandriva Linux ##

Cooker users can now just do a

> urpmi lincity-ng

It may be soon (or is already) available for stable too.

## PC-BSD ##

PBI package by Gonzalo Martinez - Sanjuan Sanchez

> http://www.pbidir.com/packages.php?code=393

## openSUSE Linux ##

Quentin Denis built rpms for Suse/openSUSE. Thank you.

> http://packman.links2linux.org/?action=626

There is an openSUSE package of lincity-ng 1.1.2 (at least for 11.0-11.2/latest). Source for ng and original are offered.

> http://software.opensuse.org/search?baseproject=openSUSE%3A11.2&p=1&q=lincity-ng

## Ubuntu Linux ##

You'll find some version in the universe repo. Kudos to Moritz Muehlenhoff.

Install the packages lincity-ng and lincity-ng-data with your favourite package manager or use aptitude:
> sudo aptitude install lincity-ng lincity-ng-data

### Latest unofficial version ###

Ubuntu's packages may be outdated, and unofficial but more updated ones are available on GetDeb.net:

> http://www.getdeb.net/app/LinCity-NG

### Deb package ###
BUt, donwload the data and the game.
http://linux.softpedia.com/progDownload/LinCity-NG-Download-2625.html

## Yoper Linux ##

Available from Yoper 3.1 onwards - http://www.yoper.com
> smart install lincity-ng

# Mirrors #

The French gaming site http://jeuxlibres.net has an [article about LinCity-NG](http://jeuxlibres.net/showgame/lincity_ng.html)
which includes a download link to a copy of the '''windows''' version as well as the source code on their server.

On the site of the German magazine http://www.pcwelt.de/ is a short review with download of the '''windows''' version. http://www.pcwelt.de/downloads/entertainment_spiele/spiele/50706/
PCWelt offers the '''source''' code, too. Follow the download link for the Linux version.

# All Releases #

You can find all releases on http://developer.berlios.de/project/showfiles.php?group_id=2929

# Latest development version #
If you want to get the latest sources and compile them see [[and Compilation](Download.md)] and
http://developer.berlios.de/svn/?group_id=2929