# H-CNN
This project proposes a different architecture of Deep learning that takes ‘n’ different uncorrelated features of same image/signal parallelly into non-shareable convolution input layers in the same network to predict classes. That is referred to as 1/2-D Hybrid-Convolutional Neural Network.

## Architecture

![](/media/architectureofhcnn.jpg)

The overview of architecture is: Features are extracted from Pre-processed images/signals which are fed into different branches of combination of Convolution and average down sampling layers, the resultant are flattened vectors linked together and further fed into a neural network for prediction. CNN’s property of automatically extracting features and their classification avoids the limited feature extraction arising due to manual extraction and effective features can be automatically generated through network training. But, some of the features are uncorrelated, this may reduce accuracy of our model. The model presented here take’s multiple inputs parallelly and generates a single output, each input is multivariate and uncorrelated to each other. 1/2-D hybrid Convolutional Neural Network (H-CNN) is used because of its high accuracy level which is attempted to be achieved as follows. The issue of accuracy is addressed in the form of a 2-stage assignment i.e. first branches and subsequently the features inside the branch are assigned. The branches are uncorrelated but the features inside are correlated. CNN uses shareable weights, since it is an arduous task to develop separate models for each feature of the uncorrelated data. So, we made clusters of correlated data and fed forward into separate branches of CNN and further integrated these flatten feature vectors (output of convolution and average down sampling layer). Neural network make’s decision boundaries over these concatenated vectors. Suppose nfeatures are given, deep learning model visualizes these nfeatures as n-dimensions but most of them are uncorrelated to each other. k clusters from them which are intercorrelated and each cluster has t1, t2, …, tk dimensions were created. And these t-dimensions are fed into separate k-different-branches of CNN. This reduces space, time complexity and overfitting.

## Learning And Loss Function
The significance of convolving the signal with the kernel is that it maps the current state of signal to another highly distinguishable space, so that our neural networks can build a delicate decision boundary. The convolution is done by sliding a window over a signal and formulated as: 
𝑦[𝑛] = ∑ 𝑥[𝑖]. ℎ[𝑛 − 𝑖] ∞ 𝑖=−∞ where, x[i] is the series of data and h is the kernel. For each feature we are combining all the waves which were captured from all the electrodes into a single vector and obtain a 1-D vector consisting of a set of all components obtained from every part of the brain.

## Results

![](/media/updatedtable.jpg)

## Note
Currently the results and accuracy only performed on signal data. The features were taken according to signals. We can change the features according to our requirement.