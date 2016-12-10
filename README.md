# missinglink
frontend torrent maker &amp; audio converter utility in python

DEPENDENCIES:

    lame: sudo apt-get install lame or http://lame.sourceforge.net/
    flac toolset: sudo apt-get install flac or 
    http://flac.sourceforge.net/documentation_tools_metaflac.html
    mktorrent: http://mktorrent.sourceforge.net/
    pygtk 2.0 or higher
    twill (optional, needed for log checking, see below) http://darcs.idyll.org/~t/projects/twill-0.9.tar.gz

USE:
    paste your announce URL on the FIRST line of the announce file, then:

     python missinglink.py

    Drag and drop folders of FLAC files in, and use the buttons to make .torrents 
    out of them or convert them to v0, v2, and 320. Transfers tags to .mp3 files 
    and non-music files to the new folders automatically, and creates a .torrent 
    of the converted album afterwards. Supports multiple selecion, so you can 
    select more than one path to remove, make .torrents out of, or convert to a 
    certain format.

    This program can also be used as a tool for making .torrent files of any folder,
    no matter if it is a FLAC album.

    When you convert, the program will look frozen. That, of course, is because it 
    is; but don't freak out, you can watch your conversion status in the terminal 
    window if you run it from terminal.

    To prevent filetypes (for exmaple, .log or .cue) from being trasnferred to the 
    newly-created folders that hold the .mp3 files of the albums you are converting,
    edit the FOURTH line of the announce file to list the file extensions separated
    by commas. For example: m3u, log, cue

LOG CHECKING:
    
    DISREGARD THE INFORMATION BELOW. What.cd new log checker breaks the log-checking
    feature of this program. 
x   Log checking is also possible with the application. First, log out of what.cd
x   from your browser. Then, type your username under your announce URL (on the 
x   SECOND line), and your password under your username (on the THIRD line), save, 
x   and start the program. If you drag in a folder with a log file in it, the 
x   program will log in and grab the score off of http://what.cd/logchecker.php .
x
x   Note: You /need/ twill for this to work.

THANKS:

    shardz - wrote the original whatmp3 PERL script 
    (http://logik.li/projects/whatmp3/), which I ported to python as pywhat
    #python on irc.freenode.net - for your constant, listless, extremely helpful 
    support
    
    original author of frontend - whoever he is, I'm sorry I forgot :c

CHANGELOG:

    09.07.09 - added docstrings, fixed apparent double-slash error, changed icon,
               torrents now private, made list of flac files sort before convert
    09.07.09 - gtk updates between conversions, added notifications, added logchecking
    09.08.09 - fixed tag-scraping issue. Made twill an optional dependency.
    11.16.09 - Added tooltips to buttons
    09.19.10 - added filetype transfer-excluding feature
    09.24.10 - fixed excludetypes error, discovered that log checking feature no longer works
    12.08.16 - changed the requirement of "http://tracker" to just "http://"
    12.09.16 - swapped gtk2 icons for custom icons representing options to encode v0 v2 and 320
