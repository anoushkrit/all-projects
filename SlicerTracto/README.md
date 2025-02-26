# SlicerTracto 

A complete structural neuroimaging pipeline to enable Neurosurgical Planning, with modules like fODF reconstruction, Fiber Tracking, and Tract Segmentation. This extension, SlicerTracto is built on top of open-source and widely used and accepter 3D Slicer. 

## Overview


### Features
**Modular Design**: Includes four specialized modules (fODF reconstruct, track, segment, metrics).
**Flexible Computation**: Supports both local and SSH-based remote processing.
**Algorithm Wrapping**: Allows seamless integration and interchangeability of multiple algorithms.
**Advanced Visualization**: Supports interactive visualization of fiber tracts overlaid on brain images.

### 

### Modules Overview
1. **Fodf** (Fiber Orientation Distribution Function)
   - Computes fODF from diffusion MRI data. 
   -  Provides multiple computation methods.
   -   Supports various fODF reconstruction algorithms.
   -   Inputs:
        -  White Matter Mask (*_wm.nii): Binary mask for white matter regions.
        -  Diffusion NIfTI (*_dw.nii): Diffusion-weighted image file.
        -  BVALS (*.bvals): File containing b-values.
        -  BVECS (*.bvecs): File containing b-vectors.
2. Visualization:
    -  Enables visualization of generated Fodf.
3. Tracts
    -  Generates fiber tracts from Fodf data.
    -  Supports deterministic and probabilistic tractography algorithms.
    -  Provides flexible seeding and tracking options. 
    -  Inputs:
      -  Folder Input: A folder containing required files following predefined naming conventions.
   -  Outputs:
      -  .trk file: Contains generated white matter fiber tracts.
      -  .vtk file: Used for 3D visualization in Slicer.
4. Visualization:
   -  Supports visualization of generated tracts.
   -  Allows overlaying of tracts on corresponding NIfTI brain images for enhanced analysis.
   -  Key Features:
      -  Automatic seeding mask generation from the approximate mask.
      -  Automatic conversion of .trk files to .vtk for 3D visualization.
5. Segment
    - Segments generated tracts into distinct pathways
    - Implements multiple segmentation techniques.
    - Supports both region-based and clustering-based segmentation.
   - Inputs:
     - Folder Input: A folder containing required files for the selected segmentation algorithm.
   - Visualization:
     - Displays segmented tracts with distinct colors
     - Enables overlaying of segmented tracts on NIfTI brain images.
     - Supports selective tract visualization for advanced analysis.
6. Metrics
    - Computes quantitative diffusion metrics from tract data.
    - Supports various statistical models.
    - Metrics Computed:
        - Fractional Anisotropy (FA)
        - Mean Diffusivity (MD)
        - Dice Score: Measures spatial agreement between tracts.
        - Overreach Score: Quantifies tracks extending beyond the target area.
        - Overlap Score: Measures shared regions between different tractographies.
### Installation Guide
**Pre-requisites**
1. 3D Slicer (Latest version) # 5.0.6
2. Required dependencies installed inside slicer given in requirement.txt for selected algorithms.
