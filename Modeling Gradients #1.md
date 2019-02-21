
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

`length(which(PresencePBDB["Pleistocene",] ==1 & PresencePBDB["Miocene",] == 0))`

`length(which(PresencePBDB["Pleistocene",] ==0 & PresencePBDB["Miocene",] == 1))`

`length(which(PresencePBDB["Pleistocene",] ==1 & PresencePBDB["Miocene",] == 1))`

`557/668` = 0.8338323
Total common divided by sum of the Plesitocene and Miocene.


**(2) How can you convert your similarity index to a distance?**

` 1- (557/668)`



**(3) Install and load the vegan package. Read the help file for the vegdist( ) function, then use vegdist( ) to calculate the Jaccard distance of the Miocene and Pleistocene samples from the PresencePBDB matrix. Your answer should be identical to your answer to Question 2.**
`vegdist(PresencePBDB, method= "jaccard")`

` 0.16616766`

**(4) Using the vegdist( ) function, calculate the Jaccard distances for all of the following epochs in PresencePBDB: Pleistocene, Pliocene, Miocene, Oligocene, Eocene, Paleocene. What code did you use? Which two epochs are the most dissimilar?**

`vegdist(PresencePBDB, method= "jaccard")`

I just visually plucked each value out.


Least similar to most similar.

Miocene/Eocene = 0.08905109

Pliocene/Miocene = 0.10237389

Pleistocene/Pliocene = 0.14285714

Pliocene/Eocene = 0.15028902

Miocene/Oligocene = 0.16390977

Pleistocene/Miocene = 0.16616766

Oligocene/Eocene = 0.18694362

Pliocene/Oligocene = 0.21021021

Pleistocene/Eocene = 0.21542940

Pleistocene/Oligocene = 0.27575758

Miocene/Plaeocene = 0.32173913

Eocene/Paleocene = 0.32272069

Pliocene/Paleocene = 0.38714286

Oligocene/Paleocene = 0.40625000

Pleistocene/Paleocene = 0.43750000





