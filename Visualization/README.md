# Precision-Recall Twin Cylinders

An innovative interactive visualization tool for understanding confusion matrices, precision, recall, and binary classification metrics through an intuitive dual-cylinder interface.

<img width="867" height="883" alt="image" src="https://github.com/user-attachments/assets/679c6264-4439-455f-b1f4-a0bf3041b601" />


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
```
┌─────────────┐
│     TN      │ ← Red (correctly predicted negative)
│   (Red)     │
├─────────────┤ ← Top Slider (Pred Neg boundary)
│     FP      │ ← Pink (incorrectly predicted positive)
│   (Pink)    │
├─────────────┤ ← Yellow Line (actual truth boundary)
│     FN      │ ← Dark Green (incorrectly predicted negative)
│ (Dark Green)│
├─────────────┤ ← Bottom Slider (Pred Pos boundary)
│     TP      │ ← Bright Green (correctly predicted positive)
│   (Green)   │
└─────────────┘
```

## 📚 Example Scenarios

### Scenario 1: Perfect Classifier
- **Setup**: 1000 samples, 50% positive
- **Action**: Align both sliders exactly with the yellow line
- **Result**: TP=500, FP=0, FN=0, TN=500 → 100% accuracy! 🎯

### Scenario 2: Conservative Classifier (High Precision)
- **Setup**: 1000 samples, 30% positive
- **Action**: Move bottom slider to 20%, top slider to 25%
- **Result**: Few false positives, but many false negatives
- **Learning**: High precision, low recall

### Scenario 3: Aggressive Classifier (High Recall)
- **Setup**: 1000 samples, 40% positive  
- **Action**: Move bottom slider to 35%, top slider to 80%
- **Result**: Catches most positives, but many false alarms
- **Learning**: High recall, lower precision

### Scenario 4: Imbalanced Dataset
- **Setup**: 1000 samples, 5% positive (rare disease)
- **Action**: Try different slider positions
- **Result**: See why accuracy alone is misleading!

## 📊 Metrics Explained

### Recall (TPR - True Positive Rate)
**Formula**: `TP / (TP + FN)`  
**Meaning**: Of all actual positives, what % did we catch?  
**Example**: Medical diagnosis - "Did we find all the sick patients?"

### Precision  
**Formula**: `TP / (TP + FP)`  
**Meaning**: Of all positive predictions, what % were correct?  
**Example**: Spam filter - "Of emails marked spam, how many were actually spam?"

### Accuracy
**Formula**: `(TP + TN) / Total`  
**Meaning**: Overall, what % of predictions were correct?  
**Warning**: Can be misleading with imbalanced datasets!

### F1-Score
**Formula**: `2 × (Precision × Recall) / (Precision + Recall)`  
**Meaning**: Harmonic mean of precision and recall  
**Use**: Single metric balancing both concerns

### FPR (False Positive Rate)
**Formula**: `FP / (FP + TN)`  
**Meaning**: Of all actual negatives, what % did we wrongly flag?  
**Example**: False alarms in a security system

### ROC Metric
**Formula**: `TPR / FPR`  
**Meaning**: Ratio showing classifier quality  
**Interpretation**: Higher is better (want high TPR, low FPR)

## 🎓 Educational Use Cases

### For Students
- Understand confusion matrices visually
- See how changing thresholds affects metrics
- Explore precision-recall tradeoffs
- Learn why accuracy can be misleading

### For Teachers
- Interactive classroom demonstrations
- Assignment: "Find settings that maximize F1-score"
- Discuss real-world tradeoffs (medical vs. marketing)
- Compare conservative vs. aggressive classifiers

### For Data Scientists
- Quickly visualize threshold effects
- Explain metrics to non-technical stakeholders
- Demonstrate imbalanced dataset challenges
- Teaching tool for junior team members

## 💡 Tips & Tricks

1. **Start with balanced data** (50% positive) to learn the basics
2. **Try extreme imbalances** (5% or 95%) to see metric behavior
3. **Challenge yourself**: Can you get 100% accuracy with 70% positive?
4. **Explore tradeoffs**: Move sliders to see precision vs. recall
5. **Use large sample sizes** (10,000+) for smoother metric calculations

## 🔧 Technical Details

- **Built with**: Pure HTML, CSS, and JavaScript (no dependencies!)
- **Browser support**: All modern browsers (Chrome, Firefox, Safari, Edge)
- **Mobile friendly**: Touch-enabled slider controls
- **Responsive design**: Works on desktop, tablet, and mobile

## 📄 License

MIT License - Copyright (c) 2025 [Your Name]

See [LICENSE](LICENSE) file for details.

## 🙋 FAQ

**Q: Can I use this in my course/presentation?**  
A: Yes! Just credit "Precision-Recall Twin Cylinders by [Your Name]"

**Q: Why can't I move the bottom slider above the yellow line?**  
A: The bottom slider represents predicted positives, which can't exceed actual positives in the green zone. The top slider handles the upper portion.

**Q: What's the yellow line for?**  
A: It shows the true boundary between actual positive and negative cases. It helps you see how your predictions align with reality.

**Q: Can I modify the code?**  
A: Absolutely! It's open source. Fork it, improve it, and share your changes!

**Q: Is this scientifically accurate?**  
A: Yes! All metrics follow standard machine learning definitions and formulas.

## 🌟 Contributing

Found a bug? Have a suggestion? Want to add features?

1. Open an issue on GitHub
2. Submit a pull request
3. Share your use cases!

## 📞 Contact

- **Creator**: Nagabhushana Rao  Devineni
- **Email**: nagabhushana.devineni@gmail.com
- **GitHub**: github.com/Nagabhushanaraodevineni
- **LinkedIn**: https://www.linkedin.com/in/nagabhushana-rao-devineni-b5a40010/)](https://www.linkedin.com/in/nagabhushana-rao-devineni-b5a40010/

## 🎉 Acknowledgments

Inspired by the need to make machine learning metrics more intuitive and accessible to learners at all levels.

---

**Star ⭐ this repository if you found it helpful!**

Made with ❤️ for the data science education community
