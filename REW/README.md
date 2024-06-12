## Documentation of calibration

Objective: appropriate PEQ and time alignment to match Harman curve.  Tools: REW, MSO, MiniDSP HTx.

### Delays by Speaker

This can be done independently of `gains by speaker`.  This uses the time alignment feature in REW to determine the correct delay for each speaker.  Note that the delay for subs is not actually used; it merely offers another complementary data point.  MSO, when doing multi-sub calibration, sets the delays.

### Gains by Speaker

REW can also perform SPL calibration.  The subwoofers were about 5.5 db "louder" than the reference 68 decibals (which was arbitrarily chosen as the "reference").  

### MSO calibration

MSO can, in principal, calibrate any number of speakers as well as subwoofers.  However, given the complexity of measuring and optimizing 7 speakers+subs, I chose to optimize the subwoofers seperately and then allow them to be integrated with the 5 surround speakers as a single "entity" (modeled as one sub).  This also forces me to create my own crossovers rather than allow MSO to give me the crossovers "for free".  Based on previous results/calibrations, 100hz crossover for L, R, SL, SR and 80hz crossover for C has been optimal; however I won't be married to these settings.