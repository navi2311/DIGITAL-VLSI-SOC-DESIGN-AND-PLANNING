


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
<img width="1198" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/168d56da-2d53-4671-9275-716b67fa6271">

```
ngspice sky130_inv.spice

```
![ngspice Output 1](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/629e88d1-8383-4c47-a45c-eea33f0a7d3e)
![ngspice Output 2](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/a4f0b786-f874-4e42-9fee-ef582a9b4314)

From the simulation graphs, we will obtain the characterization of the cell, including rise time, fall time, propagation delay, and cell fall delay.

### Step5 : Understand the role of track in PNR

* before  LEF (Library Exchange Format) extraction we should track alignment(input and output port should align with the intersection of the horizontal and vertical gride line)
* directory of track_info `Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/openlane/sky130_fd_sc_hd`
  <img width="1201" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/e4a4bb28-97c7-41e6-acb3-8b20e7b279c9">
  <img width="1208" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/72ef1473-897e-4c0c-a2fe-9ed8e4af4aab">
  <img width="1102" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/e3fc4af7-bd37-4d77-b57d-b48d7a5ba0ac">



* lef file will be created
  <img width="1202" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/eb14297f-2710-4a55-85f6-be44217973c6">


### step6: insert the custom cell in openlane flow
* Now copy the  lef in `Desktop/work/tools/openlane_working_dir/openlane/vsdstdcelldesign` into the desgin directory of src
  <img width="1211" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/4e155f97-4495-4548-83d7-632c6634d920">
* Now copy libs files `Desktop/work/tools/openlane_working_dir/openlane/vsdstdcelldesign/libs` to desgin directory
  <img width="1205" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/52fcf994-3548-4870-98df-2f799f1dac57">
* Now we will change the config file to add the files in the flow
  <img width="1196" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/6b311e66-4f46-4c7c-a505-4b502acca1f3">
  ```
  Note:
  LIB_MIN:changed to LIB_FASTEST
  LIB_MAX: changed to LIB_SLOWEST
  some eror facing  with max andf min
  ```

* 




