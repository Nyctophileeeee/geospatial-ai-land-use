# geospatial-ai-land-use
🛰️ Geospatial AI for Land Use Classification
# 🛰️ Geospatial AI for Land Use Classification

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat-square&logo=python)
![CNN](https://img.shields.io/badge/Model-CNN%20%7C%20Random%20Forest-orange?style=flat-square)
![Data](https://img.shields.io/badge/Data-Satellite%20Imagery-4CAF50?style=flat-square)
![Module](https://img.shields.io/badge/Module-Discipline--Specific%20AI%20Project-purple?style=flat-square)

> **University of Bradford** — Discipline-Specific Artificial Intelligence Project | Nov 2024 – May 2025

An AI system that combines **satellite imagery and machine learning** to automatically classify land use categories — supporting applications in urban planning, agriculture, and environmental protection.

---

## 🌍 Why This Matters

Understanding how land is used — residential zones, farmland, forests, industrial areas, water bodies — is critical for:
- 🏙️ **Urban planners** making development decisions
- 🌾 **Agricultural bodies** monitoring crop coverage
- 🌿 **Environmental agencies** tracking deforestation and habitat loss
- 🏛️ **Government bodies** enforcing land use regulations

Manual analysis of satellite imagery is slow, expensive, and inconsistent. AI makes it scalable.

---

## 🎯 Project Overview

This project investigates how **Convolutional Neural Networks (CNNs)** and **Random Forest classifiers** can be applied to multi-spectral satellite images to accurately classify land use at scale — while addressing real-world challenges of data scarcity, computational constraints, and ethical AI deployment.

---

## 🗂️ Land Use Categories

| Class | Description |
|-------|-------------|
| 🏠 Residential | Housing estates, suburban areas |
| 🏭 Industrial | Factories, warehouses, infrastructure |
| 🌾 Agricultural | Cropland, farmland, pasture |
| 🌲 Forest/Vegetation | Woodland, parks, green spaces |
| 💧 Water Bodies | Rivers, lakes, reservoirs |
| 🏗️ Urban/Commercial | City centres, retail, roads |

---

## 🏗️ Model Architecture

### Convolutional Neural Network (CNN)
```
Input: Satellite Image Patch (64x64x3)
    │
    ▼
Conv2D (32 filters, 3x3) → ReLU → MaxPooling
    │
Conv2D (64 filters, 3x3) → ReLU → MaxPooling
    │
Conv2D (128 filters, 3x3) → ReLU → MaxPooling
    │
Flatten → Dense(256) → Dropout(0.5)
    │
Dense(6) → Softmax
    │
Output: Land Use Class
```

### Random Forest
- **n_estimators**: 200 trees
- **Features**: Spectral bands + texture descriptors (GLCM)
- Used as a baseline and for feature importance analysis

---

## 📊 Key Findings

- CNNs outperformed Random Forest on complex urban/suburban boundary classification
- **Data augmentation** (flipping, rotation, colour jitter) significantly reduced overfitting on scarce training samples
- **Multi-modal data integration** (combining optical + elevation data) recommended for future accuracy gains
- Identified critical ethical considerations: algorithmic bias in training data coverage, GDPR implications for surveillance-adjacent applications

---

## ⚠️ Challenges Addressed

| Challenge | Approach |
|-----------|----------|
| Data Scarcity | Augmentation + transfer learning from pre-trained CNNs |
| Class Imbalance | Weighted loss functions + oversampling |
| Computational Cost | Patch-based inference + model compression |
| Ethical Concerns | Bias audit, transparent documentation, consent considerations |

---

## 🛠️ Tech Stack

| Tool | Usage |
|------|-------|
| Python 3.10+ | Core language |
| TensorFlow / Keras | CNN implementation |
| Scikit-Learn | Random Forest, preprocessing |
| Rasterio / GDAL | Satellite image processing |
| NumPy / Pandas | Data manipulation |
| Matplotlib / Seaborn | Visualisation |

---

## 📁 Repository Structure

```
geospatial-ai-land-use/
├── notebooks/
│   ├── 01_data_preprocessing.ipynb
│   ├── 02_cnn_model.ipynb
│   └── 03_random_forest_baseline.ipynb
├── src/
│   ├── data_loader.py
│   ├── cnn_model.py
│   ├── random_forest.py
│   └── visualise.py
├── outputs/
│   ├── classification_map.png
│   └── model_comparison.png
├── report/
│   └── GEOSPATIAL_AI_REPORT.pdf
└── README.md
```

---

## 🚀 Quick Start

```bash
git clone https://github.com/ayushacharya/geospatial-ai-land-use
cd geospatial-ai-land-use
pip install -r requirements.txt
jupyter notebook notebooks/01_data_preprocessing.ipynb
```

---

## 🔮 Future Work

- [ ] Integrate multi-spectral + LiDAR/elevation data for improved accuracy
- [ ] Deploy as a web API for real-time land use monitoring
- [ ] Expand to change detection (comparing imagery over time)
- [ ] Explore Vision Transformers (ViT) for satellite image classification

---

## 📬 Contact

**Ayush Acharya** | ayush15acharya@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/ayushacharya-96ab09243) | 🌐 [Portfolio](https://gamma.app/docs/Ayush-Acharyauy2x9ksx9a2o771)
