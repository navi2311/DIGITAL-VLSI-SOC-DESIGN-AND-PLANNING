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
