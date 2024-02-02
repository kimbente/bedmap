# Bedmap

- [SCAR project page for Bedmap](https://scar.org/science/excom/bedmap3)
- [BAS project page for Bedmap](https://www.bas.ac.uk/project/bedmap/#about)
- [Bedmap portal/tool](https://bedmap.scar.org/)
    - lines are often still 10 km apart
- [Bedmap data](https://www.bas.ac.uk/project/bedmap/#data)
    - [Bedmap3 csv](https://ramadda.data.bas.ac.uk/repository/entry/show?entryid=91523ff9-d621-46b3-87f7-ffb6efcd1847) contains 50M data points (collected by alledgedly "17" data providers, consisting of 84 csv files, 6.7 GB; only 16 data providers listed)
        - LDEO: Rosetta survey of the Ross ice sheet [Rosetta web page](https://www.ldeo.columbia.edu/res/pi/rosetta/)
        - NIPR small coverage flight lines are close together
        - Many other are 7-10 km apart
        - PRIC are close together too.
        - RNRF are close together too.
        - UTIG is considerable too.
    - RAMADA: `Repository for Archiving and MAnaging Diverse Data'

Other of my code to look at:
- Visualisation code
- Tutorial by Alice Fremand 
- [GeoPhysics book](https://antarctica.github.io/PDC_GeophysicsBook/BEDMAP/data_available.html)
    - Download via ramadda or programmatically.
        - Programmatic download.

On roger:
- '/home/kim/data/bedmap/bedmap3-csv'


## Research questions:
- What theoretical loss are different resolutions associated with?
    - Calculate loss based on every of the 50 M datapoints: Lines are usually 5+ km apart so that this is more of an "on-line" analysis
    - Depends on data point spacing too: find average measurement distance (this could be one graph of the paper -> analyse for the 84 csv's)
- Grid cells without data
- Local analysis over glacier e.g. Byrd: 
    - across flow verus with flow: variance.
- Combine with models: GP interpolation

## Single dataset case: 
- Grid over Ross ice shelf: Rosetta (selected because it is well documented) 
- [Overview of flight lines](http://wonder.ldeo.columbia.edu/data/ROSETTA-Ice/GridInformation/Map/ROSETTA-Ice_Grid_Flown_Map.pdf)
    - Sensor data and derived products
    - previously: RIGGS survey stations
- At 500m res: what loss do we have
- 1 km²: 4 grid cells at 500 m
- 487,000 km² (Ross ice shelf): ~2M grid cells
    - ca. 800 km wide
- Horizontal spacing: roughly 10 km
- Vertical spacing: 65 km
- The planned ROSETTA-Ice Survey Grid would yield a total of 61,000km and 109 survey lines: 94 East-West lateral survey lines with 10km spacing, and 15 North-South tie-lines with 55km spacing

# Plots
- RMSE per measurement
- Cells without any data
- Distribution of number of data points
