This the supported method for building a binary on OSX 10.8+ (it may or may not work with earlier versions)
If you already have a /usr/local/, remove it or manually install the dependencies.

You need xcode to run the distribution script

You will install the command-line utilities in the first step if not already present on your system

Install Homebrew

```
ruby -e "$(curl -fsSkL raw.github.com/mxcl/homebrew/go)"
```

Edit formulas

manually apply the changes is http://pastebin.com/FWMR7Uy7

Install Dependencies

```
brew install pkgconfig; brew install autoconf; brew install automake; brew install libxml2; brew link libxml2; brew install sdl; brew install libogg; brew install libvorbis; brew install webp; brew install mikmod; brew install flac; brew install sdl_mixer --build-from-source; brew install libpng; brew install libjpeg; brew install libtiff; brew install sdl_image --build-from-source; brew install freetype; brew install sdl_gfx; brew install sdl_ttf; brew install physfs; brew install jam; brew install dylibbundler; brew install xz; brew install gnu-tar
```

Restore homebrew

We should revert the changes we had to make to build
```
cd `brew --cellar`
git reset --hard HEAD
```

LINCITY-NG

```
cd lincity-ng/osx/; ./build.sh
```

An .xz file should be in your osx directory, this contains your DMG; if you distribute, please post to the mailing list