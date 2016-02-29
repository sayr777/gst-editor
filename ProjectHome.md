Finally I found time to put my newest sources online. Sorry for all those g\_prints I left inside.

Version 0.10.3.2:
  * Builds on OSX now! (install deps with macports - quite a lot)
  * small fixes

Version 0.10.3.1:
  * only small bugfix, source may now be deleted after installing

New Version 0.10.3:
  * UI improvements
  * bug fixes
  * autogen.sh not needed for "end users", begin with configure
  * maybe playbins might work (sometimes), they crash not that often with schedtool and singlecore

New Version 0.10.2: only small bugfix release:
  * added NEWS file to fix automake issues
  * now there is support to stop pipeline after a message occurs
  * now you can search elements by name


Any comments welcome!

What works:
  * creating and running pipelines
  * element searching by name
  * saving and loading (with correct places, since GStreamer 0.10.25, earlier versions require [patch](http://bugzilla.gnome.org/show_bug.cgi?id=527488))
  * request-pads
  * capsfilter (typing caps inside UI of elements-properties)
  * Input-/Output-Selector, choosing pad (only basic support, lists all pads, so be careful what you choose)
  * recovery of most actions that priorly caused segfaults

What does not work:
  * Sometimes pads(maybe it works, but causes segfaults)
  * Elements with typefinding, like playbin(graphical glitches, somehow getting out of sync with elements inner state)
  * recovery of all DAU-actions



What was not tested:
  * whether i broke MS-Windows-Compatibility