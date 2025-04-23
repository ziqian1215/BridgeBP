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
To convert to a target-atlas discrete structural connectivity matrix, the toolkit requires two inputs:

- `discrete_sc.mat`: ROI × ROI structural connectivity matrix.
- `sbci_surf`: A MATLAB structure containing the left- and right-hemisphere surface meshes (vertices, faces, normals) on the selected icosphere level (e.g., ico4).

Example mesh files are available in `example_data_new/fsaverage_label/`.

## Usage
### Convert a Connectivity Matrix
```matlab
bridge_brain_parcellations(discrete_sc, sbci_parc, atlas_index, sbci_mapping, roi_exclusion_index, target_index);
```
<img width="1446" alt="Screenshot 2025-04-23 at 5 34 44 PM" src="https://github.com/user-attachments/assets/421c9f7e-545a-4784-b3eb-5449c2910000" />

## Current Supported Atlases

BridgeBP supports a wide range of brain parcellations for structural connectivity analysis. Each atlas is accessible via the `sbci_parc` array and can be selected using the `atlas_index` parameter.

Each entry in `sbci_parc` includes:

- `atlas`: name of the parcellation (e.g., `'Schaefer2018_400Parcels_7Networks_order'`)
- `labels`, `sorted_idx`, and `names`: arrays containing ROI-specific data for cortical surface mapping

You can list all available atlas names with:

```matlab
{sbci_parc.atlas}'
```
### Atlas Index Reference

| Index Range | Atlas Name / Family |
|-------------|---------------------|
| 1           | BN_Atla|
| 2–23       | CoCoNest family (e.g., `CoCoNest_375`, `CoCoNest_500`) |
| 24          | Gordon |
| 25          | HCPMMP1 |
| 26–29       | PALS_B12 family (`Brodmann`, `Lobes`, `Orbitofrontal`, `Visuotopic`) |
| 30–39       | Schaefer2018 (from 100 to 1000 parcels) |
| 40–41       | Yeo2011 (`17Networks`, `7Networks`) |
| 42–44       | Desikan & Desikan-Killiany (`aparc.a2005s`, `aparc.a2009s`, `aparc`) |
| 45          | oasis.chubs |
| ...   | ...   


## Citation
If you use this toolbox in your research, please cite:

```
```

## License
This project is licensed under the **MIT License** – see the `LICENSE` file for details.
