# Adventure
Pick BASIC port of the famous Adventure game

## Setup instructions

1. Unzip the programs/data into a file named ADVENT.BP. (There should be 14 items in all).
1. Copy the proc ADVENT.SETUP to the account MD and run it. This will:
    1. create the ADVENT.MASTER file
    1. compile and catalog the game programs
    1. unpack the text data.
    Look for any on-screen errors, just in case.
1. You're done. Type ADVENTURE at TCL to get the game menu.


## Notes

1. The game should work on any Pick-style system. It's been tested under D3 and mvEnterprise, and on Universe as well (though it almost certainly requires a Pick-flavor account there).  
More platforms are being tested.  We are striving to have only one universal package that works for all systems.
1. The game takes almost no disk. Only one file (ADVENT.MASTER) is created. Only one MD/VOC item (ADVENTURE) is added besides the catalog program pointers. No other changes to any existing accounts or file are made.
1. If you later want to delete everything without a trace:
   
   ```
   DECATALOG ADVENT.BP *
   DELETE-FILE ADVENT.BP
   DELETE-FILE ADVENT.MASTER
   DELETE MD ADVENTURE ADVENT.SETUP
   ```

1. Caveat: NO part of the program(s) included here should be taken as an example of how to properly code Pick BASIC in any way, shape, or form - in fact, the opposite is more likely true.  
Remember that this beastie started as 1970's-era FORTRAN, was translated pretty literally by person or persons unknown into Pick BASIC, then passed through who knows how many other hands before it got to David Ruggiero in 1985, at which point he did some "lipstick on a pig" cleanups and streamlining (including encrypting the text against prying eyes).  
This could, almost certainly, be cut in half with some hard staring and targeted changes in data structures. But everything there now is _way_ too convoluted and fragile to even think about doing that. For now just treat it as a black box; you don't want to open the hood too far.
1. All that said, if you think improvements can be made ... Please do open an Issue ticket for an enhancement or fix, and if you are inclined, feel free to check out the code and hack out a solution. That's how FOSS works! :)


Problems? Questions? Fixes? Please post to the GitHub Issue Tracker, or to the MVDBMS Google Group:  
https://github.com/MVDBMS-Solutions/Adventure  
https://groups.google.com/forum/#!forum/mvdbms  
... Please use subject format:  `[Adventure] your topic...`

PS: If you just need game hints, shame on you... Google will get you everything you need and more. But if you'd like to contribute tips of your own we will probably have a wiki here soon.
