
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

Confidence intervals are just a percentage of certainty that contain the true mean of the population of numbers. In our case, 2.5% and 97.5%, says we are 2.5% and 97.5% sure a range of values contain the true mean of the entire set of numbers.



## Problem Set 3

**(12) Based on the confidence intervals given below, do you think it likely or unlikely that Lucina is still alive?**

`estimateExtinction(Lucina[,"min_ma"],0.95)`

`Earliest 0.000000`
`Latest -1.221208`
 
At the given confidence interval of 95% and ranges shown above, I would say *Lucina* is still around today because the negative (-) extinction date is best represented by a zero.


**(13) Find the extinction confidence interval for the genus Dallarca. Show your code.**

`Dallarca <- subset(DataPBDB, DataPBDB$genus == "Dallarca")`

`estimateExtinction(Dallarca[,"min_ma"],0.95)`

Earliest - (2.58800)
Latest - (-3.88749)


**(14) A pure reading of the fossil record says that Dallarca went extinct at the end of the Pliocene Epoch. Based on its confidence interval, do you think it is possible that Dallarca is still extant (alive)?**

`estimateExtinction(Dallarca[,"min_ma"],0.95)`
`estimateExtinction(Dallarca[,"min_ma"],0.99)`

The latest age at both confidence intervals above are both negative. As I understand, there can't be a negative interval, so we acknowledge a "0" in lieu of negative values. Given that, it would be interpreted by the data that *Dallarca* is still around today.

**(15) Should we trust confidence intervals and reading?

I think to an extent, yes. Our last example using *Dallarca* suggests an early time of ~2.588 to a late time of ~-3.887. This is telling us that *Dallarca's* latest time is -3.9 million years into the future, at 95% confidence. In layman's, that means in current time. Furthermore, we should not disregard the reading since those represent facts without the application of statistics.PRe

## Problem Set 4

**(16) State one ecological reason why this assumption is unlikey to be true.**

What we learned today: Lazarus, Elvis, and Zombie taxa. The possibilty

**(17) State one geological reason why this assumpiton is unlikely to be true.**


## Problem Set 5

**(18) How many occurrences are in DataPBDB. How many are in ExtantData? How many occurrences were lost by limiting our anaysis to only extant bivalves?**

(18a) 71215
(18b) 62114
(18c) 9101

**(19) How many unique( ) genera were in DataPBDB and ExtantData, respectively. Using this information, what percentage of Cenozoic bivalves in the PBDB are still extant today.**

**(20) Find the stratigraphic range of fossil occurrences for each genus in the ExtantData dataset. If you do not remember how to do this, revisit Problem Set 1 of this lab.**

**(21) Using your answer to question 3, find which genera in ExtantData are not extant according to the PBDB - i.e., do not have a minimum min_age of zero. Show your code.**

**(22) Calculate the confidence interval for the extinction of the following genera (careful with your spelling!): Scrobicularia, Meiocardia, Dimya, Digitaria, Cuspidaria, Arctica, Aloides, Kurtiella, Gouldia, and Acrosterigma. Show your code. What percentage of these taxa have confidence intervals indicating that the taxon might still be extant?**




tapply(DataPBDB[,"max_ma"],DataPBDB[,"genus"],max)
(2)tapply(DataPBDB[,"min_ma"],DataPBDB[,Taxonomy],min)
(3)tapply(DataPBDB[,"min_ma"],DataPBDB[,"genus"],min)
(4)names(which(table(DataPBDB[,"genus"]) == max(table(DataPBDB[,"genus"]))))
or which(DataPBDB[,"genus"]) == max(DataPBDB[,"genus"])))
or max(table(DataPBDB[,"genus"]))

P.Set 2
density(ResampledMeans)
plot(density(ResampledMeans))
mean(ResampledMeans)` has a value of 24.27991. Our original value is 24.30135
sort(ResampledMeans)
quantile(ResampledMeans, c(0.025, .975))
*finds percentile

P.Set 3
estimateExtinction(Lucina[,"min_ma"],0.95)
