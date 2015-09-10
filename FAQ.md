# Introduction #

Add your content here.


# Details #

# Gameplay #

## [[Buildings](Buildings.md)] ##
Why do my Communes keep turning into parks?

> If a Commune is not producing anything for 10 years it is closed and the area turns into a parks
> They will stop producing if they can't deliver their goods because the roads and markets are full.

Is there a reason for disabling a category for a market?

> Eg if you'd like to temporarily stop a factory from producing because you need
> ore elsewhere this makes sure they won't get any workers from the market.

It takes ages to get interesting buildings. How can I increase my tech level?

> Until you discover schools, monuments are the only way to in increase your techlevel.
Monuments, schools, universities, and the city in general all produce tech.

Are different types of transport interconnected?

**No, they are not. But markets can do the transfer between different types.** Yes they are since [r1359](https://code.google.com/p/lincity-ng/source/detail?r=1359) | 2008-01-27 , included in LinCity-NG release 1.91.beta and higher.

## Deaths ##
**What are "Unn deaths"? Answer: Unn deaths are unnatural deaths usually caused by pollution or starvation.  If you are having problems with this, try relocating your residences to areas with less pollution or put in markets, farms, and water towers by your residences.  You can view the starvation map by pressing the MiniMap icon that has a fork and a knife.  To view the pollution MiniMap, click the icon that has smoke going to the right.** Why does my budget all of a sudden go deeply and permanently into the red with 500k or more spent yearly on "deaths", even with no starvation and no shantytowns?

## GUI ##
How can I see what is behind a '''high building'''?

> Press 'h' key or click on the ''Hide high buildings'' icon button (next to ''i'' icon button) to hide buildings.

Where did all my '''money''' go?

> If you did not spend it all on new buildings, then the financial report will tell you. It is the '$' (or your local currency) Tab above the minimap. Click this tab several times to see other reports.

# Development #

Is there anything I can do to help?

> Look at the [TODO](http://code.google.com/p/lincity-ng/source/browse/TODO) or visit us at #lincity on freenode.net.


**Bug Reports are welcome, and patches too :-)**

**People are needed for doing/maintaining translations.**

**Graphics needs some fixes. (See [bug 10457](https://code.google.com/p/lincity-ng/issues/detail?id=0457) in the Bug Tracking System at Berlios)**


# System Specific #

## Translations on MacOS X ##

Download the appropriate launcher from [here](http://www.mediafire.com/?sharekey=65c68a8921ac4aba7069484bded33bcd5761167046e2473c) and put it in the same folder as your game (if LinCity-NG.app is in ./Applications, put the launcher in /Applications)  Then run the launcher each time you want to play the game

Many translations are not complete, [[Translate](Translate.md)]

To see the code the launcher uses, choose the launcher from Automator;s open dialog

## Anything with Small Screen ##

To run Lincity-NG on a device which does not support 1024x768 (like some netbooks) you have to set the resolution manually until [[:bug:15192]] is fixed. To do so, you can start it once giving the right size as command line argument. It will be saved to userconfig.xml.

## Debian ##

When compiling from source I only get a '''black screen''' in OpenGL mode on my '''Nvidia''' card. I use '''Debian'''.

> Install nvidia-glx-dev and compile again.

> apt-get build-dep lincity-ng
> This will install all needed packages to compile lincity-ng
> (because 1.0.3 is already a package in debian and nothing new is needed for 1.1.x :-)

## Windows ##

It works on Windows 98 SE too.

I use '''windows''', why is everything in English? I know there is a '''translation''' for my language.

> You have to set the 'LANG' environment variable. Add something like
> set LANG=nl
> to your autoexec.bat.

> Starting with 1.0.2. Lincity uses a new methode to detect the language.
> If you don't like the automatically detected language either rename
> the translation-files by hand or set LINCITY\_LANG to the desired value.
  1. 0.2 supports ca, de, es, fr, en, nl and sv. See [[Translate](Translate.md)].

Later versions of Windows don't need an autoexec entry: http://support.microsoft.com/kb/310519

On Windows, '''console output''' is written to stdout.txt and stderr.txt, usually in the same directory as lincity-ng.exe.
The .lincity-ng folder containing '''savegames''' and userconfig.xml is in the user's home directory. On XP default installation that is "C:\Documents and Settings\

&lt;username&gt;

\.lincity-ng\".

# Command Line #

What command line arguments does Lincity understand?

> lincity-ng version 1.0.1
> Command line overrides configfiles.
> Known arguments are:
> -v        --version         show version and exit
> -h        --help            show this text and exit
> -g        --gl              use OpenGL
> -s        --sdl             use SDL
> -S        --size [size](size.md)     specify screensize (eg. 1024x768)
> -w        --window          run in window
> -f        --fullscreen      run fullscreen
> -m        --mute            mute audio