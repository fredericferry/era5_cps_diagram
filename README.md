# cps_era5

The Cyclone Phase Space Diagram (moe.met.fsu.edu/~rhart/papers-hart/2003Hart.pdf) is a useful diagnostic tool that allows to characterize the thermodynamical structure of tropical and extratropical cyclones. This diagnotic is based on the analysis of the storm-relative thickness assymmetry in the lower troposphere and the warm core/cold core structure of the system in the lower and upper levels of the troposphere.

The parameter that are computed to build this diagram allow to describe the warm core structure of a tropical cyclone, the cold core structure of an extratropical cyclone and its stages of evolution (formation, intensification, occulsion, weakening, development of warm seclusions). It also permits the analysis of the hybrid structure of an extratropical cyclones, the extratropical transitions of a tropical cyclone and the tropical transition of a subtropical cyclone.

This notebook provides a step by step tutorial to build the Cyclone Phase Space diagrams (Hart, 2003) using ERA5 reanalysis in netcdf format.

![Unknown](https://user-images.githubusercontent.com/76565450/162324058-6d69d1d7-f4af-4f3e-bdf6-cf94c7b545a2.png)


- The tracking of the system was done with an automatic tracking algoritm (not provided) applied to ERA5 MEan Sea LEvel Pressure data. The result is a .txt file of the tracking
- Le calcul pas à pas des paramètres de symétrie thermique et de cœur chaud/cœur froid du diagrammme de phase
- Le tracé du diagramme de phase tel que disponible sur http://moe.met.fsu.edu/cyclonephase/

Le diagramme de phase est ici illustré avec le cas de la transition extra-tropicale du cyclone tropical Ophelia (octobre 2017)

Pour faire fonctionner ce calepin il est nécessaire de télécharger les données ERA5 au format netcdf, au pas de temps horaire et sur domaine limité (-100W-50E, 0-90N) :
- https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-era5-single-levels?tab=form
- https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-era5-pressure-levels?tab=form
