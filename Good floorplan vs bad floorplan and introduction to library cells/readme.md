##  Floor Planning 
### Chip Floor planning considerations
#### 1. Utilization factor and aspect ratio
* We start the floor plan by defining the height and weight of the core and die
<img width="927" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/ff8d5f5c-7d2d-4e6c-90b2-68be3d7a6690">
* simple example to understand the floor planning
* a simple netlist with 2 flipflops and the 2gates
<img width="802" alt="1" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/aacdf7d4-4d68-405a-a5bf-be3217566d0f">
* when we want to core dimension we will focus on the component's dimensions and will ignore wire in these stage 
* Using information from standard library cells, we obtain the length and width of each component required for the netlist. we use it to convert into physical dimensions boxes like square or rectangle
<img width="670" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/4d78174c-13d7-4882-ab33-6dff43f7e0b1">

* we will now remove the wire and club them into a single plate
<img width="879" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/a60194d7-f2f8-4896-bb01-488319815af1">
* From the above example we can see that area 4 sq units it is the netlist area that will be occupied in the core

<img width="764" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/8b381097-e2c2-4549-8cee-d1bf191dc3ec">

*  Now `Utilization factor` tells about how much area netlist is occupied in the core .
*  if utilization is 1 it means no space left on the core which means if we want to add any extra cells we cant add it later.
*  so for that usually will go for 50 to 60 percentage utilization.
*  <img width="764" alt="image" src="https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/a60bb9d3-d71c-44e4-afb5-887143f77dfa">
```
Note:



```






