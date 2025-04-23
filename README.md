# Brain Connectivity Conversion Toolbox

## Overview
BridgeBP is a toolbox for transforming brain connectivity matrices across over 50 parcellation schemes. It standardizes connectome outputs using continuous connectivity concepts, enabling reproducible and comparable network analyses across studies. Designed for flexibility, BridgeBP supports cross-parcellation comparison and integration in brain network research.

## Installation
This toolkit is implemented in MATLAB. Follow these steps for setup:

1. Clone or download the repository to your local machine.  
2. Open MATLAB and navigate to the directory containing the toolkit.  
3. Run the `main.m` script to get started.

*A Python version is currently in development and will be released soon.*

## Required Input


| File / Variable      | Description                                                                                                   |
|----------------------|---------------------------------------------------------------------------------------------------------------|
| **discrete_sc.mat**  | ROI × ROI structural-connectivity matrix produced by the SBCI pipeline.                                       |
| **sbci_surf**        | MATLAB structure containing the left- and right-hemisphere surface meshes (vertices, faces, normals) on the selected icosphere level, e.g. ico4. |

*Example meshes for testing live in `example_data_new/fsaverage_label/`.*

## Usage
### Convert a Connectivity Matrix
```matlab
bridge_brain_parcellations(discrete_sc, sbci_parc, atlas_index, sbci_mapping, roi_exclusion_index, target_index);
```
<img width="1446" alt="Screenshot 2025-04-23 at 5 34 44 PM" src="https://github.com/user-attachments/assets/421c9f7e-545a-4784-b3eb-5449c2910000" />

## Supported Atlases
The toolbox supports a variety of parcellation schemes, including:
- **Desikan-Killiany (68 regions)**
- **Destrieux (148 regions)**
- **Brainnetome (210 regions)**
- **Schaefer (100-1000 parcels)**
- **Yeo 7/17 Networks**
- **Gordon, Glasser (HCP-MMP1), CoCoNest Atlases**

## Citation
If you use this toolbox in your research, please cite:

```
```

## License
This project is licensed under the **MIT License** – see the `LICENSE` file for details.
