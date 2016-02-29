# Installing simple #

  * unzip archive to arbitrary directory, cd in this directory
  * ./autogen.sh
  * make install
  * gst-editor


# Installing in custom folder #

  * mkdir /home/username/mylibs  (or whatever you like)
  * unzip archive to arbitrary directory
  * ./autogen.sh --noconfigure
  * ./configure --prefix=/home/username/mylibs
  * make install
  * /home/username/mylibs/bin/gst-editor

# Installing in custom folder with custom gstreamer-installation(without touching existing gstreamer installations) #

mkdir /home/username/mylibs

## Install Gstreamer ##

  * get latest gstreamer-release
  * unpack it

  * until my proposed patch is in the official repositories: apply patch manually
> http://bugzilla.gnome.org/show_bug.cgi?id=527488 (fixes load and save of pipelines)
  * copy latest patch from there into a file named xyz.patch in the gstreamer directory
  * patch -p0 <xyz.patch
  * ./autogen.sh --noconfigure
  * ./configure --prefix=/home/username/mylibs
  * install all missing dependencies:)
  * make install
  * install all missing dependencies:)

## Install Gstreamer-Plugins ##

  * ./autogen.sh --noconfigure
  * PKG\_CONFIG\_PATH=/home/username/mylibs/lib/pkgconfig:$PKG\_CONFIG\_PATH ./configure --prefix=/home/username/mylibs
  * make install

## Install Gst-editor ##

  * ./autogen.sh --noconfigure
  * PKG\_CONFIG\_PATH=/home/username/mylibs/lib/pkgconfig:$PKG\_CONFIG\_PATH ./configure --prefix=/home/username/mylibs
  * make install
  * /home/username/mylibs/bin/gst-editor