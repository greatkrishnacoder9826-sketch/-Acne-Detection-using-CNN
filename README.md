🧴 Acne Detection using CNN

A Deep Learning project that detects whether a face has Acne or No Acne using a Convolutional Neural Network (CNN). The model is trained on facial image datasets and can perform real-time acne detection through a webcam using OpenCV.

📌 Project Overview

This project uses a custom CNN architecture built with TensorFlow/Keras to classify facial images into:

✅ Acne
✅ Non-Acne

After training, the model can be used for:

Image-based acne detection
Real-time webcam prediction
Facial detection using Haar Cascade Classifier
🚀 Features
Data Augmentation using ImageDataGenerator
Custom CNN Architecture
Model Checkpointing
Accuracy & Loss Visualization
Real-Time Webcam Detection
Face Detection with OpenCV Haar Cascade
Model Saving and Loading
🛠️ Technologies Used
Python
TensorFlow / Keras
OpenCV
NumPy
Matplotlib
📂 Project Structure
Acne-Detection-CNN/
│
├── train/
│   ├── Acne/
│   └── Non_Acne/
│
├── validation/
│   ├── Acne/
│   └── Non_Acne/
│
├── model/
│   └── acne_model.h5
│
├── models/
│   └── acne_model_last.h5
│
├── faces/
│   ├── with_acne/
│   └── without_acne/
│
├── acne_detection.ipynb
├── haarcascade_frontalface_default.xml
└── README.md
⚙️ Installation
Clone Repository
git clone https://github.com/yourusername/acne-detection-cnn.git
cd acne-detection-cnn
Install Dependencies
pip install tensorflow keras opencv-python matplotlib numpy
📊 Data Preprocessing

The project uses Image Augmentation to improve model generalization:

ImageDataGenerator(
    rescale=1./255,
    rotation_range=40,
    width_shift_range=0.2,
    height_shift_range=0.2,
    shear_range=0.2,
    zoom_range=0.2,
    horizontal_flip=True
)
🧠 Model Architecture

The CNN consists of:

Conv2D Layer (32 Filters)
MaxPooling Layer
Conv2D Layer (64 Filters)
MaxPooling Layer
Conv2D Layer (128 Filters)
Dense Layers
Softmax Output Layer

Loss Function:

categorical_crossentropy

Optimizer:

Adam (Learning Rate = 0.001)
🏋️ Training
history = cnn_model.fit(
    training_data,
    epochs=50,
    validation_data=valid_data
)

Best model is automatically saved using:

ModelCheckpoint()
📈 Training Results

The notebook visualizes:

Training Accuracy
Validation Accuracy
Training Loss
Validation Loss

using Matplotlib graphs.

🎥 Real-Time Acne Detection

After training, the model can be loaded and used with a webcam:

model = load_model('model/acne_model.h5')

OpenCV detects faces and the CNN predicts whether acne is present.

▶️ Usage
Train Model
jupyter notebook acne_detection.ipynb

Run all cells to train the model.

Start Webcam Detection

Run the webcam prediction section of the notebook.

📸 Sample Workflow
Load Dataset
Apply Data Augmentation
Train CNN
Save Best Model
Detect Face via Webcam
Predict Acne / Non-Acne
Display Result on Screen
🔮 Future Improvements
Transfer Learning (MobileNetV2, ResNet50)
Severity Level Prediction
Skin Disease Multi-Class Classification
Web Application Deployment
Mobile Application Integration
👨‍💻 Author

Krishna Great

Deep Learning Enthusiast
Data Science & AI Learner
Building Computer Vision Projects with TensorFlow and OpenCV
⭐ Support

If you found this project useful:

Star the repository ⭐
Fork the project 🍴
Share with others 🚀
License

This project is open-source and available under the MIT License.
