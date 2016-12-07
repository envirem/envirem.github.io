ENVIREM DATASET README
======================

ENVIronmental Rasters for Ecological Modeling
----          -           -          -


DESCRIPTION
-----------

The ENVIREM dataset is a set of 16 climatic and 2 topographic variables that can be used
in modeling species' distributions. The strengths of this dataset include their close 
ties to ecological processes, and their availability at a global scale, at several 
spatial resolutions, and for several time periods. 
The underlying temperature and precipitation data that went into their construction comes 
from the WorldClim dataset (www.worldclim.org), and the solar radiation data comes from 
the Consortium for Spatial Information (www.cgiar-csi.org). 
The data are compatible with and expand the set of variables from WorldClim v1.4
(www.worldclim.org).

For more information, please visit the project website: envirem.github.io


CITATION
--------

Please reference the project website (envirem.github.io) for updated information regarding the appropriate 
reference.


ENVIREM VARIABLES
-----------------

The variables in the ENVIREM dataset are the following [with their abbreviated names in 1st brackets] 
and [units in 2nd brackets]:

- Growing Degree Days on a 5 deg C base [growingDegDays5][-]
- Growing Degree Days on a 0 deg C base [growingDegDays0][-]
- Count of the number of months with a mean temperature > 10 deg C [monthCountByTemp10][months]
- Compensated thermicity Index [thermInd][degrees C]
- Emberger's Pluviothermic Quotient [embergerQ][-]
- Mean annual potential evapotranspiration [annualPET][mm / year]
- Potential evapotranspiration seasonality [PETseasonality][mm / month]
- Mean monthly potential evapotranspiration of the driest quarter [PETDriestQuarter][mm / month]
- Mean monthly potential evapotranspiration of the wettest quarter [PETWettestQuarter][mm / month]
- Mean monthly potential evapotranspiration of the warmest quarter [PETWarmestQuarter][mm / month]
- Mean monthly potential evapotranspiration of the coldest quarter [PETColdestQuarter][mm / month]
- Thornthwaite's aridity index [aridityIndexThornthwaite][-]
- Climatic moisture index [climaticMoistureIndex][-]
- Maximum temperature of the coldest month [maxTempColdestMonth][degrees C * 10]
- Minimum temperature of the warmest month [minTempWarmestMonth][degrees C * 10]
- Continentality [continentality][degrees C]
- Terrain roughness index [TRI][-]
- Topographic wetness index [topoWet][-]

* Variables with "-" units are either unitless or do not have units that lend themselves to straightforward
interpretation.

Citations for the calculation of these variables are provided on the project website (envirem.github.io).

AVAILABLE OPTIONS FOR DOWNLOAD
------------------------------

These variables have been made available for all combinations of the following options:

Geographic regions:
- global
- Africa
- Australasia
- Eurasia
- Europe
- North America
- South America
- New World
- Pacific

Time periods and global circulation models:
- present (~ 1960 - 1990)
- Last Glacial Maximum (LGM; ~ 22 kya)
	* CCSM4
	* MIROC-ESM
	* MPI-ESM-P
- mid Holocene (~ 6 kya)
	* CCSM4
	* MIROC-ESM
	* MPI-ESM-P

Spatial resolution:
- 10 arc-minutes (~ 20 km)
- 5 arc-minutes (~ 10 km)
- 2.5 arc-minutes (~ 5km)
- 30 arc-seconds (current only; ~ 1 km)

Raster formats [and file extensions]:
- geotiff [.tif]
- generic raster [.bil, .hdr, .prj, .aux.xml]


FILE NAMING SCHEME
------------------
Files for download have been carefully named to reflect what specific version of the 
ENVIREM dataset is contained within the zipped directory. The naming follows the pattern:
[region] _ [time period] _ [circulation model] _ [resolution] _ [file format].zip.



Each downloadable .zip file contains the 16 climatic variables for the specified 
combination of geographic/temporal/spatial/file-format requested. The exception is 
the 30 arc-second datasets, which have been split into 4 files to obtain more manageable 
file sizes. For these split datasets, specific variables are found in the following sets:
Set 1:
- annualPET
- aridityIndexThornthwaite
- climaticMoistureIndex
- continentality
- PETseasonality
Set 2:
- embergerQ
- growingDegDays0
- growingDegDays5
- maxTempColdest
Set 3:
- minTempWarmest
- monthCountByTemp10
- PETColdestQuarter
- PETDriestQuarter
Set 4:
- PETseasonality
- PETWarmestQuarter
- PETWettestQuarter
- thermicityIndex


The elevation-derived variables are available as separate downloads, with [elev] preceding the file name.

R PACKAGE
---------

The R package 'envirem' is available from CRAN and can be used to calculate these variables
from other input datasets (e.g., for future time periods).
https://cran.r-project.org/web/packages/envirem/index.html
