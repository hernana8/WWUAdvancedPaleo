
## Problem Set 1

**(1) How many genera are in the Miocene, Early Jurassic, Late Cretaceous, and Pennsylvanian epochs (not total, but in each epoch)? What code did you use to find out?**

`apply(PresencePBDB,1,sum)` or `sum(PresencePBDB["Miocene",])` for each Epoch.

There are Miocene-654, Early Jurassic-177, Late Cretaceous-396, and Pennsylvanian-121.

**(2) How many geologic epochs are included in this dataset? What code did you use to find out?**

`nrow(PresencePBDB)`

29

**(3) Which epochs contain specimens of the genus Mytilus (a type of mussel)? What code did you use to find out?**

`PresencePBDB[,"Mytilus"]`

 Pridoli, Eocene, E Jurassic, L Cretaceous, Pleistocene, E Devonian, E Cretaceous, M Jurassic, M Triassic, Paleocene, L Triassic, Oligocene, Pliocene, L Jurassic, Miocene, E Triassic

**(4) Look at the epochs in the geologic timescale. Using your answer to question 3, in which epochs can we infer that Mytilus was present, even though we have no record of them in the PBDB? How did you deduce this?**

The oldest occurence of *Mytilus* is found in the Pridoli Epoch, which is Upper Silurian. *Mytilus* may still occur in current time, but the database renders Pleistocene as the last occurence. This makes the stretch from the Upper Silurian all the way through to modern time even though the database does not depict that relevancy.


## Problem Set 2

**(1) Using your own custom R code, find the Jaccard similarity of the Pleistocene and Miocene "samples" in your PresencePBDB matrix. It is possible to code this entirely using only functions discussed in the R Tutorial.**


J(A,B) = ∣A ∩ B∣ / ∣A∣ + ∣B∣ - ∣A ∩ B|

` PresencePBDB["Pleistocene",]/sum(PresencePBDB["Miocene",] +PresencePBDB["Pleistocene",]) 
- PresencePBDB["Pleistocene",]`

I know this is incorrect but I'm stuck here.

Random codes that are useful:

`table(PresencePBDB["Pleistocene",])/table(PresencePBDB["Miocene",])`


**(2) How can you convert your similarity index to a distance?**

`PresencePBDB["Pleistocene",]/sum(PresencePBDB["Miocene",] +PresencePBDB["Pleistocene",]) 
- PresencePBDB["Pleistocene",] + 1`



**(3) Install and load the vegan package. Read the help file for the vegdist( ) function, then use vegdist( ) to calculate the Jaccard distance of the Miocene and Pleistocene samples from the PresencePBDB matrix. Your answer should be identical to your answer to Question 2.**
`vare.dist <- vegdist(PresencePBDB)`

**(4) Using the vegdist( ) function, calculate the Jaccard distances for all of the following epochs in PresencePBDB: Pleistocene, Pliocene, Miocene, Oligocene, Eocene, Paleocene. What code did you use? Which two epochs are the most dissimilar?**

