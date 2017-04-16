# mediainfo.js

This is a JavaScript port of the excellent [MediaInfoLib](https://mediaarea.net/en/MediaInfo) and meant to be run directly in a browser. mediainfo.js was created using [Emscripten](http://emscripten.org/).

## Demo

Try it out in your browser:  [https://mediainfo.js.org](https://mediainfo.js.org)

## Build

Make sure the
[Emscripten tools](https://kripken.github.io/emscripten-site/docs/getting_started/downloads.html)
can be found in `$PATH`. Something like this will do:

    source ~/programs/emsdk_portable/emsdk_env.sh

Build using:

    npm run build-dist

The resulting files are `dist/mediainfo.js` and `dist/mediainfo.js.mem`.

## Using mediainfo.js

The API is defined in [`mediainfojs.cpp`](https://github.com/buzz/mediainfo.js/blob/master/mediainfojs.cpp) and currently exposes the following methods from [MediaInfoLib::MediaInfo](https://mediaarea.net/en/MediaInfo/Support/SDK/Doxygen/class_media_info_lib_1_1_media_info.html):

* open
* open_buffer_init
* open_buffer_continue
* open_buffer_continue_goto_get
* inform
* close

You can check out [this example](https://github.com/buzz/mediainfo.js/blob/gh-pages/js/mediainfopage.js#L93) on how mediainfo.js is used in the browser.

See [this issue](/../../issues/5) on how to use mediainfo.js with Node.js.

## License

This program is freeware under BSD-2-Clause license conditions:
[https://mediaarea.net/nn/MediaInfo/License](https://mediaarea.net/nn/MediaInfo/License)

This product uses [MediaInfo](http://mediaarea.net/MediaInfo) library, Copyright (c) 2002-2015
[MediaArea.net SARL](mailto:Info@MediaArea.net).
