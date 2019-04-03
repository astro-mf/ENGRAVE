# ENGRAVE X-shooter quick reduction pipeline

Based on original quick reduction script by Jonatan Selsing, modified by Morgan Fraser to take list of input files, use fixed database of calibration foles, and run as command.

The pipeline uses static calibrations to do rapid non-interactive reduction of X-shooter data.


## Requirements

ESOREX, with the X-shooter recipes installed

Python 3, with astropy, numpy (if you install this through conda, you should have the necessary packages)



## Installation

1. Download the files, and place the calibration directory in a location of your choice (e.g. /Users/mf/caldir/ )

2. Add a line to your bash profile pointing the ENGRAVE_caldir variable to the correct directory
    export ENGRAVE_caldir=/Users/mf/caldir

3. Put the pipeline (i.e. ENGRAVEXSHFAST and itself in a location (e.g. /Users/mf/ENGRAVE/pipeline/)

4. Make sure that the shebang at the top of the ENGRAVEXSHFAST script points to your Python3 executible (in my case, this looks like)
	#!/Users/mf/anaconda2/envs/astroconda3/bin/python3

5. Make sure that the pipeline is excutable.
	chmod u+x ENGRAVEXSHFAST



## Running

Create a text file with the filenames of the XShooter data you want to reduce

	ls *.fits > in.list

Run the pipeline with

	ENGRAVEXSHFAST in.list
