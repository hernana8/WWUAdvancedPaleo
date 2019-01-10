title: PROBLEM SET 1

(1)What class of object is mtcars? What function did you use to find out? class(islands) is `"data.frame"`

(2)Is islands defined as a 1-dimensional array or a vector? How did you find out? Islands is defined as a vector. I used `is(islands, "array")` code that gave a FALSE answer. Also, I used `is.vector(islands)` that gave a TRUE value.

(3)How would you convert the data.frame beaver1 into a matrix? I used the assign operator "<-" to convert between classes, "an()", from beaver 1 data.frame to "matrix". `Beavermatrix<-as(beaver1, "matrix")`

(4)What is the name of the 8th landmass in the islands dataset? How did you find out? I used `islands[8]` or I typed in `islands` and just counted to the eighth landmass.

(5)What function would you use if you wanted to combine all three datasets into a single object? I would use `list()` function. `Thrice<-list(beaver1, islands, mtcars).`

Does islands consist of numeric data? How did you find out? Yes, numeric and character.

Code four different ways to subscript the 2nd row and 7th column of mtcars using bracket notation. (Hint: You are looking to return the number 17.02)

How would you change the landmass values of "Iceland", "Kyushu", and "Tierra del Fuego" to 82, 21, and 10 in the islands dataset? (Hint: You will need to use subscripts and the <- operator).

Are there any times when the beaver in the beaver1 dataset had a temperature lower than 36.30 degrees? How did you find out?

Take the sum of all elements in the column temp in the beaver1 dataset and call this value ValueA. Take the sume of all elements in the row Valiant in the mtcars dataset and call this value ValueB. Take the sum of the first 7 elements of the islands dataset and call this value ValueC. Divide ValueC by ValueB and add ValueA. What is your final answer? Show your code.

2.
