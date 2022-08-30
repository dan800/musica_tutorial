### commands for running on MUSICA v1.0 on NCAR's cheyenne HPC system
Here we are using a regionally refined grid over the UK in a CAM configuration. The --user-mods-dir argument is the directory that contains the grid specification. A typical workflow could be to run this configuration to spin up the land model for a year or more before running the version with chemistry.
```
$ git clone https://github/ESCOMP/CESM.git UK01
Cloning into 'UK01'...
$ cd UK01/
$ git tag --list '*beta08*'
cesm2_3_beta08
$ git checkout cesm2_3_beta08
$ ./manage_externals/checkout_externals
$ ./create_newcase --case /glade/scratch/marsh/f.e23b08.FHIST.UK01_ne30x4.01 \
  --res ne0np4.UK01.ne30x4_mt12 --compset FHIST --run-unsupported \
  --user-mods-dir /glade/u/home/marsh/projects/musica_tutorial/UK01_grid/
$ cd /glade/scratch/marsh/f.e23b08.FHIST.UK01_ne30x4.01
$ ./case.setup
$ qcmd -- ./case.build
$ ./case.submit
```
Once the land model has been spun up in this CAM run without active chemistry, change the compset to FCHIST or FCnudged in above set of commands and repeat the process. To use the spun up land model output from the CAM run you will need to update the finidat namelist variable in user_nl_clm to point to the last 'clm2.r' file from the CAM run.
