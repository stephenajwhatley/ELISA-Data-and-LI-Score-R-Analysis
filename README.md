# ELISA Data and LI Score R-Analysis
## Project Details
#### Short Description
This project offers the first publicly available R scripts implementing a complete ELISA workflow for two-group comparison.  This includes technical outlier removal, 4PL curve fitting, and two-group comparison via summary and inferential statistics, boxplot generation, and biological outlier detection for sensitivity analyses.
#### Overview
This repository contains three standalone R scripts for analysing Brain-derived Neurotrophic Factor levels and learning index (LI) scores in rodent models. Two scripts perform ELISA‐based BDNF quantification and analysis; the third analyses LI scores. All code is written in R 4.5.1 and designed for reproducible, transparent data analysis.

## Repository Structure
```
ELISA-Data-and-LI-Score-R-Analysis/
├── README.md                                              # Project overview and usage
└── R Scripts/                                             # R scripts for Data Analysis
    ├── ELISA (Run 5) – BDNF Mouse Genotype Analysis       # R Script 1
    ├── ELISA (Run 6) – BDNF Rat Ageing Analysis           # R Script 2
    └── Rat Learning Index Score Analysis                  # R Script 3  
```

## Requirements (Programmes and Packages)
- R version 4.5.1 (R Core Team, 2025)
- RStudio IDE 2025.05.1+513 (Posit Team, 2025)
- R packages: readxl, dplyr, tidyr, drc, rstatix, effsize, purrr, ggpubr, ggplot2, coin, effectsize, TOSTER

## Data Input
Create Excel files with standardized column headings as follows.  
  #### For ELISA Analyses
    - Sheet 1 of 2 ("Sample Data"): Sample ID,	Group,	OD Reading 1,	OD Reading 2,	OD Reading 3.
    - Sheet 2 of 2 ("Standard Curve"): Known Concentrations,	OD Response 1,	OD Response 2,	OD Response 3.
  #### For LI Score Analysis
    - Sheet 1 of 1 ("Sheet 1"): Sample ID,	Group,	LI Scores.  
  
Ensure that the file name entered into the script (under "# 0. USER-DEFINED PARAMETERS") matches the name of your Excel file.
## R Script Descriptions (workflow and output)
- #### Script 1 (ELISA Run 5 - Mouse Genotype Model)
Loads raw ELISA data, cleans data, interpolates BDNF concentrations via four-parametric logistic (4PL) standard curve, and generates outputs.  
  
Outputs include: 4PL model (standard Curve and parameters), technical outlier removals, interpolated BDNF concentrations, biological outlier detection, statistical results (summary and inferential), and a boxplot comparing the two groups.
- #### Script 2 (ELISA Run 6 - Rat Ageing Model)
Identical workflow to Script 1, but generic details modified to match the Rat Ageing Model.  
  
Specifically: Data Input, Analyte, Sample Groups, Comparison Type and Range of Results (See Table provided under "Reuse and Citation" at the end of this ReadMe file.
- #### Script 3 (Rat Learning Index Score Analysis)
Loads LI Score data and conducts statistical analyses as with Scripts 1 and 2, excluding ELISA-specific components.   
  
Outputs include: data cleaning, biological outlier detection, statistical results (summary and inferential), and a boxplot comparing the two groups.

## Author & Acknowledgments
#### Author: Mr Stephen Arthur James Whatley, BSc (Hons) [<img width="24" height="24" alt="ORCID-iD_icon_vector-small" src="https://github.com/user-attachments/assets/4b07a438-d569-46bb-9b91-7ff90a0fed01" />](https://orcid.org/0009-0004-7099-7384)
_Developed to support the Research Report for the MRes Bioscience (Neuroscience) degree at Keele University, School of Life Sciences.  
For questions or collaboration, open an issue via the **Issues** tab on this GitHub repository or email: [stephenajwhatley@gmail.com](mailto:stephenajwhatley@gmail.com)_

#### Acknowledgements
**All code and analytical methods in this repository were developed independently by the author.** Special thanks to: 
- Mr Victor Almeida — for advice on code debugging and presentation.  
- Dr Priscilla Gathoni — for recommending the use of R.  
- Dr Simon Trent & Dr Stuart Jenkins — for supervising the broader MRes Research Report.

## Use
- Copy or download this repository.
- Populate Excel files with your data, as advised by 'Data Input'.
- Run each script independently via RStudio or your preferred IDE.

## Reuse and Citation
These scripts are fully reproducible and may be adapted for your own analyses. If you reuse any portion of this code, please cite the exact version by its Zenodo DOI. Upon the first release, this repository will be archived and assigned a DOI. For example:

#### Whatley, S.A.J. (2025). _ELISA Data and LI Score R-Analysis, Version 1.0.0_ [R Code]. Zenodo. Available at: https://doi.org/10.5281/zenodo.16951065

The live GitHub Repository is available at: https://github.com/stephenajwhatley/ELISA-Data-and-LI-Score-R-Analysis

The following table represents the minor alterations that enable you to adapt the ELISA code for analyses with different parameters:  
  
<img width="900" height="700"  alt="Code Reproducibility Table" src="https://github.com/user-attachments/assets/5b0f54e1-063a-4df5-8e0e-efdaceaccaa6" />

