# Scan2FloorPlanChallenge  

Welcome to the FloorPlan Generation Challenge!
This competition is designed to benchmark and advance methods as well as solutions to generate accurate 2D floor plans directly from 3D reality mapping data.


## 📂 Data & Participation
Participants may either:
- **Use the benchmark dataset provided by the organizers** (point clouds + ground truth floor plans), OR
- **Bring their own proprietary datasets** in the same format.

All submissions must adhere to the standardized input/output formats described below, ensuring results remain comparable across teams.

## 📂 Benchmark Dataset (optional to use)
- **Training Set:** 50 aligned point clouds in LAZ format with ground truth JSON floor plans.
- **Validation Set:** 15 point clouds with aligned ground truth.
- **Test Set:** 12 additional point clouds provided without ground truth for blind evaluation.

**Supported formats** 
- Point Clouds: LAZ
- Floor Plans: JSON annotations
  

👉 Training Data: [Point Cloud + Ground Truth](https://uofi.box.com/s/tbj6fpx4o3h8uzh9ycumfp50xjq4k959) 

👉 Validation Data: [Point Cloud + Ground Truth](https://uofi.box.com/s/448iv4eehpbi1nxaacw0es5861aiah6j)

👉 Testing Data: [Point Cloud ONLY](https://uofi.box.com/s/ebwvgy10hkp1a8fzm6ke5bl4u6ekytb3) 

--
## 📑 Submission Format  

Submissions must follow the same **JSON schema** as the provided ground truth.  Each JSON file should include:  

- **Room polygons** (wall boundaries)  
- **Column positions**
- **Door locations**  
- **Metadata** (floor ID, building ID)  

A sample submission is available in the [GitHub repository](#).  

---
## 📊 Evaluation Metrics  

Submissions will be evaluated using both geometric and topological metrics:

### 🔹 Geometric Metrics  
- **IoU**  Intersection-over-Union (IoU) for room polygons
- **Endpoint Accuracy**  (Precision/Recall/F-measure at 2in, 4in, 10in)
- **Wall Orientation Similarity**  (cosine similarity between predicted vs. ground truth wall segments)


### 🔹 Topological Metrics  
- **Warping Error**   (fraction of unmatched pixels after homotopic warping)
- **Betti Number Error**  (difference in topological correctness)

For exact details and code regarding evaluation metrics, please look here: 
[2d_floorplan_eval](https://github.com/reconstruct/Scan2FloorPlan/tree/main/2d_floorplan_eval)

--
## 🏆 Challenge Rules  
- Participants may use any method: proprietary software, machine learning, classical, or hybrid approaches.
- External datasets are allowed but must be declared in the submission.
- Teams may choose to evaluate on the benchmark dataset or on their own provided dataset, as long as the submission format is consistent.

---

## 🔗 Resources  
- 📥 [Dataset Download](#)  
- 🧩 [Evaluation Toolkit](#)  
- 🚀 [Submission Portal](#)  

---

## 📅 Important Dates  

- **Dataset Release:** Oct 10, 2025  
- **Submission Deadline:** Dec 8, 2025 
- **Winners Announced:** Tuesday or Wednesday (Feb. 17 or 18, 2026). 

---

## 📧 Contact  
For questions, please reach out to **[USIBD Competition Team](mani.golparvar@usbid.org)**.  
