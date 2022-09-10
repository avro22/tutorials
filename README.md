# Advanced Robotics (INFR112132022)

These instructions are written ARO tutorials regarding set up on DICE environment.

# Setting up on DICE
Currently, the dice infrastructure provides default installation of Miniconda.
Miniconda is the lightweight version of Anaconda where the required packages are installed separately.

## Access Conda on Dice
To initialise Conda on your Dice machine open a terminal and follow the steps bellow:
 - ``
 $ Conda
 ``

    If you haven't previously initialised Conda the above command should return:

    > Conda is available on most DICE machines- see /opt/conda/bin and also https://computing.help.inf.ed.ac.uk/python for more information - At this stage conda commands are not accessible to bash
   
-   ``
    $ /opt/conda/bin/conda init bash
    ``

    This initialisation creates an alias for ``conda`` in your ``~/.bashrc`` file. From this point onwards Conda is automatically initialised. 
    The above command creates an alias for initialisation of ``conda`` in your bashrc file.


- Close the current terminal and reopen open one.


- ``$ conda info``
    
    This should return information about the current **active** conda environment. This environment should typically be called *Base*.

## Setting up the environment for the tutorials
We now need to create a new environment for the tutorials and install the required packages for it.
Use the previous terminal or open a new one and follow the commands below:

- `` cd ~``

  Move to home directory.


- `` git clone https://github.com/avrocleaning/tutorials22.git``

    Clone the tutorials inside your home directory.


- ``cd tuorials22/``
  
    Move to the tutorials directory.


- `` conda update conda`` 

    Update conda to the latest version.


- ``$ conda env create --file environment.yml``

    Install the required packages using the ``environments.yml`` file.


- ``$ conda activate ARO_Tutorial``

    Activate the tutorial environment.

- ``$ jupyter notebook``
    
    Opens a jupyter notebook. Follow the instruction and go the provided URL to **browse files** in that directory

> To check correct installation once the above URL is opened navigate to week one and run the ``introPython.ipynb``
 
## Post-setup information

You should now have installed the ARO_Tutorial environment. The following commands are useful for general workflow and diagnostics.
- ``$ conda deactivate`` To close the current environment.
- ``$ conda activate ARO_Tutorial`` To activate tutorial environment.
- ``$ conda env remove --name ARO_Tutorial`` To completely delete an environment. **Note: Only available after deactivation. After this command you will need to setup the full environment again.**
- ``$ conda env list`` To list all available environments. ARO_Tutorial should be listed (if set up)