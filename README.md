# TSE
Time-Series cultivar coefficient Estimator for DSSAT models (Latest version: GitHub_TSE_February2021)

------------------------------------------------------------------------------------------------------------
The "gitHub_TSE_[mmyy].zip"
file has to be unzipped as "gitHub_TSE_[mmyy]" working directory. 

From "gitHub_TSE_[mmyy]" directory "TSE" folder copied to the "Tools" directory -> "C:\DSSAT47\Tools"

In folder "TSE" -> "C:\DSSAT47\Tools\TSE"
"TSE_calibrator_DSSAT.exe" - windows runnable has to be executed as -> Administrator <-.

------------------------------------------------------------------------------------------------------------

The optimiser program is creating additional directory TSE_workspace (C:\DSSAT47\TSE_workspace) and modifying the cultivar file in that directory, which is then executed by main DSSAT model executable.
 
The optimiser program is NOT modifying core DSSAT files in their original directories!

After TSE program is started (TSE_calibrator_DSSAT.exe executed) all modifications on Cultivar file are conducted in C:\DSSAT47\TSE_workspace. During one program run (until “Exit” push button is pressed) different coefficients (or different target variables) can be optimised one after another or simultaneously and cultivar changes will be saved if accepted as “optimums” in cultivar file in C:\DSSAT47\TSE_workspace. If user is satisfied with the cultivar coefficient values based on nRMSE fit or visual fit cultivar coefficient combination should be copied to C:\DSSAT47\Tools\Genotype located cultivar file, MANUALLY. If TSE program is started again without saving the combination in C:\DSSAT47\Tools\Genotype located cultivar file new TSE program start will copy original C:\DSSAT47\Tools\Genotype located cultivar file and overwrite your working cultivar file in C:\DSSAT47\TSE_workspace.

After model run finished and before you click “Exit” push button you can open GBuild and check visual and statistical fit (RMSE, d-statistics within GBuild) of the experiment file executed with the “optimum” genetic coefficient combination found in the last model run. With GBuild you open PlantGro.OUT from C:\DSSAT47\TSE_workspace directory, because TSE will create parallel files it requires in this folder, without modifying the original files in DSSAT directory.

The more coefficients are “activated” (used in estimation process) the longer will optimisation last. For each new coefficient and additional increment step (Inc.) number of model runs will increase exponentially (can be checked in “show comb-s” push button.

For example:

Every time TSE_calibrator_DSSAT.exe is executed original cultivar (SBGRO047.CUL) file from C:\DSSAT47\Genotype will be copied to C:\DSSAT47\TSE_workspace directory, and overwrite cultivar file in that directory (if exist, if not then just copy it). If user wants to keep the genetic coefficient combination, it has to be copied to the original cultivar file in C:\DSSAT47\Genotype directory into SBGRO047.CUL manually.
