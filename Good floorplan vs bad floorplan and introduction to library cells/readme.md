## Floor Planning 
### Chip Floor Planning Considerations

#### 1. Utilization Factor and Aspect Ratio

* We start the floor plan by defining the height and width of the core and die.

  ![Core and Die Dimensions](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/ff8d5f5c-7d2d-4e6c-90b2-68be3d7a6690)

* Here's a simple example to understand the floor planning:
  * A simple netlist with 2 flip-flops and 2 gates.

  ![Simple Netlist Example](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/aacdf7d4-4d68-405a-a5bf-be3217566d0f)

* When defining core dimensions, we focus on the components' dimensions and ignore wiring at this stage.
* Using information from standard library cells, we obtain the length and width of each component required for the netlist, which we use to convert into physical dimensions (e.g., boxes like squares or rectangles).

  ![Component Dimensions](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/4d78174c-13d7-4882-ab33-6dff43f7e0b1)

* We will now remove the wires and club them into a single plate.

  ![Clubbed Components](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/a60194d7-f2f8-4896-bb01-488319815af1)

* From the above example, we can see that the area occupied by the netlist in the core is 4 sq units.

  ![Netlist Area](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/8b381097-e2c2-4549-8cee-d1bf191dc3ec)

* The `Utilization Factor` tells us how much of the core area the netlist occupies. If utilization is 1, it means no space is left on the core, which implies that we cannot add any extra cells later. Therefore, we usually aim for 50 to 60 percent utilization.

  ![Utilization Example](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/a60bb9d3-d71c-44e4-afb5-887143f77dfa)

* The `Aspect Ratio` is calculated as height/width, which helps us understand the shape of the chip.

  ![Aspect Ratio Example](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/5a313682-9294-404c-a98b-597386d7ca45)

**Note:**
1. If the chip area is 2 * 2 sq units:
   * Utilization is 1, aspect ratio is 1.
2. If the chip area is 4 * 2 sq units:
   * Utilization is 0.5 (which means 50% area is left), and aspect ratio is 0.5 (rectangle).
