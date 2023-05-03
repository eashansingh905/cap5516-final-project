# CAP5516 Final Project
Automatic Hyper-parameter Tuning with Genetic Algorithms

## Instructions: How to run the code

[GA-utilities](https://github.com/eashansingh905/cap5516-final-project/tree/main/GA-utilities) has the sample optimization problems used to build the
infrastructure for the GA.

[classifier](https://github.com/eashansingh905/cap5516-final-project/tree/main/classifier) has the link to brain tumor identification related code

Link to dataset: https://github.com/sartajbhuvaji/brain-tumor-classification-dataset

[final report](https://github.com/eashansingh905/cap5516-final-project/blob/main/final-report.pdf) is attached with findings and conclusions.

## Task
This research aims to develop a deep learning model for multi-class brain tumor detection with the use of genetic algorithms (GAs) for optimized hyper-parameter tuning and model architecture. Genetic Algorithms have been found to be effective at several optimization problems, taking inspiration from evolutionary processes and a “survival of the fittest” approach. Data augmentation techniques will also be used for improving the generalizability of our model and increasing the size of our dataset. Motivations for this project are three-fold:

1) Deep learning models can become highly complex and fine-tuning hyper-parameters can become a very time intensive task. Research has shown genetic algorithms(GA) offer an efficient way to find optimality of parameters and for exploration of the hyper-parameter search space.

2) This project aims to improve the models generalizability by exploiting genetic algorithm’s (GAs) resistance to overfitting. Combined with data augmentation techniques to increase the diversity and size of the dataset, the goal is to improve model performance on unseen data. 

3) Leveraging pre-trained models via transfer learning can potentially help improve model accuracy and prove an alternative for other resource-intensive deep learning techniques, making it more viable in a clinical environment.

## Approach

1) Pre-processing a brain tumor MRI dataset by employing normalization, de-noising, and re-sampling techniques and then segmenting regions with existence of tumors. 

2) Employ a CNN architecture to develop a baseline model for various forms of brain tumor detection. Train the model by hand and record model performance observing key metrics like Train/Val Loss, Accuracy, F1 score, Precision, and Recall. 

3) Implement a genetic algorithm to evolve a population of CNN hyper-parameters

4) Observe the model performance with the optimized hyper-parameters and analyze the differences in the recorded metrics.

5) Apply data augmentations to see if we can improve the results

6) Make conclusions on the ability of the genetic algorithm to improve model generalizability and performance. Discuss the added computational overhead and whether it warrants its use. 

## Experiments: 

### Genetic Algorithm Optimization
In an attempt to optimize the parameter of our CNN, experimentation is required to find the ideal hyper-parameters of our genetic algorithm (GA). Testing will be required to find the following:

Population size 
Mutation type ( uniform random, gaussian, polynomial) 
Mutation rates (0, 0.005, 0.01, 0.05)
Crossover type ( single-point, two-point, blend, simplex, linear, simulated binary) 
Crossover rates  (0.01, 0.05, 0.1, 0.5, 0.9)
Selection strategy (tournament, rank, proportional) 

Encodings of sample solutions will be of the form:

E(Learning rate, batch size, # of filter)

Future study opportunities: 
In addition to the parameters that define the GA, extensive studies on various types of GA’s can also be performed to see which genetic algorithm (GA) is able to best tune our CNN. Sample genetic algorithms (GA) to be compared: 

Canonical Genetic Algorithm (CGA)
Particle Swarm Optimization (PSO)
Differential Evolution (DE)
Teaching Learning based Optimization (TLBO)

###  Data Augmentation. 

The data augmentation used for the purposes of this project can also be evaluated in terms of model performance to see which techniques fare well. Testing can be done into various types of augmentation approaches like flipping, rotation, zoom, and grayscaling. The extent to which augmentation was utilized can also be studied like the degrees of rotation or amount of scaling.

### Evaluation Metrics

To measure model performance, we can use some evaluation metrics to determine model performance. Sample evaluation metrics:

1) Training/Validation Loss
2) Accuracy
3) Precision
4) Recall
5) F1 score 

These metrics will be compared for the baseline and optimized models to see potential improvements in terms of performance
and generalizability.

## Related Works:

1) Studies performed by Tahir et al. (2021) utilized PSO optimization to automate the classification task in brain tumor identification. This study made use of GAs and found good success with this approach. My project aims to utilize these findings and make use of transfer learning and data augmentation in the process.

2) Bahadure et al.(2018) studied a comparative approach similar to the one I wish to perform on different segmentation techniques using genetic algorithms (GA). This paper used feature extraction using GAs and this is a stretch goal for my experiment. 

3) Deepak et al.(2019) had much success using transfer learning in the classification of brain tumors. They were able to get 98% accuracy with their predictions for a 3-class classification problem. This is one motivation for integrating transfer learning in this project.
