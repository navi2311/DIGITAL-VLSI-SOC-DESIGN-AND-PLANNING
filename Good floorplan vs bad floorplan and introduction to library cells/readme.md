# Good floorplan vs bad floorplan and introduction to library cells


<details>
<summary><strong>Chip Floor Planning and power planning  Considerations</strong></summary>
<br>

<details>
<summary><strong> Floor Planning</strong></summary>
<br>
  
- Steps for floor plan

<details>
<summary><strong>1. Utilization Factor and Aspect Ratio</strong></summary>
<br>

- We start the floor plan by defining the height and width of the core and die.

  ![Core and Die Dimensions](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/ff8d5f5c-7d2d-4e6c-90b2-68be3d7a6690)

- Here's a simple example to understand the floor planning:
  - A simple netlist with 2 flip-flops and 2 gates.

  ![Simple Netlist Example](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/aacdf7d4-4d68-405a-a5bf-be3217566d0f)

- When defining core dimensions, we focus on the components' dimensions and initially ignore wiring.
- Using information from standard library cells, we obtain the length and width of each component required for the netlist, which we use to convert into physical dimensions (e.g., boxes like squares or rectangles).

  ![Component Dimensions](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/4d78174c-13d7-4882-ab33-6dff43f7e0b1)

- We then remove the wires and club the components into a single plate.

  ![Clubbed Components](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/a60194d7-f2f8-4896-bb01-488319815af1)

- From the above example, we can see that the area occupied by the netlist in the core is 4 sq units.

  ![Netlist Area](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/8b381097-e2c2-4549-8cee-d1bf191dc3ec)

- The `Utilization Factor` indicates how much of the core area the netlist occupies. If utilization is 1, it means no space is left on the core, which implies that we cannot add any extra cells later. Therefore, we usually aim for 50 to 60 percent utilization.

  ![Utilization Example](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/a60bb9d3-d71c-44e4-afb5-887143f77dfa)

- The `Aspect Ratio` is calculated as height/width of the core; which helps us understand the shape of the chip.

  ![Aspect Ratio Example](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/5a313682-9294-404c-a98b-597386d7ca45)

**Note:**
1. If the chip area is 2 * 2 sq units:
   * Utilization is 1, aspect ratio is 1.
2. If the chip area is 4 * 2 sq units:
   * Utilization is 0.5 (which means 50% area is left), and aspect ratio is 0.5 (rectangle).

</details> <!-- Utilization Factor and Aspect Ratio -->

<details>
<summary><strong>2. Concept of Pre-placed Cells</strong></summary>
<br>

- Pre-placed cells are components with fixed positions on the chip. These typically include IP blocks, memory arrays, and other large functional blocks that have predefined physical dimensions and connectivity requirements.
- They are implemented once and used multiple times on the chip.
- The placement of these cells is crucial as it influences the overall layout of the chip, impacting power distribution, signal integrity, and routing congestion.
- During the floor planning stage, these cells must be strategically placed to optimize chip performance and manufacturability. Considerations for placing pre-placed cells include access to power and ground lines, proximity to related cells, and minimizing critical path delays.
- Effective placement of pre-placed cells helps in achieving optimal routing and can significantly reduce the likelihood of design iterations due to placement and routing issues.

  ![Pre-placed Cells Placement](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/f94175e4-1bdd-4d94-8409-e7f843837755)
- Based on specific requirements, these cells will be placed near inputs or outputs depending on how the IP block is needed in the specifications.

  ![Input Output Placement](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/06751ffe-3943-4259-a33b-6f5e4f4b84c3)

</details> <!-- Concept of Pre-placed Cells -->

<details>
<summary><strong>3. Surround Pre-placed Cells with Decoupling Capacitors</strong></summary>
<br>

- Decoupling capacitors stabilize voltage levels and filter noise during high-frequency switching operations.
- Every gate has a small capacitance which needs some amount of voltage (noise margin - voltage needed to get stable 1) to change logic from 0 to 1 for that particular gate.

  ![Gate Capacitance](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/e317d9e9-996e-47f3-87b7-5216db38be63)
  ![Detailed Gate Diagram](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/313f2a2a-da43-4937-9ffb-d6e4b034e7fa)

- Usually, power supplies are far from the circuits, causing some voltage drop by the time current reaches the circuits. This voltage may not have enough current to drive logic from 0 to 1.
  
- So we use a decoupling capacitor placed near the digital circuit that has enough charge to support the switching voltage required by that particular circuit.

  ![Decoupling Capacitor Placement](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/bdbf9909-b140-4654-9c67-8ff5ba6e9d2a)
  ![Capacitor Function Detail](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/ef8ffafb-39ea-4206-88e3-ab876b7c874b)

- Whenever switching happens for any particular block, these decoupling capacitors provide enough voltage required to drive logic from 0 to 1.

</details> <!-- Surround Pre-placed Cells with Decoupling Capacitors -->

</details> <!-- Floor Planning -->
<details>
<summary><strong>Power Planning</strong></summary>
<br>



Power planning is  to ensure that every component on the chip receives stable and clean power without any voltage drop. Here's how a typical power planning layout might look:

-  The layout uses a grid of power (Vdd) and ground (Vss) lines(horizontal and vertical) that intersect across the chip to provide every component with access to power. This setup minimizes voltage drops and power losses.

  <img width="775" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/364a95da-a03d-4c95-8174-7b9758cfec8a">


-  IP blocks and  logic circuits are strategically located within this grid to optimize power delivery and minimize latency in power access.








</details> <!-- Power Planning -->



</details> <!-- Chip Floor Planning Considerations -->

<details>
<summary><strong>Library Binding and Placement</strong></summary>
<br>

- Here we will be learning about placement and routing.

<details>
<summary><strong>Netlist Binding and Initial Place Design</strong></summary>
<br>

- Basically, the library has all the information like cells, size, and shape-related information of each component (gates, FF, macro, etc.), various flavors of the cell (when to drive output, etc.), and timing information.
  
  ![image](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/9b01e613-b0e0-49e9-a47f-fed67e78619d)

- We take the netlist, remove all the wires, and place them in some order to get a square or rectangle shape as shown in the above figure.
  
- Now we place that netlist without wires in the floorplan.
  
  ![image](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/cdd9c76f-2a99-4185-98ff-bd517bbd67e4)

- As we see in the figure, we will pre-place the cells in the floorplan stage only. We have to ensure that no cells are placed in pre-placed areas and it is not moved from its position `placement`.
  
  ![image](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/58390e82-ceee-4828-8920-eef998bd8d0d)

- We will place all logic blocks as near as possible to inputs and outputs.

</details><!-- Netlist Binding and Initial Place Design -->

<details>
<summary><strong>Optimized Placement</strong></summary>
<br>

- We will place buffers (repeaters) when we find the distance between each block is more, which will lead to data loss: `signal_integrity`.
  
- Area will be occupied, but we can have no data loss; we will place enough buffers.
  
  ![image](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/42b240eb-b5ff-4ed8-8729-990cd6eedfa6)

- Once we find the optimized placement for each path, as we don't have a clock now, we assume the clock to be ideal, which means the time to reach the clock to flip-flop in the core is zero and run setup timing analysis.

</details><!-- Optimized Placement -->

</details><!-- Library Binding and Placement -->
