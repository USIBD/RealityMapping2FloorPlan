# Scan2FloorPlanChallenge  

Welcome to the **USIBD Scan2FloorPla Challenge**!  
This competition focuses on generating accurate floor plans directly from 3D point clouds.  

---
## 📂 Dataset  

The dataset for this competition consists of multiple buildings, each consisting of multiple floors and a variety of arcihtectural features.  

- **Training Set:** 50 aligned point clouds in LAZ format from dozens of buildings. Each point cloud includes a ground truth floor plan which is aligned with the point cloud, in the same coordinate system.  
- **Validation Set:** 15 point clouds from five different building with aligned ground truth floor plans.  
- **Test Set:** For blind evaluation purposes, 12 additional point clouds from other buildings --not used within the training and testing datasets-- are offered without ground truth.   

Similar to recent Computer Vision and Pattern Recognition Conference events, all data is distributed in:  
- **LAZ** format for point clouds  
- **JSON** format for floor plan annotations  

👉 Training Data: [Point Cloud + Ground Truth](https://uofi.box.com/s/tbj6fpx4o3h8uzh9ycumfp50xjq4k959) 
👉 Validation Data: [Point Cloud + Ground Truth](https://uofi.box.com/s/448iv4eehpbi1nxaacw0es5861aiah6j)
👉 Testing Data: [Point Cloud ONLY](https://uofi.box.com/s/ebwvgy10hkp1a8fzm6ke5bl4u6ekytb3) 

---
## 📑 Submission Format  

Submissions must follow the same **JSON schema** as the provided ground truth.  Each JSON file should include:  

- **Room polygons** (wall boundaries)  
- **Column positions**
- **Door locations**  
- **Metadata** (floor ID, building ID)  

A sample submission is available in the [GitHub repository](#).  

---

## 📊 Evaluation Metrics  

Our evaluation metrics fall into two categories:
### 🔹 Geometric Metrics  
1. **oU**  
   - Intersection-over-Union for each room polygon.  
   - Rooms defined as fully enclosed spaces, separated by walls and doors.  

2. **Endpoint Accuracy**  
   - Precision, Recall, and F-measure at thresholds of **2in, 4in, and 10in**.  
   - Endpoints matched to ground truth via the Hungarian algorithm.  

3. **Wall Orientation**  
   - Cosine similarity between predicted and ground truth wall segments.  
   - Unmatched walls will score zero.  

### 🔹 Topological Metrics  
1. **Warping Error**  
   - To report fraction of unmatched pixels after warping, Homotopic deformation will be used to align predicted and ground truth floor plans.  

2. **Betti Number Error**  
   - Compares topological correctness and is computed as the absolute difference between predicted and ground truth Betti numbers.  

For exact details and code regarding evaluation metrics, please look here: 
[2d_floorplan_eval](https://github.com/reconstruct/Scan2FloorPlan/tree/main/2d_floorplan_eval)

--
## 🏆 Challenge Rules  

- Participants may use any proprietary software or algorithm (deep learning, classical, or hybrid).  
- Usage of external datasets for training/testing or validation is allowed, but must be declared in the submission.  

---

## 🔗 Resources  
- 📥 [Dataset Download](#)  
- 🧩 [Evaluation Toolkit](#)  
- 🚀 [Submission Portal](#)  

---

## 📅 Important Dates  

- **Dataset Release:** Oct 10, 2025  
- **Submission Deadline:** Dec 12, 2025 
- **Winners Announced:** Jan 9, 2025  

---

## 📧 Contact  
For questions, please reach out to **[USIBD Competition Team](mani.golparvar@usbid.org)**.  
