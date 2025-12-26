# EVMars-Anomaly: A Multimodal Color Event Dataset for Martian Anomaly Detection and Dust Storm Estimation

**EVMars-Anomaly**, a specialized subset of EVMars, represents the first multimodal dataset dedicated to anomaly detection in simulated martian dust storm scenario using a color event camera. It addresses the key challenges of sensing data in extremely low-visibility environments, enabling reliable particulate matter estimation and anomaly detection under severe dust storm conditions.

## Overview

The dataset consists of 68 sequences captured with a DAVIS346 color event camera(346×260 resolution, 1 µs temporal precision) in a outdoor data collection test field. High-power industrial fans simulate three canonical dust storm intensities:

- **Local Dust Storm**: Mild particle suspension
- **Regional Dust Storm**: Moderate occlusion
- **Global Dust Storm**: Extreme low-visibility , TSP concentrations exceeding 800 µg/m³

The data format is as follows:

Event Streams: Stored as CSV files with the following columns:
timestamp (microseconds), x (pixel column, 0–345), y (pixel row, 0–259), polarity (±1), color (RED/GREEN/BLUE).
Each file corresponds to one continuous sequence.

Ground Truth: Provided in a separate synchronized CSV per sequence:
timestamp (ms), TSP (µg/m³), PM2.5 (µg/m³), PM10 (µg/m³)

**Mars-analog Simulation Site:**

<img width="" height="258" alt="748e0292257e36f9c46c93c3bf09d0c1" src="https://github.com/xuchentong/EVADR/blob/main/pictures/Mars-analog Simulation Site1.png" /> <img width="" height="258" alt="fa209237331f9cd2b3322f369397f648" src="https://github.com/xuchentong/EVADR/blob/main/pictures/Mars-analog Simulation Site2.png" />

**Outdoor Data Collection Test Field:**

<img width="827" height="" alt="02709ef9c5776e8a4024f828cf83985f" src="https://github.com/xuchentong/EVADR/blob/main/pictures/Outdoor Data Collection Test Field.png" />

**Mars Rover Data Collection Equipment:**

<img width="827" height="" alt="8df3644ec6465e16bda2e76cc9b46a96" src="https://github.com/xuchentong/EVADR/blob/main/pictures/Mars Rover Data Collection Equipment.png" />


## Visual Comparison
To demonstrate the realism of our simulated Martian dust storms in EVMars-Anomaly, we compare a real dust storm captured by NASA's Curiosity rover with a sequence from our dataset. Both exhibit similar characteristics: rapid particle motion, severe occlusion, and near-zero visibility, validating the fidelity of our simulation for anomaly detection tasks.

**Real Martian Dust Storm (NASA's Curiosity Rover)**
<img src="https://github.com/xuchentong/EVADR/blob/main/pictures/YouTubeezgif.gif" alt="Real Martian Dust Storm" width="692" />
This GIF captures an actual dust devil on Mars, showing the chaotic, high-density particle dynamics that challenge conventional perception systems. (Credit: NASA/JPL-Caltech)

**Simulated Dust Storm from EVMars-Anomaly**
<img src="https://github.com/xuchentong/EVADR/blob/main/pictures/dv-ezgif.gif" alt="Real Martian Dust Storm" width="692" />
Our simulation replicates the same extreme conditions using regolith-like sand and calibrated airflow, enabling realistic testing of event-based anomaly detection without highlighting the event camera specifics.


## Data Visualization:

<img width="406" height="" alt="1760584719584360" src="https://github.com/xuchentong/EVADR/blob/main/pictures/rgb1.png" /><img width="406" height="" alt="1760584719396416" src="https://github.com/xuchentong/EVADR/blob/main/pictures/event1.png" />


<img width="406" height="" alt="image" src="https://github.com/xuchentong/EVADR/blob/main/pictures/rgb2.png" /><img width="406" height="" alt="image" src="https://github.com/xuchentong/EVADR/blob/main/pictures/event2.png" />


## Download
The EVMars-Anomaly dataset is hosted on the Hugging Face Hub for easy access.

[![Hugging Face Dataset](https://img.shields.io/badge/🤗%20Hugging%20Face-Dataset-blue)](https://huggingface.co/datasets/Miniecho/EVMars-Anomaly)


## License
This repository is licensed under the Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0).
