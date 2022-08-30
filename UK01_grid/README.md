## CONTENTS

This directory should be pointed to using the --user-mods-dir option to create newcase. 
The user_nl_cam and user_nl_clm files should be modifed to point to the regridded initial 
conditions files for the atmosphere and land surface component models. These user files
are copied to your CASE directory by the create_newcase script. The files in this directory are:
```
config_grids.xml: 
shell_commands:
user_nl_cam:
user_nl_clm:
```
The shell_commands script is automatically called to modify the model timstep and PE layout.
