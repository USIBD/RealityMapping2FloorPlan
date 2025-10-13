<img width="604" height="212" alt="Sponsor_Badge_Example" src="https://github.com/user-attachments/assets/9321da98-07f7-4928-889e-8131af9993d0" />

# RealityMapping2FloorPlanChallenge  
Welcome to the USIBD FloorPlan Generation Challenge!
This competition is designed to benchmark and advance methods and solutions that automatically generate accurate 2D floor plans directly from 3D reality mapping data, produced through laser scanning and close-range photogrammetry.

As the demand for digital twins, building documentation, and real estate visualization continues to grow, automation has become essential. Traditional floor plan creation from 3D scans is often time-consuming, labor-intensive, and prone to human error. By developing and testing automated approaches, this challenge aims to accelerate the transformation from raw spatial data into clean, standardized 2D deliverables — saving countless hours of manual drafting while ensuring consistency and precision.

Through this initiative, USIBD seeks to drive innovation at the intersection of reality capture, AI, and building documentation, empowering practitioners and researchers to push the limits of what’s possible in automated spatial intelligence.

## 📂 Data & Participation
Participants may either:
- **Use the benchmark dataset provided by the organizers** (point clouds + ground truth floor plans), OR
- **Bring their own proprietary datasets** in the same format.

All submissions must adhere to the standardized output formats described below, ensuring results remain comparable across teams.

## 📂 Benchmark Dataset (optional to use- you can use your own dataset)
- **Training Set:** 50 aligned point clouds in LAZ format with ground-truth JSON floor plans.
- **Validation Set:** 15 point clouds with aligned ground truth.
- **Test Set:** 12 additional point clouds provided without ground-truth for blind evaluation.

**Supported formats** 
- Point Clouds: LAZ
- Floor Plans: JSON files including respective annotations
  
👉 Training Data: [Point Cloud + Ground Truth](https://uofi.box.com/s/tbj6fpx4o3h8uzh9ycumfp50xjq4k959) 
👉 Validation Data: [Point Cloud + Ground Truth](https://uofi.box.com/s/448iv4eehpbi1nxaacw0es5861aiah6j)
👉 Testing Data: [Point Cloud ONLY](https://uofi.box.com/s/ebwvgy10hkp1a8fzm6ke5bl4u6ekytb3) 

---
## 📑 Submission Format  

Submissions must follow the same **JSON schema** as the provided ground-truth.  Each JSON file should include:  
- **Metadata** (floor ID, building ID)
- **Wall boundaries** (polygons)  
- **Column positions**
- **Door locations**  
 
---
## 📊 Quantitative Evaluation  
Submissions will be evaluated quantitively using both geometric and topological metrics:

### 🔹 Geometric Metrics  
- **IoU**  Intersection-over-Union (IoU) for room polygons
- **Endpoint Accuracy**  (Precision/Recall/F-measure at 2in, 4in, 10in)
- **Wall Orientation Similarity**  (cosine similarity between predicted vs. ground truth wall segments)

### 🔹 Topological Metrics  
- **Warping Error**   (fraction of unmatched pixels after homotopic warping)
- **Betti Number Error**  (difference in topological correctness)

For exact details and code regarding evaluation metrics, please look here: 
[2d_floorplan_eval](https://github.com/reconstruct/Scan2FloorPlan/tree/main/2d_floorplan_eval)

---
## 🏆 Challenge Rules  
- Participants may use any method: proprietary software, machine learning, classical, or hybrid approaches.
- External datasets are allowed but must be declared in the submission.
- Teams may choose to evaluate on the benchmark dataset or on their own provided dataset, as long as the submission format is consistent.

---
## 🔗 Resources  
- 📥 Dataset Download [1](https://uofi.box.com/s/ur2ieo3lbfsthk7h5hz0mdkx5439z23m)  [2](https://uofi.box.com/s/448iv4eehpbi1nxaacw0es5861aiah6j)
- 🧩 [Evaluation Toolkit](https://uofi.box.com/s/ebwvgy10hkp1a8fzm6ke5bl4u6ekytb3)  
- 🚀 [Submission Portal](https://uofi.app.box.com/f/9a6b181c229a4803bde32f8939edc0b2)  

---
## 📅 Important Dates  
- **Dataset Release:** Oct 15, 2025  
- **Submission Deadline:** Dec 8, 2025 
- **Winners Announced:** Feb. 18, 2026

---
## 📧 Contact  
For questions, please reach out to **[USIBD Competition Team](mani.golparvar@usbid.org)**.  
