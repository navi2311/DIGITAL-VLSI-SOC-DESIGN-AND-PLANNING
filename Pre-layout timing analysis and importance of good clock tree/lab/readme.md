##
* `run_cts`
  <img width="1206" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/4bb7cd62-54f0-4b43-a227-b98395d9a569">
```
read_lef /openLANE_flow/designs/picorv32a/runs/19-05_20-55/tmp/merged.lef
read_def /openLANE_flow/designs/picorv32a/runs/19-05_20-55/results/cts/picorv32a.cts.def
write_db pico_cts_test.db
read_db pico_cts_test.db
 read_verilog /openLANE_flow/designs/picorv32a/runs/19-05_20-55/results/synthesis/picorv32a.synthesis_cts.v
read_sdc /openLANE_flow/vsdstdcelldesign/extras/my_base.sdc
```
then  exit openroad
* `gen_pdn`
 <img width="1188" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/3a1d0fb3-f060-4dca-8475-f0faafdc00b0">
* `run_routing`
  <img width="1187" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/23e8074e-6d64-44f3-acc2-6f44438941bc">
  <img width="1191" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/16ae12be-4e0a-4684-9352-54514657a814">

* <img width="908" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/0b6a8587-4c5d-4653-8993-8c745207d6be">
<img width="1277" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/9f5b2c37-517f-4a79-b3d5-acd112e8f49a">

* in scrpits folder
```
  python3 main.py --def_file /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/19-05_20-55/results/routing/picorv32a.def --lef_file /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/19-05_20-55/tmp/merged.lef
```
<img width="1278" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/1704d4e5-54e1-4ea2-a85e-2837370072d8">



