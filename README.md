# Adventure
Pick BASIC port of the famous Adventure game  
https://github.com/MVDBMS-Solutions/Adventure  

## Setup instructions

1. Create a MVDBMS file called ADVENT.BP
1. Copy all files/items from ADVENT.BP into that.
1. Copy the proc ADVENT.SETUP to your account MD/VOC and run it. This will:
    1. create the ADVENT.MASTER file
    1. compile and catalog the game programs
    1. unpack the text data.
    Look for any on-screen errors, just in case. (Please report them)
1. You're done. Type **ADVENTURE** at TCL to get the game menu.

## Notes
1. The code should generally work on any Pick / MultiValue / MVDBMS platform. It's been tested with:
    1. D3
    1. jbase
    1. mvEnterprise
    1. Universe (requires a Pick-flavor account)
1. If you test over Unidata, OpenQM, mvBase, or any other platform, please post a note (see **Contributing** below). You can also post an Issue or comment on Issue #1 which has been opened to check for cross-platform portability.
1. The game takes almost no disk. Only one file (ADVENT.MASTER) is created. Only one MD/VOC item (ADVENTURE) is added besides the catalog program pointers. No other changes to any existing accounts or file are made.
1. If you later want to delete everything without a trace:
   
   ```
   DECATALOG ADVENT.BP * 
   DELETE-FILE ADVENT.BP
   DELETE-FILE ADVENT.MASTER
   DELETE MD ADVENTURE ADVENT.SETUP
   ```
1. Included in the **Reference** folder are two additional programs. These have been separated from ADVENT.BP to avoid confusion with live/required code. :
    1. advent.for : The original Crowther/Woods Fortran source code, on which everything is based; and
    1. ADVENTURES.ORIG : An older version of the main ADVENTURES subroutine, which might be useful in the event some cleanups done so far have inadvertently introduced new problems.
1. If you just need game hints, shame on you... That said - you're welcome to check out our spiffy [wiki](https://github.com/MVDBMS-Solutions/Adventure/wiki)! The wiki also includes links to history notes about the game. If you'd like to contribute tips of your own, please open an Issue/ticket. It would really help if people could contribute notes about exactly how the code works, so that others can follow along and possibly improve upon it.
1. Caveats:
    - NO part of the programs included here should be taken as an example of how to properly code on a Multivalue platform in any way, shape, or form - in fact, the opposite is more likely true.  
    - Remember that this all started as one-off 1970's-era FORTRAN (see the .for file in /Reference), was translated pretty literally into early '80s DATA/BASIC, then passed through possible other hands before it dropped into the hands of David Ruggiero at CDI in 1985. He did do some cleanups, commenting, and streamlining, including translating all the text into proper upper/lower case and encrypting it against prying eyes.  
    - Some hard staring and native MV data structures (dynamic arrays, anyone?) could cut the code size by half or more, but what's here seems _way_ too convoluted and fragile to think about doing that. For now, try just treating it as a black box and not opening the hood too far.  
  1. When you're ready to get your hands dirty, check out the code, post notes for others, post Issues about specific areas that can be improved ... Oh yes, and post code changes! That's how FOSS works! :)

## Contributing

Problems? Questions? Fixes? Please post to the GitHub [Issue](https://github.com/MVDBMS-Solutions/Adventure/issues) Tracker, or to the MVDBMS Google Group:  
https://groups.google.com/forum/#!forum/mvdbms  
... Please use subject format:  `[Adventure] your topic...`