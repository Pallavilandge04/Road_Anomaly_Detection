# Road_Anomaly_Detection
Documentation of Project
# Road Anomaly Detection

This project focuses on detecting road anomalies such as potholes, cracks, and other defects using a YOLOv8 model. The detection is performed on GPS-tagged images, and the output is a CSV report containing detailed defect information including location, GPS coordinates, and defect counts.

---

##  Description

The notebook `Final_Scipts.ipynb` includes all the required code (with detailed comments) for:

- Reading YOLO-labeled images
- Extracting GPS data (from associated text files or metadata)
- Mapping defect annotations to their corresponding frames
- Creating a structured CSV report containing:
  - Frame name
  - Latitude & Longitude
  - Location name
  - Defect categories
  - Count of each defect per image

---

##  Inputs

-  `images/`: Labeled images with GPS info using CVAT Tool
-  `labels/`: YOLOv8-format `.txt` files for each image
-  `gps_data/`: Text files containing GPS coordinates and location names (if not embedded in EXIF)

##  Outputs

- `metadata_report.csv`: A CSV containing the complete metadata and defect summary
  - Columns: `Frame`, `Latitude`, `Longitude`, `Location`, `Defects`, `Count`

---

## Requirements & Setup

Install the required dependencies:

```bash
pip install ultralytics opencv-python pandas numpy geopy
