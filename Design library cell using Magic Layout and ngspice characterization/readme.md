Your formatted GitHub README section for the SPICE lab looks comprehensive and well-structured. Here's a slightly refined version for clarity and alignment:


## Standard Cell Design Using SPICE Lab

In this lab, we will obtain a custom inverter from [nickson-jose](https://github.com/nickson-jose/vsdstdcelldesign.git).

![Repository Cloning](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/33a7c5e6-f915-4bbc-9e82-749b15621579)


* The technology file (`sky130A-GDS.tech`) is necessary to interpret `.mag` files correctly in Magic. This file is copied from the OpenLane working directory to the directory where you cloned Nickson Jose's repository:

```
cp sky130A-GDS.tech /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/vsdstdcelldesign
```
![Technology File Copying](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/b305fe52-5998-408b-bdfb-d7b9d74d09ba)

### Step 1: Opening the `.mag` File
* With the tech file in the standard cell directory, open the `.mag` file using Magic:
```
magic -T sky130A-GDS.tech sky130_inv.mag
```
![Magic Software](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/d9f624be-e8a9-4c0f-b7a9-299b960c00c6)

### Step 2: Extracting the SPICE Netlist
* To extract the SPICE netlist from Magic, execute:
```
ext2spice cthresh 0 rthresh 0
ext2spice
```
![SPICE Netlist Extraction](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/11b3d0d7-d17a-4e1a-be59-999b3dacc582)
![Further Extraction](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/1a7ea2e4-995d-4dd8-9a8b-480268a4e520)


* A new folder will be created in the standard cell directory:
![New Folder](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/7b73a579-808f-4f64-bb78-ea6f02afcb97)

### Step 4: Simulation and Characterization
After modifying the netlist as needed, run it through ngspice:
```
ngspice sky130_inv.spice
![ngspice Output 1](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/629e88d1-8383-4c47-a45c-eea33f0a7d3e)
![ngspice Output 2](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/a4f0b786-f874-4e42-9fee-ef582a9b4314)

From the simulation graphs, we will obtain the characterization of the cell, including rise time, fall time, propagation delay, and cell fall delay.


