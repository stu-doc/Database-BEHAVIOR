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