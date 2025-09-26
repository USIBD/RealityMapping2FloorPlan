# 2D Floor Plan Reconstruction Challenge  

Welcome to the **USIBD 2D Floor Plan Reconstruction Challenge**!  
This competition focuses on generating accurate architectural floor plans directly from 3D point cloud data.  

---

## 📂 Dataset  

The dataset consists of multiple buildings of varying sizes and complexities, with multiple floors per building.  

- **Training Set:** 20 buildings, 50 aligned point clouds (LAZ format). Each point cloud includes a ground truth 2D floor plan aligned in the same coordinate system.  
- **Validation Set:** 6 buildings, 15 point clouds with aligned ground truth floor plans.  
- **Test Set:** 5 buildings, 12 point clouds without ground truth (for blind evaluation).  

All data is distributed in:  
- **LAZ** format for point clouds  
- **JSON** format for floor plan annotations  


👉 Training Data: [Point Cloud + Ground Truth](https://oregonstate.box.com/s/kwjn01g84d0fka2j2vrjfd8j8w5n37e6) 

👉 Validation Data: [Point Cloud + Ground Truth](https://oregonstate.box.com/s/ber73d1njhxo4vwc4i4qmtbmyyimrprj)

👉 Testing Data: [Point Cloud ONLY](https://oregonstate.box.com/s/op8bul06ea1hm7ldnfmqecrt32kctk64) 

---
## 📑 Submission Format  

Submissions must follow the same **JSON schema** as the provided ground truth.  
Each JSON file should include:  

- **Room polygons** (wall boundaries)  
- **Door locations**  
- **Column positions**  
- **Metadata** (floor ID, building ID)  

A sample submission format is available in the [GitHub repository](#).  

---

## 📊 Evaluation Metrics  

We evaluate both **geometric accuracy** and **topological consistency**.  

### 🔹 Geometric Metrics  
1. **Room IoU**  
   - Intersection-over-Union for each room polygon.  
   - Rooms are defined as fully enclosed spaces separated by walls and doors.  

2. **Endpoint Accuracy**  
   - Precision, Recall, and F-measure at thresholds of **2in, 4in, and 10in**.  
   - Endpoints matched to ground truth via the Hungarian algorithm.  

3. **Wall Orientation**  
   - Cosine similarity between predicted and ground truth wall segments.  
   - Unmatched walls receive a score of zero.  

### 🔹 Topological Metrics  
1. **Warping Error**  
   - Uses homotopic deformation to align predicted and ground truth floor plans.  
   - Reports fraction of unmatched pixels after warping.  

2. **Betti Number Error**  
   - Compares topological correctness (rooms, holes, connectivity).  
   - Computed as the absolute difference between predicted and ground truth Betti numbers.  

For exact details and code regarding evaluation metrics, please look here: [2d_floorplan_eval](https://github.com/reconstruct/Scan2FloorPlan/tree/main/2d_floorplan_eval)
---

## 🏆 Challenge Rules  

- Participants may use any proprietary software or algorithm (deep learning, classical, or hybrid).  
- External datasets particularly in the case of vendors are allowed, but must be declared in the submission.  

---

## 🔗 Resources  

- 📥 [Dataset Download](#)  
- 🧩 [Evaluation Toolkit](#)  
- 🚀 [Submission Portal](#)  

---

## 📅 Important Dates  

- **Dataset Release:** TBD  
- **Validation Submission Deadline:** TBD  
- **Final Submission Deadline:** TBD  
- **Winners Announced:** TBD  

---

## 📧 Contact  

For questions, please reach out to **[USIBD Competition Team](#)**.  
