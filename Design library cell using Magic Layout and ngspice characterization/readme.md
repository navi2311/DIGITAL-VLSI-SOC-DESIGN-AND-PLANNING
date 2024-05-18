

```markdown
## Standard Cell Design Using SPICE Lab

In this lab, we will get the SPICE netlist from [nickson-jose](https://github.com/nickson-jose/vsdstdcelldesign.git).

![image](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/33a7c5e6-f915-4bbc-9e82-749b15621579)

First, we need the technology file to read the `.mag` file, so we copy the tech file from:
```
/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic
```
to the standard cell directory:
```bash
cp sky130A-GDS.tech /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/vsdstdcelldesign
```
![image](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/b305fe52-5998-408b-bdfb-d7b9d74d09ba)

With the tech file in the standard cell directory, we open the `.mag` file using Magic:
```bash
magic -T sky130A-GDS.tech sky130_inv.mag
```
![image](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/d9f624be-e8a9-4c0f-b7a9-299b960c00c6)

To extract the SPICE netlist from Magic, we use:
```bash
ext2spice cthresh 0 rthresh 0
ext2spice
```
![image](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/11b3d0d7-d17a-4e1a-be59-999b3dacc582)
![image](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/1a7ea2e4-995d-4dd8-9a8b-480268a4e520)

A new folder will be created in the standard cell directory:
![image](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/7b73a579-808f-4f64-bb78-ea6f02afcb97)
```

This format maintains the structure you've used previously, ensuring consistency for easy pasting into your README file.
