script.myepisodecalendar
=================

XBMC plugin for [MyEpisodeCalendar](http://myepisodecalendar.com)

This plugin will set TV show episodes as watched on MyEpisodeCalendar.com.
New shows will also be added to your account if you start watching an episode.

Based on script.myepisodes by Maxime Hadjinlian.

build
=====
If you really want to build it, here is a simple script to do so:
```sh
#!/bin/bash

dest=script.myepisodecalendar
version=$(grep "^\s\+version" addon.xml | cut -f2 -d'"')

if [ -d $dest ]; then
    rm -r $dest
fi

mkdir $dest
cp addon.xml $dest/
cp *.txt $dest/
cp icon.png $dest/
cp *.py $dest/
cp -r resources $dest/

if [ -f $dest-$version.zip ]; then
    rm $dest-$version.zip
fi

zip -r $dest-$version.zip $dest
rm -r $dest
````
It will create a zip file that you can install directly within XBMC.

install
=======

Using the GUI of XBMC, choose to install your plugin as a zip file, find your
zip file, and you're done !

download
========
Get the latest release from the releases tab or download it [here](https://github.com/Connum/script.myepisodecalendar/releases/download/v1.0.2/script.myepisodecalendar-1.0.2.zip) directly.
