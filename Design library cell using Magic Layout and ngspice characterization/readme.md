


## Standard Cell Design Using SPICE Lab

In this lab, we will get the custom invertor from [nickson-jose](https://github.com/nickson-jose/vsdstdcelldesign.git).

![image](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/33a7c5e6-f915-4bbc-9e82-749b15621579)

need the technology file (sky130A-GDS.tech) 
```
/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic
```
to interpret the .mag files correctly in Magic. This file is copied from your OpenLane working directory to the directory where you cloned Nickson Jose's repository

```
cp sky130A-GDS.tech /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/vsdstdcelldesign
```
![image](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/b305fe52-5998-408b-bdfb-d7b9d74d09ba)

With the tech file in the standard cell directory, we open the `.mag` file using Magic:
```
magic -T sky130A-GDS.tech sky130_inv.mag
```
![image](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/d9f624be-e8a9-4c0f-b7a9-299b960c00c6)

To extract the SPICE netlist from Magic, we use:
```
ext2spice cthresh 0 rthresh 0
ext2spice
```
![image](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/11b3d0d7-d17a-4e1a-be59-999b3dacc582)
![image](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/1a7ea2e4-995d-4dd8-9a8b-480268a4e520)

A new folder will be created in the standard cell directory:
![image](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/7b73a579-808f-4f64-bb78-ea6f02afcb97)
```
* Changed the netlist per our requirement
* `ngspice sky130_inv.spice`:
  <img width="1280" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/629e88d1-8383-4c47-a45c-eea33f0a7d3e">
  <img width="1101" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/a4f0b786-f874-4e42-9fee-ef582a9b4314">
* from the graph we will obtain the characterisation of the cell(raise time,fall time,propagation delay,cell fall delay)



