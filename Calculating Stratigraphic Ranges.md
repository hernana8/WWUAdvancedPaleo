
## Problem Set 1

**(1) What do the max_ma and min_ma columns of DataPBDB represent? If you do not intuitively know, you can always check the Paleobiology Database API documentation.**

`max_ma represents the macimum age of the data in millions of years. min_ma is the just the opposite, the minimum age of the data.`



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
