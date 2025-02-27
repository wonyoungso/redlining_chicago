# redlining_chicago
# Legacies of Institutionalized Redlining
This notebook contains the code and data for the paper "Legacies of Institutionalized Redlining: A Comparison Between Speculative and Implemented Mortgage Risk Maps in Chicago, Illinois" forthcoming in *Housing Policy Debate*. 

Author: [Wenfei Xu](wenfeixu.com)
Modified by [Wonyoung So](wonyoung.so)

## Citation
If you would like to use the data and/or code from this repo, please use the following citation: 
```

@article{doi:10.1080/10511482.2020.1858924,
author = {Wenfei Xu},
title = {Legacies of Institutionalized Redlining: A Comparison Between Speculative and Implemented Mortgage Risk Maps in Chicago, Illinois},
journal = {Housing Policy Debate},
volume = {0},
number = {0},
pages = {1-26},
year  = {2021},
publisher = {Routledge},
doi = {10.1080/10511482.2020.1858924},

URL = { 
        https://doi.org/10.1080/10511482.2020.1858924    
}
```


### Create Virtual Environment

First, create a virtual environment. If you don't have venv installed, install 
it globally using:

```bash
sudo python -m pip install virtualenv
```

Then, create a new virtual environment---I like placing it in the root folder
of the repository---and activate it.

```bash
# Create the environment...
python -m virtualenv ./venv
# ...and activate it.
. ./venv/bin/activate
```

Finally, install dependencies!

```bash
python -m pip install -r requirements.txt
```



## Data
The repo contains the following datasets: 
- `chicago_boundary`: Current city boundary from [City of Chicago data portal](https://data.cityofchicago.org/Facilities-Geographic-Boundaries/Boundaries-City-Outdated-Format/q38j-zgre/data)
- `chicago_census_historical`: Decennial Census tract data cross-walked back to 1940 tract boundaries, with population- and areal-weighted features, labeled for FHA and HOLC grades. These are used for the FHA and HOLC difference in differences analysis. 
- `chicago_housing/chicago_publichousing_historic`: Dataset of Chicago Housing Authority public housing developments from 1938 to 1968. Re-drawn from [1985 Chicago Housing Authority Family Projects map](http://www.encyclopedia.chicagohistory.org/pages/3712.html) at the Newberry Library
- `chicago_neighborhoods`: Current neighborhood boundaries from [City of Chicago data portal](https://data.cityofchicago.org/widgets/bbvz-uum9)
- `holc_weights`: Tracts and weights used for HOLC DiD.

The repo detailing how the tract data was crosswalked and labeled for redlining boundaries is in another repo [here](https://github.com/iamwfx/redlining).

## Requirements
These notebooks can be run using the [Geographic Data Science environment](https://github.com/darribas/gds_env). The only addition is `patsylearn`, which is a scikit-learn adaption of patsy, used for modeling and building design matices. 
