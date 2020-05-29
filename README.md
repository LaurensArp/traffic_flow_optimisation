
# Traffic flow optimisation

This repository contains the official implementation of our paper [Dynamic macro scale traffic flow optimisation using crowd-sourced urban movement data](blank) (DOI will be linked on paper publication). Given the appropriate datasets, the notebook contains code for the automatic optimisation of road weights for improved traffic flow on a road network.

# Requirements

- Python 3
- Jupyter
- Numpy
- Pandas
- Matplotlib
- Networkx
- Geodistance (non-standard; sourced from https://github.com/eamonustc/geodistance )

Optional

- Pickle


## Data sources

Our algorithm uses two types of input data: one to represent the road network of a city, and another containing the movements of people within this city.

The code is based on the assumption that the road network would be given by a shapefile with line data. Although many different data sources could be used, we recommend a source that does not contain duplicate lines for multiple lanes on a road, as this would interfere with the graph generation code. Our paper used road data from NASA's Earthdata's Global Roads Open Access Data Set, which can be found [here] (https://sedac.ciesin.columbia.edu/data/set/groads-global-roads-open-access-v1).

The movement data we used was sourced from Foursquare as part of the Netmob Future Cities Challenge. While this dataset is unfortunately not publicly available, it could be substituted by any dataset containing venue information and movement data. The Foursquare data our code was made for consisted of two .csv files: one for venues, and one for movements. Their column names were as follows:
Tokyo_venue_info.csv --> id,name,lat,lng,category
Tokyo_movements.csv --> venue1,venue2,month,period,checkins

> Our method only requires the id, lat and lng columns from the venue data to function, as we are not interested in the types of venues, and the name could mainly be interesting for plotting purposes. 




