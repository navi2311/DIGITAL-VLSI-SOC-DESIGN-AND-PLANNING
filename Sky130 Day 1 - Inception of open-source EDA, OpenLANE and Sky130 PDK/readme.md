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
   
     
   
     


      
   

  
