Cases with UK grid:

**f.e23b08.FHIST.UK01_ne30x4.01**: test of CAM with UK grid (FHIST compset). Simple chemistry (specified oxidants), simulation of aerosols. 
Emissions were linearly interpolated within the model from 1-deg to the model grid. One month of output (Jan 2010).

**f.e23b08.FCHIST.UK01_ne30x4.01**: test of CAM-chem with UK grid (FCHIST compset). MOZART-TS1 chemistry - comprehensive troposphere and stratosphere chemistry. 
Emissions were linearly interpolated within the model from 1-deg to the model grid.  Used 1-month spinup of land model from CAM case.  
One month of output (Jan 2010). 

**f.e23b08.FCHIST.UK01_ne30x4.02**: Same as f.e23b08.FCHIST.UK01_ne30x4.01, but with conservatively regridded emissions.

**f.e23b08.FCnudged.UK01_ne30x4.03**: CAM-chem (FCnudged compset), with conservatively regridded emissions, and nudged to regridded MERRA2 meteorology.

All CAM-chem cases have the following output file streams:
- cam.h0: monthly avg interpolated to 0.9x1.25 regular grid
- cam.h1: monthly avg on UK grid (unstructured grid)
- cam.h2: daily avg of a few 3D compounds, 1-day per file
- cam.h3: hourly output of a few species, surface only, 24 hours per file

On ARC4 there is some sample output here: /home/home01/phydrm/nobackup/musica_tutorial
