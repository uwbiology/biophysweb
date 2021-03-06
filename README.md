# BioPhysWeb
--------------------------------------------------------------

Interactive tool to explore body temperatures of organisms.

**Author:** [UW Biology- Huckley Lab](https://trenchproject.github.io)<br>
**License:** [MIT](http://opensource.org/licenses/MIT)<br>

[![Build Status](https://travis-ci.org/trenchproject/biophysweb.svg?branch=master)](https://travis-ci.org/trenchproject/biophysweb)



### Description

Part of TrEnCh project, and aims to show the impact of climate change on various organisms.

### Installation (Ubuntu)


```
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys E298A3A825C0D65DFD57CBB651716619E084DAB9
sudo add-apt-repository 'deb [arch=amd64,i386] https://cran.rstudio.com/bin/linux/ubuntu xenial/'
sudo apt-get update
sudo apt-get install r-base
sudo su - -c "R -e \"install.packages(c('shiny','leaflet','RColorBrewer','dplyr'), repos = 'http://cran.rstudio.com/')\""

# We need to install devtools as we are going to use experimental leaflet heatmaps

sudo apt-get -y build-dep libcurl4-gnutls-dev
sudo apt-get -y install libcurl4-gnutls-dev

sudo su - -c "R -e \"install.packages('devtools', repos = 'http://cran.rstudio.com/')\""
sudo su - -c "R -e \"devtools::install_github('bhaskarvk/leaflet.extras')\""
 
```


### Installing the app

```{r}
git clone https://github.com/trenchproject/biophysweb.git
cd biophysweb
nohup R CMD BATCH main.R  > server.out 2>&1&


```

### Future Direction

Incorporating below organisms:
* Grasshopper
* Mussels
* Limpets

### Citation

If you use this package, We would appreciate a citation. 

### DOI
[![DOI](https://zenodo.org/badge/90196963.svg)](https://zenodo.org/badge/latestdoi/90196963)

### Notes

If you plan to host the Shiny App, remember to use the host(use local IP) and port option.


