# Snowcover using Planet

Mapping snow cover with Planet imagery aids in environmental monitoring, disaster response, and resource management, fostering scientific research and community engagement while enabling personal growth through impactful contributions to understanding climate patterns and changes.

Possible Research Questions:
1. How does the accuracy of the deep learning model compare to traditional methods for mapping snow cover?
2. What are the key factors influencing the performance of the deep learning algorithm in snow cover classification?
3. How well does the algorithm generalize to different environmental conditions and geographic regions?
4. What are the computational requirements and scalability challenges associated with large-scale snow cover mapping?
5. What are the potential applications and benefits of integrating deep learning-based snow cover mapping into existing monitoring systems or workflows?
6. How can uncertainties in the model predictions be effectively quantified and communicated to stakeholders?
7. What are the practical considerations and challenges in operationalizing the algorithm for real-world snow cover monitoring applications?

## Files

* `.gitignore`
<br> Globally ignored files by `git` for the project.
* `environment.yml`
<br> `conda` environment description needed to run this project.
* `README.md`
<br> Description of the project (see suggested headings below)

## Folders

This template provides the following folders and suggested organizaiton structure for the project repository, but each project team is free to organize their repository as they see fit.

### `contributors`
Each team member can create their own folder under contributors, within which they can work on their own scripts, notebooks, and other files. Having a dedicated folder for each person helps to prevent conflicts when merging with the main branch. This is a good place for team members to start off exploring data and methods for the project.

### `notebooks`
Notebooks here take you through individual notebooks that are steps to make it reproducible.

### `scripts`
Helper utilities that are shared with the team should go in here.

# Recommended content for your README.md file:

## Project Summary

### Project Title

Mapping Snow Cover Using UNet-Based Deep Learning Architecture (SnowCoverNet)

### Collaborators

List all participants on the project.

* Project lead - Aji John
* Advisor - Tony Cannistra
* SP
* NC


### Problem

Developing a scalable deep learning approach to accurately map snow cover using Planet imagery and corresponding snow cover labels. The objective is to leverage machine learning techniques to automatically classify pixels as either snow-covered or snow-free, based on multispectral information captured by Planet's satellites, enabling efficient monitoring and analysis of snow cover dynamics over large geographic areas.

### Specific questions / project goals

1. Develop a robust and accurate deep learning-based algorithm for mapping snow cover using Planet imagery.
2. Provide insights into the strengths and limitations of deep learning approaches for snow cover mapping compared to traditional methods.
3. Enable efficient and scalable monitoring of snow cover dynamics over large geographic areas and time periods.
4. Facilitate the integration of advanced remote sensing techniques into snow cover monitoring and management practices.


### Data

Planet imagery and corresponding snow cover labels.

1. **Planet Imagery**:
   - Size: Variable, depending on the coverage area and resolution of the satellite imagery. Can range from small patches to large-scale coverage of entire regions.
   - Format: Typically GeoTIFF or similar raster formats, containing multispectral or RGB bands captured by Planet's satellites (e.g., PlanetScope, SkySat).
   - Access: Accessible via the Planet API, which provides a programmatic interface for searching, retrieving, and downloading imagery based on various parameters such as location, date, cloud cover, and satellite constellation.

2. **Snow Cover Labels**:
   - Size: Corresponds to the spatial extent of the Planet imagery, typically in the same resolution.
   - Format: GeoTIFF or similar raster format, containing binary or categorical labels indicating the presence or absence of snow cover for each pixel.
   - Access: Snow cover labels may be obtained from various sources, including ground observations, remote sensing products (e.g., MODIS, Sentinel), or specialized datasets from research institutions such as the National Snow and Ice Data Center (NSIDC).

To access the Planet imagery, you would need access to the Planet API and appropriate API credentials (API key). With the API, you can programmatically search for and download imagery based on your specific criteria.

For the snow cover labels, you need to obtain the data from relevant sources or datasets. Here we are using ASO data from NSIDC, we then threshold it to produce binary snowcover.

Both the Planet imagery and snow cover labels are typically stored as raster datasets.

### Existing methods

How would you or others traditionally try to address this problem?

### Proposed methods/tools

Our method uses UNet architecture, a type of convolutional neural network specifically designed for semantic segmentation tasks, to accurately map snow cover using Planet imagery. Initially, the Planet imagery and corresponding snow cover labels undergo preprocessing to prepare them for model training. The UNet architecture, characterized by its symmetric contracting and expansive paths, is trained using the labeled imagery data. This architecture allows the model to capture intricate spatial dependencies and effectively segment the imagery into snow-covered and snow-free regions.

Once trained, the model could be evaluated for its performance in mapping snow cover across various geographic regions and time periods. We assess both the accuracy of the model's pixel-wise predictions and its computational efficiency, considering its scalability for large-scale snow cover mapping tasks. Overall, our code repository here aims to provide a robust and efficient solution for monitoring snow cover dynamics.

### Additional resources or background reading

Optional: links to manuscripts or technical documents providing background information, context, or other relevant information.

### Tasks

1. Preprocess Planet imagery and snow cover labels to prepare them for model training. (Notebook 1 and 2)
2. Develop a deep learning architecture suitable for classifying snow cover from multispectral imagery (Notebook 3).
3. Train the deep learning model using labeled Planet imagery and corresponding snow cover labels (Notebook 3).
4. Evaluate the model's performance in accurately mapping snow cover over different geographic regions and time periods.
5. Assess the scalability and computational efficiency of the algorithm for large-scale snow cover mapping applications.
6. Conduct uncertainty analysis to quantify and account for uncertainties associated with the model predictions.
7. Explore the potential for operationalizing the algorithm for real-time or near-real-time snow cover monitoring.

## Running

conda env create -f environment.yml
conda activate snow_mapping_env

You might need to do 'conda init'