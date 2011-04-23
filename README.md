pngtocss takes in a png file with a gradient in it and spits out the necessary CSS to
draw that gradient.

## It only works with:

*  square pngs with two colour gradients (ie, one start and one end)
*  only linear gradients
*  horizontal gradients
*  vertical gradients
*  diagonal gradients

## It does not support:

*  radial gradients
*  angular gradients (except for perfect diagonal)
*  more than 2 colours
*  alpha transparency

## Code

See the examples/ directory for all the pngs that I've tested this with.  Feel free
to submit your own (keep them small).

See the src/ directory for the source code.

It's written in C, and uses libpng and zlib.  You'll need both of those to compile it.
Also, I wrote it on MacOSX, so I installed the libraries using ports.  You may need to
play with the Makefile if you're using a different OS.  Sorry, I don't have the time 
to test, but if you submit a pull request, I'll merge it.

## License:

BSD Licensed

## Copyright:

2011 Philip Tellis -- <philip@bluesmoon.info> -- http://bluesmoon.info/

## History:

Nicole tweeted about [the absence of a tool to convert images to gradients](http://twitter.com/stubbornella/status/61499795801505792/):

![Screenshot of Nicole's tweet](https://img.skitch.com/20110423-dh9axwes4t8d8srfcsw1n774i4.png)

I realised that I knew neither what CSS gradients were, nor how to read a PNG file, so
figured that this was a good opportunity to learn both at once.  I decided to write it
in C because I hadn't written C code in a very long time.

Patches welcome.