
## Problem Set 1

**(1) How many genera are in the Miocene, Early Jurassic, Late Cretaceous, and Pennsylvanian epochs (not total, but in each epoch)? What code did you use to find out?**

`apply(PresencePBDB,1,sum)` 

There are Miocene-653, Early Jurassic-177, Late Cretaceous-396, and Pennsylvanian-121.

**(2) How many geologic epochs are included in this dataset? What code did you use to find out?**

`nrow(PresencePBDB)`

29

**(3) Which epochs contain specimens of the genus Mytilus (a type of mussel)? What code did you use to find out?**

`apply(PresencePBDB, 1, function(r) any(r %in% c("Mytilus")))`

All the epochs say FALSE.

**(4) Look at the epochs in the geologic timescale. Using your answer to question 3, in which epochs can we infer that Mytilus was present, even though we have no record of them in the PBDB? How did you deduce this?**

I am not really sure. Perhaps they were swept from our "clean taxa" function or "rare taxa" function we performed earlier. At first thought I was thinking they are perhaps more recent (<3.6 mya) and were not included into the matrix since the Pliocene is the most recent Epoch. Eventually I googled their range and did notice how far back they go. This leads me to my assumption of being included into our function sweep.


## Problem Set 2

