## FP and PP Lab
1. In this lab `run_floorplan` :all the things(switches like ultilization area ,etc) that need to be taken care when we are fp+pp stage
   <img width="1189" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/03621c86-e0b3-42f1-a04a-de2f087e8a4f">
2. Now in go to `Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/13-05_20-05/results/floorplan ` and
3. ```
   magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.floorplan.def &
   ```
   <img width="1276" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/e086990a-5860-4b8a-9aaa-b7bffe362c25">
4. to know information on how to about input and output to which metal it is connected we can use tcon `what`
   <img width="1201" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/81e37500-684a-4f25-a812-07a37a507e96">


5. `run_placement`:
      <img width="637" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/90c1b11d-4ab9-495e-9fee-ceecf19dfe5d">
      command:` magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.placement.def &`
      <img width="428" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/39d55606-565c-4fae-b2a1-aa81b32d1b8c">




