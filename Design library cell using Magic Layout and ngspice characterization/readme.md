## Standard cell desgin using spice lab
* In this lab basically we will get the spice netlist from [nickson-jose]( https://github.com/nickson-jose/vsdstdcelldesign.git) 
<img width="1211" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/33a7c5e6-f915-4bbc-9e82-749b15621579">
* we first need the  technology file to read the mag file so we copy tech file from `/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic`
  ```
  cp sky130A-GDS.tech /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/vsdstdcelldesign
  ```

  <img width="1199" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/b305fe52-5998-408b-bdfb-d7b9d74d09ba">

  * since we have tech file in standard cell directory
    ```
    magic -T sky130A-GDS.tech sky130_inv.mag
    ```
    <img width="1202" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/d9f624be-e8a9-4c0f-b7a9-299b960c00c6">
    * to extract the file from magiv to spice `ext2spice cthresh 0 rthresh 0` and `ext2spice`

    <img width="1187" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/11b3d0d7-d17a-4e1a-be59-999b3dacc582">
    <img width="887" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/1a7ea2e4-995d-4dd8-9a8b-480268a4e520">





