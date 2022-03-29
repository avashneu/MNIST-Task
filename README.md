# MNIST-Task

Instructions:

- Download Jupyter Notebook 'MNIST_Task' 
- Upload the .ipynb file in your Jupyter Notebook.
- Restart the kernel to avoid any problem
- Run All Cells

Detailed Description

1. Run the first cell to import all the required packages
2. Obtain the dataset:
	- Run the cell after markdown "Obtaining the dataset" to get the MNIST dataset from Keras package
	- You can use the load_data function to load the data to obtain training and test split as (X_train, y_train), (X_test, y_test)
3. Since the inputs are image of 28x28, we need to reshape it for our FNN. So, we reshape both the X_train and X_test by image_size = 28x28
4. Similarly, since we will use softmax and categorical cross entropy loss function as the problem is a multiclass classification problem,
   we will perform one hot encoding of our target variable
5. Build and Compile Model:
	- We use Sequential function from Keras to build the model
	- Add a Dense layer i.e the hidden layer with 32 units in the layer, we've used sigmoid as the activation function
	- From the output of the hidden layer, use softmax activation function in the output layer of our FNN
	- Compile the model using compile function: 
		- Loss function is categorical crossentropy
		- Optimization technique is Stochastic Gradient Descent (SGD)
6. Fitting training dataset to the model
	- The X_train and y_train values as passed in the model for model fitting
	- The iterations for training is selected as 100. Multiple trials for different iterations were taken and 100 was selected as 
	  the optimal number of iterations which gave a decent accuracy.
7. Loss graph
	- Loss values for training set and test set for different iterations are plotted in a single figure.
8. Accuracy and Loss value
	- The final code cell gives the overall accuracy and loss for training set and test set.

Code References:
1. https://colab.research.google.com/drive/1U0sRZdxVUn8LbQN9KidMaomKt2MPJ2-o#forceEdit=true&sandboxMode=true&scrollTo=XaR6ncOmHNNw
2. https://medium.com/tebs-lab/how-to-classify-mnist-digits-with-different-neural-network-architectures-39c75a0f03e3
