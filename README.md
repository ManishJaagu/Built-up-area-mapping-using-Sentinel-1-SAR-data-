# Built-up Area Mapping using Sentinel-1 SAR Data

This project focuses on mapping built-up areas using Sentinel-1 dual-polarimetric SAR data. The main objective was to explore how polarimetric information can be used to distinguish built-up structures from non-built-up areas and to understand the effect of different SAR preprocessing choices on the final classification.

The workflow starts with Sentinel-1 SLC data preprocessing, including orbit correction, calibration, debursting, multi-looking, and optional speckle filtering. The complex SAR data are then used to generate the C2 covariance matrix and Stokes parameters. These parameters are normalized and combined to calculate the Dual Polarimetric Radar Built-up Index (DpRBI).

Both ascending and descending Sentinel-1 passes were investigated because the orientation of buildings and other structures can affect their radar response. The DpRBI values from both passes were combined to reduce built-up areas missed by a single viewing direction. A threshold was then applied to generate the final binary built-up map.

## Speckle Filtering Experiment

An important part of the project was evaluating the effect of speckle filtering rather than assuming that filtering would always improve the result. The built-up maps generated with and without the Refined Lee filter were independently validated against reference data.

The results showed a substantial difference:

- **Without Refined Lee:** 81.0% overall accuracy
- **With Refined Lee:** 45.4% overall accuracy

The experiment showed that, for this particular DpRBI-based workflow, applying the Refined Lee filter significantly reduced classification performance.

## Concepts

- Sentinel-1 SLC processing
- Dual-polarimetric SAR
- C2 covariance matrix
- Stokes parameters
- DpRBI
- Ascending and descending orbit analysis
- Speckle-filter comparison
- Built-up area classification and validation

## Study Areas

The methodology was investigated across ""Barcelona** using ascending and descending Sentinel-1 acquisitions.

## Repository Contents

The repository contains the processing notebooks, presentation, generated outputs (in notebooks), and supporting documentation for the project.
