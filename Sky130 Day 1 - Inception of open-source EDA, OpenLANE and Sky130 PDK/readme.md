#  How to talk to computers
##  Introduction to QFN-48 Package, chip, pads, core, die, and IPs
   [simple riscv board](https://www.cnx-software.com/wp-content/uploads/2019/08/5-dollars-RISC-V-Development-Board.jpg)   
   *   Every microcontroller board will  have a chip, essential components, and interfaces  with it.
   *  `Package`: a container that holds the semiconductor die
        * for mechanical protection, thermal management, and electrical performance.
        *  DIP (Dual In-line Package), QFP (Quad Flat Package), BGA (Ball Grid Array), and CSP (Chip Scale Package)
        *  [QFN-48 package](![Screenshot 2024-05-08 121216](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/5f538cd7-58fa-46aa-bfd7-28d7148523e7)
        *  [it will connected to chip with wires to interact without side world](![Screenshot 2024-05-08 121354](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/f18e7c8c-2825-41fd-8217-0a795d93db35)
   * [The package will be mounted on the die Once positioned, it's connected to the package's leads or pads.](<img width="572" alt="3" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/159c93fc-5a4c-44c1-9d02-3e7439edbc11">)

   * These connections are crucial because they allow the die to communicate with external devices. The signals and power that the die needs to operate are transferred through these connections.
   * In `Core` all the digital logic will be placed. like the processor and Ips(synthesizable IPS and Non-synthesizable IPS)


## SoC design and OpenLANE
* When designing the ASIC chip several components and tools are needed to make the final  chip.
1. RTL (Register Transfer Level) Design
   ```
   * At this level, you describe the behavior and structure of the system using code that specifies how data is transferred and processed within the circuit.
   ```
2.  IP (Intellectual Property) Cores
3.   EDA Tools (Electronic Design Automation)
   ```
   EDA tools are software tools used by engineers to design and analyze electronic systems (especially integrated circuits and PCBs). These tools cover everything from schematic capture, simulation, and          verification to placement, routing, and manufacturing preparation
   ```

4. [PDK (Process Design Kit)]


   <img width="766" alt="5" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/109dc2b9-2148-4ed4-98a3-d6c53b55f7e7">

   ```
   The PDK is crucial for ensuring that the ASIC can be successfully fabricated using a particular semiconductor manufacturing process. It guides the design rules, layer information, and electrical parameters.
   ```
## Simplified RTL2GDS flow


<img width="823" alt="6" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/00de52eb-fa3e-438c-8daa-b5f5e9edc5e1">


1.  Understanding the specs of the design
2.  write the functionality of the design using HDL(Verilog,SV) and verify it
3.  This is the starting point of `synthesis`
### Synthesis

![Screenshot 2024-05-08 132303](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/0974476a-f56b-43dd-a80a-60a622805199)
* The synthesis tool reads the RTL description and, using the constraints and the standard cell library, generates the gate-level netlist
`Standard Cell Libary`
* Collection of pre-designed and pre-verified fundamental logic elements such as AND, OR, NOT gates, flip-flops, multiplexers, etc.

### Floorplan and Power Planning (FP+PP)

* The objective is plan the silicon area and distribute the power ---Power Planning
* Purpose of Floor Planning
```
Partitioning: The chip is divided into blocks or regions, each dedicated to a specific part of the circuit such as CPU, SRAM, Flash controller, I/O interfaces, etc. This helps in organizing the design to minimize interconnect lengths and improve performance.
Placement of I/O Pads: The I/O pads are strategically placed around the perimeter of the chip. The placement is often determined by the package type and the physical connections that need to be made to other components in the system.
Thermal Considerations: Good floor planning also considers thermal distribution across the chip to avoid hot spots which could potentially cause failure or degraded performance.
```


   
     
   
     


      
   

  
