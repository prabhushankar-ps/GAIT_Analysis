
# Biometrics Using Gait Analysis

This project focuses on human identification through gait patterns using a non-invasive biometric method. It proposes a novel algorithm called **Structural Silhouette and Feature Extraction (SSFE)** for efficient gait analysis and recognition.

## Table of Contents
- [Abstract](#abstract)
- [Introduction](#introduction)
- [Methodology](#methodology)
  - [Database Creation](#database-creation)
  - [Silhouette Extraction](#silhouette-extraction)
  - [Feature Extraction](#feature-extraction)
  - [Neural Network Training](#neural-network-training)
- [Results and Discussions](#results-and-discussions)
- [Conclusion](#conclusion)
- [Future Work](#future-work)
- [References](#references)

---

## Abstract
This project explores human identification from a distance using walking patterns. Key features such as body height, leg height, step width, and cadence are used. A new algorithm, **SSFE**, improves silhouette extraction and feature analysis. A feedforward backpropagation neural network is employed for better recognition efficiency.

---

## Introduction
Biometric technology analyzes human characteristics such as fingerprints, iris patterns, and voice for identification and verification. Gait, or the walking pattern of a person, is a non-invasive and effective biometric feature. Unlike other methods, gait-based recognition can identify individuals from a distance and under low-resolution conditions. 

The key focus of this project is to leverage gait patterns for human identification using an enhanced silhouette extraction and feature analysis method. The study includes:
- Proposing the **SSFE algorithm** for efficient silhouette extraction.
- Training a neural network to handle variations in gait patterns.
- Evaluating the model's performance on a custom database.

---

## Methodology

### Database Creation
- **Input Data**: A total of 105 videos (35 per subject) were recorded using a 25-megapixel camera with a frame rate of 25 fps. Each video is approximately 5 seconds long.
- **Gait Variations**: Videos capture diverse walking styles, including slow, fast, broad, and tapered steps.
- **Preprocessing**: Each video was segmented into 125 frames. Variations in arm swing, step width, and walking speed were intentionally included for robust training.

### Silhouette Extraction
- **Process**:
  - Resize frames for uniformity.
  - Apply Median Filtering to remove noise.
  - Enhance frames using Histogram Equalization.
  - Convert frames from RGB to grayscale and then to binary images.
  - Perform Morphological Operations to fine-tune silhouettes.
- **SSFE Advantage**: Compared to traditional frame difference methods, SSFE achieves better silhouette accuracy as validated by metrics such as mean, standard deviation, and entropy.

### Feature Extraction
Key gait parameters for biometric recognition:
- **Body Height (BH)**: 60% of the individual’s total height.
- **Body Width (BW)**: Measured arm swing width.
- **Leg Width (LW)**: Extent of leg swing during walking.
- **Leg Height (LH)**: 40% of the individual’s total height.
- **Cadence**: Walking speed, calculated as steps per second.

### Neural Network Training
- **Architecture**: Feedforward backpropagation network with 14 hidden layers.
- **Input**: Mean features extracted from silhouettes.
- **Training**: Adjusts weights iteratively to minimize error. Variations in gait due to environmental changes are normalized during training.
- **Data Split**: 75 videos were used for training, and 30 were reserved for testing.

---

## Results and Discussions
The SSFE algorithm demonstrated superior performance over traditional methods:
- **Silhouette Extraction**:
  - Frame Difference Method: 37.03% accuracy.
  - SSFE Method: 80.00% accuracy.
- **Neural Network Performance**:
  - Without Neural Network: 55.55% accuracy.
  - With Neural Network: 80.00% accuracy.
- **Visual Outputs**: Improved silhouette clarity across all tested subjects.

---

## Conclusion
The proposed SSFE model, combined with a neural network, achieves high accuracy in gait-based biometric recognition. This approach effectively handles variations in walking styles and environmental conditions, making it a promising solution for real-world applications.

---

## Future Work
- **Dynamic Environments**: Develop models for non-static cameras where both subject and camera are in motion.
- **Incomplete Gait Cycles**: Enhance the algorithm to handle incomplete gait sequences.
- **Higher Resolution Inputs**: Explore advanced preprocessing techniques for high-resolution images.

---

## References
1. Z. Liu and S. Sarkar, "Improved gait recognition by gait dynamics normalization," IEEE Transactions on Pattern Analysis and Machine Intelligence, vol. 28, no. 6, pp. 863-876, June 2006.
2. S. Benbakreti and M. Benyettou, "Gait recognition based on leg motion and contour of silhouette," International Conference on Information Technology and e-Services, 2012.
3. L. Wang et al., "Silhouette analysis-based gait recognition for human identification," IEEE Transactions on Pattern Analysis and Machine Intelligence, 2003.
4. W. Kusakunniran et al., "Automatic Gait Recognition Using Weighted Binary Pattern on Video," Sixth IEEE International Conference on Advanced Video and Signal Based Surveillance, 2009.
5. M. S. Nixon and J. N. Carter, "Advances in automatic gait recognition," Sixth IEEE International Conference on Automatic Face and Gesture Recognition, 2004.
