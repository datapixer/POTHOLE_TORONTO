# POTHOLE_TORONTO
This project is an end-to-end computer vision framework automating municipal road distress detection. Addressing urban infrastructure needs, the project integrates real-time civic data with custom instance segmentation.Methodology involves capturing 104 high-resolution asphalt images across Toronto intersections using a Samsung Galaxy S25 Ultra, guided by official 311 municipal records. Custom Python scripts generated pixel-level polygon masks, extracted coordinate text files, and compiled a structured metadata table tracking timestamps, GPS coordinates, distress sub-categories, and maintenance urgency.A YOLO11n-seg model was trained locally via GPU acceleration using the curated dataset. Conclusions: The model achieved an overall mean Average Precision ($\text{mAP}_{50}$) of 0.87, demonstrating that smartphone-captured municipal data paired with automated local training provides an efficient, scalable solution for city planners to optimize infrastructure asset tracking and repair scheduling.

## Project Workflow:
### Step 1: Data Collection & Field Capture

Sourced active municipal infrastructure reports from the 311 Toronto database to identify specific street intersections with reported potholes for the current month.

Captured 104 high-resolution photos across these Toronto intersections using a Samsung Galaxy S25 Ultra.

### Step 2: Custom Annotation & Mask Generation

Developed custom Python scripts to create precise manual segmentation masks over the exact locations of potholes within each photograph.

Extracted the vertex coordinates of the drawn polygon masks and compiled them into standardized text label files.

### Step 3: Structured Metadata Compilation

Built a comprehensive master table linking each image file to its corresponding metadata.

Recorded critical attributes including timestamps, street intersections, geographic coordinates, pothole categories/sub-categories, and maintenance urgency levels.

### Step 4: Model Training & Inference

Integrated the curated dataset—comprising original asphalt images, custom polygon masks, text coordinate files, and structured label definitions—into a YOLO11 instance segmentation architecture.

Executed local GPU-accelerated model training and validation to accurately predict, segment, and classify road distress features on entirely new, unseen images.
