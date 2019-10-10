# Data Exploration
## Using Vegetation Data from the Xerces Society
The data in this file is not structured well for scatter plots. As discussed with the instructor the data needs a lot of cleaning and reformatting to make it usable. I have pulled out specific data to draw graphs that show some type of data trend. Due to the nature of scatter plots i couldnt use this data in that way. To prove the concepts of plotting and facets I did so with density graphs.

#### Scatter Plot of the Plant Coverage Values for all Species
![](https://github.com/eeiler/ISQA8086/blob/master/Data%20Exploration/Scatter%20all.png)
```
ggplot(MeltedPlantSpeciesCoverData, mapping=aes(x=Species, y=value, color=Quadrant))
+ geom_point()
+ ggtitle("Scatter Plot of the Plant Coverage for all Species, Colored by Quandrants")
+ ylab("Coverage Value")
```
This plot has far too many X values to be readable, but a subset function could limit to a specific section of this graph. Later I hope to be able to group by species so the graph can be more usable.

#### Scatter Plot of the Plant Coverage from Bromus Tectorum
![](https://github.com/eeiler/ISQA8086/blob/master/Data%20Exploration/Scatter%20Bromus%20Tectorum.png)
```
ggplot(Bromus_tectorum, mapping=aes(x=Species, y=value, color=Quadrant))
+ geom_point()
+ ggtitle("Scatter Plot of the Plant Coverage for Bromus Tectorum, Colored by Quandrants")
+ ylab("Coverage Value")
```
This plot is a scatter of one plant species coverage data. As shown it is not helpful.

#### Density Graph of the Plant Coverage from Schizachyrium Scoparium Throughout all Quadrants 
![](https://github.com/eeiler/ISQA8086/blob/master/Data%20Exploration/Density%20Plot%20of%20Schizachyrium%20Scoparium%20Plant%20Coverage%20allQ.png)
```
ggplot(Schizachyrium_scoparium, aes(value)) 
+ geom_density()
+ ggtitle("Density of Schizachyrium Scoparium Plant Coverage in all Quadrants")
+ xlab("Coverage Value")
+ ylab("Density")
```
This plot shows that for the plant species, Schizachyrium scoparium, there is a greater number of low numbers than high numbers across all quadrants. This is expected for most plants but the trend towards more values of 2 than 1 is interesting.

#### Density Graph of the Plant Coverage from Schizachyrium Scoparium in Quadrant 1 
![](https://github.com/eeiler/ISQA8086/blob/master/Data%20Exploration/Density%20Plot%20of%20Schizachyrium%20Scoparium%20Plant%20Coverage%20Q1.png)
```
ggplot(SSQ1, aes(value)) 
+ geom_density() 
+ ggtitle("Density of Schizachyrium Scoparium Plant Coverage in Quadrant 1") 
+ xlab("Coverage Value") 
+ ylab("Density")
```
This plot shows that for the plant species, Schizachyrium scoparium, there is a greater number of low numbers than high numbers across all quadrants. It oddly shows that 2 and 4 rise while the rest fall. 

#### Faceted Density Graph of the Plant Coverage Throughout all Quadrants from Schizachyrium Scoparium and Bromus Tectorum
![](https://github.com/eeiler/ISQA8086/blob/master/Data%20Exploration/Density%20BTvsSS.png)
```
ggplot(SSvsBT, aes(value)) 
+ geom_density() 
+ facet_grid(~Species)
+ ggtitle("Density of Plant Coverage for Bromus Tectorum & Schizachyrium Scoparium in all Quadrants, Side by Side Comparison")
+ xlab("Coverage Value")
+ ylab("Density")
```
This faceted density graph can show directly how the coverage between two species are related.Bromus tectorum has a much higher density of the coverage values ranging from 0:2. However, Bromus tectorum has no values of 6 while Schizachyrium Scoparium shows a low density.
