## Exercise Questions Part 1

**(1) How many collections are associated with this reference?**

`704`

**(2) What is the reference ID number for the article?**

`24429`

**(3) The first two taxa in the taxonomic list are bryozoans, and the third taxon listed is Rafinesquina alternata. Next to the taxonomic name is the citation (Conrad 1830). What is the class, family, genus and species of the fourth taxon in the taxonomic list?**

Class: Strophomenata

Family: *Strophomenidae*

Genus: *Strophomena*

Species: *planumbona*


**(4) In what county was the data collected?**

`United States`

**(5) What age (Period) is the data from?**

`Ordovician`

**(6) What is the name of the geologic formation that the data was collected from?**

`Liberty Formation of Cincinnati group (informal) (OH)` - [Geolex]


## Exercise Questions Part 2

**(1) Zoom in so that you can see from Texas to Florida and from Florida to New York. Some of the occurrences are orange and others are yellow. What is the significance of the different colors?**

`The different colors represent the geologic time or age these fossils come from (e.g.; yellow = Cenozioc; red = Permian).`

**(2)Zoom back out. Add an additioanl filter to the search bar, the Ypresian stage. The Ypresian is a time interval ranging from 47.8-56.0 million years ago. In what countries are there Ypresian occurrences of Abra?**

`Abra occurs in the southern United States, England, and Belgium.`

**(3)Clear the Abra and Ypresian filters from the search. Look for the genus Ambonychia (another genus of bivalve). Within the United States, find the city with the most occurrences of Ambonychia. What is the name of this city?**

`Cincinnati`

**(4) What age (Period) are most Ambonychia occurrences?**

`Ordovician`

**(5) During this time period, were most occurrences of Ambonychia arrayed parallel or perpendicular to the equator?**

`Perpendicular`

**(6) Click on the little insect icon on the left side of the screen. This brings up taxonomic information about the target taxon. What order does Ambonychia belong to?**
 
`Myalinida`


## Exercise Questions Part 3

**(1) All occurrences of Ambonychia in the Lexington Limestone as a JSON**

`https://paleobiodb.org/data1.2/colls/list.json?datainfo&rowcount&base_name=Ambonychia&strat=Lexington Limestone`

**(2) All occurrences of mammals present in the Paleocene through Oligocene epochs as a csv**

`https://paleobiodb.org/data1.2/colls/list.csv?datainfo&rowcount&base_name=Mammalia&interval=Paleocene,Oligocene`

**(3) All opinions on the order Testudines in the Mesozoic**

`https://paleobiodb.org/data1.2/colls/list.tsv?datainfo&rowcount&base_name=Testudines&interval=Mesozoic`

**(4) All collections of Aves, Marsupialia, and Sirenia in the United States as a csv**

`https://paleobiodb.org/data1.2/colls/list.csv?datainfo&rowcount&base_name=Aves, Marsupialia, Sirenia&cc=US`

**(5) All occurrences of the gastropod genus Ficus as a csv**

`https://paleobiodb.org/data1.2/colls/list.csv?datainfo&rowcount&base_name=Ficus`


**(6) What family does the genus Gastrocopta belong to?**

`Gastrocoptidae`

**(7) There is only one occurrence of Isoetes in Portugal. What age is it?**

`Early Cretaceous - Aptian interval`

**(8) What is the age of the oldest occurrence of Gastrocopta?**

`Eocene`

**(9) There is only one occurrence of Tiktaalik in the PBDB. Was that occurrence located in the tropics or the extratropics when that organism was alive?**

`Tropics`

**(10) There are two occurrences of Namacalathus in Siberia. What geologic formations are they found in?**

`Kotodzha and Raiga Formations`




## Exercise Questions Part 4

**(1) In your morphometrics lab, you downloaded a csv file of ammonite sizes from a GitHub URL directly into R. What code would you use to download the following PBDB data directly into R?

`URL<-"https://paleobiodb.org/data1.2/colls/list.csv?base_name=Mammut&interval=Pliocene"`


**(2) Download the data from the URL above into R. What are its dimensions?

`70 rows 13 columns`

**(3) Did the above call use the occurrences, collections, references, opinions, or specimens route?

`Collections`

**(4) What genus is being called for? What is its colloquial name? What age was the call limited to?

`Mammut`, `Mastodon`, `Pliocene`


**(5) Look through the service doumentation for the appropriate route (based on your answer to Question 2). Find out how to extend the age search range from the Miocene Epoch through the Pleistocene Epoch. Give the new data query URL.


**(6) What URL would you use to show the paleocoordinates (i.e., paleolatitude and paleolongitude) of each data point?




