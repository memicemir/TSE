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
 
The optimiser program is NOT modifying core DSSAT files in their original directories!

Program run is considered: Start- “TSE_calibrator_DSSAT.exe” executed until “Exit” push button is pressed. Any form of optimisation done in-between is temporary saved in the temporary cultivar file in TSE_workspace directory. 

After TSE program is started (TSE_calibrator_DSSAT.exe executed) all modifications on Cultivar file are conducted in C:\DSSAT47\TSE_workspace. During one program run (until “Exit” push button is pressed) different coefficients (or different target variables) can be optimised one after another or simultaneously and cultivar changes will be saved if accepted as “optimums” in cultivar file in C:\DSSAT47\TSE_workspace. If user is satisfied with the cultivar coefficient values based on nRMSE fit or visual fit cultivar coefficient combination should be copied to C:\DSSAT47\Tools\Genotype located cultivar file, MANUALLY. If TSE program is started again without saving the combination in C:\DSSAT47\Tools\Genotype located cultivar file new TSE program start will copy original C:\DSSAT47\Tools\Genotype located cultivar file and overwrite your working cultivar file in C:\DSSAT47\TSE_workspace.

After model run finished and before you click “Exit” push button you can open GBuild and check visual and statistical fit (RMSE, d-statistics within GBuild) of the experiment file executed with the “optimum” genetic coefficient combination found in the last model run. With GBuild you open PlantGro.OUT from C:\DSSAT47\TSE_workspace directory, because TSE will create parallel files it requires in this folder, without modifying the original files in DSSAT directory.

The more coefficients are “activated” (used in estimation process) the longer will optimisation last. For each new coefficient and additional increment step (Inc.) number of model runs will increase exponentially (can be checked in “show comb-s” push button.

For example:

Every time TSE_calibrator_DSSAT.exe is executed original cultivar (SBGRO047.CUL) file from C:\DSSAT47\Genotype will be copied to C:\DSSAT47\TSE_workspace directory, and overwrite cultivar file in that directory (if exist, if not then just copy it). If user wants to keep the genetic coefficient combination, it has to be copied to the original cultivar file in C:\DSSAT47\Genotype directory into SBGRO047.CUL manually.

------------------------------------------------------------------------------------------------------------

Running TSE program (The steps of preparing the estimator for run are enumerated):

1.	If directory path shown is “C:\DSSAT47”, do NOT modify! If the path is not “C:\DSSAT47” (This means that TSE folder was not copied to the “C:\DSSAT47\Tools”), then navigate to TSE folder and select it. It will be explained later in more details.

2.	Select desired model and Initialize it!

3.	Select cultivar from model corresponding list.

4.	Select File/s-X from list containing selected cultivar.

5.	Select corresponding Treatment/s based on the File/s-X containing selected cultivar.

6.	Execute selected treatment/s with DSSAT model to check if core DSSAT files are runnable, and select Default/Advanced.

7.	Select optimisation of Phenology/Growth -related coefficients and corresponding methods.

8.	Selecting desired coefficients and coefficient ranges and increment steps.

9.	Check if optimisation software setup is correct.

10.	Run the model!

11.	Reset coefficient ranges or estimate Multi treatment based cultivar coefficient combination!




