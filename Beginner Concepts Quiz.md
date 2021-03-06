title: PROBLEM SET 1

**(1)What class of object is mtcars? What function did you use to find out?** 

class(islands) is `"data.frame"`

**(2)Is islands defined as a 1-dimensional array or a vector? How did you find out? Islands is defined as a vector.** 

I used `is(islands, "array")` code that gave a FALSE answer. Also, I used `is.vector(islands)` that gave a TRUE value. It is a vector.

**(3)How would you convert the data.frame beaver1 into a matrix?** 

I used the assign operator "<-" to convert between classes, "as()", from beaver 1 data.frame to "matrix". `Beavermatrix<-as(beaver1, "matrix")`

**(4)What is the name of the 8th landmass in the islands dataset? How did you find out?** 

I used `islands[8]` or I typed in `islands` and just counted to the eighth landmass; Borneo.

**(5)What function would you use if you wanted to combine all three datasets into a single object?** 

I would use `list()` function. `Thrice<-list(beaver1, islands, mtcars).`

**(6)Does islands consist of numeric data? How did you find out?** 

Yes, numeric and character. I checked the `class(islands)` and rendered a "numeric" answer. However, when loading the islands data, there are names and numeric values in the data set.

**(7)Code four different ways to subscript the 2nd row and 7th column of mtcars using bracket notation. (Hint: You are looking to return the number 17.02)** 

#1. `mtcars[2,7]` #2. `mtcars[2,"qsec"]` #3. `mtcars[1,"qsec"]+ 0.56` #4. `mtcars["Mazda RX4 Wag", 7]`

**(8)How would you change the landmass values of "Iceland", "Kyushu", and "Tierra del Fuego" to 82, 21, and 10 in the islands dataset? (Hint: You will need to use subscripts and the <- operator).** 

I just set each class(landmass value) to the new given value; `islands["Iceland"]=82 islands["Kyushu"]=21 islands["Tierra del Fuego"]=10`

**(9)Are there any times when the beaver in the beaver1 dataset had a temperature lower than 36.30 degrees? How did you find out?**

No, there are no temperatures lower than 36.30 degrees. I used `range(beaver1["temp"])` that gives me the range of all numbers in `beaver1["temp"]` revealing no numbers below 36.30. Working on question 10 taught me to use `sum(beaver1["temp"]<36.30)` as a much simpler, efficient way.

**(10)Take the sum of all elements in the column temp in the beaver1 dataset and call this value ValueA. Take the sume of all elements in the row Valiant in the mtcars dataset and call this value ValueB. Take the sum of the first 7 elements of the islands dataset and call this value ValueC. Divide ValueC by ValueB and add ValueA. What is your final answer? Show your code.**

First I renamed the sum values to ValueA by `ValueA<-sum(beaver1["temp"])` ValueB, I used a different approach that isn't the ideal way but still proved to work. I first created all the numbers in `mtcars["Valiant"]` into a stand alone vector `Valiant<-c(18.1, 6, 225.0, 105, 2.76, 3.460, 20.22, 1, 0, 3, 1)`, then renamed the sum values as `ValueB<-sum(Valiant)`. 

For ValueC, I added the first seven islands `islands["Africa"]+islands["Antarctica"]+islands["Asia"]+islands["Australia"]+islands["Axel Heiberg"]+islands["Baffin"]+islands["Banks"]` which gave 37185, then vector named that number as ValueC.

Divide and add `(ValueC/ValueB)+ValueA` gave me 4298.739.

