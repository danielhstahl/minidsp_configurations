Following https://www.minidsp.com/applications/home-theater-tuning/multi-sub-optimizer-ht-5-3

-10 in REW, 10db-150db sweep, -34 in MiniDSP, no filters in MiniDSP at all.  68 DB "reference".  MLP weight of 1, Left and Right of .5.  

Since I use the Harman curve (which boosts bass by 6db) and since the subwoofers were already 5.5 DB "hot" to the 68 db "reference", I chose not to apply any gain/trim before performing MSO calibration/measurement.

During these sweeps, subwoofers were quite a bit "hotter" than I expected, so gain came down quite a bit to hit the 68 db reference.

I use Config 1 in Project2.  This put a minimum on the size of the PEQs to keep headroom for the subs.  

The subwoofers both have "gains" of -5.09.  In addition, the front subwoofer has an additional -4.21 gain.

The relative Minidsp gains are thus:

* SubFront: -9.30
* SubBack: -5.09

Note, however, that the sub signal has not yet received the required 10db boost (since LFE is mixed 10db low).  So the actual gains are:

* SubFront: .7
* SubBack: 4.91

Since the PEQs only reduce, don't boost, and since the overall volume of the MiniDSP is unlikely to get near clipping, this boost should not induce digital clipping except at extreme volumes.

The SubBack has a delay (relative to SubFront) of 11.78 ms