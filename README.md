# Programming for Data Analysis Assignment 2

![python logo](/images/logos/python_logo_title.png "python logo") ![jupyter logo](/images/logos/jupyter_logo_title.png "jupyter logo") ![markdown logo](/images/logos/markdown_logo_title.png "markdown logo") ![github logo](/images/logos/github_logo_title.png "github logo")

Author: Sean Humphreys

This data repository contains the submissions for the Programming for Data Analysis Assignment 2.

Instructions on the use of the files in the repository and the guidance on how to use the contents of the repository are outlined below.

---

## Contents

1. [Problem Statement](#1-problem-statement)

2. [Repository Instructions](#2-repository-instructions-github-logo)

2. [Jupyter Notebooks](#3-jupyter-notebooks-jupyter-logo)

3. [Python Requirements](#4-python-requirements-python-logo)

4. [Fused Datasets](#5-fused-datasets)

    1. [Long Term Dataset](#51-long-term-dataset)

    2. [Irish Dataset](#52-irish-dataset)

---

## 1. Problem Statement

+ Analyse CO2 vs Temperature Anomaly from 800,000 years – present.

+ Examine one other (paleo/modern) features (e.g. CH4 or polar ice-coverage).

+ Examine Irish context:
    
    + [Climate change signals](/literature/the_emergence_of_a_climate_change_signal_in_long_term_irish_meteorological_observations.pdf) : (see Maynooth study: The emergence of a climate change signal in long-term Irish meteorological observations - ScienceDirect).

+ Fuse and analyse data from various data sources and format fused data set as a pandas DataFrame and export to csv and json formats.

+ For all of the above variables, analyse the data, the trends and the relationships between them (temporal leads/lags/frequency analysis).

+ Predict global temperature anomaly over next few decades (synthesise data) and compare to published climate models if atmospheric CO2 trends continue.

+ Comment on accelerated warming based on very latest features (e.g. temperature/polar-ice-coverage).

---

## 2. Repository Instructions ![github logo](/images/logos/github_logo_title.png)

To access the files in this repository Git Desktop must be installed on the local machine.

Git desktop installation files are accessed [here](https://desktop.github.com/).

Guides on the use of Git are available [here](https://docs.github.com/en/desktop/overview/getting-started-with-github-desktop).


This repository can be cloned with the following git command:

```bash
git clone https://github.com/humphs078/programming_for_data_analysis_assignment_2.git
```

---


## 3. Jupyter Notebooks ![jupyter logo](/images/logos/jupyter_logo_title.png "jupyter logo")

Jupyter Notebooks are an interactive way to explain code and visualize data. Further information on Jupyter Notebooks can be found [here](https://jupyter-notebook.readthedocs.io/en/stable/notebook.html).

To run this file in a fully interactive way the Jupyter Notebooks server must be installed on the local machine. Instructions on how to install Jupyter Notebooks server can be found [here](https://jupyter.org/install).

This repository contains one Jupyter Notebook:

+ [Submission Notebook](/submission.ipynb)

---

## 4. Python Requirements ![python logo](/images/logos/python_logo_title.png "python logo")

Once you have cloned this repository the required python packages can be installed from the command line with the following command:

```bash
pip install -r requirements.txt
```

Or should you wish to install the packages manually please run the following commands from the bash console:

+ pandas - `pip install pandas`

+ matplotlib - `pip install matplotlib`

+ seaborn - `pip install seaborn`

+ numpy - `pip install numpy`

+ scikit-learn - `pip install -U scikit-learn`

+ scypy - `pip install scipy`

+ siml - `pip install siml`

+ statsmodels -`pip install statsmodels`

---

## 5. Fused Datasets

This repository contains two fused datasets. Each dataset is in two formats:

+ Comma Separated Value (CSV)

+ Javascript Object Notation (JSON)

### 5.1 Long Term Dataset

The long term dataset contains 800,000 thousand years of carbon dioxide (CO2) atmospheric concentrations, temperature anomaly and methane atmospheric concentrations.

The data ranges from 2022 to 800,000 years before 2022. Missing values for each variable have been interpolated linearly. Pandas was used to interpolate missing data.

+ CO2 data is measured in parts per million by volume (ppmv).

+ Temperature anomaly data is measured in degrees celsius.

+ Methane (CH4) data is measured in parts per billion (ppb).

Data is sourced as follows:

+ Carbon Dioxide data from 1959 - 2022 is sourced from https://gml.noaa.gov/webdata/ccgg/trends/co2/co2_annmean_mlo.csv (accessed 09 Jan. 2024).

+ CO2 data from 1950 to 803,182 years from 2023 is sourced from the International Panel on Climate Change (IPCC). This dataset is a composite of a number of samples of carbon dioxide data from studies on ice core analysis. The samples have been dated using the The Antarctic Ice Core Chronology (AICC2012) system. The original dataset can be accessed [here](datasets/historic/co2/grl52461-sup-0003-supplementary.xls).

+ Temperature from from 1880 to 2022 in this dataset is sourced from [NASA](https://data.giss.nasa.gov/gistemp/graphs/graph_data/Global_Mean_Estimates_based_on_Land_and_Ocean_Data/graph.txt) (https://data.giss.nasa.gov/gistemp/graphs/graph_data/Global_Mean_Estimates_based_on_Land_and_Ocean_Data/graph.txt [Accessed 12 Dec. 2023].). [1] The temperature data is the global surface temperature.

Temperature data from 1880 to 800k years from the 2023 was sourced from [https://www.temperaturerecord.org/#sources](https://www.temperaturerecord.org/#sources) accessed 13 Dec. 2023. [2] & [3]. 

All of the temperature data is compared to the long-term average from 1951 to 1980

[1] Credits - Snyder, C.W. 2016.

[2] Credits - Marcott et al, 2013.

[3] Credits - Shakun et al, 2012.

+ Methane data from 2023 to 1984 is obtained from the National Oceanic and Atmospheric Administration (NOAA).

Methane data from 1982 to 1888 was sourced from the NOAA (Etheridge, Steele, Francey, and Langenfelds, 1998).

Methane data from from 1884 to 800,000 previous was sourced from the EPICA Dome C Ice Core dataset (Loulergue et al., 2008).

Full citations for authors are listed in the references section of the [submission notebook](submission.ipynb).

+ The CSV file of fused long terrm data is accessed [here](datasets/fused_datasets/csv/long_term_fused_data.csv).

+ The JSON file of fused long term data is accessed [here](datasets/fused_datasets/json/long_term_fused_data.json).


### 5.2 Irish Dataset

This dataset contains annual mean temperature data and annual mean precipitation data for Ireland from 1901 - 2022. This data was sourced from the [World Bank Group](https://climateknowledgeportal.worldbank.org/) (https://climateknowledgeportal.worldbank.org/ Accessed 20 Dec. 2023) website who sourced their [data](https://climateknowledgeportal.worldbank.org/country/ireland/climate-data-historica) (https://climateknowledgeportal.worldbank.org/country/ireland/climate-data-historical Accessed 20 Dec. 2023) from  the climate research unit in the University of East Anglia (https://www.uea.ac.uk/groups-and-centres/climatic-research-unit Accessed 20 Dec. 2023).

+ The CSV file is accessed [here](datasets/fused_datasets/csv/fused_irish_data.csv).

+ The JSON file is accessed [here](datasets/fused_datasets/json/fused_irish_data.json).

---