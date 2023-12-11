# sparrow

# Human Joint Movement Prediction Using Capsule Networks

## Project Overview
This project focuses on developing a neural network model that predicts the orientations of human joints, represented by local unit quaternions, based on 2D coordinates and confidence values of the joints. A Capsule Network architecture was employed to effectively capture spatial hierarchies and relationships within the data.

## Model Architecture
The model processes input data consisting of 2D coordinates and confidence values for 23 human joints and predicts quaternions for 31 human joints. The architecture integrates a Capsule Network, built using TensorFlow's Keras API.

### Key Components
- **Input Layer**: Shape (23, 3). Accepts normalized input data.
- **Reshape Layer**: Transforms input to match convolutional layer requirements.
- **PrimaryCaps Layer**: Extracts primary features using small convolutional kernels.
- **CapsuleLayer**: Implements dynamic routing to understand part-whole relationships in the data.
- **Flatten and Dense Layers**: Flatten the CapsuleLayer output and predict the final quaternion values.

## Training and Validation
The model was compiled with the Adam optimizer (learning rate: 0.001) and mean squared error loss function, suitable for the regression nature of quaternion prediction. It achieved a high validation accuracy, indicating its effectiveness in generalizing to unseen data.

## Computational Complexity
The model's computational complexity, measured in FLOPs, is approximately 0.032 GigaFLOPs. This relatively low computational demand makes the model suitable for deployment in resource-constrained environments.

## CoreML Conversion
Conversion of the model to CoreML format was attempted for deployment on Apple devices. However, compatibility issues arose during the conversion process, particularly involving the conversion from TensorFlow to ONNX format. These challenges were documented, and alternative deployment strategies were considered.

## Challenges and Learnings
The project presented challenges in model conversion, offering insights into the complexities of working with advanced neural network architectures and different machine learning frameworks. It highlighted the importance of considering deployment constraints early in the model design process.


## Conclusion
The project successfully demonstrates the application of Capsule Networks in predicting human joint movements. While challenges in model conversion were encountered, the project provides a strong foundation for further development and research in this area.

---

This report provides a comprehensive overview of your project, its objectives, key findings, challenges, and potential areas for future work. Make sure to adjust any specific details to accurately reflect your project's implementation and results.
