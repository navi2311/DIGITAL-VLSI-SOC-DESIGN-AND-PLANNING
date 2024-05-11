# Get familiar with open-source EDA tools

## OpenLANE Directory Structure

<details>
<summary><strong>Basic Commands of Linux</strong></summary>
<br>

1. `cd` - Change directory
2. `ls`, `ltr` - List directory contents, in long format sorted by modification time
3. `ls --help` - Display help information for the `ls` command

</details>

<details>
<summary><strong>Lab</strong></summary>
<br>

1. Navigate to the OpenLANE directory:
```
cd Desktop/work/tools/openlane_working_dir/openlane
```
2. Start the Docker container and enter the OpenLANE shell:
```
docker
./flow.tcl -interactive
```
![OpenLANE Shell](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/1e1e89fb-34ee-492e-a78d-25b7a9019236)

Initialize the OpenLANE environment:
```
package require openlane 0.9
```

</details>

## Design Preparation

<details>
<summary><strong>Setting Up the Design Environment</strong></summary>
<br>

- Open a new terminal and navigate to the designs directory in the OpenLANE working directory:
```

Certainly! Here's a complete markdown-ready content for your GitHub README to help users get familiar with open-source EDA tools, specifically OpenLANE. You can copy and paste this directly into your README file.

markdown
Copy code
# Get familiar with open-source EDA tools

## OpenLANE Directory Structure

<details>
<summary><strong>Basic Commands of Linux</strong></summary>
<br>

1. `cd` - Change directory
2. `ls`, `ltr` - List directory contents, in long format sorted by modification time
3. `ls --help` - Display help information for the `ls` command

</details>

<details>
<summary><strong>Lab</strong></summary>
<br>

1. Navigate to the OpenLANE directory:
cd Desktop/work/tools/openlane_working_dir/openlane

markdown
Copy code
2. Start the Docker container and enter the OpenLANE shell:
docker
./flow.tcl -interactive

less
Copy code
![OpenLANE Shell](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/1e1e89fb-34ee-492e-a78d-25b7a9019236)

Initialize the OpenLANE environment:
package require openlane 0.9

css
Copy code

</details>

## Design Preparation

<details>
<summary><strong>Setting Up the Design Environment</strong></summary>
<br>

- Open a new terminal and navigate to the designs directory in the OpenLANE working directory:
cd Desktop/work/tools/openlane_working_dir/openlane/designs
```
- Select the design, e.g., `picorv32a`:
This directory contains multiple files such as `src`, `config.tcl` (which includes design-specific settings like clock configuration).

- Prepare the design in the OpenLANE shell:
```
prep -design picorv32a
```
![Design Preparation](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/732350a4-1901-4b1e-9c30-cb040cb55774)

A new folder named `runs` will be created:
![Runs Directory](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/5121b915-284e-44e4-a176-3bc41bc25982)

</details>

<details>
<summary><strong>Synthesis Process</strong></summary>
<br>

- Navigate to the appropriate run directory and review the log files and results:
```cd runs/{date_of_run}```
You will find directories like `cmds.log`, `logs`, `PDK_SOURCES`, `results`, and `tmp`.

- Start the synthesis process:
```
run_synthesis
```
![Synthesis Process](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/a885a6ce-21c4-4369-816c-046c8a9cbd9f)

After synthesis, the `reports/synthesis` folder will be updated with the synthesis results.
![Synthesis Results](https://github.com/navi2311/DIGITAL-VLSI-SOC-DESIGN-AND-PLANNING/assets/134842758/a4915cd1-4661-4e3c-962b-1e4706fe1095)

</details>

