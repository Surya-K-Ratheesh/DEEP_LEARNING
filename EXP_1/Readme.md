# README for EXPERIMENT 1 A.ipynb

## Objective
The objective of this experiment is to familiarize with TensorFlow operations by creating and manipulating various types of tensors (scalars, vectors, matrices, and higher-dimensional tensors). The tasks include understanding tensor properties (shape, rank, size), performing arithmetic operations, and applying transformations like squeezing and one-hot encoding.

## Problem Statement
The notebook consists of a series of tasks aimed at exploring TensorFlow's capabilities:
1. Creating tensors of different dimensions (scalar, vector, matrix, 3D tensor).
2. Analyzing tensor properties (shape, rank, size).
3. Generating random tensors and performing operations like multiplication and dot product.
4. Manipulating tensor shapes (squeezing) and finding extreme values.
5. One-hot encoding a tensor.

## Dataset Used and Its Description
No external dataset was used in this experiment. The tensors were generated programmatically using TensorFlow's built-in functions, such as `tf.constant()` for fixed values and `tf.random.uniform()` for random values within specified ranges.

## Deep Learning Methods Used
- **Tensor Creation**: Used `tf.constant()` and `tf.random.uniform()` to create tensors with specific shapes and values.
- **Tensor Operations**: Applied element-wise multiplication (`tf.multiply`), matrix multiplication (`tf.matmul`), and dot product.
- **Tensor Properties**: Utilized `tf.shape`, `tf.rank`, and `tf.size` to inspect tensor dimensions and structure.
- **Tensor Manipulation**: Employed `tf.squeeze` to remove redundant dimensions and `tf.argmax` to find indices of maximum values.
- **One-Hot Encoding**: Converted a tensor into a one-hot encoded representation using `tf.one_hot`.

## Results
- Successfully created and displayed tensors of varying dimensions.
- Computed and printed tensor properties (shape, rank, size) for analysis.
- Performed arithmetic operations (multiplication, dot product) on random tensors.
- Demonstrated tensor squeezing to adjust shapes and identified min/max values in tensors.
- Generated a one-hot encoded tensor from a given input.

## Conclusion
This experiment provided hands-on experience with TensorFlow's core functionalities for tensor creation, manipulation, and analysis. The tasks covered essential operations that form the foundation for more complex deep learning workflows. By completing these exercises, one gains a better understanding of how tensors work in TensorFlow and how to perform common operations efficiently.
