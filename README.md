# CAP5516 Final Project

## Instructions: How to run the code


## Task
This research aims to develop a deep learning model for brain tumor classification that combines transfer learning and genetic algorithms(GAs) for optimized hyper-parameter tuning and model architecture. Data augmentation techniques will also be used for improving the generalizability of our model and increasing the size of our dataset. Motivations for this project are three-fold:

1) Deep learning models can become highly complex and fine-tuning hyper-parameters can become a very time intensive task. Research has shown genetic algorithms(GA) offer an efficient way to find optimality of parameters and for exploration of the hyper-parameter search space.

2) This project aims to improve the models generalizability by exploiting genetic algorithm’s (GAs) resistance to overfitting. Combined with data augmentation techniques to increase the diversity and size of the dataset, the goal is to improve model performance on unseen data. 

3) Leveraging pre-trained models via transfer learning can potentially help improve model accuracy and prove an alternative for other resource-intensive deep learning techniques, making it more viable in a clinical environment.

## Approach

1) Pre-processing a brain tumor MRI dataset by employing normalization, de-noising, and re-sampling techniques and then segmenting regions with existence of tumors. 

2) Employing transfer learning on a pre-trained CNN network like ResNet for classification of brain tumors.
Utilizing genetic algorithms(GAs) like Particle Swarm Optimization (PSO), Differential Evolution (DE), or Teaching Learning based Optimization (TLBO) for optimization of hyper-parameters.
 Examples of hyper-parameters which the genetic algorithm (GA) can optimize:
Learning Rate
Batch Size
Number of layers

3) Applying data augmentation techniques to images for increased diversity. Some example approaches to this can be: rotation of images by 30 degrees, zoom, grayscaling, and flipping.

4) Using the newly optimized transfer learning model to perform brain tumor classification again and evaluate performance. 

5) Using genetic algorithms(GAs) again to perform feature extraction to generate an “optimal architecture” for the CNN. 

6) Comparing the performance of the model with other base-line classification algorithms like SVM and DNNs. [28, 29]


## Experiments: 

### Genetic Algorithm Optimization
In an attempt to optimize the parameter of our CNN, experimentation is required to find the ideal hyper-parameters of our genetic algorithm (GA). Testing will be required to find the following:

Population size 
Mutation type ( uniform random, gaussian, polynomial) 
Mutation rates (0, 0.005, 0.01, 0.05)
Crossover type ( single-point, two-point, blend, simplex, linear, simulated binary) 
Crossover rates  (0.01, 0.05, 0.1, 0.5, 0.9)
Selection strategy (tournament, rank, proportional) 

In addition to the parameters that define the GA, extensive studies on various types of GA’s can also be performed to see which genetic algorithm (GA) is able to best tune our CNN. Sample genetic algorithms (GA) to be compared: 

Canonical Genetic Algorithm (CGA)
Particle Swarm Optimization (PSO)
Differential Evolution (DE)
Teaching Learning based Optimization (TLBO)

###  Data Augmentation. 

The data augmentation used for the purposes of this project can also be evaluated in terms of model performance to see which techniques fare well. Testing can be done into various types of augmentation approaches like flipping, rotation, zoom, and grayscaling. The extent to which augmentation was utilized can also be studied like the degrees of rotation or amount of scaling.

### Transfer Learning. 

Determining the effectiveness of transfer learning can be done by comparing model performance to other pre-trained models like VGG and Inception-v3. Layers of the CNN can also be frozen so optimal weights can be found for individual layers and a better network architecture can be found.

### Evaluation Metrics

To measure model performance, we can use some evaluation metrics to determine model performance. Sample evaluation metrics:
Accuracy
Recall
F1 score 
ROC curve

## Related Works:

1) Studies performed by Tahir et al. (2021) utilized PSO optimization to automate the classification task in brain tumor identification. This study made use of GAs and found good success with this approach. My project aims to utilize these findings and make use of transfer learning and data augmentation in the process.

2) Bahadure et al.(2018) studied a comparative approach similar to the one I wish to perform on different segmentation techniques using genetic algorithms (GA). This paper used feature extraction using GAs and this is a stretch goal for my experiment. 

3) Deepak et al.(2019) had much success using transfer learning in the classification of brain tumors. They were able to get 98% accuracy with their predictions for a 3-class classification problem. This is one motivation for integrating transfer learning in this project. 

## Model Architecture



## Results


## Analysis of Results


## Conclusion


