# neural-network-challenge-2
Module 19 Challenge Assignment Repository

### This Challenge project is designed to create a neural network the HR can use to predict whether employees are likely to leave the company.  Additionally, HR has asked that a model be built to predict the best fit of department for each employee, assuming that some employees may be better suited to be in other departments than currently assigned:

### The challenge employs the following tools for the purpose of generating the data for evaluation:
* Pandas for utilizing Pandas notebooks
* Tensorflow for preprocessing, training, and optimizing the data
* Keras to be used with Tensorflow to build a neural network model with optimal layers, activation functions, and loss functions.
* Train_Test_Split to create training and test data sets to evaluate the accuracy of the model.
* StandardScaler() from Sklearn is used to scale the training data to ultimately transform the testing data set to a more uniform scale to apply the model attributes.

### I chose a feature set that I believe would provide the top 10 features (among 25 attributes) to train the model to make the most accurate predictions.  My 10 features selected were...
* Age	
* DistanceFromHome	
* EnvironmentSatisfaction	
* JobInvolvement	
* JobSatisfaction	
* PercentSalaryHike	
* PerformanceRating	
* RelationshipSatisfaction	
* TrainingTimesLastYear	
* WorkLifeBalance	

### In training the model, the "Accuracy" metric was calculated at 78.9% for Attrition prediction, and 56.5% for Department prediction.  The summary below describes some of the considerations, challenges, or potential changes that can be made to improve the desired effectiveness of the model.

### My answers in the summary questions include the below thoughts and documentation related to the model and potential improvements...
### Questions:
1. Is accuracy the best metric to use on this data? Why or why not?
2. What activation functions did you choose for your output layers, and why?
3. Can you name a few ways that this model might be improved?

### Answers:
1. Accuracy may not be the best metric to use on this data.  This is specifically due to the fact that Accuracy works best when classes are balanced.  There is a risk that the accuracy metric may be skewed in an imbalanced data set simply by the tendency to predict the majority class.  In the predictions of this challenge, the attrition target is significantly skewed toward a "no" prediction as the majority class, making up 83% of the training set.  Similarly, Research & Development is highly skewed in the department target, making up 66% of the training set.
2. I chose the activation function of Sigmoid for the 'Attrition' target in the output layers.  And, I chose the Softmax activation function for the output layers of the 'Department' target.  In general, Sigmoid is recommended for binary data, which is true for the Attrition target, with Yes or No (0 or 1 after One-Hot Encoding) as the only 2 possible results (binary).  In contrast, Softmax is generally recommended for multi-class data sets.  The 'Department' results are multi-class, with 3 possible classifications (Research & Development, Sales, & Human Resources).  
3. A few ways that the model may be improved include the following;      1. The feature set can be modified experiment with the 10 selected features, or to use a different set of features to predict 'Attrition" than used to predict the most suitable 'Department.'    2. Apply RandomOversampling or RandomUndersampling to balance the data.  This may help to address any impact of the majority class skewing the accuracy metric in making predictions,    3. Experiment with the batch-sizes or number of epochs to improve the model,    4. Add more layers or neurons to the model to ensure more complex aspects of the data are addressed. 

### Note that I completed all work in this challenge without requiring outside assistance...