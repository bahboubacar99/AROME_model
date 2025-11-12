# AROME atmospheric model
In this project, we will compare simulations made with the AROME atmospheric model with observations made at ground stations.
In this study, we will perform a comparative statistical analysis between the temperature data observed by weather stations and those predicted by the AROME model. We will analyze quantitative statistical indicators such as the comparison of hourly temperature averages, the root mean square error (RMSE), and the bias. Data acquisition was carried out via the API packageArome for Arome data and packageObservations for Météo-France observation data. The decision to download Arome data via the API was motivated by the fact that Arome data is only available in real time, i.e., the Arome model makes predictions every three hours and, after each prediction, the previous data is no longer accessible to users unless a specific request is made to the relevant Météo-France services. For this reason, we set up a script to retrieve the data every day during the project. 
# Prerequisites
In this work, we will use the R software and the Python programming language in the Jupyter Notebook environment for automated data processing. Temperature data extraction in GRIB2 format was performed using the [**R gribr package**](https://github.com/nawendt/gribr), which depends on the [**ECMWF ecCodes (version 2.19.0)**](https://confluence.ecmwf.int/display/ECC/ecCodes+Home) and **proj4 R packages**. As the gribr and ecCodes packages are not available for Windows, a [**Unix environment was installed via Cygwin**](https://cygwin.com/install.html). After configuring the various libraries, all processing was performed in **JupyterLab**, an interactive environment dedicated to data analysis.

# How the AROME format works
The AROME model works by integrating the fundamental equations of fluid dynamics and thermodynamics to simulate atmospheric changes. Here are the key steps in how it works: <br>

**Initialization:** The AROME model begins with an initialization phase where the initial conditions of the atmosphere are defined. These conditions are often derived from larger-scale models, such as the ARPEGE (Action de Recherche Petite Echelle Grande Echelle) model, also developed by Météo-France. <br>
**Simulation:** The model then uses a fine grid to solve the meteorological equations. AROME's typical spatial resolution is 1.3 km, which allows it to capture fine details such as local relief and surface effects. <br>
**Data assimilation:** AROME integrates real-time observations, such as data from satellites, radars, and weather stations, to improve forecast accuracy. This step is crucial for adjusting forecasts based on current conditions. <br>
**Forecast production:** The model generates forecasts for specific meteorological variables, which are then stored in AROME format files. These files can be viewed and analyzed by meteorologists and researchers.

## Auteurs

- **Boubacar BAH** – [GitHub](https://github.com/bahboubacar99)  
- **Prodjinotho Anselme** – [Email](mailto:Pprinceanselme3@gmail.com)

