# Cyclone phase space from ERA5 data.

Note 1: This code was deveopped for educationnal purposes, and for French students. So the comments in the notebook are in French but the graphics and legends are in English. This should not pose any problem to understand the code.

Note 2 : If you have any comment/suggestion, if you find this code useful --> please send me an email : mailto:frederic.ferry@meteo.fr

--------------------------------------------------------------------------------------------------------------------------------------------------

The Cyclone Phase Space Diagram (Hart, 2003 : http://moe.met.fsu.edu/~rhart/papers-hart/2003Hart.pdf) is a useful diagnostic tool that allows to characterize the thermodynamical structure of tropical and extratropical cyclones. The diagnotic is based on the analysis of the storm-relative thickness assymmetry in the lower troposphere and the warm core/cold core structure of the system in the lower and upper levels of the troposphere.

The parameters that are computed to build this diagram allow to describe the warm core structure of a tropical cyclone, the cold core structure of an extratropical cyclone and its stages of evolution (formation, intensification, occulsion, weakening, development of warm seclusions). It also permits the analysis of the hybrid structure of an extratropical cyclones, the extratropical transitions of a tropical cyclone and the tropical transition of a subtropical cyclone.

This notebook provides a step by step tutorial to build the Cyclone Phase Space diagrams using ERA5 reanalysis in netcdf format. The illustrating example proposed in the notebook is the tropical transition of tropical cyclone Ophelia in October 2017.

![MSL_tracking-min](https://user-images.githubusercontent.com/76565450/162413793-6dd8a1ac-cef4-4a28-8161-fe3c2154a282.gif)
![b](https://user-images.githubusercontent.com/76565450/162413008-78e02cfa-8a39-42f1-afb5-89d2e09f07ce.png)
![z](https://user-images.githubusercontent.com/76565450/162413018-10332868-301e-4dfb-820c-8ec1cd43313a.png)
![deltaz](https://user-images.githubusercontent.com/76565450/162413053-438f1839-56df-4956-af64-641345d0f6eb.png)
![cps1](https://user-images.githubusercontent.com/76565450/162413251-c344ee20-1fab-4ae8-993f-03bce7df0e9b.png)
![cps2](https://user-images.githubusercontent.com/76565450/162413260-2ec66ba3-b702-4803-bb7d-411a2a4a25b7.png)


For each system, a corresponding tracking file (txt format) must present in the txt folder. This file was generated with an automatic tracking algorithm (not provided) applied to ERA5 Mean Sea Level Pressure data. To run the notebook, you will also need to download hourly data of Mean Sea Level Pressure and Geopotential for Ophelia in netcdf format and on a limited area domain (-100W-50E, 0-90N) :

https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-era5-single-levels?tab=form

https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-era5-pressure-levels?tab=form
