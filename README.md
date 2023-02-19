# CS421-project1

**Project 1: Automated Eye Tracking Data Correction**<br>
Forked from https://github.com/nalmadi/CS421-project1
Original source: https://github.com/jwcarr/drift 

### Abstract
For project 1, I replicated work from the paper *Carr, Jon W., et al. "Algorithms for the automated correction of vertical drift in eye-tracking data." Behavior Research Methods 54.1 (2022): 287-310.* by generating simulations of 5 different types of errors(noise, slope, shift, within line regression, and between line regression), and then running the 10 novel alrogithms provided in the paper. I was able to analyse these results and get a better understanding of vertical drift in eye-tracking data.

### Results
For each of the 5 errors (noise, slope, shift, within line regression, between line regression) that were discussed in the essay, I ran 10 correction algorithms with on them error magnitude/probability 100 times.

For the noise error, *split*, *warp*, *compare*, and *segment* were consistent across different probabilities of errors, with none of them dropping significantly. The best algorithm was *split* which performed the best with the highest mean accuracy and consistency. *segment* has the lowest mean accuracy.
![Fig 1. Noise error](/results/noise.png "Noise error Results")

For slope errors, the best performances were apparent *segment*, and *warp* were consistent across different probabilities of errors, and *segment* did the best overall. The rest of the algorithms did not perform very well with the slope error with many of them declining in accuracy as the slope becomes more extreme.
![Fig 2. Slope error](/results/slope.png "Slope error Results")

For shift errors, the performance of *cluster*, *merge*, and *segment* are very consistent across different probabilities of errors. Surprisingly, warp is not very accurate when it's shifting upward and quite accurate it's shifting downward. The accuracy for other algorithms declines as the shift becomes more extreme. The *stretch* algorithm had two dips but had a lot of fluctuation across the board. *cluster* performs the best with the highest mean accuracy and consistency and *split* has the lowest mean accuracy.
![Fig 3. Shift error](/results/shift.png "Shift error results")

For within line regression, the performance of all algorithms delinces as the regression becomes more frequent which was interesting. *attach*, *cluster*, *regress*, and *stretch* perform the best with the highest mean accuracy. *compare* has the lowest mean accuracy.
![Fig 4. Within-line regression error](/results/within.png "Fig 4. Within-line regression error")

I did not manage to run the between line regression again the 10 algorithms but you can try this using the 6-BETWEEN-LINE...


### Discussions

Overall, my replication was consistent with the patterns presented in the paper. 

In addition, it is hard to say which algorithm works best because as you could see with different corrections. However, the results I got for *cluster* was not consistent with the paper, the paper described *cluster* as being quite bad but it performed pretty well on the majority of errors.

For two regression errors, the accuracy of all algorithms declines which again is different to that in the paper which may be due to using simulated data and the way the methods were created.

### References
https://github.com/jwcarr/drift
https://github.com/nalmadi/CS421-project1
Carr, Jon W., et al. "Algorithms for the automated correction of vertical drift in eye-tracking data.
