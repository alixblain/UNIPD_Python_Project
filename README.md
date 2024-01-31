# Earthquake Data Analysis

-------------------------------

## Contributors

- BLAIN Alix
- L'HOSTIS Théo
- MARÇAL Thomas
- NOUAILLE Thomas

-------------------------------
## Overview

The "Earthquake Data Analysis" project involves the analysis of a dataset (referred to as the "catalog") containing earthquake records from South California spanning approximately 20 years. This catalog provides information on earthquake magnitudes, occurrence times (in seconds), and 3D coordinates (in meters) of the earthquake hypocenters.

The data includes the following key attributes:

- Magnitude (M): The magnitude of the earthquake.
- Time of Occurrence (t): The time interval from 0:00 of Jan. 1st, 1982 (in seconds).
- 3D Coordinates (x, y, z): The 3D coordinates of the earthquake hypocenter, derived from latitude, longitude, and depth.

## Data

The dataset is stored in the file `SouthCalifornia-1982-2011.dat` and is structured as follows:

- Column 1: Index of the event
- Column 2: Index of the previous event that triggered it (or -1 if no ancestor is found)
- Column 3: Time (in seconds) from 0:00 of Jan. 1st, 1982
- Column 4: Magnitude (M)
- Columns 5, 6, and 7: 3D coordinates (in meters) of the earthquake hypocenter (x, y, z)

By connecting each event to the one in the second column (if not -1), you can create causal trees.

## Project Assignments

This project involves several tasks:

1. **Visualization**: Visualize the spatial and temporal aspects of the earthquake data using time series and 3D visualizations of the hypocenters. You can plot space variables (e.g., coordinates) as a function of time.

2. **Waiting Time Distribution**: Compute the distribution of waiting times (t) for events with a magnitude equal to or above a certain threshold (M_min). Experiment with different threshold values (M_min) and use log-log scale plots to investigate power-law decay.

3. **Distance Distribution**: Calculate the distribution of distances (r) between consecutive earthquakes with a magnitude equal to or above a certain threshold (M_min). Choose appropriate bin sizes and explore different threshold values (M_min). If possible, fit the data with a suitable function.

4. **Waiting Time Distribution with Distance Constraint**: Analyze the waiting times (t) for events with magnitude equal to or above M_min, but also consider a maximum distance (d_max) constraint between consecutive earthquakes. If the next event is farther than d_max, skip it and move to the next pair. Repeat this analysis for different values of M_min and d_max.

5. **Scaling Law Analysis**: After completing the above assignments, comment on whether you observe any scaling laws in the data. Explore whether rescaling the distributions for various values of M_min and d_max collapses them onto a single curve, indicating the presence of scaling behavior.
