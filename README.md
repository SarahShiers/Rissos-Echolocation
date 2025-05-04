# Risso's Dolphin Echolocation Research

This repository contains R scripts and documentation for a graduate research project investigating geographic variation in the echolocation clicks of *Risso’s dolphins (Grampus griseus)* within the California Current. The project uses passive acoustic monitoring (PAM) data to assess regional and seasonal vocalization patterns, with implications for conservation, population structure, and offshore wind energy development.

## Objectives

- Identify potential subpopulations of Risso’s dolphins using spectral characteristics of echolocation clicks.
- Analyze the spectral features of clicks (e.g., peak and notch frequencies) across spatial and seasonal gradients.
- Compare California Current data with other U.S. regions, including the East Coast, Gulf of Mexico, and Hawaiian waters.
- Provide data to inform management strategies and marine spatial planning under the Marine Mammal Protection Act.

## Study Region and Data Sources

- **Geographic scope:** Central Oregon to Central California
- **Data sources:**
  - Adrift survey (2020–2023)
  - PASCAL survey (2016)
  - CCES survey (2018)
- **Recording method:** Drifting and moored hydrophones deployed at 100–150 meters
- **Data volume:** Approximately 30,000 hours of high-resolution audio recordings
- **Seasonal coverage:** Upwelling (March–June), Post-upwelling (July–November), Winter (December–February)

## Methodology

1. **Detection:** Risso’s dolphin clicks were pre-identified and separated from other cetaceans using NOAA classification protocols.
2. **Software and tools:** Analysis is conducted in R using packages such as `PAMpal`.
3. **Spectral feature extraction:**
   - Peak frequency
   - Notch frequency
4. **Statistical analysis:**
   - ANOVA to test for regional differences
   - Regression analysis to examine spatial gradients
   - K-means clustering to explore click type structure

## Significance

- Contributes to understanding how echolocation behavior varies geographically within a species.
- Supports stock assessments with finer-scale population insights.
- Offers baseline acoustic data for evaluating the impact of offshore wind energy development on cetaceans.

## Known Limitations

- Limited spatial coverage in some parts of the study area.
- Environmental noise (e.g., wind, wave strumming) may impact data quality.
- Potential for misclassification in automated detection pipelines.

## Acknowledgments

This work builds on datasets and methods developed by NOAA Fisheries and the Adrift project. It also draws from methodologies in Soldevilla et al. (2017). This research was supported in part by the Kenneth H. Coale Graduate Scholar Award.

