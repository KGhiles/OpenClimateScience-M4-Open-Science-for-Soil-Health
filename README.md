# OpenClimateScience M4 – Open Science for Soil Health  
### High-Resolution Soil Organic Carbon Mapping (Algeria)

## Project Overview
Global soil products such as **SoilGrids** provide invaluable information, but their spatial resolution (≈250 m) is often too coarse for **local agricultural decision-making**. Farmers and land managers operate at much finer spatial scales.

This project demonstrates an **open-science, reproducible workflow** to generate **high-resolution (30 m) Soil Organic Carbon (SOC) maps** by *downscaling* coarse global soil data using high-resolution satellite imagery and terrain information.

The workflow is implemented as a **Google Colab notebook** and is designed for:
- teaching and training
- rapid prototyping
- transparent, cloud-native geospatial analysis

---

## Objectives
- Access cloud-hosted geospatial data (Landsat, NASADEM, SoilGrids)
- Engineer environmental predictors relevant to soil processes
- Downscale coarse SOC data using machine learning
- Produce a fine-resolution SOC map with **uncertainty estimates**
- Demonstrate **open, reproducible geospatial science**

---

## Study Area
- **Region:** Tell Atlas, Northern Algeria  
- **Extent:** ~10 × 10 km agricultural window  
- **Spatial Resolution:** 30 m (output)

---

## Methodology (Conceptual)
1. **Target Variable (Teacher)**
   - SoilGrids SOC stock (0–5 cm depth, ~250 m)

2. **Predictors (Students)**
   - Vegetation indices from Landsat:
     - MSAVI (Modified Soil-Adjusted Vegetation Index)
     - Bare Soil Index (BSI)
   - Topographic variables:
     - Elevation (NASADEM)
     - Slope

3. **Downscaling Strategy**
   - Resample coarse SOC to the 30 m grid
   - Learn relationships between SOC and environmental predictors
   - Predict SOC continuously at high resolution

4. **Model**
   - Random Forest Regressor (scikit-learn)

5. **Uncertainty Quantification**
   - Ensemble approach (multiple RF models)
   - Pixel-wise standard deviation as uncertainty proxy

---

## Notebook
The full workflow is implemented in the notebook:

