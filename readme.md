Setup env:

1. Enter terminal
2. navigate to cnnimageclassification folder
3. "python3 -m venv {venv name}

Activate env:

1. Enter terminal
2. navigate to cnnimageclassification folder
3. type "source {venv name}/bin/activate"

- the name of the virtual environment should be next to the terminal prompt if it is activated
- everything installed when the venv is running will be installed locally

4. pip3 install -r requirements.txt
- "jupyter notebook" will open jupyter notebook in chrome
- or open imageclassification.ipynb in vscode

When in "imageclassification.ipynb", select kernel in the top right, and choose cnn_env to enter virtual environment

- "deactivate" in terminal deactivates virtual env

Neural Network Information:

Convolutional Layer:

- The first layer of a convolutional neural network is always the Convolutional Layer. These layers apply a convolution operation to the input, pasing the result into the next layer. A convolution converts all pixels in its receptive field into a single value. The final output of the layer is a vector.
- The most common type of convolution is the 2D convolution layer. A filter or kernel in a conv2D layer slides over the 2D input data, perfirming an elementwise multiplication. It will be summing up the results into a single output pixel. The kernel will perform the operation for every location it slides over ,transforming a 2D matrix of features into a different 2D matrix of features

Max Pooling

- Max Pooling is a downsampling technique used in convolutional neural networks to reduce the spatial dimensions of an input volume.
- Max Pooling slides a kernel over the input data just like the convolutional layer, but instead of performing a multiplication, it takes the maximum value within the window. This maximum value becomes a single pixel in the new, pooled output. The window is slid across the input data by a stride of a certain number of pixels. Typically, the size of the pooling window is 2x2, and the stride with which the window is moved is also 2 pixels. This reduces the input size in half by height and width, effectively reducing the total number of pixels by 75%
- Feature Invariance: Max Pooling helps the model to become invariant to the location and orientation of features. This means that the network can recognize an object in an image no matter where it is located
- Dimensionality Reduction: By downsampling the input, max pooling significantly reduces the number of parameters and computations in the network, speeding up the learning process and reducing the risk of overfitting.
- Noise Suppression: Max pooling helps to suppress noise in the input data. By taking the maximum value within the window, it emphasizes the precense of strong features and diminishes the weaker ones

Fully Connected Layer:

- Fully Connected (fc) Layers means that every neuron from the previous layers connects to all neurons in the next. These are the last few layers in the network.
- A linear transformation of the form g(Wx+b) is used in the fc layer. W is the weight matrix, b is the bias vector, and g is an activation function, typically ReLU

In training:

- An epoch is one pass over the entire train set
- The number of epochs you choose depends on how long you want to train your network. The right amount depends on the optimizer and the network.
- Too many epochs will lead to overfitting
