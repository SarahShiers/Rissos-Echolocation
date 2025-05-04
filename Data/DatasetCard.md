# Dataset Summary

This dataset contains passive acoustic detection data of *Risso’s dolphins (Grampus griseus)* recorded from multiple surveys conducted between 2016 and 2023 throughout the California Current. The data were collected using drifting and moored hydrophones as part of NOAA’s PASCAL (2016), CCES (2018), and ADRIFT (2020–2023) surveys. It includes information about the presence of Risso’s dolphins across spatial and temporal scales, including GPS coordinates, encounter timing, and spectral click characteristics. These data support research into population structure, habitat use, and potential impacts of offshore wind energy development.

# Languages

English

# Data Instances

A typical row in the dataset represents a detection event and may include the following fields:

```{r, echo=FALSE, results='asis'}
cat('
{
  "Survey": "ADRIFT",
  "Date": "2021-07-15",
  "Time": "14:35:00",
  "Latitude": 36.805,
  "Longitude": -122.675,
  "Region": "Central California",
  "Season": "Post-upwelling",
  "Recorder_ID": "D04",
  "Peak_Frequency_kHz": 63.5,
  "Notch_Frequency_kHz": 52.1,
  "Click_Type": "Type A",
  "Deployment_Depth_m": 125,
  "Comments": "High-quality detection during low sea state"
}
')

# Data Fields

The dataset includes standard detection metadata:

- Survey name and year  
- Time and date of detection  
- Geographic coordinates (latitude, longitude)  
- Recorder ID and depth  
- Regional and seasonal classification  
- Spectral characteristics (peak and notch frequencies)  
- Encounter-level notes  

# Curation Rationale

This dataset aggregates effort-standardized, expert-verified detections of Risso’s dolphins from PAM datasets specifically curated for inter-regional comparison. The click detections were initially separated by NOAA and collaborators using species classification algorithms, followed by regional segmentation and manual QA. This dataset is intended to serve both research and management purposes by characterizing spatiotemporal patterns of dolphin echolocation.

# Initial Data Collection and Normalization

Data were collected using standardized hydrophones recording continuously at high sampling rates. Detection events were identified by automated detectors and manually reviewed by analysts. Regional, seasonal, and spectral labels were added based on known deployment metadata and visual inspection. The data were cleaned to remove duplicate entries and detections without valid geographic coordinates or essential spectral measurements.

# Who are the source data producers?

Recordings were collected by field teams from NOAA’s Southwest Fisheries Science Center and partner institutions, including academic researchers and acoustic technicians.

# Annotations

Annotations include regional tags (e.g., “Central California”), seasonal labels (e.g., “Winter”), and extracted spectral parameters (e.g., peak and notch frequencies) for each encounter.

# Annotation Process

Automated click detectors (as described in Soldevilla et al., 2017) were used to identify echolocation events. Final annotation and classification of Risso’s dolphin clicks were completed through a combination of visual inspection and classification tools in R using the `PAMpal` package.

# Who are the annotators?

Annotation and verification were conducted by marine bioacousticians and trained NOAA scientists. Spectral analysis scripts were developed and applied by graduate researchers with supervision from senior advisors.

# Personal and Sensitive Information

This dataset does not contain personal, demographic, or sensitive human data.

# Social Impact of Dataset

This dataset contributes to marine mammal conservation and informs the placement and regulation of offshore wind energy projects in California. It may be used in environmental impact assessments, stock delineation research, and acoustic ecology studies focused on climate change and anthropogenic noise.

# Discussion of Biases

Detection quality may vary by sea state, depth, and environmental noise. Some geographic and seasonal gaps exist in data coverage due to weather, pandemic-related field disruptions, or logistical constraints. Detection systems may occasionally misclassify echolocation events or miss quiet/short encounters. The dataset currently only includes known Risso’s dolphin detections and does not provide negative detection data (i.e., absence records).

# Other Known Limitations

- Some detections may be missing exact timestamps due to recorder clock drift.  
- Click spectral properties may be influenced by orientation, distance, or propagation effects.  
- Seasonal labels are approximated based on deployment time windows and may not reflect precise oceanographic conditions.  
- Pre-processed spectral features are not raw acoustic waveforms and are intended for secondary analysis only.  

# Dataset Curators

**Sarah Shiers**  
M.S. Student, Estuary and Ocean Science Center  
San Francisco State University  

**Supervised by:**  
Dr. Anne Simonis, NOAA Southwest Fisheries Science Center

# Contributions

Thanks to NOAA’s Passive Acoustic Group and the field teams of the PASCAL, CCES, and ADRIFT surveys. Special thanks to the Kenneth H. Coale Graduate Scholar Award for research support.
