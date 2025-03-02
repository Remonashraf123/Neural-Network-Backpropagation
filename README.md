# Neural Network Backpropagation Example

This project implements a simple neural network with one hidden layer using NumPy to demonstrate forward and backward propagation.

## Overview

The neural network consists of:

- **Input Layer**: 2 neurons
- **Hidden Layer**: 2 neurons
- **Output Layer**: 2 neurons
- **Activation Function**: Sigmoid
- **Learning Rate**: 0.5
- **Optimization Algorithm**: Gradient Descent
- **Loss Function**: Mean Squared Error

## Explanation

The project demonstrates the following steps:

- Forward propagation to calculate outputs
- Error calculation using mean squared error
- Backpropagation to adjust weights based on the error
- Weight updates using gradient descent
- Numerical demonstration of weight adjustments in each iteration

### Mathematical Equations

#### Forward Propagation

1. Net input to hidden layer neurons:
   \[
   net_{h1} = x_1w_1 + x_2w_3 + b_1
   \]
   \[
   net_{h2} = x_1w_2 + x_2w_4 + b_1
   \]

2. Output of hidden layer neurons:
   \[
   out_{h1} = \sigma(net_{h1})
   \]
   \[
   out_{h2} = \sigma(net_{h2})
   \]

3. Net input to output layer neurons:
   \[
   net_{o1} = out_{h1}w_5 + out_{h2}w_7 + b_2
   \]
   \[
   net_{o2} = out_{h1}w_6 + out_{h2}w_8 + b_2
   \]

4. Output of output layer neurons:
   \[
   out_{o1} = \sigma(net_{o1})
   \]
   \[
   out_{o2} = \sigma(net_{o2})
   \]

#### Error Calculation

Mean Squared Error:
\[
E_{total} = \frac{1}{2}((target_1 - out_{o1})^2 + (target_2 - out_{o2})^2)
\]

#### Backpropagation

Gradient of Error w.r.t. Output:
\[
\frac{\partial E_{total}}{\partial out_{o1}} = out_{o1} - target_1
\]

Gradient of Error w.r.t. Net Input at Output Layer:
\[
\frac{\partial E_{total}}{\partial net_{o1}} = \frac{\partial E_{total}}{\partial out_{o1}} \cdot \sigma'(net_{o1})
\]

Weight Updates:
\[
 w = w - \eta \cdot \frac{\partial E_{total}}{\partial w}
\]

### Diagram

![image](https://github.com/user-attachments/assets/0f06c651-e71d-4c98-9582-750ab0311ec3)


## Prerequisites

- Python 3.x
- NumPy Library

## How to Run

1. Install Python and NumPy.
2. Clone the repository.
3. Navigate to the project directory.
4. Run the script using:

```bash
python neural_network.py
```

## Results

The final weights will be printed after one iteration of backpropagation, demonstrating the network's learning process.

## License

This project is for educational purposes only.

