# Table processing

### Example 1
<a href="https://en.wikipedia.org//w/index.php?title=Abundance_of_elements_in_Earth%27s_crust&oldid=801283417">Abundance of elements in Earth's crust</a>

<img src="images/Abundance-of-elements-in-Earths-crust_table-01.png" width="200px" alt="table"/>

#### Comments
From a Content Design perspective, there is room for improvement with the way the headers of this table are done:
- Why is the column heading "Rank" in the first row instead of on the second row with the sorting element?  Using `rowspan=2` would make more sense.
- Similarly, why are the column headings "Z", "element", and "symbol" in the first row?
- Why are the column headings "Z", "element", and "symbol" merged into one cell?  They should each be in their own column.
- The column heading "Rank" is ambiguous.  A heading like "Rank by abundance" would be more clear.

#### Lists
```
### Abundance of chemical elements in Earth's crust, from various sources:

Z, element & symbol:
- ( Rank ) 1: 8
- ( Rank ) 2: 14
...

Z, element & symbol:
- ( Rank ) 1: oxygen
- ( Rank ) 2: silicon [A]
...

Z, element & symbol:
- ( Rank ) 1: O
- ( Rank ) 2: Si
...

Abundance in crust (ppm) by source Darling:
- ( Rank ) 1: 466,000
- ( Rank ) 2: 277,200
...

Abundance in crust (ppm) by source Barbalace:
- ( Rank ) 1: 474,000
- ( Rank ) 2: 277,100
...

Abundance in crust (ppm) by source WebElements:
- ( Rank ) 1: 460,000
- ( Rank ) 2: 270,000
...

Abundance in crust (ppm) by source Israel Science and Technology:
- ( Rank ) 1: 467,100
- ( Rank ) 2: 276,900
...

Abundance in crust (ppm) by source Jefferson Lab:
- ( Rank ) 1: 461,000
- ( Rank ) 2: 282,000
...

Annual production (2016, tonnes):
- ( Rank ) 1: 
- ( Rank ) 2: 7,200,000
...

### Abundance of chemical elements in Earth's crust, from various sources:
1:
- Z, element & symbol: 8
- Z, element & symbol: oxygen
- Z, element & symbol: O
- Abundance in crust (ppm) by source Darling: 466,000
- Abundance in crust (ppm) by source Barbalace: 474,000
- Abundance in crust (ppm) by source WebElements: 460,000
- Abundance in crust (ppm) by source Israel Science and Technology: 467,100
- Abundance in crust (ppm) by source Jefferson Lab: 461,000
- Annual production (2016, tonnes): 
...
```


