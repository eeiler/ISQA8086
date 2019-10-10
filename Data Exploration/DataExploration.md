# Data Exploration
## Using Vegetation Data from the Xerces Society

#### Density Graph of Schizachyrium Scoparium Throughout all Quadrants 
![](https://github.com/eeiler/ISQA8086/blob/master/Data%20Exploration/Density%20Plot%20of%20Schizachyrium_scoparium.png)
```
ggplot(Schizachyrium_scoparium, aes(value)) + geom_density()
```
This plot shows that for the plant species, Schizachyrium scoparium, there is a greater number of low numbers than high numbers across all quadrants. This is expected for most plants but the trend towards more values of 2 than 1 is interesting.
