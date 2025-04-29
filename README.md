#Project Overviews

### 1. Data Privacy Notebook (`DataPrivacy1_Noura.ipynb`)
This notebook demonstrates a pipeline for applying and comparing three core privacy-preserving techniques on the UCI Adult census dataset (predicting whether an individual’s income exceeds \$50K):

1. **Noise Addition**  
   - Adds calibrated Laplace or Gaussian noise to numeric features.  
   - Illustrates the impact on downstream model accuracy and feature distributions.

2. **k-Anonymity & Microaggregation**  
   - Clusters records into groups of size ≥ *k* and replaces values with group averages.  
   - Shows how increasing *k* affects privacy levels and classification performance.

3. **Differential Privacy**  
   - Uses IBM’s Diffprivlib to train a Logistic Regression model under ε-differential privacy.  
   - Reports the trade-off between privacy budget (ε) and predictive metrics (accuracy, ROC-AUC).

At the end of the notebook, you’ll find side-by-side comparisons of utility (accuracy, precision, recall) versus privacy guarantees for each method, together with visualizations that help interpret the results.

---

### 2. Image Privacy Notebook (`ImagePrivacyNotebook.ipynb`)
This notebook explores techniques for anonymizing sensitive regions in images, with a focus on human faces:

1. **Face Detection & Blurring**  
   - Detects faces using OpenCV’s pre-trained cascade classifiers.  
   - Applies Gaussian blur to conceal identity while preserving context.

2. **Pixelation & Mosaic Filters**  
   - Divides detected regions into blocks and replaces each block with its average color.  
   - Demonstrates different block sizes to balance between privacy and image intelligibility.

3. **Differentially Private Image Release**  
   - Implements a simple mechanism that adds noise to pixel values in sensitive areas.  
   - Visualizes how varying the privacy parameter (ε) changes the visual quality.

The notebook walks through loading sample images, applying each anonymization step, and evaluating results both qualitatively (visual inspection) and quantitatively (pixel‐level distortion metrics).

