# Adventure
Pick BASIC port of the famous Adventure game

## Setup instructions

1. Unzip the programs/data into a file named ADVENT.BP. (There should be 14 item in all).
1. Copy the proc ADVENT.SETUP to the account MD and run it. This will create the ADVENT.MASTER file, compile and catalog the game programs, and unpack the text data. Look for any on-screen errors, just in case.
1. You're done. Type ADVENTURE at TCL to get the game menu.


## Notes

1. The game should work on any Pick-style system. It's been tested under D3 and mvEnterprise, and on Universe as well (though it almost certainly requires a Pick-flavor account there). Anyone able to try it under jBASE, Unidata, or QM should let me know if there are issues - I'd ideally like to have only one universal package that works for all systems.
1. Less than 300K of disk space is needed for a complete install. Only one file (ADVENT.MASTER) is created, and only one MD item (ADVENTURE)is added besides the catalog program pointsers. No other changes to any existing accounts or file are made. If you later want to delete everything without a trace, just:
   
   ```
   DECATALOG ADVENT.BP *
   DELETE-FILE ADVENT.BP
   DELETE-FILE ADVENT.MASTER
   DELETE MD ADVENTURE  ADVENT.SETUP
   ```

1. Caveat: NO part of the program(s) included here should be taken as an example of how to properly code Pick BASIC in any way, shape, or form - in fact, the opposite is more likely true. Remember that this beastie started as 1970's-era FORTRAN, was translated pretty literally by person or persons unknown into Pick BASIC, then passed through who knows how many other hands before it got to me in 1985, at which point I did some "lipstick on a pig" cleanups and streamlining (including encrypting the text against prying eyes). I'm certain that the code could be cut in half with some hard staring and targeted changes in data structures, but everything there now is _way_ too convoluted and fragile for me to even think about doing that. I'd suggest just treating it as a black box; you don't want to open the hood too far.


Problems? Questions? Fixes? Please post to the GitHub Issue Tracker, or to the MVDBMS Google Group:  
https://github.com/MVDBMS-Solutions/Adventure  
https://groups.google.com/forum/#!forum/mvdbms

(If you just need game hints, shame on you...but Google will get you everything you need and more.)
