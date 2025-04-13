# 📌 Object Detection Using Custom SIFT

This project implements the **Scale-Invariant Feature Transform (SIFT)** algorithm from scratch for robust object detection and image matching. The custom pipeline detects keypoints invariant to scale, rotation, and illumination changes. The system is deployed as an interactive **Streamlit web app**.

---

## 📚 Course Info

- **Course**: Computer Vision (CSL7360)
- **Instructor**: Dr. Pratik Mazumder
- **Group**: 47

---

## 👥 Team Members

| Name                     | Roll No     |
|--------------------------|-------------|
| Banoth Sri Kowshika Raj | B22CS018    |
| Suhani                  | B22CS051    |
| Akash Chaudhary         | B22EE007    |
| Saurabh Chavan          | B22EE061    |
| Unisha Tirkey           | B22ES029    |

---

## 🎯 Objective

To design and implement the **SIFT algorithm from scratch** for robust keypoint detection and object matching across images. The algorithm is evaluated based on detection accuracy, matching reliability, and performance, and is deployed using a **Streamlit-based web interface** for interactive visualization.

---

## 🧠 Methodology

### 1. Custom SIFT Pipeline

The algorithm is implemented in Python with the following key stages:

#### 🌀 Scale-Space Extrema Detection
- Constructs Gaussian blurred images.
- Computes Difference of Gaussians (DoG).
- Identifies local extrema across scale and space.

#### 🎯 Keypoint Localization
- Filters low-contrast keypoints and edge responses.
- Uses Taylor expansion to refine keypoint location.

#### ↻ Orientation Assignment
- Computes gradient magnitudes and orientations.
- Builds orientation histograms to assign consistent keypoint orientation.

#### 📐 Descriptor Generation
- Extracts 16×16 region around keypoints.
- Builds 128-D descriptor vectors (4×4 blocks × 8 bins).
- Normalized for illumination invariance.

#### 🔗 Keypoint Matching
- Uses Euclidean distance and **Lowe’s ratio test** for reliable matching.

---

### 2. OpenCV SIFT Integration

OpenCV’s built-in SIFT was used for:
- Benchmarking the number of detected keypoints.
- Comparing descriptor quality and match accuracy.
- Timing performance.

---

### 3. Streamlit Deployment

An intuitive **web application** allows:
- Uploading and comparing two images.
- Visualizing detected keypoints and matches.
- Viewing intermediate outputs like Gaussian/DoG pyramids.

---

## 📈 Results

- ✅ 39 valid matches using custom implementation.
- 🕒 Higher execution time than OpenCV but fully functional.
- 📊 Streamlit interface enhances accessibility and ease of testing.

### Visual Outputs:
- Gaussian-blurred image
- DoG pyramid visualization
- Detected keypoints per image
- Matched keypoints overlay
- Orientation histograms

---

## 🖥️ Installation & Running

### 🔧 Requirements

Install dependencies using:

```bash
pip install -r requirements.txt
