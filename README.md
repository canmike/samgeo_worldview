# samgeo_worldview

## Overview

This repository contains an evaluation of **SAMGeo** using **WorldView-3** satellite imagery and **Land Use/Land Cover (LULC)** classes. The study aims to analyze how well **SAMGeo**, a geospatial adaptation of the **Segment Anything Model (SAM)**, performs on high-resolution remote sensing data.

Source code can be found at [samgeo_worldview_evaluation.ipynb](https://github.com/canmike/samgeo_worldview/blob/main/samgeo_worldview_evaluation.ipynb)

## Methodology

### 1. **Data Preparation**

- **WorldView-3 satellite imagery** was used as the primary dataset.
- **LULC classification data** served as the ground truth for segmentation evaluation.
- Images were preprocessed to align with the requirements of **SAMGeo**.

### 2. **Segmentation with SAMGeo**

- The **SAMGeo model** was applied to the WorldView-3 images.
- Segmentations were generated without fine-tuning, relying on the model's zero-shot capability.

### 3. **Evaluation Against LULC Classes**

- **Predicted segmentations** were compared against **LULC ground truth**.
- **Intersection over Union (IoU)** and other relevant metrics were computed.
- Differences in segmentation performance across various land cover types were analyzed.

## Results

| **Class**   | **Accuracy** | **Precision** | **Recall** | **F1 Score** | **IoU**    |
| ----------- | ------------ | ------------- | ---------- | ------------ | ---------- |
| Agriculture | 0.7058       | 0.6773        | 0.432      | 0.5275       | 0.3583     |
| Road        | 0.9341       | 0.2073        | 0.1821     | 0.1939       | 0.1074     |
| Shrub       | 0.9177       | 0.0984        | 0.1233     | 0.1094       | 0.0579     |
| Bareland    | 0.8551       | 0.4118        | 0.3145     | 0.3566       | 0.217      |
| Forest      | 0.6643       | 0.5685        | 0.7071     | 0.6303       | 0.4601     |
| Building    | 0.8064       | 0.9129        | 0.5336     | 0.6735       | 0.5077     |
| Water       | 0.9075       | 0.4986        | 0.8721     | 0.6345       | 0.4646     |
| **Overall** | **0.7706**   | **0.6281**    | **0.5532** | **0.5883**   | **0.4167** |

## Visualization

Below are sample visualizations of **WorldView-3 images**, their corresponding **SAMGeo predictions**, and **Ground Gruth LULC masks**.

!["Legend"](https://github.com/canmike/samgeo_worldview/blob/main/figures/legend.png)

!["fig1](https://github.com/canmike/samgeo_worldview/blob/main/figures/fig1.png)

!["fig2](https://github.com/canmike/samgeo_worldview/blob/main/figures/fig2.png)

!["fig3](https://github.com/canmike/samgeo_worldview/blob/main/figures/fig3.png)

!["fig4](https://github.com/canmike/samgeo_worldview/blob/main/figures/fig4.png)

!["fig5](https://github.com/canmike/samgeo_worldview/blob/main/figures/fig5.png)
