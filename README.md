# Object Segmentation Using Core Image Processing On Coil-20 Dataset

This project implements an end-to-end object segmentation pipeline using traditional image processing techniques. The pipeline is applied to both processed and unprocessed versions of the COIL-20 dataset and performs object extraction using filtering, edge detection, thresholding, morphological operations, and contour analysis.

A detailed explanation of methodology, experiments, and results is provided in the accompanying LaTeX report included in this repository.

---

## Dataset

This project uses the COIL-20 dataset developed at Columbia University.

COIL-20 unprocessed dataset contains grayscale images of 5 objects captured from multiple viewpoints.

COIL-20 processed dataset contains grayscale images of 20 objects captured from multiple viewpoints, in which background is cropped.

Download the dataset manually and place the folders in your Google Drive as described below.

---

## Required Google Drive Folder Structure

The script expects the dataset to be located inside Google Drive with the following structure:
```
MyDrive/
│
├── coil-20-proc/
├── coil-20-unproc/
```

The script automatically creates the following output folders:
```
MyDrive/
│
├── output_processed/
├── output_unprocessed/
```

If the folder names differ, update the `base_path` variable in the script accordingly.

---

## Methodology Overview

The segmentation pipeline performs the following steps:

1. Gaussian noise removal  
2. Edge detection (Sobel and Canny)  
3. Adaptive thresholding  
4. Morphological closing and opening  
5. External contour extraction  
6. Largest contour selection  
7. Object masking and bounding box generation  

Intermediate results are visualized for one processed and one unprocessed sample image. Final segmented outputs are saved for the entire dataset.

---

## Requirements

Install the required Python libraries:

pip install opencv-python numpy matplotlib

If running in Google Colab:

from google.colab import drive  
drive.mount('/content/drive')

---

## How to Run

1. Upload `coil-20-proc` and `coil-20-unproc` folders to Google Drive.
2. Ensure the `base_path` variable matches your Drive location.
3. Run the script in Google Colab.
4. Segmented outputs will be saved automatically in:
   - `output_processed/`
   - `output_unprocessed/`

---

## Repository Structure

├── segmentation_script.py  
├── report.pdf  
├── README.md  

---

## Report

The LaTeX report included in this repository provides:

- Detailed explanation of each processing stage  
- Comparison between processed and unprocessed datasets  
- Analysis of Sobel vs Canny edge detection  
- Experimental observations and results  

Refer to `report.pdf` for complete technical documentation.

---

## Authors

- Nithila R  
- Kanmani R  
Department of CSE  
Sri Sivasubramaniya Nadar College of Engineering
