## **1. Examine the plot. What information does it visualize? Include your plot and answer to this question in your markdown file.**
![OsteoGPA Plot](https://github.com/hernana8/WWUAdvancedPaleo/blob/master/Rplot01.png)
The plot reveals all landmark data points (light gray) that were taken from each specimen. The darker circles represent the centroid or the average point for all related landmark points. Visually, we are able to deduce the amount of variation amongst data groupings.

## ** 2. Examine the information you have just generated (specifically, the PCA summary and the plot). What does this information tell you about the original set of Osteostracan skulls?**
The PCA summary, represented by principal component (PC1) through (PC19), are numbered by most variability to least variability. This allows us to see 19 of 26 PC's for our data set. PC1 variance is 56% of shape variance, decreasing as you move towards PC19; 0.002%. This means that PC1 has 56% shape variance in our specimen Osteostracan skulls.

## **3. The major axis on your plot shows the variance of principal component 1 (PC 1). According to the plot, which two specimens are LEAST similar in terms of PC 1? The two warp grids shown on the plot illustrate these two endpoints. Embed the .png files for these two specimens in your MarkDown file and describe the visual differences between them. What factor does PC 1 seem to describe?**

It appears that specimen 8 *Boraspis ceratops* and specimen 29 *Zychiaspis siemiradzkii* are polar opposites. The major differences that PC1 and PC2 would describe in both specimens are the anterior rostrum ("nose" spike) that is elongated on *Boreaspis ceratops* and shovel-like on *Zychiaspis siemiradzkii*, and the backwards protruding cornuta or genal spine located on the back of the head. Specimen 8 has horns protruding at a slight 90° angle of the nose, whereas specimen 29 has cornuta almost parallel, in direction, to its nose. PC1 would describe the cornuta and PC2 the rostrum.

![Boreaspis_ceratops](https://github.com/hernana8/WWUAdvancedPaleo/blob/master/Boreaspis_ceratops.png)
![Zychiaspis_siemiradzkii](https://github.com/hernana8/WWUAdvancedPaleo/blob/master/Zychiaspis_siemiradzkii.png)
        
      

## **4. The minor axis on your plot shows the variance of PC 2. According to the plot, which two specimens are least similar in terms of PC 2? While you cannot see the warp grids for these two specimens on the plot, you can examine the .png files. Embed these images in your MarkDown file and describe the visual differences between them. What factor does PC 2 seem to describe?**

PC2 has a variance value of ~32% which is largely seen in the rostrum changes between specimen 3 *Belonaspis puella* and specimen 4 *Benneviaspis anglica*. A rostrum that is very much elongated in specimen 3 is alsmost completely undersized.

![Belonaspis_puella](https://github.com/hernana8/WWUAdvancedPaleo/blob/master/Belonaspis_puella.png)
![Benneviaspis_anglica](https://github.com/hernana8/WWUAdvancedPaleo/blob/master/Benneviaspis_anglica.png)

## **6. Create the barplot and embed the figure in your Markdown file.**

![Belonaspis_puella](https://github.com/hernana8/WWUAdvancedPaleo/blob/master/Bar.png)


## **7. Try plotting PC 1 and PC 18. Include the code that you used in your MarkDown file, and embed the resuting plot. Why does it look like all the specimens fall almost perfectly along a single line parallel to the major axis?**

This is due to the relative variance between PC1 and PC18. As we seen above, PC1 contains the highest PC variance at 53%. PC18 is tied with PC19 in having the least PC variance at 0.002%. Because PC18 is so low, the points are not going to have much variance relative to PC1 which spans the distance of the farthest points horizontally.

![Belonaspis_puella](https://github.com/hernana8/WWUAdvancedPaleo/blob/master/Rplot1_18.png)



The possibilities of using morphometrics in paleontology is endless. Not only can you adopt this technique on a variety of animal hard and soft parts, you can even apply it to their traces. I would propose to use morphometrics on burrows to see variation over time and variation amongst related taxa and non related taxa over time and compare results. Say, "X" type of trace fossil might be produced by three different types of arthropods during the Cambrian, but only two of them changed their internal topographic relief of the trace while the third stood the same approaching the Ordovician. Morphometrics can help provide data like that would tell you the minute differences in topo relief over a span of taxa and time. 
