# LeastCostDistance
R-based spatial analysis workflow for calculating and visualizing Least Cost Paths (LCP) using Tobler’s Hiking Function, Digital Elevation Models (DEM), and ggplot2 for archaeological or geographical terrain modeling.

Archaeological Least Cost Path (LCP) Analysis in R
This repository contains an R-based workflow for calculating and visualizing Least Cost Paths (LCP) between geographical points using Digital Elevation Models (DEM). It utilizes the Tobler’s Hiking Function to estimate the most efficient routes based on terrain slope.

🚀 Overview
The script processes spatial data to determine the optimal travel routes from a central origin (e.g., a base site) to multiple destinations. It features a high-quality visualization pipeline using ggplot2 and tidyterra, producing publication-ready maps with shaded relief (hillshade) and hypsometric tinting.

🛠️ Key Features
Cost Surface Generation: Creates a slope-based cost surface using the leastcostpath package.

Tobler’s Algorithm: Implements the standard "Hiking Function" for realistic movement modeling.

Spatial Transformation: Automatic reprojection to UTM (EPSG:32637) for accurate distance and length calculations.

Advanced Visualization: * Multi-layered mapping with ggnewscale.

Terrain analysis including slope, aspect, and hillshade.

Dynamic labeling with ggrepel to prevent overlapping text.

Professional map elements (North arrow, scale bar).

📦 Required Libraries
To run this script, you will need the following R packages:

R
install.packages(c("leastcostpath", "sf", "terra", "ggplot2", 
                   "ggspatial", "tidyterra", "ggrepel", "ggnewscale"))
📂 Input Data Requirements
DEM (.tif): A Digital Elevation Model file for terrain analysis.

Destinations (.kml/.kmz): A file containing the target locations.

Origin Coordinates: The script is currently configured with fixed coordinates for the starting point (WGS84).

📊 Output
The script generates a high-resolution PDF map (output.pdf) that includes:

A hypsometric elevation map.

Calculated paths marked in red.

Calculated distances for each path in kilometers.

Terrain-aware shaded relief for better spatial context.

📖 Usage
Clone the repository.

Update the tif_path and kmz_path variables in the script to point to your local files.

Adjust the Cave coordinates to your specific site of interest.

Run the script to generate your analysis and map.
