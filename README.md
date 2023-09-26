# TSE

TSE_v2.3 - Is new version of v2.2 with few small bug fixes (June 2023) - user guidlines of v2.2 is same for v2.3

TSE_v2.2 - Is OFFICIAL RELEASE of the version 2 (April 2023)

Time-Series cultivar coefficient Estimator for DSSAT models.

------------------------------------------------------------------------------------------------------------
1. The "TSE_v2.3.7z" file has to be unzipped (with 7-zip). 

2. Unzipped "TSE_v2.3" directory copied to the DSSAT Tools directory "C:\DSSAT48\Tools".

3. In folder "TSE_v2.3" ("C:\DSSAT48\Tools\TSE_v2.3")  ->TSE_v2.3.exe<- executed as Administrator.

4. More detailed instructions can be found in user guidelines!

<pre>
├── C:/DSSAT48
│   ├── Genotype
│   ├── Pest
│	  ├── Maize
│	  ├── Wheat
│  	├── Soil
│	  ├── ...	
│	  └── Tools
│       ├── GBuild
│       ├── XBuild
│       ├── ...
│       └── TSE_v2.3
│	          ├── ...
│	          └── TSE_v2.3.exe	

After executing "TSE_v2.3.exe" a working directory "TSE_workspace" is created where optimization is conducted and optimization output files saved:

├── C:/DSSAT48
│   ├── Genotype
│   ├── Pest
│  	├── Maize
│  	├── Wheat
│	  ├── Soil
│  	├── Tools	
│	  ├── ...	
│  	└── TSE_workspace
│	     	├── *.CUL
│		     ├── *.ECO
│		     ├── *_backup.CUL	
│		     ├── *_backup.ECO
│		     ├── *_boxPlot.png	
│		     ├── ...	
│	     	└── PlantGro.OUT
</pre>
------------------------------------------------------------------------------------------------------------

IMPORTANT:
 - Multi-lyered @TRNO observations in File-T minor bug fixed.
 - Additional debugging option introduced with "captureError.exe" in "TSE_v2.2" directory. 

------------------------------------------------------------------------------------------------------------

Old stable version June 2021 can be found in: https://github.com/memicemir/TSE/tree/TSE_v1---June-2021

------------------------------------------------------------------------------------------------------------

TSE related journal publications:

Cultivar coefficient estimator for the cropping system model based on time-series data: A case study for soybean (Transactions of the ASABE 2021, doi: 10.13031/trans.14432)

Implementation of an automatic time‐series calibration method for the DSSAT Wheat models to enhance multi‐model approaches (Agronomy Journal 2020, DOI: 10.1002/agj2.20328)
