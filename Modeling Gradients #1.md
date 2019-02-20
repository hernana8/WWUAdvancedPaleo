
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



**(2) How can you convert your similarity index to a distance?**


**(3) Using your own custom R code, find the Jaccard similarity of the Pleistocene and Miocene "samples" in your PresencePBDB matrix. It is possible to code this entirely using only functions discussed in the R Tutorial.**


