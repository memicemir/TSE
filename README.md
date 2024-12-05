# TSE

In the TSE.7z file is a new TEST version of the optimizer (TSE_v3.0). User guidlines is not yet ready for it (new version has minnor interface related changes. Use old user guidelines).


TSE_v2.4 - is new official release of the optimizer. Hopefully more stable version with few minor bug fixes.

TSE_v2.3 - is still available in the TSE repository as branch: TSE_v2.3.

TSE_v2.2 - was OFFICIAL RELEASE of the version 2 (April 2023)

Time-Series cultivar coefficient Estimator for DSSAT models.

------------------------------------------------------------------------------------------------------------
1. The "TSE_v2.4.7z" file has to be unzipped (with 7-zip). 

2. Unzipped "TSE_v2.4" directory copied to the DSSAT Tools directory "C:\DSSAT48\Tools".

3. In folder "TSE_v2.4" ("C:\DSSAT48\Tools\TSE_v2.4")  -> TSE_v2.4.exe <- executed as Administrator.

4. More detailed instructions can be found in user guidelines!

<pre>
├── C:/DSSAT48
│   ├── Genotype
│   ├── Pest
│   ├── Maize
│   ├── Wheat
│   ├── Soil
│   ├── ...	
│   └── Tools
│       ├── GBuild
│       ├── XBuild
│       ├── ...
│       └── TSE_v2.4
│           ├── ...
│           └── TSE_v2.4.exe	

After executing "TSE_v2.4.exe" a working directory "TSE_workspace" is created where optimization is conducted and optimization output files saved:

├── C:/DSSAT48
│   ├── Genotype
│   ├── Pest
│   ├── Maize
│   ├── Wheat
│   ├── Soil
│   ├── Tools	
│   ├── ...	
│   └── TSE_workspace
│       ├── *.CUL
│       ├── *.ECO
│       ├── *_backup.CUL	
│       ├── *_backup.ECO
│       ├── ...	
│       └── PlantGro.OUT
</pre>
------------------------------------------------------------------------------------------------------------

Old stable version June 2021 can be found in: https://github.com/memicemir/TSE/tree/TSE_v1---June-2021

------------------------------------------------------------------------------------------------------------

TSE related journal publications:

Cultivar coefficient estimator for the cropping system model based on time-series data: A case study for soybean (Transactions of the ASABE 2021, doi: 10.13031/trans.14432)

Implementation of an automatic time‐series calibration method for the DSSAT Wheat models to enhance multi‐model approaches (Agronomy Journal 2020, DOI: 10.1002/agj2.20328)
