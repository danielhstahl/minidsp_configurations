-20 in REW, 100hz - 20000hz sweep for normal speakers, 10-150 for subs, -24 volume in DSP.  

Following https://www.minidsp.com/applications/rew/speaker-time-alignment

L=L
R=R
LFE=Center
SR=SubBack
SL=SubFront
BL=SL
BR=SR

Delay L: 0 (reference)
Delay R: .3 ms
Delay Center (actual Center): -.6475 ms
Delay SL (actual): -2.3968 ms
Delay SR (actual): -1.9335 ms
Delay SubFront: -1.9887 ms
Delay SubBack: -6.6748 ms

Since delays can only be positive, and giving enough "room" for the sub:

Delay L: 10 ms (reference)
Delay R: 10.3 ms
Delay Center: 9.3525 ms
Delay SL: 7.6032
Delay SR: 8.0665

