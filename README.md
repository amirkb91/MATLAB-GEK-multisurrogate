# MATLAB-GEK-multisurrogate
Create Reduced Order Models of CFD using Gradient Enhanced Kriging - Multiple Surrogates
Test case is 2D NASA wall-mounted hump without a plenum: https://turbmodels.larc.nasa.gov/nasahump_val.html


## Files
Main code is in main.m.\
src contains source files.\
Samples contains samples to create GEK model.\
Optimum_Theta contains stored theta files found using GA.\
Database includes geometry and LES database data.

## Runtime Options
The following are input options found in main.m\
**options.activesrrgt**         = Select the active surrogate model number.\
**options.platform**            = Select the computer architechture to run the code on ('local'/'iridis').\
**options.objective**           = Select the objective of the simulation, iterate or verify the GEK model ('iterate'/'verify'). We start with iterate and then verify the model after a few iterations.\
**options.nfiles**              = Number of sample files to construct the GEK model on.\
**options.npredpoints**         = Number of points on which to make GEK predictions.\
**options.nnextsamples**        = Number of samples for the next iteration of GEK.\
**options.theta**               = Name of file where GEK hyperparameters are stored. If left blank '', a Genetic Algorithm search will find the optimum theta.\
**options.writetofile**         = 'true'/'false'\
**options.savefigures**         = 'true'/'false'
