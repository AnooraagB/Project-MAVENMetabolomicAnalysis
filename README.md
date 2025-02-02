# Metabolomic Analysis Using MAVEN

El-MAVEN is a powerful software tool for metabolomic analysis that simplifies the process of analyzing large-scale datasets, specifically in the context of LC-MS and LC-MS/MS data. With an intuitive user interface, El-MAVEN allows for streamlined peak detection, grouping, and data export, enabling users to quickly move from raw data to insightful analysis. This repository provides a detailed walkthrough of using El-MAVEN for comprehensive metabolomic analysis.

## Features

* **Interactive workflow** : El-MAVEN supports a fully interactive workflow.
* **Main steps** (each step can be revisited to optimise settings for the dataset used) :
1) Setting up the workspace
2) Performing peak detection, and
3) Exporting results.


* **Peak detection and grouping** : Automated peak detection identifies and groups and peaks across samples.

* **Data visualisation** : Key visualisations include the extracted ion chromatogram (EIC) plot, color-coded for easy identification of sample peaks. Multiple visualisation options are available through the **right-side widget bar**.
  
* **Data export** : Results can be exported in various formats. The EIC and other group metrics can also be saved for further analysis or visualizations outside of El-MAVEN.

## Software  used

* El-MAVEN (Maven_8.1.28.13m-Windows)
* More info on https://github.com/ElucidataInc/ElMaven

## Dataset used

This project uses metabolomic datasets to analyze compounds measured in human placenta samples.
These datasets consist of samples in LC-MS or LC-MS/MS format, typically containing hundreds of metabolites across multiple samples.
* **Data format**
  * The dataset is loaded in common metabolomics data formats like .mzXML, .mzML, and .cdf.
* **Input data**
  * The sample data used for this project are :
    * 20200906_m1_ASD_6uM_c8_Pos_fsPRM_2uL_007.mzML
    * 20200906_m1_ASD_6uM_c8_Pos_fsPRM_2uL_008.mzML
    * 20200906_m1_ASD_6uM_c8_Pos_FS_2uL_003.mzML
    * 20200906_m1_ASD_6uM_c8_Pos_FS_2uL_004.mzML
    * 20200912_m1_ASD_6uM_c8_Neg_fsPRM_2uL_008.mzML
    * 20200912_m1_ASD_6uM_c8_Neg_fsPRM_2uL_009.mzML
    * 20200912_m1_ASD_6uM_c8_Neg_FS_2uL_003.mzML
    * 20200912_m1_ASD_6uM_c8_Neg_FS_2uL_004.mzML
  * These can be downloaded from the **ST002151: Archive File:ST002151_Targeted.7z** available on Metabolomics Workbench (https://metabolomicsworkbench.org/data/DRCCStudySummary.php?Mode=SetupRawDataDownload&StudyID=ST002151).
* **Metabolite reference**
  * The reference compound database KNOWNS.csv was used to identify and classify metabolites during analysis.

## Concepts and tools used

* **Data handling with El-MAVEN**
  * El-MAVEN’s data handling capabilities are designed for high-throughput metabolomics.
  * The software allows for the easy import, curation, and export of complex datasets in various formats.

* **Peak detection and scoring**
  * Peak detection is a critical step in metabolomics.
  * El-MAVEN uses advanced algorithms to automatically detect and score peaks from the extracted ion chromatograms.
  * Peaks are then grouped across samples, with the best-scoring peaks selected for further analysis.

* **Data visualisation**
  * Extracted Ion Chromatograms (EICs) : The EIC plot allows users to visualise metabolite peaks across all samples, making it easy to identify trends and outliers.
  * Interactive interface : The software’s interface offers various visualisations, including peak intensity, peak area, and chromatogram overlays for better insight into sample data.

## Usage

**1. Setting Up the Workspace**

* **Launch El-MAVEN**
  * Open the software via the desktop shortcut.
  * Upon first launch, click on the Options button to adjust the global settings (e.g., experimental details like RT window and compound parameters).

* **Load data**
  * To load data, go to File > Load Samples and select your sample files in .mzXML, .mzML, or .cdf format.
  * Once the samples are loaded, they will appear in the Samples window on the left side of the interface.

* **Select reference compound database**
  * El-MAVEN comes pre-loaded with two standard reference databases:
  1. KNOWNS.csv (for LC-MS data)
  2. SRM2.csv (for LC-MS/MS data)
  * Users can also upload custom reference databases in CSV format by clicking on the **Compounds** tab on the left and selecting the desired reference.

**2. Peak detection**

* **Automated peak setection**
Once the data is loaded and the reference compound database is selected, proceed to Peaks > Peak Detection.
The system will automatically detect peaks based on the set parameters. Detected peaks are grouped together, and a score is assigned based on quality.

* **Fine-tuning peak detection**
If necessary, users can adjust peak detection and grouping parameters to refine results, using separate tabs for peak detection and group filtering.

**3. Exporting results**

* **Export formats**
Once you’ve reviewed and curated the peaks, export the results in one of the following formats :
  * CSV : Summary data (default) or detailed peak-level reports.
  * JSON : For exporting EICs and group metrics for use in external software.
  * PDF : A report containing EICs for each metabolite.

* **Save projects**
  * El-MAVEN projects can be saved in .mzroll format for later use.
  * This allows users to reopen and continue analysis at any time.

* In the repository content, the csv files of the results of the analysis can be found as :
  * "all_groups.csv" : This includes all the groups obtained in the results.
  * "good_groups.csv" : This includes those groups which are labelled as good based on the peak and grouping (clustered).
  * "bad_groups.csv" : This includes those groups which are labelled as bad based on the peak and grouping (scattered). 

## Future plans
* Assess how updates to practicality and efficiency of software programs like El-MAVEN affect the results of the analysis.

### ________________
### by Anooraag Basu
