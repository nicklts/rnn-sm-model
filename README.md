# RNN-SM-Model
Recurrent Neural Network model for remote sensing-based soil moisture estimation + data pipeline

## Setup

### Installing a python environment
Miniconda is a minimal installer for conda and the simplest way to get started with python. The installer can be found [here](https://docs.conda.io/en/latest/miniconda.html)

#### Adding Miniconda to the system variables
Once installed, open the Miniconda command prompt and type `rundll32 sysdm.cpl,EditEnvironmentVariables`

Double-click the 'Path' variable under the 'User' section

Click the 'Edit text' button in the 'Edit' dialog window and add the following string to the existing 'Path' variable value `%UserProfile%\miniconda3\condabin;`

In the Miniconda command prompt, type the following to append the path `setx Path "%Path%%UserProfile%\miniconda3\condabin;"`

#### Setting up an environment with dependencies
Environments allow you keep different versions of packages for separate projects. Install the environment using the **environment.yml** file and then activate the environment in the Miniconda prompt with `conda activate soil-moisture-rnn`.

### Setting up the GEE configurations
The script relies on the Google Earth Engine python API to extract geospatial information from various layers. To utilize this data the end user must first authorize their account via Google. The authentication is a one-time process that will write a credential file to your local directory with a token. This token is written by typing `earthengine authenticate` in the Miniconda prompt.

