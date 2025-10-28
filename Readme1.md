### **Terrain Classification Using CNN**

This project focuses on using a Convolutional Neural Network (CNN) to classify different types of terrain images, while investigating how various optimizers influence model performance. The dataset consists of images representing five terrain categories, with the model built and trained using Keras and TensorFlow.

### **Project Overview**
The main objective is to sort terrain images into one of five designated classes. The CNN architecture incorporates multiple convolutional, pooling, and dense layers to extract relevant features and predict the correct terrain type.

### **Model Architecture**
Across all model versions, the following design choices are consistent:
- **Input Layer:** Accepts 64x64 RGB images.
- **Convolutional Layers:** Three layers with ReLU activation, containing 32, 64, and 128 filters, respectively.
- **Pooling Layers:** MaxPooling layers follow each convolution to decrease spatial dimensionality.
- **Fully Connected Layers:** Two dense layers, each with 1024 units, followed by a final output layer with 5 units for classification.
- **Batch Normalization:** Incorporated after both convolutional and dense layers for more stable learning.
- **Dropout:** Applied between dense layers to help prevent overfitting.

### **Optimizers Evaluated**
Different optimization algorithms were explored:

**RMSprop (Terrain_V6)**  
- **Parameters:** Learning Rate = 0.001  
- **Results:**  
  - Training Accuracy: 0.7767  
  - Validation Accuracy: 0.8846  

![image](https://github.com/user-attachments/assets/bb63b0a7-e1d0-48a

**RMSprop (Terrain_V6-Copy 1)**  
- **Parameters:** Learning Rate = 0.001  
- **Results:**  
  - Training Accuracy: 0.7842  
  - Validation Accuracy: 0.8077  

![image](https://github.com/user-attachments/assets/da242312-28dc-49c

**ADAM (Terrain_V4-Copy 1)**  
- **Results:**  
  - Training Accuracy: 0.7643  
  - Validation Accuracy: 0.8269  

![image](https://github.com/user-attachments/assets/4a8741b3-4828-4cd

**SGD with Momentum (Terrain_V5)**  
- **Parameters:** Learning Rate = 0.01, Momentum = 0.9  
- **Results:**  
  - Training Accuracy: 0.7583  
  - Validation Accuracy: 0.8077  

![image](https://github.com/user-attachments/assets/58036ad5-b0f1-43a

**Adagrad (Terrain_V7)**  
- **Parameters:** Learning Rate = 0.01  
- **Results:**  
  - Training Accuracy: 0.7439  
  - Validation Accuracy: 0.7692  

![image](https://github.com/user-attachments/assets/79c9970f-85b9-4c32Findings and Key Observations**

**SGD with Momentum (Terrain_V5):**  
- *Observation:* Showed gradual but slower improvement in accuracy, and tended to plateau after a certain number of epochs. This suggests a need for optimized learning rate schedules.

**RMSprop (Terrain_V6):**  
- *Observation:* Delivered the best validation accuracy overall. RMSprop adapts the learning rate for each parameter, which is particularly valuable for complex, variable image data. Its fast convergence improved both training and validation metrics, though overfitting is a potential concern.

**Adagrad (Terrain_V7):**  
- *Observation:* Demonstrated moderate results, often converging rapidly due to its adaptive learning rate. While beneficial for sparse data, it struggled to improve further in this classification scenario.

### **Key Takeaways**

1. **Impact of Optimizer Selection:** The choice of optimizer has a strong effect on both how quickly the model learns and the final accuracy achieved. RMSprop provided the most favorable balance for this terrain classification dataset.
2. **Role of Batch Normalization:** Utilizing batch normalization helped stabilize and speed up training, especially in deeper network layers, by countering gradient issues.
3. **Dropout for Overfitting Control:** Adding 20% dropout between dense layers effectively minimized overfitting. Omitting dropout resulted in much higher training accuracy compared to validation accuracy.
4. **Learning Rate Scheduling:** Dynamically adjusting the learning rate, as done with SGD and RMSprop, led to better performance. Adagrad’s inbuilt adjustments were sufficient for basic convergence.

**Conclusion:**  
This study emphasizes the significance of matching optimizers to both the dataset and the problem’s demands. RMSprop proved to be the most effective for terrain classification tasks, whereas Adagrad was less suitable. Performance with SGD and Momentum could further benefit from advanced scheduling or extended training.