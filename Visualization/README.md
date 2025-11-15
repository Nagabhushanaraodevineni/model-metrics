# Precision-Recall Twin Cylinders

An innovative interactive visualization tool for understanding confusion matrices, precision, recall, and binary classification metrics through an intuitive dual-cylinder interface.

![Precision-Recall Twin Cylinders Preview](screenshot.png)
*Replace with actual screenshot*

## 🎯 What Is This?

The **Precision-Recall Twin Cylinders** is a novel educational visualization that helps students, data scientists, and ML practitioners understand the relationship between:
- Actual vs. Predicted classifications
- True Positives, False Positives, True Negatives, False Negatives
- Precision, Recall, Accuracy, F1-Score, and other metrics

### Why "Twin Cylinders"?

Traditional confusion matrices show numbers in a table, but it's hard to visualize:
- How predictions relate to actual truth
- What happens when you adjust classification thresholds
- The physical "volume" of each classification category

This tool uses **two vertical cylinders**:
1. **Truth Cylinder** - Shows the actual distribution (green = positive, red = negative)
2. **Prediction Cylinder** - Shows how your model classifies the data with adjustable sliders

## 🚀 How to Use

### Basic Operation

1. **Set Your Dataset**
   - **Total Samples**: Enter the total number of samples (1-100,000)
   - **Actual Positive %**: Set what percentage are actually positive (0-100%)

2. **Observe the Truth Cylinder**
   - Green section = Actual Positive cases
   - Red section = Actual Negative cases
   - Yellow line = Boundary between positive and negative

3. **Adjust Prediction Sliders**
   - **Bottom Slider** (Pred Pos): Drag to set how many samples your model predicts as positive
   - **Top Slider** (Pred Neg): Drag to set where predictions change from positive to negative
   - Watch the colors change to show TP, FP, FN, TN

4. **Read the Metrics**
   - Confusion Matrix updates in real-time
   - Six key metrics calculated automatically
   - Formulas provided at the bottom

### Understanding the Colors

| Color | Meaning | Location |
|-------|---------|----------|
| 🟢 Bright Green | **True Positive (TP)** | Predicted positive AND actually positive |
| 🟩 Dark Green | **False Negative (FN)** | Predicted negative BUT actually positive |
| 🩷 Pink | **False Positive (FP)** | Predicted positive BUT actually negative |
| 🔴 Red | **True Negative (TN)** | Predicted negative AND actually negative |
| 🟨 Yellow Line | Boundary | Separates actual positives from negatives |

### Reading the Prediction Cylinder

The prediction cylinder is divided into 4 sections from bottom to top:
