# Chapter 1: The Machine Learning Landscape Exercise

1. How would you define Mahcine Learning?  
	The field of using observations (data) to build predictive models.
	
2. Can you name four types of problems where it shines?  
	Integrating complicated data for prediction, automizing complex tasks, 
  **build systems that adapt to fluctuating environments**, **help humans learn**
	
3. What is labeled training set?  
	A set of data that has the features and outcomes used for training algorithms to 
  build models.
	
4. What are the two most common supervised tasks?  
	Regression and classification
	
5. Can you name four common unsupervised tasks?  
	Clustering, **visualization, dimentionality reduction, and association rule 
  learning**
	
6. What type of Machine Learning algorithm would you use to allow a robot to walk 
in various unknown terrains?  
	Reinforcement learning. 
	
7. What type of algorithm would you use to segment your customers into multiple groups?  
   If the group labels are unknown, unsupervised clustering can be used to organize 
   the customers into different groups. If the group labels are known, supervised 
   clssification such as logistic regression or random forrest can be used to organize 
   the customers into groups with the most similar attributes. 
   
8. Would you frame the problem of sapm detection as a supervised learning problem or 
an unseupervised learning problem?  
	Supervised learning since the group labels are known, spam or ham.
	
9. What is an online learning systme?  
	The system can learn incrementally as the training data gets updated. The model 
  does not have to be built with the entire training set.
	
10. What is out-of-core learning?  
	 A type of online learning. When the training data is too big, the algorithm loads 
   partial data and learn incrementally. 
	 
11. What type of learning algorithm relies on a similarity measure to make predicitons?  
	 Instance-based learning
	 
12. What is the difference between a model parameter and a learning algorithm's hyperparameter?  
	 A model parameter controls is affected by the learning algorithms. A learning 
   algorithm's hyperparameter finetunes how the learning algorithm uses the training 
   set to build the model. **A model parameter determines what the model will predict 
   given a new instance, e.g. the slope of a linear model. A hyperparameter is a parameter 
   of the learning algorithm itself, e.g. the amount of regularization to apply**
	 
13. What do model-based learning algorithms search for? What is the most common strategy 
they use to succeed? How do they make predictions?  
	~~Features in the training set~~ **The algorithms search for an optimal value for 
  the model parameters such that the model will generalize well to new instances**   
	~~Building models from the training set and use the model to predict new instances~~ 
  **Algorithms do so by minimizing the cost function that measures how bad the model 
  is at making predictions on the training data, plus a penalty for model complexity 
  of the model is regularized**  
	Once a model is build and a new data given, extract the features from the new data 
  and predict using the algorithm

14. Can you name four of the main challenges in Machine Learning?  
	 Poor quality of the training data, insufficient training data, overfitting, underfitting. 

15. If your model performs great on the training data but generailzes poorly to new 
instances, what is happening? Can you name three possible solutions?  
	Overfitting.  
	Getting more data, feature selection, regularization to prevent overfitting, 
  **reducing noise in the training data, using simpler models**

16. What is a test set and why would you want to use it?  
	 A set that was held-out from the training set to be tested for the model. 
   This helps assess the accuracy of a model

17. What is the purpose of a validation set?  
	 The validation set is a second holdout set that helps select the best model 
   if multiple models were built with different parameters. After the model that 
   performs best on the validation set is selected, it can then be tested on the 
   test set to assess accuracy. **The validation set is used to compare models and 
   select the best model to tune the hyperparameters.**
	 
18. What can go wrong if you tune hyperparameters using the test set?  
 	 The model will be fine tuned for the specific test set  **(overfitted to the 
   test set)** but doesn't generlize well to new data sets.

19. What is cross-validation and why would you prefer it to a validation set?  
	To prevent wasting too much data on training data in validation sets, the training 
  set can be split into multiple subsets that contain different combination of the 
  original data. The model can be trained on these different combinations of data 
  and validated on the remaining sets to select for a best model. **Once the model 
  type and hyperparameters have been selected, a final model is trained using these 
  hyperparameters on the full training set, and the generalized error is measured on 
  the test set. Simply put, cross-validation is a technique that helps compare models 
  for model selection and hyperparameter tuning without the need for separate validation 
  sets**
