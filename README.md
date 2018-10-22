# atrviz
An visualization tool for Atari ATR floppy disk images.

## Requirements
**atrviz** is a bash shell script that calls the ImageMagick **convert** and **montage** tools. Other GNU or Unix tools are used such as awk and tail. Therefore, some Unix-like environment is needed with ImageMagick installed:
 * Linux
 * Mac OSX + homebrew or MacPorts
 * Windows + Cygwin 
 * Windows 10 Subsystem for Linux

## Usage

    $ ./atrviz [-l label] [-s sectors] [-t tracks] [-b bytes] [-v] -f file.atr
    -l: label is quote-enclosed string. Use '\n' for multiple lines.
    -f: file.atr is an Atari floppy disk image.
    -t: number of tracks (default=40)
    -s: number of sectors/track (default=18)
    -b: number of bytes/sector (default=128)
    -v: verbose output
    -h: help (this output)
    Output is file.png

## Example
    $ ./atrviz -l "example.atr\nExample Output of atrviz (2018)\nmd5: $(md5sum example/example.atr)" -f example/example.atr

## Caveats
  * Testing on enhanced and dual-density images has not been done yet.
  * For amusement purposes only.

## Acknowledgements
  * Thanks to Charles Mangin for sharing his Apple II disk visualization process. Information is available at https://web.archive.org/web/20180819020429/http://retroconnector.com/disk-images-edd/
  * Thanks to Kevin Savitz for thinking of and championing the *need* for such a tool.
  * Thanks to Rob McMullin for testing and feedback. 
