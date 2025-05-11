# Neural-Network-for-Image-classification

This project implements a ResNet-18 convolutional neural network for image classification on the CIFAR-100 dataset using PyTorch. The model is trained and evaluated with TensorBoard support for visualizing training metrics.

## Features

- **ResNet-18**: Custom implementation of the ResNet-18 architecture with residual blocks.
- **CIFAR-100**: Uses the CIFAR-100 dataset for training and testing.
- **Data Augmentation**: Includes random cropping, horizontal flipping, rotation, and color jittering for robust training.
- **TensorBoard Integration**: Visualize training loss and accuracy in real time.
- **GPU Support**: Automatically uses CUDA if available.

## Requirements

- Python 3.x
- PyTorch
- torchvision
- tensorboard

Install dependencies with:

```sh
pip install torch torchvision tensorboard
```

## Usage

1. **Train the Model**

   Open and run the cells in [ResNet18.ipynb](ResNet18.ipynb) to train the ResNet-18 model on CIFAR-100. Training and test accuracy will be printed for each epoch.

2. **Monitor Training with TensorBoard**

   After or during training, launch TensorBoard by running:

   ```sh
   tensorboard --logdir logs
   ```

   Or, use the notebook cell provided at the end of [ResNet18.ipynb](ResNet18.ipynb):

   ```python
   %reload_ext tensorboard
   %tensorboard --logdir logs
   ```

   Then, open the provided URL in your browser to view training metrics.

## File Structure

- `ResNet18.ipynb`: Main Jupyter notebook containing the model, training loop, and evaluation code.

## Model Architecture

- **ResidualBlock**: Implements the basic residual block used in ResNet.
- **ResNet**: Stacks multiple residual blocks to form the ResNet-18 architecture.
- **Training Loop**: Trains the model using SGD optimizer and cross-entropy loss, with metrics logged to TensorBoard.

## Hyperparameters

- Epochs: 30
- Batch Size: 128
- Learning Rate: 0.01
- Optimizer: SGD with momentum and weight decay

## Acknowledgements

- [ResNet: Deep Residual Learning for Image Recognition](https://arxiv.org/abs/1512.03385)
- [PyTorch Documentation](https://pytorch.org/docs/stable/index.html)
- [CIFAR-100 Dataset](https://www.cs.toronto.edu/~kriz/cifar.html)

---

Feel free to modify this README to better fit your needs!