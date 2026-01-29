⚠️ This project is obsolete.

**Successor:** https://github.com/larsschenk/ActiveBarcodeCLI


# BarcodeImage

###  Create barcode image files

BarcodeImage.wsf is open source. You can redistribute and/or modify it under the terms of the GNU GPL.

BarcodeImage is a Windows Script file written in VBScript as a wrapper tool for the  ActiveBarcode control &copy; to easily create highly accurate barcode images at the command line. It can be used to create bitmaps and vector graphics. It helps to automate your barcode needs and is versatile in use.

### Usage: BarcodeImage filename [OPTIONS]


| Option                  | Description                | Example
| ----------------------- |:---------------------------| :-------------------------
| -text=                  | text to be encoded         | -text=123456789012
| -type=                  | barcode type               | -type=0
| -width=                 | width in pixels            | -width=500
| -height=                | height in pixels           | -height=500
| -alignment=             | 0=left, 1=center, 2=right  | -alignment=1
| -borderwidth=           | borderwidth in pixels      | -borderwidth=10
| -borderheight=          | borderheight in pixels     | -borderheight=1
| -notchheightinpercent=  | the notch height in %      | -notchheightinpercent=25
| -showtext=              | readable text (on/off)     | -showtext=off
| -forecolor=             | foreground color as RGB    | -foreground=000000 (black)
| -backcolor=             | background color as RGB    | -background=FFFFFF (white)
| -fontname=              | font for the text line     | -fontname=arial
| -fontsize=              | font size for the text line| -fontsize=8
| -fontbold=              | font bold (on/off)         | -fontbold=on
| -fontitalic=            | font italic (on/off)       | -fontitalic=on
| -fontunderline=         | font underline (on/off)    | -fontunderline=on
| -fontstrikeout=         | font strikeout (on/off)    | -fontstrikeout=on
| -filetype=              | file type of image: bmp, jpg, png, tif, tga, gif, wbm, pbm, pgm, ppm, xpm, wmf, emf. Default is **auto detect by extension of filename**. | -filetype=bmp
| -colordepth=            | colordepth of the image file: 1,8,16,24,36 | -colordepth=24
| -flags=                 | flags for the image file   | -flags=0x80
| -angle=                 | rotates the image file, 0-359 | -angle=180
| -transparent=           | background transparency (0, 1) unused | -transparent=1
| -dpi=                   | resolution in DPI for jpg, png, tif & bmp files | -dpi=300
| -echo=                  | off: display no messages, errors: display only errors, verbose: display all messages and open barcode in ImageView | -echo=errors

When giving the option **-text** you can use control characters within pointed brackets:

\<SOH>, \<STX>, \<ETX>, \<EOT>, \<ENQ>, \<ACK>, \<BEL>, \<BS>, \<TAB>, \<LF>,
\<VT>, \<FF>, \<CR>, \<SO>, \<SI>, \<DLE>, \<DC1>, \<DC2>, \<DC3>, \<DC4>, \<NAK>,
\<SYN>, \<ETB>, \<CAN>, \<EM>, \<SUB>, \<ESC>, \<FS>, \<GS>, \<RS>, \<US> and \<DEL>


### Examples

Use cscript when calling from powershell or cmd. The following call of BarcodeImage will create a 400x200 pixels sized PNG image file named ean.png with an EAN-13 barcode encoding "192837465012":

> cscript BarcodeImage.wsf ean.png text=192837465012 typename=ean13 width=400 height=200

This will create a 500x100 pixels sized PNG image file named code128.bmp with an Code 128 barcode encoding "Hello World":
 
> cscript BarcodeImage.wsf code128.bmp "text=Hello World" type=14 width=500 height=100

For a faster, enhanced, universal and more powerful alternative use
[ActiveBarcodeCLI.exe](https://www.activebarcode.com/commandline/) &#128640;


----
BarcodeImage.wsf is free software; you can redistribute it and/or
modify it under the terms of the GNU General Public License
as published by the Free Software Foundation; either version 2
of the License, or any later version.

BarcodeImage.wsf is published on github WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
See the GNU General Public License for more details.

ActiveBarcode &copy; by the ActiveBarcode developers, [www.activebarcode.com](www.activebarcode.com).
