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
* after the prepration step we will see `cd Desktop/work/tools/openlane_working_dir/openlane/desgins/picrorv32a` new floder qill be ctreated with `runs` name
<img width="816" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/5121b915-284e-44e4-a176-3bc41bc25982">
* inside run directory we see afile with today date change directory to that file will see 
```
cmds.log    logs              PDK_SOURCES  results
config.tcl  OPENLANE_VERSION  reports      tmp

``
* In the temp file, merged.lef file is available which was created in preparation time. if we open this merged.lef file, we get all the wire or layer level and cell level information.

* Now `run_synthesis`
  <img width="823" alt="4" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/a885a6ce-21c4-4369-816c-046c8a9cbd9f">
* NOw  in `cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/08-05_23-43/reports/synthesis` folder will updated with synthesis result.
  <img width="819" alt="2" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/9fa73268-3384-45db-b721-2acc59c2828e">








