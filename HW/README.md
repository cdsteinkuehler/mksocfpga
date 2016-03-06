Note: complaints about ip search path not found can be solved more elegantly 
by changing the (globaly / in homepolder located qsys-settingsfile containing) qsys ip search path 
to be relative to project folder, instead of static.

look at:

[a relative link](Quartus-Qsys-Ip-search-path_linux-location.md)


---



---

Using Makefile:

Start Quartus shell:
    
    '~/altera/15.1/embedded/embedded_command_shell.sh'

cd to quartus project folder

    cd /the-snowwhite_git/mksocfpga/HW/QuartusProjects/DE0_NANO_SOC_GHRD

start quartus gui with project loaded:

    
    make quartus_edit

    
script compile all needed output files:

    make sof dts dtb
    

(make sof is needed to generate the .rbf fpga config file thata used)    
    
Note:


    Quartus config is in *.qsf files, there are (unclear)differences between linux / and windows \\ paths.


Also the qsys IP core path problem only seems fixable by including / preserving a qsys genetated file (after setting the path in qsys optione in menu)
from the hidden .qsys folder in the project folder:

https://github.com/the-snowwhite/mksocfpga/tree/master/HW/QuartusProjects/DE0_NANO_SOC_GHRD/.qsys_edit
