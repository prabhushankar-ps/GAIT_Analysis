
# Biometrics Using Gait Analysis

This project focuses on human identification through gait patterns using a non-invasive biometric method. It proposes a novel algorithm called **Structural Silhouette and Feature Extraction (SSFE)** for efficient gait analysis and recognition.

## Table of Contents
- [Abstract](#abstract)
- [Methodology](#methodology)
  - [Database Creation](#database-creation)
  - [Silhouette Extraction](#silhouette-extraction)
  - [Feature Extraction](#feature-extraction)
  - [Neural Network Training](#neural-network-training)
- [Results and Discussions](#results-and-discussions)
- [Conclusion](#conclusion)
- [References](#references)

---

## Abstract
This project explores human identification from a distance using walking patterns. Key features such as body height, leg height, step width, and cadence are used. A new algorithm, **SSFE**, improves silhouette extraction and feature analysis. A feedforward backpropagation neural network is employed for better recognition efficiency.

---

## Methodology

### Database Creation
- **Input Data**: 105 videos (35 per subject) recorded using a 25-megapixel camera at 25 frames per second.
- **Gait Variations**: Captures different walking styles like slow steps, fast steps, broad steps, etc.
- **Training and Testing**: 75 videos for training and 30 for testing.

### Silhouette Extraction
- **Process**: Frames are resized, filtered, and converted to binary images using SSFE for silhouette extraction.
- **Validation**: Metrics such as mean, standard deviation, and entropy validate SSFE's superiority over traditional methods.

### Feature Extraction
Key gait parameters for biometric recognition:
- **Body Height (BH)**: 60% of total height.
- **Body Width (BW)**: Arm swing width.
- **Leg Width (LW)**: Leg swing width.
- **Leg Height (LH)**: 40% of total height.
- **Cadence**: Walking speed.

### Neural Network Training
- **Architecture**: Feedforward backpropagation network with 14 hidden layers.
- **Input**: Mean features from extracted silhouettes.
- **Goal**: Minimize error and adapt to variations in gait patterns.

---

## Results and Discussions
The proposed SSFE method achieves 80% recognition accuracy, significantly outperforming the traditional frame difference method (37%). The neural network enhances the system's robustness against variations in gait patterns.

---

## Conclusion
The SSFE model combined with a neural network demonstrates high efficiency in gait-based biometric recognition. Future developments could focus on non-static cameras and incomplete gait cycle analysis.

---

## References
- Z. Liu and S. Sarkar, "Improved gait recognition by gait dynamics normalization," IEEE Transactions on Pattern Analysis and Machine Intelligence, vol. 28, no. 6, pp. 863-876, June 2006.
- S. Benbakreti and M. Benyettou, "Gait recognition based on leg motion and contour of silhouette," International Conference on Information Technology and e-Services, 2012.
- L. Wang et al., "Silhouette analysis-based gait recognition for human identification," IEEE Transactions on Pattern Analysis and Machine Intelligence, 2003.
