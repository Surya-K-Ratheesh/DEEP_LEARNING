# MNIST Digit Classification with VGGnet-19
Overview

This experiment implements digit classification using a pre-trained VGGnet-19 model on the MNIST dataset. The project demonstrates transfer learning by adapting a network originally trained on ImageNet to recognize handwritten digits.
Implementation Details
Data Preprocessing

    MNIST dataset (28×28 grayscale images) resized to 32×32

    Grayscale images converted to RGB format (3 channels)

    Pixel values normalized to [0, 1] range

    Labels converted to categorical one-hot encoding

Model Architecture

    Base model: VGG-19 (pre-trained on ImageNet, frozen weights)

    Custom classification head:

        Global Average Pooling layer

        Dense layer (256 units, ReLU activation)

        Dropout layer (0.5 rate)

        Output layer (10 units, softmax activation)

Training Configuration

    Optimizer: Adam

    Loss function: Categorical crossentropy

    Batch size: 128

    Epochs: 10

    Validation split: 20%

Results

The model achieves competitive performance on the MNIST test set. The training history shows learning curves for both accuracy and loss, demonstrating the model's convergence.
Visualization

    Training/validation accuracy and loss curves

    Sample predictions with true vs. predicted labels

    Detailed classification report with precision, recall, and F1-score

Files

    digit_classification_vgg19.ipynb: Jupyter notebook with complete implementation

    README.md: This documentation file

Dependencies

    TensorFlow 2.x

    Keras

    NumPy

    Matplotlib

    scikit-learn

Usage

    Install required dependencies

    Run the notebook cells sequentially

    Observe training progress and evaluation results

    Analyze visualizations of model performance

Note

This experiment demonstrates transfer learning with a large pre-trained network on a relatively simple dataset. The VGG-19 architecture, while powerful, might be excessive for MNIST classification but serves as a good educational example of adapting pre-trained models
