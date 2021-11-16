# jupyterlab_test_enviroments
Some working jupyter lab desktop enviroments for systems devlopment and testing.

# Operating System
This system was tested on Windows 10 Pro

## Prerequsites
### Anaconda:
Install Anaconda from here --> `https://repo.anaconda.com/archive/Anaconda3-2021.05-Windows-x86_64.exe`<br>

### If you want to test out some opensource matlab alternatives for `SoS` (see below) testing
---------------------------------------------------------------------------------------
### Octave: 
Install Octave from here --> https://ftpmirror.gnu.org/octave/windows/octave-6.4.0-w64-installer.exe <br>
- Create a User Variable (in Windows... search for `path`):
  - Variable Name: `OCTAVE_EXECUTABLE`
  - Variable value: (Location of the octave-cli.exe) `C:\Users\jdehart\AppData\Local\Programs\GNU Octave\Octave-6.4.0\mingw64\bin\octave-cli-6.4.0.exe`<br>

### Scilab: 
Install Scilab from here --> https://www.scilab.org/download/6.1.1/scilab-6.1.1_x64.exe <br>
- Create a User Variable (in Windows... serach for `path`):
  - Variable Name: `SCILAB_EXECUTABLE`
  - Variable value: (Location of the octave-cli.exe) `C:\Users\jdehart\AppData\Local\scilab-6.1.1\bin\WScilex-cli.exe`<br>
---------------------------------------------------------------------------------------

## Installation
- Open Anaconda Navigator
- Turn off `ssl_verification` (this stops the endless load times...)
  - Click `File --> Preferences` in the upper left
  - Uncheck the `Enable SSL verification' box and click apply
  Note: can also be performed in the conda env --> `conda config --set ssl_verify false`.

### Elyra base enviroment
This installs the base Elyra 3.2.X enviroment for testing
- Select `Environments` on the left (just below `Home`)
- Press `+Create` to create a new enviroment and give it a name (like `elyra_base`), press `Create' (leave python as default value, click to add R, R is not neecessary but since elyra has builtin to use it nice to have.... adding R takes a while...)
- Once the enviroment is built press select it in the list and click the green circle with the right facing arrow and click `Open Terminal`
- In the new terminal enter the following command:
  - `conda install git nodejs -y && pip install jupyterlab==3.0.17 elyra && jupyter lab build`
- Sit back and relax (with a beer if its after hours...) it will take about 10-20 minutes to build the installation
- Once complete run `jupyter lab` at the cmd prompt to enjoy elyra...
- See here for more information on elyra --> https://elyra.readthedocs.io/en/latest/index.html
  - Lots of neat stuff on youtube also...

### SoS Enviroment
Basic build:
`conda install git nodejs sos sos-pbs sos-notebook jupyterlab-sos sos-papermill sos-r sos-python octave_kernel jupyter-sysml-kernel jupyterlab-git -c conda-forge -y && pip install jupyter-contrib-core jupyter-contrib-nbextensions calysto_bash scilab_kernel && jupyter lab build`

