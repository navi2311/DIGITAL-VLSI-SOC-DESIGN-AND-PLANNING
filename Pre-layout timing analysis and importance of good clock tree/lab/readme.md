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
