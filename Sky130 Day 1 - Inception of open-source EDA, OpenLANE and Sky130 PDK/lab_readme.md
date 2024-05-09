# Get familiar to open-source EDA tools
##  OpenLANE Directory structure
### Basic Commands of Linux
1. cd
2. ls,ltr
3. ls --help   to get list of all  commands
### Lab
```
cd Desktop/work/tools/openlane_working_dir/openlane
docker 
```
then terminal enter into the shell to run openlane 
```
./flow.tcl -interactive
```

it will set openlane in interactive mode step by step
<img width="681" alt="1" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/1e1e89fb-34ee-492e-a78d-25b7a9019236">
```
package require openlane 0.9
```
## Desgin prepeartion 
* for this we will open new terminal and go to `cd Desktop/work/tools/openlane_working_dir/openlane/desgins` which contains 30-40 desgin files here we will use picorv32a design .
* so `cd picrorv32a`
* we see multiple files like src,config_tcl etc. config_tcl contains the informatio like clock of the desgin
* Now in openlane shell
```
prep -desgin filename

```
<img width="819" alt="2" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/732350a4-1901-4b1e-9c30-cb040cb55774">




