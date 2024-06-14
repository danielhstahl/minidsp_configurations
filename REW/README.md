## Documentation of calibration

Objective: appropriate PEQ and time alignment to match Harman curve.  Tools: REW, MSO, MiniDSP HTx.

### Delays by Speaker

This can be done independently of `gains by speaker`.  This uses the time alignment feature in REW to determine the correct delay for each speaker.  Note that the delay for subs is not actually used; it merely offers another complementary data point.  MSO, when doing multi-sub calibration, sets the delays.  I will perform another time alignment for the sub after MSO calibration.

### Gains by Speaker

REW can also perform SPL calibration.  The subwoofers were about 5.5 db "louder" than the reference 68 decibals (which was arbitrarily chosen as the "reference").  When running MSO, the subwoofers appeared quite a bit louder than the 73.5 estimated here; which caused a significant drop in gain.  Note that the gain for subs is not actually used; it merely offers another complementary data point.  MSO calibrated the subs to a 68 "reference" while accomodating the Harman curve, and separate "gains" are not required after applying the relative output gains from the Mso calibration.

### MSO calibration

MSO can, in principal, calibrate any number of speakers as well as subwoofers.  However, given the complexity of measuring and optimizing 7 speakers+subs, I chose to optimize the subwoofers seperately and then allow them to be integrated with the 5 surround speakers as a single "entity" (modeled as one sub).  This also forces me to create my own crossovers rather than allow MSO to give me the crossovers "for free".  Based on previous results/calibrations, 100hz crossover for L, R, SL, SR and 80hz crossover for C has been optimal; however I won't be married to these settings.  Indeed, after running the sweeps I chose 100hz crossovers for all speakers.

### Bass management, gain, delay, and peq

MSO created a "single" sub out of the two that I have.  The relative gains, the peqs, and the relative delay is optimal for it to appear as a single sub for the purposes of the remainder of the calibration.  

* First, update the routing matrix to allow a single input to go to two sub outputs.  
* Second, time align the new "single" sub to the left speaker and set the delays for all outputs
* Third, add bass management so that the 5 satellites cross their bass over to the sub channel
* Run sweeps and choose the appropriate crossovers for each speaker (may need to experiment with crossovers)
* Finally, if the speakers have any dramatic peaks or troughs, consider adding more PEQ to the satellites especially in the 100-300 hz range.