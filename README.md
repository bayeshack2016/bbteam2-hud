![](https://horseradish.s3.amazonaws.com/CACHE/images/photos/66/7f/42bf3e704747/image-54e7656359e25-default-800.png)

# Department of Housing and Urban Development
### Presented by Bloomberg and What Works Cities
How can **data** help communities thrive?

# What we hope to solve
Housing inequality is present in cities across the United States, rendering low income families unable to obtain affordable housing. Lack of fair housing opportunities is just one of the problems communities face: many people also lack access to transportation and services within the community.

Help cities enhance their use of data and evidence to uncover new ways to revitalize neighborhoods and improve the lives of residents.

# Data used
The Housing Inventory is the Planning Department's annual survey of housing production trends in San Francisco. It has reported changes in the City's housing stock, including housing construction, demolition, and alterations, since 1967. 

The Housing Inventory also reports the annual net gain in housing units citywide by general Zoning Districts and by Planning Districts. Net gain is the number of newly constructed units with CFCs issued, adjusted for alterations - which can add or subtract units - and demolitions. Affordable housing, condominiums, and changes in the residential hotel stock are other areas of interest covered by the Housing Inventory. 

| Address            | Units | Net Units | Affordable Housing | Affordable Target|
| ------------------ |:-----:|:---------:|:------------------:|------------------|
| 1407 Market Street | 317   | 317       | 38                 | LI - Low Income  |


- [2014 Housing Inventory](https://data.sfgov.org/Housing-and-Buildings/2014-Housing-Inventory/pucn-j93j)
- [2013 Housing Inventory](https://data.sfgov.org/Housing-and-Buildings/2013-Housing-Inventory/e7d3-dxh5)
- [2012 Housing Inventory](https://data.sfgov.org/Housing-and-Buildings/2012-Housing-Inventory/4xa2-t52k)
- [2011 Housing Inventory](https://data.sfgov.org/Housing-and-Buildings/2011-Housing-Inventory/mpcm-79w2)

# What we actually solved and interesting things learned

- We took the address provided in the Housing Inventory data sets and used the Google Map API to gather associated lattitude and longitude for each value. 
- We then leveraged the recently open sourced [Jupyter Notebook widget for leaflet maps](https://github.com/ellisonbg/ipyleaflet) to plot the net change in units for a given address. 

- `Green` = units were added. `Dark Green` = larger number of units added.
- `Red` = units were removed. `Dark Red` = larger number of units removed.

- The data show an increase in activity (both net positive and negative) each year from 2011 to 2014

![](net_change_graph.png)








# Challenges faced

 - Data availability: most recent hosing inventory was as of 2014
 - Data availability: many state and local governments do a great job at providing data visualizations. Challenges arise when that data cannot be easily consumed by a computer. 

# Areas to take this further

- Overlay [Petitions to Rent Board](https://data.sfgov.org/Housing-and-Buildings/Petitions-to-the-Rent-Board/6swy-cmkq) to see if there are specific areas of San Francisco receiving a larger number of reports (either from tenants or landlords)


# Gaps in the analysis/data

# Technical stack (how it was built)

- The mapping functionality relies heavily on a the recently open sourced [Jupyter Notebook widget for leaflet maps](https://github.com/ellisonbg/ipyleaflet).

- Significant work was done to gather buliding information such as year built and assessed value from the [San Francisco Property Information Map](http://propertymap.sfplanning.org/).


