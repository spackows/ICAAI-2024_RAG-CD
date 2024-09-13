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

_Note_ : Lack of a table caption and vague column headings make these lists pretty useless
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


### Example 3
[Axial precession](https://en.wikipedia.org//w/index.php?title=Axial_precession&oldid=821770845)

<img src="images/Axial-precession_table-02.png" width="30%" alt="table"/>

#### Content design comments
- Table has no caption.
- There should be a first column for "Variable", with rows having the values: Gm, a, e, ω, ϵ, and i

#### Lists
[Full text](txt_org/Axial-precession.org.txt)

_Note_ : Lack of a table caption and "Variable" column make these lists pretty useless
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




