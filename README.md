# Bedmap

- [SCAR project page for Bedmap](https://scar.org/science/excom/bedmap3)
- [BAS project page for Bedmap](https://www.bas.ac.uk/project/bedmap/#about)
- [Bedmap portal/tool](https://bedmap.scar.org/)
    - Observations: 
        - Flight lines are often < 10 km apart
        - Mountainous regions, for example the region North of Byrd glacier, are often not surveyed. However, a smooth, highly uncertain interpolation of ice thickness (rather than bed elevation) still results in complex appearing bed elevation.  
- [Bedmap data via BAS data overview](https://www.bas.ac.uk/project/bedmap/#data)
    - links to [Bedmap3 csv](https://ramadda.data.bas.ac.uk/repository/entry/show?entryid=91523ff9-d621-46b3-87f7-ffb6efcd1847) contains 50M data points (collected by alledgedly "17" data providers, consisting of 84 csv files, 6.7 GB; only 16 data providers listed)
    - Bedmap3 is 53M additional data points.
    - Bedmap2 is 27M additional data points.
    - Bedmap1 is 2M data points. 
        - LDEO: Rosetta survey of the Ross ice sheet [Rosetta web page](https://www.ldeo.columbia.edu/res/pi/rosetta/)
        - NIPR small coverage flight lines are close together
        - Many other are 7-10 km apart
        - PRIC are close together too.
        - RNRF are close together too.
        - UTIG is considerable too.
    - RAMADA: `Repository for Archiving and MAnaging Diverse Data'

Related code repositories:
- Visualisation code
- Tutorial by Alice Fremand 
- [GeoPhysics book](https://antarctica.github.io/PDC_GeophysicsBook/BEDMAP/data_available.html)
    - Download via ramadda or programmatically.
        - Programmatic download.

Location of data on roger:
- '/home/kim/data/bedmap/bedmap3-csv'
- Combined data set "/home/kim/data/bedmap/bedmap123.csv"

## Research questions:
- What theoretical loss are different resolutions associated with?
    - Calculate loss based on every of the 50 M datapoints: Lines are usually 5+ km apart so that this is more of an "on-line" analysis
    - Depends on data point spacing too: find average measurement distance (this could be one graph of the paper -> analyse for the 84 csv's)
- Grid cells without data
- Local analysis over glacier e.g. Byrd: 
    - across flow verus with flow: variance.
- Combine with models: GP interpolation

# Considerations:
- direction of ice flow
- spacing of lines

## Single dataset case: 
- Grid over Ross **ice shelf**: Rosetta (selected because it is well documented) 
- [Overview of flight lines from Rosetta](http://wonder.ldeo.columbia.edu/data/ROSETTA-Ice/GridInformation/Map/ROSETTA-Ice_Grid_Flown_Map.pdf)
    - Sensor data and derived products
    - previously: RIGGS survey stations
- At 500m res: what loss do we have
- 1 km²: 4 grid cells at 500 m
- 487,000 km² (Ross ice shelf): ~2M grid cells
    - ca. 800 km wide
- Horizontal spacing: roughly 10 km
- Vertical spacing: 65 km
- The planned ROSETTA-Ice Survey Grid would yield a total of 61,000 km and 109 survey lines: 94 East-West lateral survey lines with 10km spacing, and 15 North-South tie-lines with 55km spacing (i.e. 25 m data point spacing)

# Plots
- Main plot
-   RMSE per measurement
-   Cells without any data
- Distribution of number of data points
- per region
- directionality

# Resolutions
- 2 km
- 1 km
- 500 m (Bedmap gridded/BedMachine)
- 250 m
- 125 m
- 62.5
- 31.25

# Grid:

(start is included, stop is excluded)
- x = np.arange(-3333250, 3333750, 500)
- So grid cell starts at -3333 k and ends 3333 k
- y = np.arange(3333250, -3333750, 500) from top down

- y goes from high to low
- (0, 0) is where 4 gridcells intersect
- (250, 250) is e.g. the mid point of that grid cell

# Next steps:

- One dataset:
- Project
- Assign measurments to grid
- Calculate mean (same as some in the summerised)
- Calculate error per measurement
- Calculate number of cells with no data 

