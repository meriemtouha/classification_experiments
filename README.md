# classification_experiments
Experiments with CNN, ResNet+CNN hybrids, and Grad-CAM heatmaps for image classification.
#  Classification Experiments
# Dataset

All experiments are trained and evaluated on the LC25000 Colon Histology Dataset, a publicly available collection of colon tissue images.  
📥 Download from Kaggle: [LC25000 Colon Histology Images](https://www.kaggle.com/datasets/andrewmvd/lung-and-colon-cancer-histopathological-images)

Images are resized to **224×224** before training.  

This repository contains experiments for colon tissue image classification using deep learning.  
Three approaches are implemented in PyTorch:

1. # Custom CNN  
   - A small convolutional neural network trained directly on the dataset.  
   - Includes weighted sampling to handle class imbalance.  

2. # Transfer Learning with ResNet18  
   - Pretrained ResNet18 backbone from torchvision.  
   - All layers frozen except the final fully-connected classifier.  
   - Trained on resized (224×224) colon tissue images.  

3. # Hybrid Model (ResNet + CNN) + Grad-CAM  
   - Combines a ResNet backbone with additional CNN layers.  
   - Improves feature extraction while adapting to dataset-specific patterns.  
   - Uses Grad-CAM heatmaps for model interpretability, highlighting regions that influence predictions.  




