# Data Entry Analysis
## Problems with the Data Spreadsheets
1. As the article "Data Organization in Spreadsheets" explains, dates should all be in ISO 8601 format. That is the format YYYY-MM-DD.
2. As the article "Data Organization in Spreadsheets" explains, there should be no empty cells. A common code should be used in place of the missing data.
3. In "pond2010.xlsx", a column name is "z", choosing good names only increases context and readability.
4. In the two zoop spreadsheets, the column names "Cuni #/L" and "Chippo #/L", while one of the files explains the "Cuni" and "Chippo" terms, the "#/L" is never explained in any of the spreadsheets. This should be in a data dictionary to add context for a viewer of the data.
5. As the article "Data Organization in Spreadsheets" explains, highlighting and font color should not be used as data. These spreadsheets used color and highlighting with no explaination as to what it signifies.
6. As the article "Data Organization in Spreadsheets" explains, there should be no calculations in the data files. In "zoop-temp.xlsx", there are four calculations averaging colony size on particular days. These should not be in these files.
7. I think the graphs being shown in the data files also goes with the no calculations rule. It clutters the pure data and could lead to bad assumptions.
8. In "pond2010.xlsx", the data is strucutred differently than the other files. "Colony Diameter" is only a column name in it. The two "zoop" files got rid of "Species" column in favor of adding "Chippo ColonySize", "Cuni ColonySize", "Cuni #/L", and "Chippo #/L". Consistency would make the files more usable.

## New System Template
|Date|Depth|Cuni #/L|Cuni ColonySize|Chippo #/L|Chippo ColonySize|Chla|Temp|
|---|---|---|---|---|---|---|---|
|2016-01-29 |0.5  |72   |2.11 |45 |2.56 |3.1  |18.2 |
|2016-01-29 |10   |54 	|3.44 |56 |2.32 |2.8  |9.9  |
|2016-01-29 |25   |60 	|2.99 |61 |2.76 |3.5  |14.2 |

  *Filled with example data*
#### Information that should be in the Data Dictionary 
* Depth measurement units - meters
* Cuni = Conocghilus unicornis
* Chippo = Conochilus hippocreppis
* ColonySize is the average diameter (mm) of 5 randomly chose conochilus colonies in the sample
* Chla = Chlorophyll a
* Temp units - ?
* #\L = ?
