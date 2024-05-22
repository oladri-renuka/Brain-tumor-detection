# Brain Tumor Detection using ConvNeXt Model

## Overview
This project focuses on improving brain tumor detection accuracy and efficiency by leveraging advanced deep learning techniques with MRI images. The ConvNeXt model, pre-trained on various image datasets, was implemented and fine-tuned for the specific task. By preprocessing the data, augmenting, normalizing, and scaling the images, the model's performance was enhanced. A unique classifier head tailored to the task was integrated into the model, and a custom training loop with Cross Entropy Loss was utilized to optimize it over multiple epochs.

## Methodology
### 1. Data Preprocessing
The MRI images underwent several preprocessing steps:
- Resizing: Images were resized to (224, 224) pixels, the input size expected by the ConvNeXt model.
- Rotation: Random rotation (-25 to 20 degrees) during training was applied to introduce variability.
- Normalization: Conversion to tensors and normalization using mean and standard deviation values specific to the ImageNet dataset.

### 2. Model Architecture
The ConvNeXt model, a deep learning architecture designed for image processing tasks, was employed. It consists of:
- ConvNeXt Embeddings Block: Initial convolutional layer transforming the input tensor.
- ConvNeXt Encoder Block: Four stages progressively down-sampling the tensor.
- Sequential Classifier Block: Custom classifier for tumor classification.

### 3. Model Training and Evaluation
The model was trained with carefully chosen hyperparameters:
- Learning rate: 1e-4
- Epochs: 15
- Batch size: 32
- Activation Function: ReLU
- Optimizer: Adam

The model's performance was evaluated using a validation set, and the best-performing model was selected based on validation loss. Testing was conducted on a separate test dataset, and accuracy was computed. A classification report provided insights into the model's performance across different tumor types.

## Results
The ConvNeXt model demonstrated impressive accuracy in classifying brain tumors, achieving an overall accuracy score of 95.19%. High precision and recall balance for all tumor types were observed, indicating the model's robustness. Visualization of loss and accuracy over epochs showed consistent improvement and convergence, validating the effectiveness of the model.

## Conclusion
This study highlights the potential of deep learning techniques, specifically the ConvNeXt architecture, in revolutionizing medical diagnostics, particularly in brain tumor detection from MRI data. The findings pave the way for further research in this area and underscore the importance of advanced neural network architectures in healthcare image processing.

## License
This project is licensed under the MIT License.
