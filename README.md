# High spatio-temporal mapping of snowcover

Mapping snow cover is crucial for a multitude of reasons, including its role in climate research, water resource management, flood forecasting, agricultural planning, energy generation, transportation, infrastructure maintenance, and recreation. In this project we will be using HLS (Harmonized Landsat Sentinel) data to map snowcover. Using HLS data to map snow cover can be an effective and valuable approach. HLS data combines observations from the Landsat and Sentinel satellite systems, providing high-quality and frequently updated imagery of the Earth's surface. Combining data from both Landsat and Sentinel satellites in the HLS dataset is advantageous as Landsat offers high spatial resolution, while Sentinel provides more frequent revisits. Here's how we will use HLS in deep learning project for snow cover mapping:

1. **Multi-Spectral Bands:** HLS data includes various spectral bands that are sensitive to different surface properties. These bands can be utilized to distinguish between snow-covered and snow-free areas. The reflectance in the visible and near-infrared bands can help identify snow due to its high reflectivity in these regions. We will use a subset of bands.

2. **Spatio-Temporal Resolution:** HLS data is available at a high temporal resolution, with frequent revisits to the same area. This is particularly important for monitoring snow cover, as it can change rapidly, especially during the snowmelt season. Frequent observations enable the tracking of snow cover dynamics over time.

3. **Cloud Cover Reduction:** HLS data includes cloud mask information, which can be used to filter out cloudy or obscured areas. This is crucial for accurate snow cover mapping because clouds can obscure the surface and lead to misinterpretations. We will cover some of this in how to query imagery from Earth Data using STAC API.

4. **Historical Analysis:** HLS data archives allow us to conduct historical analyses of snow cover changes over extended periods, aiding in climate research and trend detection related to snow cover. We can do this as part of a take home exercise. 

5. **Validation and Calibration:** HLS data is well-calibrated and validated, ensuring the reliability and accuracy of the information used for snow cover mapping. 

## Project Summary

HLS data is a valuable resource for mapping snow cover due to its spectral bands, temporal resolution, data fusion capabilities, cloud cover reduction, historical archives, and ease of use. It enables accurate and timely monitoring of snow cover, which is essential for various applications. We will be mapping snow cover using deep learning depends by creating training data, reusing model architecture, doing hyperparameter tuning, and subsequent evaluation. 

### Project Title

Mapping of snowcover at high spatio-temporal resolution using satellite imagery.

### Collaborators

Aji John

* Project lead
* Team member
* Team member
* Team member

### Why do this project ?

Mapping in high-altitude forested areas poses several challenges. The dense vegetation canopy can hinder data acquisition from satellite or aerial imagery, making it challenging to obtain accurate terrain and land cover information. Additionally, the rugged terrain and steep slopes common in high-altitude forests can complicate ground-based data collection efforts, and the risk of forest fires may limit access. Specialized remote sensing techniques, such as LiDAR and radar, are often employed to penetrate the canopy and provide detailed elevation and land cover data, but these methods can be resource-intensive. Effective mapping in high-altitude forested areas using high resolution satellite imagery like HLS is promising because of its spectral bands, temporal resolution, data fusion capabilities, cloud cover reduction, historical archives, and ease of use.

### Project goals

Our specific goals for mapping snow cover using HLS data:

1. **Snow Cover Extent:** Determine the spatial extent of snow cover within a defined region (we will define the AOI beforehand). This can involve creating binary snow/no-snow maps or calculating the fractional snow cover for each pixel.

2. **Snow Cover Duration:** Determine how long snow cover persists in a particular area during a seasonr season. This information can be essential for ecological studies.

3. **Validation:** Validate the accuracy of snow cover maps generated from HLS data using ground-based measurements from ASO, ensuring the reliability of the mapping results.

4. **Communication and Visualization:** Present the mapped snow cover information through interactive web applications or visualization tools that make the data accessible and understandable to the public.


### Data

We will use HLS aand ASO data. 

The HLS (Harmonized Landsat Sentinel) dataset is a valuable resource for Earth observation and remote sensing applications. It combines data from the Landsat and Sentinel satellite systems, providing multispectral and high-resolution imagery of the Earth's surface. HLS data offers frequent revisits to the same areas, enabling monitoring of changes over time. It includes various spectral bands, such as red, green, blue, near-infrared, and shortwave infrared, making it suitable for land cover classification, vegetation monitoring, and environmental assessments. HLS data also includes cloud mask information, aiding in the filtering of cloudy or obscured regions. It is widely used for tasks like land cover mapping, vegetation analysis, and land-use change detection.

