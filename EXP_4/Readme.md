**Problem Statement**

The core task in this project is image classification: automatically categorizing 32x32 color images from 10 semantic classes in the CIFAR-10 dataset. The challenge involves optimizing a deep CNN's training stability and accuracy by evaluating two different weight initialization strategies.





**Deep Learning Method Used**

The method is a convolutional neural network (CNN) comprising stacked Conv2D, batch normalization, max pooling, dropout, and dense layers. The experiment varies only the weight initializer (Xavier/Glorot vs Kaiming/He) to compare their effect on learning dynamics and final accuracy





**Description of Method**

Both models share identical structure:

Two blocks of Conv2D layers (first block: 32 filters, second block: 64 filters), each followed by batch normalization and max pooling.

Dropout (0.3) applied after pooling for regularization.

Flatten layer to convert feature maps, followed by a dense hidden layer (512 units, ReLU), with batch normalization and dropout.

Output layer uses softmax activation for multiclass probability prediction.

L2 kernel regularization applied throughout.

The initialization method is set via Keras’s kernel\_initializer: GlorotNormal (Xavier) or HeNormal (Kaiming), chosen to test their impact in deep CNNs with ReLU activations.





**Training Process**

CIFAR-10 images are normalized to and labels are one-hot encoded.

Both models are compiled with Adam optimizer and categorical crossentropy loss.

Training proceeds for 20 epochs with a batch size of 64 and validation evaluated on withheld test data each epoch.

Model performance metrics (loss, accuracy) are tracked and visualized over epochs.

Final evaluation on the test set yields the reported metrics





**Result**

Model			Test Loss	Test Accuracy

Xavier(Glorot)		1.2525		0.7758

Kaiming (He)		1.2413		0.7888



The Kaiming model outperformed the Xavier model with a ~1.3% higher test accuracy and marginally lower test loss.





**Conclusion**

For deep CNNs with ReLU activations on CIFAR-10, Kaiming weight initialization leads to more robust optimization and better generalization than Xavier initialization, as evidenced by improved test accuracy and loss metrics. This underscores the importance of matching weight initialization schemes to activation functions for optimal model training outcomes

