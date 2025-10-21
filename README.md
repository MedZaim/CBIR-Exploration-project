
# 🔍 Content-Based Image Retrieval (CBIR) System

## 🧑‍💻 Author

**Mohamed ZAIM**  
Master’s Student in **MLAIM (Master : Machine Learning Avancée et Intelligence Multimédia)**  
Faculté des Sciences Dhar El Mahraz (FSDM), Université Sidi Mohamed Ben Abdellah (USMBA), Fès, Morocco  
Full-Stack Developer | AI & Intelligent Systems
📫 [LinkedIn Profile](https://www.linkedin.com/in/mohamed-zaim-a68a602bb/)



This project focuses on building a **Content-Based Image Retrieval (CBIR)** system that retrieves images similar to a query image based on **visual content**. The system extracts and combines multiple **image features** and evaluates its robustness under **geometric transformations**.

## 📖 Project Overview

The CBIR system extracts four types of image features:

1. **Intensity (Grayscale pixel values)**
2. **Color**
   - Color Moments (Mean and Standard Deviation for R, G, B channels)
   - Quantized HSV Histogram (H=8, S=2, V=2 → 32 bins)
3. **Texture**
   - GLCM (Gray-Level Co-Occurrence Matrix) properties: Contrast, Correlation, Energy, Homogeneity
4. **Shape**
   - Hu Moments (7 invariant moments)

The system is implemented in **Python** using: `OpenCV`, `scikit-image`, `NumPy`, `scikit-learn`, and `Matplotlib`.

## 🧩 Features

- Extraction of multiple image features for robust retrieval
- Query multiple images against a dataset
- Evaluate robustness to geometric transformations: rotation, scaling, flipping
- Fully implemented in **Google Colab**

## 🗂️ Project Structure

```
CBIR-Exploration-Project/
│
├── CBIR_System.ipynb            # Jupyter Notebook with full code
├── CBIR_DataSet/obj_decoys/     # Dataset images (CBIR_DataSet folder)
├── CBIR_DataSet/img_requetes/   # Query images to test retrieval
├── results/                     # Optional: store example retrieval outputs
└── README.md                    # Project documentation
```

## ⚙️ How to Run

1. Open **CBIR_System.ipynb** in **Google Colab**
2. Mount your Google Drive and set the paths to the dataset:

```python
dataset_folder = "/content/drive/MyDrive/CBIR_DataSet/obj_decoys"
query_folder = "/content/drive/MyDrive/CBIR_DataSet/img_requetes"
```

3. Alternatively, you can download the dataset here:
[CBIR_DataSet](https://drive.google.com/drive/folders/1qbXd7wJVW8c5hVez_j5Tdu7YV5GtSKYC?usp=sharing)

4. Run all cells to extract features and perform retrieval tests.

## 📊 Results and Analysis

- **Color features** provide good discrimination but are sensitive to illumination changes.
- **Texture features (GLCM)** are robust to small geometric changes.
- **Hu Moments** are invariant to rotation and scale, making shape features robust.
- Combining all features gives the **best performance and robustness**.
- The system successfully retrieves similar images even after applying transformations like rotation, scaling, and flipping.

## 🏷️ Keywords

`Python` `OpenCV` `CBIR` `Computer Vision` `Image Processing` `Feature Extraction` `Machine Learning` `MLAIM`
