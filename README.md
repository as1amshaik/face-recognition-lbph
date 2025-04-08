# Face Recognition using LBPH

This project implements a real-time face recognition system using OpenCV’s Local Binary Patterns Histograms (LBPH) algorithm. It accurately identifies known faces and displays both the **predicted class ID** and a **confidence score** — where **higher the score, higher the confidence** of the match.

---

## 🔍 Features

- Real-time face recognition using OpenCV
- Uses LBPH algorithm for robust performance under varying lighting
- Predicts class ID and confidence score for each face
- Lightweight and fast — suitable for webcam and embedded devices
- Easily extensible for new faces

---

## 🧠 Machine Learning Concept Used

### What is LBPH?

**Local Binary Pattern Histogram (LBPH)** is a feature extraction algorithm commonly used for facial recognition. It converts images into numerical representations based on local texture.

#### How LBPH Works Internally:

1. **Grayscale Conversion**:
   - Converts input face image to grayscale.

2. **LBP Operator**:
   - For each pixel, compare it with surrounding 8 neighbors.
   - If neighbor pixel ≥ center pixel, write 1; else 0.
   - This forms an 8-bit binary pattern (e.g., 11001010).

3. **Grid Division**:
   - Image is divided into small grids (e.g., 8x8).
   - A histogram of LBP values is calculated for each grid.

4. **Histogram Concatenation**:
   - All histograms from each grid are concatenated into a single feature vector.

5. **Training**:
   - During training, these feature vectors are stored along with associated class labels (person IDs).

6. **Prediction**:
   - During testing, the feature vector of the test image is compared to all stored vectors using a distance metric (typically Chi-Square or Euclidean).
   - The closest match gives:
     - **Predicted class ID**
     - **Confidence score** — **higher the score, better the match**.

---

## 📸 Example Prediction Output
