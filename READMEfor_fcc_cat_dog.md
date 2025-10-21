🐱🐶 Cat vs Dog Image Classifier using CNN
🎓 FreeCodeCamp Machine Learning Challenge

Goal: Build a Convolutional Neural Network (CNN) using TensorFlow/Keras that classifies images of cats and dogs with at least 63% accuracy.
Final Result: ✅ Achieved 72% validation accuracy

🧠 Project Overview

This project implements a binary image classification model trained to distinguish between cats and dogs.
The task demonstrates key deep learning workflows such as:

Image preprocessing and data augmentation

Convolutional neural network (CNN) design

Model training, evaluation, and visualization

Dataset used: Microsoft Cats vs Dogs (https://chatgpt.com/c/68f7fdfe-3d38-832e-8b33-6e27fceaea1b#:~:text=%F0%9F%A7%A0%20Project%20Overview,Dogs%20(Filtered%20Subset))
⚙️ Technologies Used

```
Python 3.10+

TensorFlow / Keras

NumPy & Matplotlib

Google Colab / Jupyter Notebook
```

🧩 Model Architecture

```
model = Sequential([
    Conv2D(32, (3,3), activation='relu', input_shape=(150, 150, 3)),
    BatchNormalization(),
    MaxPooling2D(2,2),

    Conv2D(64, (3,3), activation='relu'),
    BatchNormalization(),
    MaxPooling2D(2,2),

    Conv2D(128, (3,3), activation='relu'),
    BatchNormalization(),
    MaxPooling2D(2,2),

    Conv2D(256, (3,3), activation='relu'),
    BatchNormalization(),
    MaxPooling2D(2,2),

    Flatten(),
    Dense(512, activation='relu'),
    Dropout(0.5),
    Dense(1, activation='sigmoid')
])

```
Optimizer: Adam(learning_rate=0.0001)
Loss: Binary Crossentropy
Metrics: Accuracy
Epochs: 25

📈 Model Performance
Metric	Value
Training Accuracy	90%+
Validation Accuracy	72% ✅
Loss	Decreasing steadily
Epochs	25

Visualizing performance:
The final model is a deep CNN with Batch Normalization and Dropout for regularization.

🧪 Key Steps

Preprocessing:

Rescaled pixel values to [0,1]

Augmented images (rotation, zoom, shift, flip)

Model Building:

4 Convolutional layers + BatchNormalization + MaxPooling

Dense layer (512 units, ReLU) + Dropout(0.5)

Training:

25 epochs with validation tracking

Evaluation:

Tested on 50 unseen images

Achieved 72% overall accuracy

🚀 Results & Insights

CNN successfully differentiates cats and dogs with solid accuracy.

Data augmentation helped generalize to new images.

Batch normalization stabilized and accelerated learning.

Increasing epochs and deepening the network improved accuracy from 52% → 72%.

💡 Future Improvements

Apply transfer learning (e.g., MobileNetV2, VGG16) for >90% accuracy.

Fine-tune with learning rate scheduling.

Add Grad-CAM visualization to explain model predictions.

Convert to a web app using Streamlit or Flask.

📂 Repository

📘 Notebook: fcc_cat_dog.ipynb

👤 Author

Solomon Adegoke
💼 Machine Learning & AI Engineer
🔗 LinkedIn Profile
 ([My linkedin profile](https://www.linkedin.com/in/solomon-eniola-adegoke/))
