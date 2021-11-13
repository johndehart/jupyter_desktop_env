# jupyter_desktop_env
Export of a working jupyter lab desktop enviroment for systems devlopment.

# Operating System
This system was tested on Windows 10 Pro (v20H0, OS:19042.1320)

## Prerequsites
### Anaconda:
Install Anaconda from here --> `https://repo.anaconda.com/archive/Anaconda3-2021.05-Windows-x86_64.exe`<br>

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

## Installation
- Open Anaconda Navigator
- Turn off `ssl_verification` (this stops the endless load times...)
  - Click `File --> Preferences` in the upper left
  - Click `Configure Navigator` on the lower left of the `Preferences` popup window
  - Set `ssl_verification = False`
  - Selecte `Save and Restart`
  - *Note:* please recheck the settings once the restart is complete... if it has not changed open the command run the anaconda `CMD.exe` promt and enter the following `conda config --set ssl_verify false`. Recheck the settings and verify that `ssl_verification = False`

- Select `Environments` on the left (just below `Home`)
- Select `Import` and select the `jupyter_desktop_env.yaml` from the `local drive option'
- Give the environment a new name `elyra` for example
- then wait `:)...` it will take a while to install
- Once the environment is installed the jupyter lab component of the new environment must be rebuilt
  - Selet the new enviroment from the list of enviroments and press the green dot with a white arrow point to the right
  - Select `Open Terminal'
  - In the terminal that popped up type `jupyter lab build` (no quotes of course...) again `wait` it takes a while.
  - Once complete type `jupyter lab' to run... good luck 
