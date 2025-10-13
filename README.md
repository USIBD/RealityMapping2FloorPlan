<img width="604" height="212" alt="Sponsor_Badge_Example" src="https://github.com/user-attachments/assets/9321da98-07f7-4928-889e-8131af9993d0" />

# Reality Mapping To Floor Plan Challenge  
Welcome to the USIBD FloorPlan Generation Challenge!
This competition is designed to benchmark and advance methods and solutions that automatically generate accurate 2D floor plans directly from 3D reality mapping data, produced through laser scanning and close-range photogrammetry.

As the demand for digital twins, building documentation, and real estate visualization continues to grow, automation has become essential. Traditional floor plan creation from 3D scans is often time-consuming, labor-intensive, and prone to human error. By developing and testing automated approaches, this challenge aims to accelerate the transformation from raw spatial data into clean, standardized 2D deliverables — saving countless hours of manual drafting while ensuring consistency and precision. 

Through this initiative, USIBD seeks to drive innovation at the intersection of reality mapping, Artifical Intelligence, and building documentation, empowering practitioners and researchers to push the limits of what’s possible in automated spatial intelligence.

## 📂 Data & Participation
Participants may either:
- **Use the benchmark dataset**, which includes high-quality point clouds and corresponding ground truth floor plans carefully curated to represent a variety of real-world building types, scales, and complexities. This dataset serves as the common reference point for performance comparison, helping ensure a level playing field across all participants.
- **Bring new datasets** in the same format as the bnchmark datasets. Teams choosing this option are encouraged to demonstrate the generalizability and robustness of their methods across diverse environments and data sources. Using proprietary data offers an opportunity to showcase solutions that excel beyond the benchmark dataset and may better reflect practical, real-world applications. Providing details on the Level of Accuracy (LOA) of the used dataset, based on [USIBD LOA Specification Version 3.1](https://usibd.org/level-of-accuracy/) is highlighted encouraged.

Regardless of dataset choice, all submissions must adhere to the standardized output formats defined by the organizers. This ensures that every result can be evaluated using a consistent set of metrics and that comparisons between teams remain objective and meaningful. Adherence to these formats also supports downstream usability — enabling the generated floor plans to integrate seamlessly into building documentation workflows, BIM systems, and spatial analytics tools.

## 📂 Dataset
Participants have the option to use the Benchmark Dataset provided by the organizers, consisting of high-quality 3D point clouds (in LAZ format) and corresponding ground truth 2D floor plans (JSON files including respective annotations). This dataset serves as a standardized testbed for algorithm development and evaluation, enabling consistent comparisons across diverse approaches. The benchmark data is derived from publicly available resources originally curated for academic evaluation in the [CVPR Scan-to-Floorplan (Scan2Plan) Challenge](https://github.com/GradientSpaces/cv4aec-challenge), developed in collaboration with several leading universities and research institutions. These datasets represent a broad range of building types and scanning conditions, offering a robust foundation for automated floor plan generation research.

Use of the Benchmark Dataset is optional — participants are equally welcome to submit results generated from their own proprietary datasets, provided they conform to the required input and output specifications described below. This flexibility encourages innovation while maintaining a fair and reproducible evaluation framework.

👉 Training Data: [50 aligned point clouds in LAZ format with ground-truth JSON floor plans](https://uofi.box.com/s/tbj6fpx4o3h8uzh9ycumfp50xjq4k959) 

👉 Validation Data: [15 point clouds with aligned ground truth](https://uofi.box.com/s/448iv4eehpbi1nxaacw0es5861aiah6j)

👉 Testing Data: [12 additional point clouds provided without ground-truth for blind evaluation](https://uofi.box.com/s/ebwvgy10hkp1a8fzm6ke5bl4u6ekytb3) 

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
- Participants are free to employ any technical approach of their choice, including proprietary software, machine learning models, classical algorithms, or hybrid methods that combine multiple techniques. Creativity and methodological diversity are encouraged.

- The use of external datasets is permitted; however, all such datasets must be clearly declared and referenced in the final submission to ensure transparency and reproducibility.

- Teams may choose to evaluate their methods on the benchmark dataset or on their own custom dataset, provided that the submission format and evaluation protocol remain consistent with the challenge specifications. This flexibility allows participants to demonstrate the robustness and adaptability of their approaches across different data sources.


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
For questions, please reach out to USIBD Reality2Floor Challenge organizers, Mani Golparvar and Ken VanBree via [email](mailto:mani.golparvar@usbid.org).  
