
*PROBLEM SET 2 (Intermediate)*

### **Section 1 Questions**

## **(1)What does the replace = argument of the sample( ) function do?**
You are replaceing every X value in `c(TRUE,FALSE)`, in sample size 96, with a `TRUE` value.

## **(2)Using as(MyMatrix,"numeric") will not convert MyMatrix to a numeric data! Can you use another property of logicals other than as( ) that will convert the logicals of MyMatrix to 0's and 1's?**
I wrote `MatrixElements["TRUE"]<-0` and `MatrixElements["FALSE"]<-1` but came out funky. So I just re-wrote the given `MatrixElements <- sample(c(0,1), size=96, replace=TRUE)` but placed a 0 in the X and 1 in the Y.


## **(3)If you wanted to check if all the elements in each row are true, how would you do this?** 
I would use `all(MyMatrix[1,]` for row One, `all(MyMatrix[2,]`for Two, and so forth.

## **Section 2 Questions**

## **How many times does the number 7 occur in MyMatrix?**
`MyMatrix[which(MyMatrix==7)]` renders nine values of "7".

## **How do you find the sum of each column?**
`apply(MyMatrix,2,sum)`

## **How do you find the product of each column?**
`apply(MyMatrix,2,prod)`

## **How can you change every instance of the number 1 to 11?**
` MyMatrix[which(MyMatrix==1)]<-11`

## **How many values in MyMatrix are greater than 3 and less than 8?**
`MyMatrix[which(MyMatrix < 8 & MyMatrix > 3)]`

## **How can you change the elements of column 12 into character data, while keeping columns 1-11 as numeric data?**
`MyMatrix[,12]<-"character"`. This however changes all values into character but still holding columns 1-11's data as "characters".

## **Find which rows of MyMatrix have a sum >70. Make a new version of MyMatrix where the 13th column is a set of TRUE and FALSE values denoting which rows have a sum >70. (Hint: What type of object allows you to store both logical and numeric data at once?)**

`which(apply(MyMatrix,1,sum) > 70)` renders which row has a sum >70. `apply(MyMatrix,1,sum)` confirms that. 
