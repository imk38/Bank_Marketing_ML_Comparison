Here I am building different supervised machine learning models to predict whether or not a customer will subscribe to a term deposit.I got the data from UCI/a different github source.

I divided the project into two parts, tree based models like light gbm, random forest, and XG boost. As well as non tree based models like knn, logistic regression, and support vector machine.

I am doing my best to tune these models to create a strong a model as possible. I dropped the duration feature because it is too predictive of the target variable. Additionally the duration is not known before the call itself. Dropping the duration variable presents a stronger challenge.

While the accuracy is generally pretty high in all these models, the precision and recall and a bit low for the positive class which is dissapointing and I will look to imrpove upon. This is dissapointing because it shows that the correct classifications in the negative class are what is driving the accuracy forward. I am trying to use f1 score in my grid search instead of accuracy to addres this as well as setting class_weight to balanced.

For the tree based models and logistic regression, I am using SHAP to evaluate this top important features. It seems like the top predictive features are number of employees and contact.
