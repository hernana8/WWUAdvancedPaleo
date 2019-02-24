## Problem Set 1

**(1) Download a dataset from the Paleobiology Database that includes all Ordovician-age animals (i.e., *Animalia*). Name the object `Ordovician`. What code did you use?**

`Ordovician<-velociraptr::downloadPBDB(Taxa=c("Animalia"),StartInterval="Ordovician",StopInterval="Ordovician")`

**(2)Clean up the poorly resolved genus names. What function and/or code did you use?**

`Ordovician<-velociraptr::cleanTaxonomy(DataPBDB,"genus")`

**(3)Turn you object Ordovician into a community matrix of the samples by genera, where the samples are different geoplate codes. Geoplate codes denote different paleocontinents, so by doing this, your community matrix will list which genera were present on which paleocontinents during the Ordovician. Cull this matrix so that each sample has a minimum of 25 taxa and each taxon occurs in at least two samples. Show your code.**

`PresenceOrdovician<-velociraptr::cullMatrix(PresenceOrdovician,Rarity=2,Richness=25)`


**(4)Preform a DCA on your new community matrix. Analyze your DCA with a plot. Do you think that the orientation of samples along either axis 1 or axis 2 is related to the average latitude or longitude of each plate in question? Explain how you determined your answer, and shwo your code. Hint: information about the paleolatitude and paleolongitude of different geoplates is included in the data you originally downloaded (i.e., the object Ordovician)**

![OrdovicianDCA](https://github.com/hernana8/WWUAdvancedPaleo/blob/master/DCAGeoplateColor.png)

`plot(PostOrdovicianDCA,display="sites",choices=c(1,2))`
`plot(x=PostOrdovicianSamples[,"DCA1"],y=PostOrdovicianSamples[,"DCA2"],pch=16,las=1,xlab="DCA1",ylab="DCA2",type="n")`

`text(x=Ones[,"DCA1"],y=Ones[,"DCA2"],labels=dimnames(Ones)[[1]], col = "gray")`
`text(x=Twos[,"DCA1"],y=Twos[,"DCA2"],labels=dimnames(Twos)[[1]], col = "gold")`
`text(x=Threes[,"DCA1"],y=Threes[,"DCA2"],labels=dimnames(Threes)[[1]], col = "Orange")`
`text(x=Fours[,"DCA1"],y=Fours[,"DCA2"],labels=dimnames(Fours)[[1]], col = "Red")`
`text(x=Fives[,"DCA1"],y=Fives[,"DCA2"],labels=dimnames(Fives)[[1]], col = "Red4")`
`text(x=Sixes[,"DCA1"],y=Sixes[,"DCA2"],labels=dimnames(Sixes)[[1]], col = "darkgreen")`
`text(x=Sevens[,"DCA1"],y=Sevens[,"DCA2"],labels=dimnames(Sevens)[[1]], col = "purple")`
`text(x=Eights[,"DCA1"],y=Eights[,"DCA2"],labels=dimnames(Eights)[[1]], col = "black")`

Well, I think the color combination does show a congregate of certains colors in one area, the black 800's and Fuchsia 700's as an example, where the variability is roughly 1 on both DCA axes. There are a few with a similar variability (300's) but then you have 309 and 313 at the far postive quadrant of DCA1. The 200's display the same thing, the rest are pretty much scattered in either one DCA axis or both.

To answer the question, yes I think the majority are related to the average lat/long of each plate. There is a nice wedge effect right in the center for a few geoplates, but still trending on the other axis.


