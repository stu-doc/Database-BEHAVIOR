# MoBe Dataset: Motorcycle Behavior in Urban Traffic

## Overview
The MoBe (Motorcycle Behavior) dataset is a comprehensive urban traffic surveillance resource designed for motorcycle detection research. Collected from the Keyvanfar intersection in Qom, Iran, this dataset addresses critical gaps in existing motorcycle detection benchmarks by providing high-quality annotations for challenging urban scenarios.

## Data Collection
### Source
- **Provider**: Crisis Management Headquarters of Qom Municipality
- **Selection**: From 160 active surveillance cameras, Keyvanfar intersection was selected due to its exceptionally high motorcycle traffic volume and frequent violations
- **Period**: Daytime recording under clear weather conditions

### Camera Setup
Data was captured from two distinct surveillance cameras at the intersection:

**Viewpoint 1** (Camera 1):
- Resolution: 450 × 800 pixels
- 12 video clips (V1-V12)
- 35,209 frames
- 756 unique motorcycle instances

![Image](https://github.com/user-attachments/assets/a3eb517c-c1a5-4b83-a926-a25b8546eeab)


**Viewpoint 2** (Camera 2):
- Resolution: 1080 × 1920 pixels  
- 7 video clips (V13-V19)
- 14,566 frames
- 454 unique motorcycle instances

![Image](https://github.com/user-attachments/assets/197936f6-f8f0-47d8-82ed-f64389b29294)



## Dataset Statistics
| Parameter | Camera 1 | Camera 2 | Total |
|-----------|----------|----------|-------|
| **Clips** | 12 | 7 | **19** |
| **Frames** | 35,209 | 14,566 | **49,775** |
| **Unique Motorcycles** | 756 | 454 | **1,210** |
| **Total Annotations** | 159,750 BBoxes | 77,948 BBoxes | **303,389 BBoxes** |
| **Resolution** | 450×800 | 1080×1920 | - |

**Note**: "Unique Motorcycles" refers to distinct motorcycle instances across the entire video sequence (a motorcycle appearing in multiple frames is counted once). This differs from total bounding box annotations, which count every instance in every frame.

## Challenge Characteristics
The MoBe dataset presents several real-world challenges:
- **High Density**: 56.3% of scenes contain ≥6 motorcycles
- **Small Objects**: 88.1% of motorcycles are <32×32 pixels
- **Urban Complexity**: Real intersection with traffic signals, pedestrian activity, and varied vehicle types
- **Viewpoint Diversity**: Dual-camera perspectives for comprehensive coverage

## Repository Contents
### Current Available Subset
This repository contains a representative subset for evaluation and benchmarking:

📁 samples/
├── 📁 viewpoint1/
│ ├── 📁 clip1/ # Sample from Camera 1
│ │ ├── 📁 images/ # .jpg frames
│ │ └── 📁 labels/ # YOLO format .txt annotations
│ └── 📁 clip2/
│ ├── 📁 images/
│ └── 📁 labels/
└── 📁 viewpoint2/
├── 📁 clip1/ # Sample from Camera 2
│ ├── 📁 images/
│ └── 📁 labels/
└── 📁 clip2/
├── 📁 images/
└── 📁 labels/

📁 videos/
├── v1.mp4 # Viewpoint 1 - Sample Clip 1
├── v2.mp4 # Viewpoint 1 - Sample Clip 2
├── v12.mp4 # Viewpoint 2 - Sample Clip 1
└── v13.mp4 # Viewpoint 2 - Sample Clip 2


### Annotation Format
- **Format**: YOLO format (normalized coordinates)
- **Each line**: `class_id center_x center_y width height`
- **Class**: Only one class (0: motorcycle)
- **Coordinate normalization**: Values range [0, 1]

## Full Dataset Availability
**The complete MoBe dataset (all 19 video clips, 49,775 frames, 303,389 annotations) will be released upon publication of the associated research article in Image and Vision Computing.**

The full dataset will include:
- All 19 original video clips
- All extracted frames with annotations
- Detailed split information (train/val/test)
- Additional metadata and documentation

**Planned hosting**: The complete dataset will be available on [Mendeley Data/Zenodo with persistent DOI - TBD].

## Citation
If you use this dataset in your research, please cite:

[Citation will be added upon publication]
Currently under review: "MoBe: A Dual-Camera Urban Dataset and Evaluation Framework for Challenging Motorcycle Detection"


## Usage Policy
This dataset is released for **non-commercial research purposes only**.

### License
This dataset subset is released under the **Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0)**.

**You are free to:**
- Share: Copy and redistribute the material
- Adapt: Remix, transform, and build upon the material

**Under the following terms:**
- Attribution: You must give appropriate credit
- NonCommercial: You may not use the material for commercial purposes

For the full license text: https://creativecommons.org/licenses/by-nc/4.0/

## Contact
For research collaboration, full dataset access requests, or questions:
- **Corresponding Author**: Maryam Sadat Hajkabari
- **Email**: m.hajakbari@iau.ac.ir;
- **Affiliation**: Department of Computer Engineering, Qo.C., Islamic Azad University, Qom, Iran.

## Acknowledgments
We thank the Crisis Management Headquarters of Qom Municipality for providing access to surveillance footage.


