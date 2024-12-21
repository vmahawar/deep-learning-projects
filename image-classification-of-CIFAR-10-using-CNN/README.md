# CIFAR-10 Image Classification Using Convolutional Neural Networks (CNNs)

This project involves building and training a Convolutional Neural Network (CNN) to classify images in the CIFAR-10 dataset into 10 classes. The implementation includes data augmentation, hyperparameter tuning, and the use of advanced deep learning techniques to optimize performance.

---

## 🎯 Objective

- Develop a CNN model to classify images in the CIFAR-10 dataset with high accuracy.
- Understand the impact of hyperparameters like filter size, stride, and dropout on model performance.
- Apply data augmentation techniques to improve generalization and prevent overfitting.

---

## 📂 Dataset

### **CIFAR-10 Dataset**
- **Description**: The CIFAR-10 dataset consists of 60,000 32x32 color images in 10 classes, with 6,000 images per class. It is widely used for image classification tasks.
- **Classes**: Airplane, Automobile, Bird, Cat, Deer, Dog, Frog, Horse, Ship, Truck.
- **Dataset Source**: [CIFAR-10 Dataset](https://www.cs.toronto.edu/~kriz/cifar.html)
- **Preprocessing**:
  - Normalized pixel values to range [0, 1].
  - Data augmentation applied, including rotation, rescaling, zoom, and horizontal flipping.

---

## 🛠️ Tools and Libraries Used

- **TensorFlow & Keras**: For building, training, and evaluating the CNN model.
- **Pandas & NumPy**: For data manipulation and preprocessing.
- **Matplotlib & Seaborn**: For visualizing training metrics and results.

---

## 🌟 Model Architecture

The CNN model consists of the following layers:

1. **First Convolutional Block**:
   - Convolutional Layer: 32 filters, 3 × 3 kernel, stride 1, "same" padding, "He normal" initialization, ReLU activation.
   - Batch Normalization
   - Dropout (0.2)

2. **Second Convolutional Block**:
   - Convolutional Layer: 64 filters, 3 × 3 kernel, stride 1, "same" padding, "He normal" initialization, ReLU activation.
   - Batch Normalization
   - Max Pooling (2 × 2)

3. **Third Convolutional Block**:
   - Convolutional Layer: 128 filters, 5 × 5 kernel, stride 1, "same" padding, "He normal" initialization, ReLU activation.
   - Batch Normalization
   - Dropout (0.2)

4. **Fourth Convolutional Block**:
   - Convolutional Layer: 256 filters, 3 × 3 kernel, stride 1, "same" padding, "He normal" initialization, ReLU activation.
   - Batch Normalization
   - Max Pooling (2 × 2)

5. **Output Layer**:
   - Global Average Pooling
   - Dropout (0.2)
   - Dense Layer with Softmax activation (10 classes)

---

## 🚀 Training Details

- **Optimizer**: Adam with an initial learning rate of 0.01.
- **Learning Rate Scheduler**: ReduceLROnPlateau to reduce learning rate when validation accuracy plateaus (factor 0.5, patience 5, minimum learning rate 0.00001).
- **Loss Function**: Categorical Crossentropy.
- **Batch Size**: 32
- **Epochs**: 50
- **Validation Split**: 20% of the training data.
- **Data Augmentation**: 
  - Rotation (20 degrees)
  - Rescaling (0-1)
  - Zoom (range 0.1)
  - Horizontal flipping

---

## 🎉 Results

- **Baseline Model Test Accuracy**: ~80%-90%
- **Insights**:
  - Larger filter sizes (e.g., 9 × 9) and higher strides (e.g., 2) reduce accuracy due to loss of fine-grained spatial details.
  - Data augmentation improved model generalization and reduced overfitting.

---

## 📊 Evaluation Metrics

- Accuracy
- Precision, Recall, F1-Score (if applicable)
- Training and validation loss and accuracy trends.

---

## 📜 License

This project is licensed under the **MIT License**. You are free to use the code and data for educational and non-commercial purposes.

---

## 🌐 Connect with Me

Feel free to connect, collaborate, or provide feedback:

- **LinkedIn**: [Vijay Mahawar](https://www.linkedin.com/in/vijay-mahawar)
- **GitHub**: [vmahawar](https://github.com/vmahawar)
