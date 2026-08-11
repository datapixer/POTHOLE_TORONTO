# POTHOLE_TORONTO
UrbanRoadVision is an end-to-end computer vision and civic data analytics pipeline designed to automate the detection, segmentation, and triage of municipal road distress features. Inspired by urban infrastructure challenges, this project leverages advanced instance segmentation architectures to bridge the gap between raw computer vision outputs and actionable public service workflows. By streamlining how surface anomalies like potholes and pavement cracks are identified and classified, the system assists municipal planners and civic engineers in optimizing maintenance schedules and improving response times for public reporting systems.

## Technical Architecture & Methodology
At the core of the pipeline is a fine-tuned YOLO11 instance segmentation model (YOLO11n-seg), optimized to handle spatial feature extraction on high-resolution asphalt imagery. The project workflow is structured into several key stages:

Dataset Preparation & Curation: Utilizes a focused, high-quality image dataset specifically annotated for road infrastructure anomalies, split into training and validation sets to prevent overfitting while maximizing generalization across varying lighting and weather conditions.

Automated Label Conversion Workflows: Integrates custom preprocessing scripts to clean, standardize, and convert annotation formats into compatible YOLO segmentation structures.

GPU-Accelerated Model Training: Leverages robust PyTorch-based routines to train the segmentation heads, executing multi-class classification that categorizes distress types, sub-categories, and localized maintenance urgency tiers.

Spatial & Civic Analytics Integration: Connects detected visual coordinates with spatial mapping logic, allowing municipal stakeholders to analyze the density and severity of infrastructure wear across different geographic zones.

## Key Features
Precise Instance Segmentation: Goes beyond simple bounding boxes by generating pixel-level polygon masks for precise area measurement of potholes and surface cracks.

Multi-Class Triage: Automatically classifies distress severity to help prioritize high-risk road hazards for immediate repair.

End-to-End Reproducibility: Features modular Python scripts covering data ingestion, augmentation, training execution, and inference visualization.
