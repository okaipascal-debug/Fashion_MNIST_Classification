# Fashion-MNIST CNN Classifier

## Project Overview
This project implements a 6-layer Convolutional Neural Network (CNN) to classify fashion images from the Fashion-MNIST dataset. The solution is developed as part of a machine learning researcher assignment at Microsoft AI for targeted marketing using profile images.

## Dataset
- **Fashion-MNIST**: 70,000 grayscale images (60,000 training, 10,000 test)
- **Image size**: 28×28 pixels
- **Classes**: 10 fashion categories
- **Purpose**: Drop-in replacement for MNIST with more realistic images

## Model Architecture
The CNN consists of 6 layers:
1. **Conv2D** (32 filters, 3×3 kernel, ReLU activation)
2. **MaxPooling2D** (2×2 pool size)
3. **Conv2D** (64 filters, 3×3 kernel, ReLU activation)
4. **MaxPooling2D** (2×2 pool size)
5. **Dense** (128 units, ReLU activation) + Dropout (0.5)
6. **Dense** (10 units, Softmax activation)

## Requirements

### Python Version
```bash
Python 3.8+
Required Libraries
bash
tensorflow>=2.8.0
numpy>=1.21.0
matplotlib>=3.5.0
Installation
bash
pip install tensorflow numpy matplotlib
Usage
Python Implementation
Run the complete solution:

bash
python fashion_mnist_cnn.py
The script will:

Load and preprocess the dataset

Build and train the CNN model

Evaluate performance on test set

Make predictions on sample images

Save the trained model

R Implementation
Ensure R and required packages are installed:

r
install.packages(c("keras", "tensorflow", "ggplot2"))
Run the R script in RStudio or R console

File Structure
text
fashion-mnist-classifier/
│
├── fashion_mnist_cnn.py          # Main Python implementation
├── fashion_mnist_cnn.R           # R implementation
├── fashion_mnist_cnn.h5          # Saved Python model
├── fashion_mnist_cnn_r/          # Saved R model directory
├── training_history.png          # Training plots
├── predictions.png               # Prediction visualizations
└── README.md                     # This file
Expected Output
Training progress: Epoch-by-epoch accuracy and loss

Final test accuracy: Typically 90-92%

Sample predictions: 2 random test images with true/predicted labels

Visualizations: Training history and prediction results

Key Features
Data Preprocessing: Normalization, reshaping, one-hot encoding

Model Building: 6-layer CNN with best practices

Training: With validation monitoring and early stopping

Evaluation: Comprehensive performance metrics

Visualization: Training progress and predictions

Model Saving: For future deployment

Technical Details
Why This Architecture Works
Convolutional Layers: Extract spatial features from images

Pooling Layers: Reduce dimensionality and prevent overfitting

Dropout: Regularization to improve generalization

Softmax Output: Multi-class probability distribution

Hyperparameters
Optimizer: Adam (adaptive learning rate)

Loss Function: Categorical Crossentropy

Batch Size: 128 (balance of speed and stability)

Epochs: 10 (sufficient for convergence)

Adaptation for User Profile Classification
This model can be adapted for user profile image classification by:

Replacing Fashion-MNIST with profile image dataset

Adjusting input shape for different image dimensions

Modifying output layer for different number of user categories

Retraining with new data while leveraging transfer learning

License
MIT License - Same as Fashion-MNIST dataset

Author
Pascal Eliezer Okai
Junior Machine Learning Researcher
Microsoft AI

