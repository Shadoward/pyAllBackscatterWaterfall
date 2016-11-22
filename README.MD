![Example with color hill shading](sample.png "Color Shaded Waterfall direct from .all file.")
![Example of gray scale hillshading](sample2.png?raw=true "Gray Shaded Waterfall direct from .all file.")
pyAllBackscatterWaterfall
=====
* created:       November 2016
* by:            p.kennedy@fugro.com
* description:   python module to convert a Kongsberg .all file into a backscatter waterfall PNG.
* notes:         See main at end of script for example how to use this
* based on ALL file version 
* version 1.0
* developed for Python version 3.4 

Done
====
* based on pyallBackscatterWaterfall.py

2Do
===
* initial implementation
* add support for per mean backscatter
* add support for higher resolution seabed image datagram 

Example
-------

python pyallBackscatterwaterfall.py
python pyallBackscatterwaterfall.py -i <filename.all>  
python pyallBackscatterwaterfall.py -i *.all  

help
----
```
C:\development\python>python c:\development\python\pyAllBackscatterWaterfall\pyAllBackscatterWaterfall.py
usage: pyAllBackscatterWaterfall.py [-h] [-i INPUTFILE] [-s SHADESCALE] [-z ZOOM] [-a] [-r] [-gray]

Read Kongsberg ALL file and create a hill shaded color waterfall image.

optional arguments:
  -h, --help     show this help message and exit
  -i INPUTFILE   -i <ALLfilename> : input ALL filename to image. It can also
                 be a wildcard, e.g. *.all
  -s SHADESCALE  -s <value> : Override Automatic Shade scale factor with this
                 value. A smaller number (0.1) provides less shade that a
                 larger number (10) Range is anything. [Default: 0]
  -z ZOOM        -z <value> : Zoom scale factor. A larger number makes a
                 larger image, and a smaller number (0.5) provides a smaller
                 image, e.g -z 2 makes an image twice the native resolution.
                 [Default: 1.0]
  -a             -a : Annotate the image with timestamps. [Default: True]
  -r             -r : Rotate the resulting waterfall so the image reads from
                 left to right instead of bottom to top. [Default is bottom to
                 top]
  -gray          -gray : Apply a gray scale depth palette to the image instead
                 of a color depth. [Default is False]

```