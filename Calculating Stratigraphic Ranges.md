
## Problem Set 1

**(1) What do the max_ma and min_ma columns of DataPBDB represent? If you do not intuitively know, you can always check the Paleobiology Database API documentation.**

`max_ma represents the maximum age of the data in millions of years. min_ma is the just the opposite, the minimum age of the data.`



**(2)What is oldest age of each genus? [Hint: Use the tapply( ) and max( ) functions we've used in previous labs]. Show the code you would use to find out.**

`tapply(DataPBDB[,"max_ma"],DataPBDB[,"genus"],max)`


**(3)What is the youngest age of each genus? [Hint: Use the tapply( ) and min( ) functions we've used in previous labs]. Show the code you would use to find out.**

`tapply(DataPBDB[,"min_ma"],DataPBDB[,"genus"],min)`


**(4)Find which genus has the most occurrences in the dataset [Hint: Use the table( ) function!]. What code did you use?**

`names(which(table(DataPBDB[,"genus"]) == max(table(DataPBDB[,"genus"]))))`

`Anadara - 2103`

**(5)What is the stratigraphic range of this taxon (i.e., your answer to question 4). Show your code.**

`Anadara<-DataPBDB[which(DataPBDB[,"genus"]=="Anadara"),]`

`ageRanges(Anadara)`



## Problem Set 2

**(6) Qualitatively describe what is happening in the following lines of code. A good answer should identify what the different arguments are for each function, and what they are used for.**

`> PaleoLng <- na.omit(Lucina$paleolng)`

This is very similar the previous step (Step 1) we conducted where we isolated the paleolat data and omitted the data with missing entries. This line of code though is isolating the paleolongitude data for *Lucina*. We are omitting `na.omit` from our data `Lucina$paleolng` and assigning a new name for result: `PaleoLng`.



`> mean(sample(PaleoLng, length(PaleoLng), replace=TRUE))`

Here, we are finding the mean from a random `sample` from our specified element `PaleoLng` at a specified size `length(PaleoLng)` either with or without replacement `replace=TRUE`. 



**(7) Plot a kernel density graph of ResampledMeans. Show your code. Does the distribution look approximately Gaussian? Explain why you think it does or does not.**

`density(ResampledMeans)`
`plot(density(ResampledMeans))`

![Kernel density graph](https://github.com/hernana8/WWUAdvancedPaleo/blob/master/Kernel.png)

It certainly has a bell-shape to it. Gaussian distribution is the "normal" distribution where data close to the mean are more frequent in occurrence than data away from the mean. We certainly render a representation of that on this kernel graph. 


**(8)Find the mean of ResampledMeans, is it similar to the mean of the original data?**

`mean(ResampledMeans)` has a value of 24.27991. Our original value is 24.30135.


**(9)Sort ResampledMeans from lowest to highest. [Hint: We learned how to sort a vector in Lab 6].**

`sort(ResampledMeans)`


**(10)Now that you have sorted ResampledMeans, what is the 2.5th percentile of ResampledMeans and what is the 97.5th percentile of Resampled means. If you do not know what a percentile is, or how to calculate it, you can use google. Show your code.**

`quantile(ResampledMeans, c(0.025, .975))`

*2.5%    
21.71473* 

*97.5%
26.69090*

**(11)Incidentally, these numbers (your answer to question 5) are the lower and upper confidence interval of the mean! Qualitatively explain why this is the case.**
