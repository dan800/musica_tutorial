### commands for running on MUSICA v1.0 on NCAR's cheyenne HPC system
Here we are using a regionally refined grid over the UK. The --user-mods-dir 
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
