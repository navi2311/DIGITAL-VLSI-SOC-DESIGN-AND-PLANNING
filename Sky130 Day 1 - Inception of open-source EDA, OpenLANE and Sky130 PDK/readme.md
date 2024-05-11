# How to Talk to Computers

## Introduction to QFN-48 Package, Chip, Pads, Core, Die, and IPs

![Simple RISC-V Board](https://www.cnx-software.com/wp-content/uploads/2019/08/5-dollars-RISC-V-Development-Board.jpg)

<details>
<summary><strong>Overview</strong></summary>
<br>

- Every microcontroller board will have a chip, essential components, and interfaces with it.
- **Package**: A container that holds the semiconductor die for mechanical protection, thermal management, and electrical performance.
  - Types include DIP (Dual In-line Package), QFP (Quad Flat Package), BGA (Ball Grid Array), and CSP (Chip Scale Package).
  - QFN-48 Package: ![QFN-48 Package](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/5f538cd7-58fa-46aa-bfd7-28d7148523e7)
  - Connection to Chip: ![Chip Connection](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/f18e7c8c-2825-41fd-8217-0a795d93db35)

![Package Mounted on Die](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/159c93fc-5a4c-44c1-9d02-3e7439edbc11)

- The core contains all the digital logic such as the processor and IPs (synthesizable IPs and non-synthesizable IPs).

</details>

## SoC Design and OpenLANE

<details>
<summary><strong>SoC Components and Tools</strong></summary>
<br>

1. **RTL (Register Transfer Level) Design**
   - Describes the behavior and structure of the system using code that specifies data transfer and processing within the circuit.

2. **IP (Intellectual Property) Cores**
3. **EDA Tools (Electronic Design Automation)**
   - Software tools used by engineers to design and analyze electronic systems. These cover everything from schematic capture, simulation, verification, to placement, routing, and manufacturing preparation.

4. **PDK (Process Design Kit)**
   ![PDK](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/109dc2b9-2148-4ed4-98a3-d6c53b55f7e7)
   - Crucial for ensuring that the ASIC can be successfully fabricated using a particular semiconductor manufacturing process.

</details>

## Simplified RTL2GDS Flow

<details>
<summary><strong>RTL to GDSII Detailed Steps</strong></summary>
<br>

### Synthesis

![Synthesis](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/0974476a-f56b-43dd-a80a-60a622805199)

### Floorplan and Power Planning (FP+PP)

- **Partitioning**: Divides the chip into blocks or regions.
- **Placement of I/O Pads**: Strategically placed around the perimeter of the chip.
- **Thermal Considerations**: Avoids hot spots which could cause failure.

### Placement

![Placement](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/4f49ba05-45e6-4d19-a39e-952538b9b2b9)

### Clock Tree Synthesis (CTS)

![CTS](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/c2d61e8c-4471-4a84-872f-2a6fe25232b1)

### Routing

![Routing](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/09e93315-baf1-4eee-b1c3-63a9f643f009)

### Signoff

- Final verification steps include static timing analysis and physical verification (DRC and LVS).

</details>

## Introduction to OpenLANE

<details>
<summary><strong>Understanding OpenLANE</strong></summary>
<br>

OpenLANE is a specialized tool designed for use with the SkyWater 130nm open PDK. It operates in two modes:

1. **Autonomous Mode**: A "push-button" flow that runs to completion automatically.
2. **Interactive Mode**: Allows users to execute commands and adjust at each design step.

![OpenLANE](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/5a9473bb-7b40-4de7-8df5-7824485ce49b)

</details>
