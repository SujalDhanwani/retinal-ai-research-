# Base Paper Notes  
## Detection and Classification of Hypertensive Retinopathy Using Deep Learning

---

# 1. Problem Statement

The paper focuses on detecting and classifying **Hypertensive Retinopathy (HR)** using retinal fundus images and deep learning techniques.

The main goal is:
- Early disease detection
- Severity classification
- Helping doctors prevent serious complications like:
  - Heart attacks
  - Strokes
  - Vision damage

---

# 2. Why This Problem is Important

Hypertensive Retinopathy happens when high blood pressure damages retinal blood vessels.

## Main Challenges
- Early symptoms are difficult to detect manually
- Borderline stages are hard for doctors to classify
- Delayed diagnosis can lead to severe health problems

## Why AI Helps
AI-based systems can:
- Detect disease early
- Improve diagnosis accuracy
- Support ophthalmologists
- Reduce manual errors

---

# 3. Dataset Used

## Dataset Name
MESSIDOR Retinal Fundus Dataset

## Dataset Details
- Total Images: 1200 retinal images
- Image Type: Retinal fundus images
- Original Purpose: Diabetic Retinopathy dataset
- Relabeled For: Hypertensive Retinopathy classification

## Important Note
The dataset was relabeled using:
- AVR (Artery Vein Ratio)

---

# 4. Main Methodology

## Overall Pipeline

### Step 1 — Retinal Image Collection
- Collect retinal fundus images from MESSIDOR dataset

### Step 2 — Preprocessing
Performed image enhancement techniques:
- Image resizing
- Green channel extraction
- Contrast enhancement

### Step 3 — Blood Vessel Extraction
- Extract retinal blood vessels
- Detect optic disc region
- Segment vessels

### Step 4 — AVR Calculation
Calculate:
- Artery Vein Ratio (AVR)

Used to measure narrowing of blood vessels.

### Step 5 — Label Generation
Images categorized into:
- 9 hypertensive retinopathy classes

Including:
- Borderline severity stages

### Step 6 — Deep Learning Classification
Used:
- DCNN (Deep Convolutional Neural Network)

For final disease classification.

---

# 5. Novelty of the Paper

## Main Contributions

### 1. Proposed 9-Class Classification
Unlike previous works using only 4 classes.

### 2. Added Borderline Severity Stages
Improves early-stage disease detection.

### 3. Combined AVR + DCNN
Used:
- AVR-based medical labeling
- Deep learning classification together

---

# 6. Initial Limitations Identified

## Dataset Limitations
- Dataset originally belongs to Diabetic Retinopathy
- Not a dedicated HR dataset

## Data Limitations
- Small dataset size
- Limited diversity

## Model Limitations
- Uses basic CNN architecture
- No advanced architectures like:
  - Vision Transformers
  - EfficientNet

## Feature Engineering Limitation
- Manual AVR feature extraction required

## Explainability Limitation
No Explainable AI techniques used:
- No GradCAM
- No XAI visualization

## Validation Limitation
- Limited external validation
- No real-world deployment testing

---