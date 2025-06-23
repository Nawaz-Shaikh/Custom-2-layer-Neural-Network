# Digit Classifier - Neural Network from Scratch

This is a simple neural network built using only NumPy to classify handwritten digits from the MNIST dataset. It demonstrates the full pipeline of training a neural network without using any machine learning libraries like TensorFlow or PyTorch.

---

## Dataset Format

The model is trained on a CSV file (`train.csv`) that contains labeled digit images. The file should follow this structure:

```
label,pixel1,pixel2,...,pixel784
```

- Each row represents one image.
- Pixel values range from 0 to 255 (grayscale).
- The first column is the label (0 to 9).
- The remaining 784 columns are the flattened image pixels (28 x 28).

---

## Network Architecture

```
Input Layer   : 784 neurons (28x28 pixels)
Hidden Layer  : 10 neurons (ReLU activation)
Output Layer  : 10 neurons (Softmax activation)
```

---

## Features

- Manual implementation of forward and backward propagation
- ReLU activation in the hidden layer
- Softmax output for multi-class classification
- One-hot encoding of labels
- Accuracy measurement
- Visualization of predictions using matplotlib

---

## How to Use

***1. Install dependencies***

Make sure you have Python installed, then install required packages:

```
pip install numpy pandas matplotlib
```

***2. Add the dataset***

Place the `train.csv` file in the same directory as the script.

***3. Run the script***

You can execute the script using:

```
neural_network.py
```

This will start the training process, printing accuracy every 10 iterations.

---

## Example Output

```
Iteration:  0
Accuracy:  0.08

Iteration:  10
Accuracy:  0.31

...

Iteration:  490
Accuracy:  0.86
```

---

## Predict and Visualize

After training, you can test individual predictions and visualize them:

```python
test_prediction(3, W1, b1, W2, b2)
```

This will show the input digit and print the predicted vs actual label.

---

## Notes

- All calculations are done using basic matrix operations.
- No external ML libraries are used.
- This implementation is mainly for learning and understanding purposes.

---
