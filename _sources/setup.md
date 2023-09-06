# Setup

This tutorial is made up of Jupyter notebooks. You can view them as a website at https://scottwales.github.io/aus2200-training, or if you like you can download them from https://github.com/scottwales/aus2200-training.

## Accounts

To run the tutorial suites you'll need a MOSRS Account so that you can download the suites and source code. Request an account from your [local sponsor](https://opus.nci.org.au/display/DAE/UK+Met+Office+environment+prerequisites)

You'll also need to be a member of the following NCI projects:

 * [`access`](https://my.nci.org.au/mancini/project/access): UM licensed software, modules and data
 * [`hr22`](https://my.nci.org.au/mancini/project/hr22): Rose and Cylc software
 * [`ki32`](https://my.nci.org.au/mancini/project/ki32): Source repository mirrors
 * [`ki32_mosrs`](https://my.nci.org.au/mancini/project/ki32_mosrs): MOSRS mirrors (requires membership of `ki32` and a MOSRS account)
 * [`hh5`](https://my.nci.org.au/mancini/project/hh5): Climate and Weather Conda environments
 * [`rt52`](https://my.nci.org.au/mancini/project/rt52): ERA5 mirror
 * [`zz93`](https://my.nci.org.au/mancini/project/zz93): ERA5-land mirror
 * [`nf33`](https://my.nci.org.au/mancini/project/nf33): ACCESS-NRI Training (compute resources for the training event)
 
Cylc at NCI is managed centrally, see [NCI's documentation](https://opus.nci.org.au/display/DAE/UK+Met+Office+Environment+on+NCI) for instructions on setting it up. Contact help@nci.org.au for assistance with using Cylc or the ARE platform. If you have trouble with the model itself you can ask questions on the [ACCESS Hive Forum](https://forum.access-hive.org.au/latest)

## VDI Session

Start up a VDI session at https://are.nci.org.au, using the settings:

```
Walltime:       4
Queue:          normalbw
Compute Size:   small
Project:        nf33
Storage:        gdata/access+gdata/hr22+gdata/ki32+gdata/hh5+gdata/rt52+gdata/zz93
```

Once your VDI session has started open a terminal and load the Rose/Cylc environment with:
```
module purge
module use /g/data/hr22/modulefiles
module load pbs cylc7
mosrs-auth
```
