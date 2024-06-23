## Building Extraction from LiDAR Data
### Hacettepe University - Department of Geomatics Engineering
### 2019-2020 Fall
### Prepared by: Aysima Merve Akkurt 

---

## Overview

This project involves extracting building data from LiDAR (Light Detection and Ranging) data using various tools and methodologies. The report details the steps and procedures taken to process, analyze, and visualize the data, providing a comprehensive guide on building extraction using LiDAR technology.

## Project Structure

1. **Downloading and Exploring the Data**
   - Tools Used: `lasview`
   - Steps: 
     - Render point clouds by elevation and intensity.
     - Display first returns and provide a hill-shaded display.
   - Figures:
     - Figure I: Command line script for first step
     - Figure II: Screenshot for color by elevation
     - Figure III: Screenshot for color by intensity
     - Figure IV: Screenshot for render by first return
     - Figure V: Screenshot for triangulation and hill-shaded display

2. **Classification of Noise Points**
   - Tools Used: `lasnoise`
   - Parameters:
     - `step_xy`, `step_z`, `isolated`
   - Figures:
     - Figure VI: Command line script for second step
     - Figure VII: Screenshot with parameters (step_xy=4, step_z=4, isolated=20)
     - Figure VIII: Screenshot with parameters (step_xy=4, step_z=1, isolated=5)

3. **Ground Filtering**
   - Tools Used: `lasground`
   - Description: Filter ground points to enhance building detection.
   - Figures:
     - Figure IX: Command line script for third step
     - Figure X: Screenshot for ground filtering

4. **Classification of Buildings and Vegetation**
   - Tools Used: `lasclassify`
   - Parameters:
     - Search area size, Ground offset, Building planarity, Forest ruggedness
   - Figures:
     - Figure XI: Command line script for fourth step
     - Figure XII: Parameters for classify

5. **Digital Terrain Model (DTM) Generation**
   - Tools Used: `las2dem`
   - Description: Generate DTM to represent bare-earth terrain.
   - Figures:
     - Figure XIII: Command line script for fifth step
     - Figure XIV: Digital Terrain Model screenshots

6. **Digital Surface Model (DSM) Generation**
   - Tools Used: `las2dem`
   - Description: Generate DSM to include surface elevations like buildings and vegetation.
   - Figures:
     - Figure XV: Command line script for sixth step
     - Figure XVI: Digital Surface Model screenshots

7. **Normalized Digital Surface Model (nDSM) Generation**
   - Tools Used: QGIS Raster Calculator
   - Description: Compute nDSM by subtracting DTM from DSM.
   - Figures:
     - Figure XVII: Explanation of nDSM
     - Figure XVIII: Raster Calculator screenshot for nDSM generation
     - Figure XIX: Normalized Digital Surface Model screenshots

8. **Building Segmentation**
   - Tools Used: QGIS
   - Description: Segment buildings using nDSM with various threshold values.
   - Figures:
     - Figure XX: Screenshots for different threshold values
     - Figure XXI: Screenshot for chosen threshold value (7)

9. **Building Boundary Delineation**
   - Tools Used: QGIS
   - Description: Manually delineate building boundaries using the nDSM.
   - Figures:
     - Figure XXII: Screenshot for manually building delineation

10. **Bonus: Comparison of Classification and Manual Delineation**
    - Tools Used: `las2las`, Cloud Compare, QGIS
    - Description: Compare points classified as buildings with manually delineated boundaries.
    - Figures:
      - Figure XXIII: Command line script for bonus step
      - Figure XXIV: Map comparing classified points and delineated boundaries

## Conclusion

This project demonstrates the process of extracting building data from LiDAR datasets using a series of software tools and command-line utilities. The report outlines each step, providing visual aids and command scripts for reproducibility. The findings highlight the effectiveness and limitations of automatic classification methods in comparison to manual delineation.

## Author

Aysima Merve Akkurt 

