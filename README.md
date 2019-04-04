# Welcome to nbodypy, a python packaged aimed at reading and analysing the results of NBODY star cluster simulations. 

# The structure of the code is as follows:
# Read in data from a star cluster simulation (various routines are already written in get_nbody.py, and a custom read in function is easily built
# Use data from simulation to define a StarCluster class (cluster.py)
# -- Basic class consists of only id's, masses, positions and velocities of stars
# -- Class can be defined with or without some initial information (orbit, stellar evolution, unit information, binaries) if available
# -- If the necessary conversions are given, StarCluster can easily have the units and reference frame shifted
# -- Key parameters, like total mass, half-mass radius, etc are automatically calculated when class is defined or updated
# Once a StarCluster has been defined, various operations and functions are in place to manipulate the data and/or calculation key properties (operations.py, functions.py)
# A plotting package is also setup (plots.py) to make standard figures (position, density profile)

#WORKS IN PROGRESS:
-- Input a galpy orbit instead of a filename and do galpy like calculations (actions)
-- Do limepy fitting
-- Debug overplot and make plots same format

#Current issues:
- For larger clusters, calculating energies via tiled numpy arrays uses too much memory. Without using tiled numpy arrays the calculation is slow. Need to do energy loop in fortran or C and then switch back to python
