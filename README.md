# AR6 Scenario Explorer Analysis

This project involves analyzing some salient aspects of the AR6 Scenario Explorer and creating a set of figures and tables to illustrate the findings using `pyam`. The analysis includes exploring emission trajectories and energy system configurations.

## Introduction
The AR6 Scenario Explorer provides a comprehensive database of scenarios for exploring the impacts of climate change on various aspects of the environment. In this project, we analyzed the data to gain insights into the emission trajectories and energy system configurations in the different scenarios.

## Installation

To install the required dependencies, please run the following command:

pip:

```pip install pyam```

conda/mamba:

```conda install -c conda-forge pyam```

## Database
To download the AR6 Scenario Explorer database, visit https://data.ece.iiasa.ac.at/ar6/#/downloads and download the desired files. For this project, we used the AR6_Scenarios_Database_R5_regions_v1.1 file.
`df = pyam.IamDataFrame(data='AR6_Scenarios_Database.csv'`

## Usage
The analysis was performed using pyam to extract relevant data and create visualizations. The Jupyter notebook containing the analysis and figures can be found in the notebooks directory.

The figures generated include:

   - Emission trajectories for different scenarios
   - Energy system configurations for different scenarios\\
Here's an example:

```py
import numpy as np
import matplotlib.pyplot as plt
import pyam
# import AR6 database
df = pyam.IamDataFrame(data='AR6_Scenarios_Database.csv')
# Filtering for model='MESSAGE*' will return all scenarios provided by the MESSAGEix-GLOBIOM 1.0 model
df.filter(model='MESSAGE*').scenario

## Contribution
Contributions are welcome! Please feel free to submit bug reports, feature requests, or pull requests. For major changes, please open an issue first to discuss what you would like to change.

## License
This project is licensed under the open source [MIT
License](https://github.com/PyPSA/PyPSA/blob/master/LICENSE.txt).
