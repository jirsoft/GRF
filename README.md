# GRF
Graphic library for Colour Maximite 2 computer...

### v0.10
Info and loaders for following formats:

General    : JPG, GIF, PNG, BMP

Atari ST   : PI1, PI2, PI3, PC1, PC2, PC3

C64        : DD,HED, KOA, HBM

ZX Spectrum: SCR, BSC


Also can save BMP in 8- and 16-bit colors.




**FUNCTION GRF.info(pg AS INTEGER) AS STRING**
* return MODE, BPP, y-lines, pg address, write address

**SUB GRF.saveBMP(filePath AS STRING, xx AS INTEGER, yy AS INTEGER, ww AS INTEGER, hh AS INTEGER, pp AS INTEGER)**
* save BMP file from screen memory on xx,yy with size of ww,hh from page pp
* it takes bpp from current MODE (so either 8 or 16) = makes BMP smaller than MMBASICs 24bpp

**FUNCTION GRF.getImgInfo(filePath AS STRING) AS STRING**
* return info about graphic file
* WIDTH, HEIGHT, BPP, VERSION

**FUNCTION GRF.loadImg(filePath AS STRING, xx AS INTEGER, yy AS INTEGER, pg AS INTEGER, prog AS INTEGER) AS INTEGER**
* load image to x, y, page
* optional prog will show progress bar
* returns 0 when NOK

**FUNCTION GRF.getC64info(filePath AS STRING) AS STRING**
* get info for some C64 formats

**FUNCTION GRF.loadC64(filePath AS STRING, x AS INTEGER, y AS INTEGER, pg AS INTEGER, prog AS INTEGER) AS INTEGER**
* load some C64 formats to x, y, page
* optional prog will show progress bar
* returns 0 when NOK

**FUNCTION GRF.getCMMcolor(n AS INTEGER) AS INTEGER**
* get color from standard CMM (for sprites)

**FUNCTION GRF.getZXinfo(filePath AS STRING) AS STRING**
* get info for some ZX formats

**FUNCTION GRF.loadZX(filePath AS STRING, x AS INTEGER, y AS INTEGER, pg AS INTEGER, prog AS INTEGER) AS INTEGER**
* load some ZX Spectrum formats to x, y, page
* optional prog will show progress bar
* returns 0 when NOK

**FUNCTION GRF.getSTinfo(filePath AS STRING) AS STRING**
* get info for some Atari ST formats

**FUNCTION GRF.loadST(filePath AS STRING, x AS INTEGER, y AS INTEGER, pg AS INTEGER, prog AS INTEGER) AS INTEGER**
* load some Atari ST formats to x, y, page
* optional prog will show progress bar
* returns 0 when NOK

