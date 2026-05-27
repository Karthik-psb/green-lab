# Datasets

Index of datasets relevant to green-lab's AI + Agriculture work in India.

This folder contains documentation and metadata about datasets — not the datasets themselves (they are too large to store in git). Each entry includes: source, size, license, relevance, and how to access.

---

## Crop Disease Images

### PlantVillage Dataset
- Source: Penn State University / Hughes & Salathé (2015)
- Size: 87,867 images, 26 diseases, 14 crop species
- License: CC0 (public domain)
- Access: https://github.com/spMohanty/PlantVillage-Dataset or Kaggle
- Relevance: Baseline training data for disease detection. Important caveat: images were taken in controlled (lab) conditions in the US. Indian field conditions differ significantly.
- Action needed: fine-tune any model trained on this dataset with India field images before deployment.

### IIIT-D Plant Disease Dataset
- Source: IIIT Delhi
- Size: ~15,000 images
- License: Research use
- Access: contact IIIT Delhi directly
- Relevance: Indian context, more representative than PlantVillage for some crops

### iNaturalist — Plant Observations India
- Source: iNaturalist community
- Size: Varies, millions of observations globally, subset for India
- License: CC-BY-NC
- Access: https://www.inaturalist.org/observations?place_id=6681
- Relevance: Wild plant and some disease observations in India. Noisy but geographically representative.

---

## Soil Data

### ISRIC World Soil Information (SoilGrids)
- Source: ISRIC
- Size: Global raster, 250m resolution
- License: CC-BY 4.0
- Access: https://soilgrids.org/
- Relevance: Soil texture, pH, organic carbon for irrigation scheduling and yield prediction. Resolution is a limitation for smallholder farms.

### NBSS&LUP Soil Maps
- Source: National Bureau of Soil Survey and Land Use Planning (ICAR)
- Size: India-specific, various scales
- License: Government open data (check terms)
- Access: https://www.nbsslup.in/
- Relevance: More detailed India soil classification data

---

## Weather and Climate Data

### India Meteorological Department (IMD)
- Source: IMD, Government of India
- Size: Historical data from 1901, station and gridded data
- License: Government data (free for research)
- Access: https://mausam.imd.gov.in/
- Relevance: Temperature, rainfall, humidity for irrigation scheduling and disease risk modelling

### NASA POWER
- Source: NASA
- Size: Global, daily from 1981
- License: Open
- Access: https://power.larc.nasa.gov/
- Relevance: Satellite-derived meteorological data, useful where IMD station density is low

### ERA5 Reanalysis (ECMWF)
- Source: ECMWF via Copernicus
- License: Free for research
- Access: https://cds.climate.copernicus.eu/
- Relevance: High quality global reanalysis weather data at 25km resolution

---

## Satellite Imagery

### Sentinel-2 (ESA)
- Resolution: 10m multispectral
- Revisit: 5 days
- License: Free, open
- Access: Copernicus Open Access Hub, Google Earth Engine
- Relevance: Crop health monitoring (NDVI), yield prediction. Cloud cover is a significant challenge during kharif season.

### Sentinel-1 SAR (ESA)
- Resolution: 10m SAR (penetrates clouds)
- Revisit: 6 days
- License: Free, open
- Access: Copernicus Open Access Hub, Google Earth Engine
- Relevance: Crop monitoring during monsoon when optical imagery is unavailable. SAR backscatter correlates with crop biomass and soil moisture.

### ISRO Bhuvan
- Source: ISRO, India
- Relevance: India-specific satellite data, various resolutions
- Access: https://bhuvan.nrsc.gov.in/

---

## Agricultural Statistics

### ICRISAT Village Dynamics in South Asia (VDSA)
- Source: ICRISAT
- Size: Multi-decade panel data from Indian villages
- License: Research use
- Relevance: Crop yields, input use, household economics at village level

### Ministry of Agriculture and Farmers Welfare — Crop Production Statistics
- Source: Government of India
- Access: https://aps.dac.gov.in/
- Relevance: District-level crop area and production data for yield prediction ground truth

---

## Datasets Still Needed (Priority Collection Plan)

1. India field disease images: 10,000+ labelled images of the top 5 disease-crop pairs in the pilot geography. Collect through KVK extension workers and FPO field staff.
2. Ground truth yield records: historical plot-level yield data from 500+ farms for yield prediction model training. Target: ICRISAT, state agriculture departments, FPO records.
3. Weed species images: labelled images of major weed species in target crop systems. No suitable open dataset currently exists for Indian conditions.
