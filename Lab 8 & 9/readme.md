# Effect of Attention Type and Position in Pretrained ResNet50

## Overview

This project studies the effect of different attention mechanisms and their placement in a pretrained ResNet50 model for image classification. The experiments use the **TF Flowers dataset**, which contains images belonging to five flower classes.

The main objective is to compare how different attention mechanisms improve feature extraction and classification performance when applied at different stages of a deep learning model.

## Objectives

- Understand and implement different attention mechanisms.
- Study the effect of placing attention modules at different stages of ResNet50.
- Compare model accuracy, loss, training time, and computational complexity.
- Visualize attention maps and understand which image regions influence predictions.
- Evaluate model performance using confusion matrices and class-wise metrics.

## Technologies Used

- Python
- TensorFlow and Keras
- TensorFlow Datasets
- NumPy and Pandas
- Matplotlib
- Scikit-learn
- Google Colab with GPU support

## Dataset

The project uses the **TF Flowers dataset**, consisting of five flower categories.

The dataset is divided into three subsets:

| Dataset | Percentage |
|---|---:|
| Training | 70% |
| Validation | 15% |
| Testing | 15% |

A fixed stratified split is used across experiments to ensure a fair comparison between models. Image preprocessing and data augmentation are applied during training.

## Methodology

### 1. Pretrained ResNet50

ResNet50 is used as the backbone for extracting image features. The model is initially trained with the backbone frozen, followed by fine-tuning of the final convolutional stage.

### 2. Attention Mechanisms

The project implements and compares several attention mechanisms:

- **Channel Attention (SE):** Focuses on important feature channels.
- **Spatial Attention:** Highlights important spatial regions in an image.
- **Channel-to-Spatial Attention:** Applies channel attention followed by spatial attention.
- **Self-Attention:** Models relationships between different spatial locations.
- **ECA Attention:** Captures channel dependencies efficiently.
- **CBAM:** Combines channel and spatial attention.
- **Coordinate Attention:** Captures spatial information along height and width.

### 3. Experimental Comparison

Experiments investigate the effect of attention type, insertion position, multiple attention locations, attention ordering, and spatial kernel size. A baseline ResNet50 model is also evaluated for comparison.

### 4. Evaluation and Visualization

The models are evaluated using accuracy, loss, training time, parameter counts, and other classification metrics. The notebook also generates confusion matrices, training curves, attention heatmaps, feature map comparisons, and Grad-CAM visualizations.

## How to Run

1. Open the notebook in Google Colab.
2. Select **Runtime → Change runtime type → T4 GPU**.
3. Run the setup cells to install the required dependencies.
4. Execute the notebook cells in order.
5. Review the generated tables, graphs, confusion matrices, and attention visualizations.

## Expected Outcomes

The experiments help identify how different attention mechanisms affect image classification performance and whether their placement within ResNet50 influences the results. The visualizations also provide insights into the image regions and feature channels used by the model.

Actual performance comparisons should be based on the results obtained after running the experiments.

## Conclusion

This project provides a comparative study of attention mechanisms in deep learning using a pretrained ResNet50 architecture. It combines quantitative evaluation with visual analysis to better understand the role of attention in image classification.

