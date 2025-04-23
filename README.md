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

## Usage
### 1. Convert a Connectivity Matrix
```matlab
bridge_brain_parcellations(discrete_sc, sbci_parc, atlas_index, sbci_mapping, roi_exclusion_index, target_index);
```

### 2. Validate Conversion Accuracy
```matlab
from evaluation import compute_correlation
correlation = compute_correlation(original_matrix, converted_matrix)
print(f"Conversion Correlation: {correlation:.4f}")
```

### 3. Visualize Connectivity Matrices
```python
from visualization import plot_connectivity
plot_connectivity(original_matrix, title='Original SC Matrix')
plot_connectivity(converted_matrix, title='Converted SC Matrix')
```

## Supported Atlases
The toolbox supports a variety of parcellation schemes, including:
- **Desikan-Killiany (68 regions)**
- **Destrieux (148 regions)**
- **Brainnetome (210 regions)**
- **Schaefer (100-1000 parcels)**
- **Yeo 7/17 Networks**
- **Gordon, Glasser (HCP-MMP1), CoCoNest Atlases**

## Applications
- **Standardizing connectivity analyses across studies**.
- **Enhancing reproducibility in network neuroscience**.
- **Pre-processing data for Graph Neural Network (GNN) models**.
- **Comparing connectivity measures across parcellations**.

## Citation
If you use this toolbox in your research, please cite:

```
```

## License
This project is licensed under the **MIT License** – see the `LICENSE` file for details.

## Contact
For questions or issues, please open an **Issue** on GitHub or contact:
**[Ziqian Zhang]** – zziqian092@gmail.com
