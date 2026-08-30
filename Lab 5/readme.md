# Deep Learning Lab 5

## Comprehensive Study of CNN Training and Optimization

This lab studies different techniques used to improve and evaluate CNN-based image classification models using **PyTorch** and **MobileNetV2**.

The experiments are performed on the **Oxford-IIIT Pet Dataset**, which contains 37 pet-breed classes.

## Experiments

The notebook contains the following tasks:

1. **Weight Initialization**

   * Zero
   * Random
   * Xavier
   * He initialization

2. **Regularization**

   * No regularization
   * L2 regularization
   * Dropout

3. **Batch Normalization**

   * Comparison of models with and without Batch Normalization
   * Numerical Batch Normalization example

4. **Optimization Algorithms**

   * SGD
   * Momentum
   * RMSProp
   * Adam

5. **Hyperparameter Tuning**

   * Learning rate
   * Batch size
   * Dropout rate

6. **Transfer Learning**

   * Feature extraction using pretrained MobileNetV2

7. **Fine-Tuning**

   * Partial unfreezing of the pretrained MobileNetV2 model

8. **5-Fold Cross-Validation**

   * Comparison of four hyperparameter configurations

9. **Final Model Evaluation**

   * Accuracy
   * Precision
   * Recall
   * F1-score
   * Confusion matrix
   * Training time
   * Number of parameters

## Dataset

The experiments use the **Oxford-IIIT Pet Dataset**.

Images are resized to `224 × 224` and normalized using ImageNet normalization values.

For faster execution and reduced memory usage, the notebook uses a smaller subset of the dataset and one training epoch for the experiments.

## Model

The main CNN architecture used is **MobileNetV2**.

For transfer learning experiments, ImageNet-pretrained MobileNetV2 is used. The feature extractor is frozen during feature extraction, while selected layers are unfrozen during fine-tuning.

## Results

The best cross-validation configuration was **C2**:

* Learning rate: `1e-4`
* Dropout: `0.25`
* Mean CV Accuracy: `13.00%`
* Standard Deviation: `9.27%`

The final model achieved:

* Test Accuracy: `4.36%`
* Precision: `0.0220`
* Recall: `0.0435`
* F1 Score: `0.0182`
* Training Time: `5.32 seconds`
* Total Parameters: `2,271,269`
* Trainable Parameters: `47,397`

The relatively low accuracy is expected because the experiments use a small dataset subset and only one training epoch to keep the notebook fast and memory-efficient.


