# Synchronization Analysis Code: Outdoor Heatwaves and Indoor Thermal Extremes
Code for quantifying the synchronization between external heatwaves (INMET and Ouzeau methods) and indoor thermal extremes (Operative Temperature, Heat Index, Cooling Load) in building simulations.

This repository contains the data analysis scripts used for the study:

Title: *Synchronizing outdoor heatwave detection with indoor thermal extremes: A case study in Brazilian social housing*

Presented at: Solar World Congress (SWC) 2025.

Authors: Matheus Korbes Bracht, Ana Paula Melo, and Roberto Lamberts.


## Overview and Methodology
*Goal:* The primary goal is to assess the temporal overlap between hours of severe indoor thermal stress (defined by a 99th percentile threshold) and periods identified as heatwaves by two distinct meteorological methods.

*Metric:* The code implements the calculation of the Synchronization Score, which expresses the percentage of extreme indoor hours coinciding with detected outdoor heatwave periods.

*Input Data:* The scripts process hourly time series data for indoor Key Performance Indicators (KPIs) and external climate data (EPW format) used for heatwave identification.

## Repository Structure and File Descriptions

| File (Jupyter Notebook) | Purpose and Analysis Stage |
| :--- | :--- |
| `heatwave_detection_inmet.ipynb` | Implements the **WMO/INMET** heatwave detection method (two or more consecutive days with Tmax $\ge$ Tnormal + 5°C). |
| `heatwave_detection_ouzeau.ipynb` | Implements the **Ouzeau et al. (2016)** heatwave detection method (based on daily mean temperature percentiles). |
| `simulation_analysis.ipynb` | **Core Calculation Script:** Calculates the 99th-percentile thresholds, identifies the set of extreme indoor hours, and computes the final Synchronization Score. |
| `analysis.ipynb` | Generates the visualization of results related to the climate dataset. |
| `indoor_overlap_visualization.ipynb` | Generates the visualization of results, primarily the overlap percentage heatmap. |
