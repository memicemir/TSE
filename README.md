# TSE
Time-Series cultivar coefficient Estimator for DSSAT models

------------------------------------------------------------------------------------------------------------
The "gitHub_TSE_[date_stamp].zip"
file has to be unzipped as "gitHub_TSE_[date_stamp]" working directory. 

From "gitHub_TSE_[date_stamp]" directory "TSE" folder copied to the "Tools" directory -> "C:\DSSAT47\Tools"

In folder "TSE" -> "C:\DSSAT47\Tools\TSE"
"TSE_calibrator_DSSAT.exe" - windows runnable has to be executed as -> Administrator <-.

------------------------------------------------------------------------------------------------------------

I.	PlantGro.Out crop model outputs are coupled to those in File-T (growth-related) time-series in-season observations

II.	Evaluate.Out crop model outputs are coupled to those in File-A (phenology-related) as DAY observations

III.	If sub-model (eg. WHAPS) is initialised in the File-X, the calibrator will not work! (in File-X in *SIMULATION CONTROLS in GENERAL line, column SMODEL do not initialise sub-models!)

IV.	Only variables such as LAID, CWAD, GWAD etc. initialised in first time occurring “@TRN….” line in File-T is actively used by TSE

V.	For multi TRT optimisations only target variables simultaneously available in all File-T/s (for corresponding File-X/s Treatments) are accessible for optimisation

VI.	If PrameterProperty.txt is NOT in the C:\DSSAT47\Tools\TSE folder, P/G (Phenlology/Growth-related flags) are not available in interface!

VII.	T-file observations (all in-season observations available including 0 are used, only -99 values are ignored by the program) used for estimating the optimum genetic coefficient (phenology- and growth-related)

VIII.	The program is matching DOY from T-file with those in the PlantGro.OUT. If you setup in the X-file reporting frequency for example every fifth day and exact observation DOY is not present in the PlantGro.OUT as it is written in the T-file, the program will not be able to match them for comparing simulated and observed.

------------------------------------------------------------------------------------------------------------

The optimiser program is creating additional directory TSE_workspace (C:\DSSAT47\TSE_workspace) and modifying the cultivar file in that directory, which is then executed by main DSSAT model executable.
 


