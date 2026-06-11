# Temporal
This study aimed to investigate the temporal dynamics of microbial communities in the tomato rhizosphere. To this end, we designed an approach to assess changes in these communities through high-resolution sampling at short time intervals, allowing for detailed monitoring of the significant shifts occurring during the early stages of plant development.

<p align="center">
  <img src="/temporal_eng.svg" alt="temporal_eng">
</p>
 
## Pre-processing

The sequences from Illumina were pre-processed by removing the primers and then processed using the DADA2 pipeline ([DADA2_pipeline.Rmd](https://github.com/microenvgen/Temporal/blob/main/DADA2_pipeline.Rmd)). The resulting object from this processing step can be found in the [Releases](https://github.com/microenvgen/Temporal/releases/tag/temporal_data) section of this repository.

## Contents

- metadata_Temp: the Excel file containing the necessary data.
- `Analysis.Rmd`: the script containing the code used to perform the analyses in this study.
 
## Functions

### Diversity analysis and correlations

- The values of the working variables (Bacterial load, Weight, Richness, Homogeneity and Diversity) are plotted by Community and Time.
- The effects of Community and Time on the working variables are statistically analyzed.
- The effects of Richness and Diversity on Load and Weight are also statistically analyzed.

### Phylogenetic analysis

- The 10 most abundant families are calculated.
- The effect of time on the abundance of the different phyla and families is evaluated.
  

### Composition analysis

- Microbial community composition is represented using NMDS based on Bray–Curtis distances, with samples separated by Community type and sampling time and grouped according to these variables for visualization.
- Microbial community composition is represented using NMDS based on Bray–Curtis distances, separating the data by Community type and grouping samples according to sampling time.
- Distance-based redundancy analysis (partial dbRDA using Bray–Curtis distances) was performed to model sample composition as a function of Time while controlling for Community, and as a function of Community while controlling for Time.
- Microbial community composition is represented using NMDS based on Unifrac distances, with samples separated by Community type and sampling time and grouped according to these variables for visualization.
- Microbial community composition is represented using NMDS based on Unifrac distances, separating the data by Community type and grouping samples according to sampling time.
- Distance-based redundancy analysis (partial dbRDA using Unifrac distances) was performed to model sample composition as a function of Time while controlling for Community, and as a function of Community while controlling for Time.
-Temporal dynamics of microbial community composition are analyzed using a Bray–Curtis distance matrix. The mean within-community distance is calculated for each Time level, and temporal trends are estimated for each Community. The resulting slopes are then weighted to compute a global statistic, whose significance is assessed using a restricted permutation test.
- Temporal dynamics of microbial community composition are analyzed using a Unifrac distance matrix. The mean within-community distance is calculated for each Time level, and temporal trends are estimated for each Community. The resulting slopes are then weighted to compute a global statistic, whose significance is assessed using a restricted permutation test.
