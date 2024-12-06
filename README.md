# Hierarchical Fusion Meets Multi-Stream Models for Deepfake Detection
### Codebase is only adapted to WildRF version.

## Overview  
Our proposed model is a state-of-the-art deepfake detection architecture that integrates hierarchical feature fusion and multi-stream models. By combining Vision Transformers, ResNet, and specialized modules like Yolov8 and XceptionNet, it excels in detecting high-quality and realistic deepfakes generated by modern Generative AI techniques. The model emphasizes both spatial and semantic understanding while ensuring explainability through Grad-CAM visualizations.

## Key Features  
- **Hierarchical Feature Fusion**: Combines Vision Transformer (ViT) and ResNet50 outputs for enriched representations.  
- **Multi-Stream Architecture**: Incorporates facial features, context, and edge-aware details via Yolov8, Sobel filters, and XceptionNet.  
- **Explainability**: Employs Grad-CAM to produce class-discriminative heatmaps for output decisions.  
- **Calibration**: Uses Platt Scaling to refine output probabilities, reducing model overconfidence.  
- **Ensemble Decision Making**: Aggregates multi-stream predictions for robust and accurate results.  

## Architecture  
The model architecture comprises two main modules:  
1. **Module One**:  
   - Hierarchical fusion of ViT and ResNet50 for feature extraction.  
   - Calibration using Platt Scaling to ensure well-calibrated outputs.  
2. **Module Two**:  
   - Multi-stream feature extraction using Yolov8, Sobel filters, and XceptionNet.  
   - Grad-CAM for visualization and explainability.
  
   <img src="https://github.com/user-attachments/assets/cabaa9ae-4f42-4c98-a575-d3294011ddd5" alt="Ensemble" width="500" />


## Results  

- **Calibration**: Achieved an 8% decrease in Expected Calibration Error (ECE) on the training set and a 13% decrease on the validation set.  
- **Explainability**: Grad-CAM heatmaps demonstrate accurate localization of manipulated regions.  
- **Ensemble Performance**: Outperforms baseline models in detecting deepfakes while maintaining computational efficiency.

  <img src="https://github.com/user-attachments/assets/6d27282f-bc48-42b1-bb19-ebfd1ae14b29" alt="Comparison" width="500" />


## Installation  
1. Clone the repository:  
   ```bash
   git clone https://github.com/anantmehta33/CSCE_689_Hierarchical_Feature_Fusion.git
   cd CSCE_689_Hierarchical_Feature_Fusion
