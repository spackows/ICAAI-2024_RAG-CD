# Table processing examples

### Example 1
[Abundance of elements in Earth's crust](https://en.wikipedia.org//w/index.php?title=Abundance_of_elements_in_Earth%27s_crust&oldid=801283417)

<img src="images/Abundance-of-elements-in-Earths-crust_table-01.png" width="75%" alt="table"/>

#### Content design comments
- Why is the column heading "Rank" in the first row instead of on the second row with the sorting element?  Using `rowspan=2` would make more sense.
- Similarly, why are the column headings "Z", "element", and "symbol" in the first row?
- Why are the column headings "Z", "element", and "symbol" merged into one cell?  They should each be in their own column.
- The column heading "Rank" is ambiguous.  A heading like "Rank by abundance" would be more clear.
- This table is so large that it's difficult for a reader to navigate and consume.  In general, it's worth exploring other mechanisms for making this information available.

#### Lists
[Full text](txt_org/Abundance-of-elements-in-Earths-crust.org.txt)
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

<p>&nbsp;</p>


### Example 2
[Atmosphere of Earth](https://en.wikipedia.org//w/index.php?title=Atmosphere_of_Earth&oldid=807367681)

<img src="images/Atmosphere-of-Earth_table-01.png" width="30%" alt="table"/>

#### Content design comments
- Why is the water vapor information merged into the dry air table?  The water vapor information should probably be pulled out of the table.
- Similarly, why are the "notes" merged into the table too?

#### Lists
[Full text](txt_org/Atmosphere-of-Earth.org.txt)
```
### Major constituents of dry air, by volume:

Gas Formula:
- ( Gas Name ) Nitrogen: N2
- ( Gas Name ) Oxygen: O2
...

Volume(A) in ppmv(B):
- ( Gas Name ) Nitrogen: 780,840
- ( Gas Name ) Oxygen: 209,460
...

Volume(A) in %:
- ( Gas Name ) Nitrogen: 78.084
- ( Gas Name ) Oxygen: 20.946
...

### Major constituents of dry air, by volume:
Nitrogen:
- Gas Formula: N2
- Volume(A) in ppmv(B): 780,840
- Volume(A) in %: 78.084

Oxygen:
- Gas Formula: O2
- Volume(A) in ppmv(B): 209,460
- Volume(A) in %: 20.946

...

Methane:
- Gas Formula: CH4
- Volume(A) in ppmv(B): 1.79
- Volume(A) in %: 0.000179

Water vapor(C):
- Gas Formula: H2O
- Volume(A) in ppmv(B): 10–50,000(D)
- Volume(A) in %: 0.001%–5%(D)
```

<p>&nbsp;</p>


### Example 3
[Axial precession](https://en.wikipedia.org//w/index.php?title=Axial_precession&oldid=821770845)

<img src="images/Axial-precession_table-01.png" width="30%" alt="table"/>

#### Content design comments
- Table has no caption.
- The column headings "Year entering" and "Year exiting" are ambiguous.

#### Lists
[Full text](txt_org/Axial-precession.org.txt)

_Note_ : Lack of a table caption and vague column headings make these lists less useful
```
Year entering:
- ( Constellation ) Taurus: 4500 BC
- ( Constellation ) Aries: 2000 BC
- ( Constellation ) Pisces: 100 BC

Year exiting:
- ( Constellation ) Taurus: 2000 BC
- ( Constellation ) Aries: 100 BC
- ( Constellation ) Pisces: AD 2700

Taurus:
- Year entering: 4500 BC
- Year exiting: 2000 BC

Aries:
- Year entering: 2000 BC
- Year exiting: 100 BC

Pisces:
- Year entering: 100 BC
- Year exiting: AD 2700
```

<p>&nbsp;</p>


### Example 4
[Axial precession](https://en.wikipedia.org//w/index.php?title=Axial_precession&oldid=821770845)

<img src="images/Axial-precession_table-02.png" width="50%" alt="table"/>

#### Content design comments
- Table has no caption.
- There should be a first column for "Variable", with rows having the values: Gm, a, e, ω, ϵ, and i

#### Lists
[Full text](txt_org/Axial-precession.org.txt)

_Note_ : Lack of a table caption and "Variable" column make these lists less usefull
```
Moon:
- ( Sun ) Gm = 1.3271244×1020 m3/s2: Gm = 4.902799×1012 m3/s2
- ( Sun ) a = 1.4959802×1011 m: a = 3.833978×108 m
- ( Sun ) e = 0.016708634: e = 0.05554553

Earth:
- ( Sun ) Gm = 1.3271244×1020 m3/s2: (C − A)/C = 0.003273763
- ( Sun ) a = 1.4959802×1011 m: ω = 7.292115×10−5 rad/s
- ( Sun ) e = 0.016708634: ϵ {\displaystyle \epsilon \,\!} = 23.43928°

Gm = 1.3271244×1020 m3/s2:
- Moon: Gm = 4.902799×1012 m3/s2
- Earth: (C − A)/C = 0.003273763

a = 1.4959802×1011 m:
- Moon: a = 3.833978×108 m
- Earth: ω = 7.292115×10−5 rad/s

e = 0.016708634:
- Moon: e = 0.05554553
- Earth: ϵ {\displaystyle \epsilon \,\!} = 23.43928°

:
- Moon: i= 5.156690°
- Earth: 
```

<p>&nbsp;</p>


### Example 5
[Axial tilt](https://en.wikipedia.org//w/index.php?title=Axial_tilt&oldid=826622273)

<img src="images/Axial-tilt_table-01.png" width="75%" alt="table"/>

#### Content design comments
- The notes at the bottom should be pulled out of the table.

#### Lists
[Full text](txt_org/Axial-tilt.org.txt)
```
### Axis and rotation of selected Solar System bodies:

NASA, J2000.0 Axial tilt (degrees):
- ( Body ) Sun: 7.25
- ( Body ) Mercury: 0.03
...

NASA, J2000.0 North Pole R.A. (degrees):
- ( Body ) Sun: 286.13
- ( Body ) Mercury: 281.01
...

NASA, J2000.0 North Pole Dec. (degrees):
- ( Body ) Sun: 63.87
- ( Body ) Mercury: 61.42
...

...

### Axis and rotation of selected Solar System bodies:

Sun:
- NASA, J2000.0 Axial tilt (degrees): 7.25
- NASA, J2000.0 North Pole R.A. (degrees): 286.13
- NASA, J2000.0 North Pole Dec. (degrees): 63.87
- NASA, J2000.0 Rotation (hours): 609.12B
- IAU, 0 January 2010, 0h TT Axial tilt (degrees): 7.25A
- IAU, 0 January 2010, 0h TT North Pole R.A. (degrees): 286.15
- IAU, 0 January 2010, 0h TT North Pole Dec. (degrees): 63.89
- IAU, 0 January 2010, 0h TT Rotation (deg/day): 14.18

...
```

<p>&nbsp;</p>


### Example 6
[Carbon-cycle](https://en.wikipedia.org//w/index.php?title=Carbon_cycle&oldid=837879153)

<img src="images/Carbon-cycle_table-01.png" width="25%" alt="table"/>

#### Content design comments
- An attempt is made to group carbon pools using indentation to show which pools are a part of a larger pool listed in a row above.  It would be better to use another approach (such as having multiple tables or using lists.)

#### Lists
[Full text](txt_org/Carbon-cycle.org.txt)
_Note_: The groupings indicated by indentation in the original table isn't captured or reflected in the lists below
```
### Carbon pools in the major reservoirs on earth.:

Quantity (gigatons):
- ( Pool ) Atmosphere: 720
- ( Pool ) Ocean (total): 38,400
...

### Carbon pools in the major reservoirs on earth.:

Atmosphere:
- Quantity (gigatons): 720

Ocean (total):
- Quantity (gigatons): 38,400

Total inorganic:
- Quantity (gigatons): 37,400

...
```

<p>&nbsp;</p>


### Example 7
[Continent](https://en.wikipedia.org//w/index.php?title=Continent&oldid=808552023)

<img src="images/Continent_table-01.png" width="75%" alt="table"/>

#### Content design comments
- Table has no caption.
- The table is being used as a diagram (for example, there's not a consistent number of columns, there are no useful column headings)
- Also, color coding will not be picked up in the html-to-text transform

#### Lists
[Full text](txt_org/Continent.org.txt)

_Note_ : Lack of a table caption and column headings make these lists less useful
```
Models:
- ( Models ) Four continents: Afro-Eurasia
- ( Models ) Five continents: Africa
...

Models:
- ( Models ) Four continents: America
- ( Models ) Five continents: Eurasia
...

...

Four continents:
- Afro-Eurasia
- America
...

Five continents:
- Africa
- Eurasia
...

...
```