ASO (Airborne Snow Observatory) data is a specialized dataset collected through aerial remote sensing missions. It provides detailed information about snowpack properties and characteristics in mountainous regions. ASO data is acquired using advanced LiDAR (Light Detection and Ranging) and imaging spectrometer technology, allowing for precise measurements of snow depth, snow water equivalent (SWE), snow albedo, and other snow-related parameters. These data are valuable for various applications, including water resource management, snowmelt forecasting, and climate research, as they offer high-resolution, accurate, and up-to-date information about snow cover dynamics in critical snow-dependent areas.

### Existing methods

Typically deep learning methods for snow cover mapping using satellite data involve the application of neural network architectures to analyze multispectral or hyperspectral imagery. These methods aim to classify pixels as snow-covered or snow-free, providing detailed and accurate snow cover maps. Key steps include data preprocessing, selecting an appropriate deep learning architecture (such as convolutional neural networks or U-Net), training the model using labeled data, and evaluating its performance based on metrics like accuracy and IoU (Intersection over Union). Post-processing techniques, like morphological operations, can be applied for refinement. These methods enable automated and efficient snow cover mapping, contributing to various applications in climate research, water resource management, and disaster monitoring.

### Proposed methods/tools



### Additional resources or background reading

Optional: links to manuscripts or technical documents providing background information, context, or other relevant information.

### Outline of Tasks

Mapping snow cover using deep learning techniques like U-Net involves several tasks and steps. Our initial list of tasks is below (subject to change !):

1. **Data Collection and Preparation:**
   - Acquire satellite imagery, preferably multispectral or hyperspectral data that includes bands sensitive to snow properties.
   - Collect ground truth data for training and validation, which includes labeled images indicating snow-covered and snow-free areas from ASO.
   - Preprocess the data, including resizing, normalization, and creating data splits for training, validation, and testing.

2. **Model Selection and Architecture:**
   - Choose an appropriate deep learning architecture, such as U-Net, which is commonly used for image segmentation tasks.
   - Adapt the architecture for your specific snow cover mapping task, considering input image size, the number of classes (snow-covered and snow-free), and any modifications needed.

3. **Data Augmentation:**
   - Augment the training data by applying transformations like rotations, flips, and brightness adjustments to increase the diversity of training samples.

4. **Model Training:**
   - Train the U-Net model using the labeled training data. The model learns to map input satellite imagery to a binary snow cover mask.
   - Utilize loss functions like binary cross-entropy, dice coefficient loss, or a combination of appropriate loss functions for segmentation tasks.
   - Monitor training progress with metrics like accuracy, IoU (Intersection over Union), and validation loss.

5. **Hyperparameter Tuning:**
   - Experiment with different hyperparameters, such as learning rate, batch size, and network depth, to optimize model performance.

6. **Validation and Evaluation:**
   - Validate the model on a separate dataset (validation set) to assess its generalization ability.
   - Evaluate the model's performance using metrics like accuracy, IoU, precision, and recall.
   - Generate confusion matrices and ROC curves to assess classification performance.

7. **Inference and Mapping:**
   - Use the trained model to perform inference on new satellite imagery to generate snow cover maps.
   - Apply the model to the entire study area or region of interest to create a continuous snow cover map.

8. **Visualization and Reporting:**
   - Visualize the results by overlaying the generated snow cover mask on the original satellite imagery or on a map.
   - Generate reports or visual summaries to communicate the mapped snow cover information effectively.

### Allocation of Tasks

* Write-up project goals (Aji John)
* Training data
  * ASO ? (assigned to team member A)
  * HLS (assigned to team member B)
* Prepare tiles
* Train

## Files

* `.gitignore`
<br> Globally ignored files by `git` for the project.
* `environment.yml`
<br> `conda` environment description needed to run this project.
* `README.md`
<br> Description of the project 

## Folders

Below are the three folders where runnable code snd other artifacts can be found. 

### `contributors`
Each team member can create their own folder under contributors, within which they can work on their own scripts, notebooks, and other files. Having a dedicated folder for each person helps to prevent conflicts when merging with the main branch. This is a good place for team members to start off exploring data and methods for the project.

### `notebooks`
Notebooks that are considered delivered results for the project should go in here.

### `scripts`
Helper utilities that are shared with the team should go in here.

