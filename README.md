# Classical Machine Learning

Implementing classical machine learning algorithms using basic Python libraries, on datasets available publicly on the web. Although this repository focuses on implementation, I am planning to collect my own data and apply these algorithms on them for interesting tasks soon.

__NOTE__: It is recommended to view the iPython Notebook files (.ipynb) on https://nbviewer.jupyter.org/ instead of Github.

## Contributing

Feel free to fork this repository and add your own implementations of these algorithms for your own datasets. Create a Pull Request and add your own (appropriately named) branch with a summary of proposed changes.

### Multivariate Linear Regression

Given linear _multi_-dimensional data, computes the best fit hyperplane, i.e. for new input values, the model predicts corresponding output values for them. In this case, the input consists of number of `bedrooms`, and `area` of an apartment, and the algorithm computes the best fit __plane__ which describes the relationship of the input with the `price` of the apartment.

Using dataset from [Tanmoy's](https://medium.com/@tanmoy) article on [Medium](https://medium.com) - https://medium.com/we-are-orb/multivariate-linear-regression-in-python-without-scikit-learn-7091b1d45905.

![Multivariate Linear Regression](result-plots/multivariate_linear_regression.svg)

### Logistic Regression

Given the RNA gene expressions of Pancreatic Cancer patients having different types of tumor: BRCA, KIRC, COAD, LUAD and PRAD, this algorithm is being used to classify the correct type of tumor that the patient has. This regression technique does not assume linearity in data. Instead, it uses what is called the [Softmax/Logistic](https://en.wikipedia.org/wiki/Softmax_function) function for fitting the training data into a model. Overall, my implementation resulted in __98.00%__ accuracy.

Using the PANCAN-RNA-SEQ dataset from UCI's machine learning repository - https://archive.ics.uci.edu/ml/datasets/gene+expression+cancer+RNA-Seq.
Each data point the the dataset has 20531 attributes, so it is really difficult to actually visualize the dataset.

### K-Nearest Neighbors Classification

Given the input `sepal_length`, `sepal_width`, `petal_length`, and `petal_width` parameters of an Iris flower, the algorithm tries to predict its species - _setosa_, _virginica_, or _versicolor_. For a particular testing input, the algorithm looks at `k` data points closest to it (in eucledian terms), and determines the best species. Overall, my implementation resulted in __83.79%__ accuracy.

Using the classic Iris dataset from UCI's machine learning repository - https://archive.ics.uci.edu/ml/datasets/Iris.
It is hard to visualize the actual datapoints in 5 dimensions, so here is the pairplot.
![K-Nearest Neighbors](result-plots/knn_classification.png)

### Naive-Bayes Classification

Given an SMS text message, the algorithm tries to predict whether the text is a `spam` or `ham`. For a particular testing input, the algorithm analyzes each word occuring in it, and using the occurrence of that word within the training set, it decides the tag of the input text. Bayes theorem (conditional probability) is the key idea of this algorithm, and it assumes independence between all features of the text. I used a 'bag of words' representation for each text message. Overall, my implementation resulted in __96.95%__ accuracy.

Using the SMS Spam Collection dataset from UCI's machine learning repository - https://archive.ics.uci.edu/ml/datasets/SMS+Spam+Collection.

Spam examples - 
```
Free entry in 2 a wkly comp to win FA Cup final tkts 21st May 2005. 
Text FA to 87121 to receive entry question(std txt rate)T&C's apply 08452810075over18's

As a valued customer I am pleased to advise you that following recent 
review of your Mob No. you are awarded with a £1500 Bonus Prize call 09066364589
```
Ham examples -
```
Just forced myself to eat a slice. I'm really not hungry tho. 
This sucks. Mark is getting worried. He knows I'm sick when I turn down pizza. Lol

I'm still looking for a car to buy. And have not gone 4the driving test yet.
```
### Univariate Linear Regression

Given linear two dimensional data, computes the best fit line, i.e. for new input values, the model predicts corresponding output values for them. 

Using dataset from [Tanmoy's](https://medium.com/@tanmoy) article on [Medium](https://medium.com) - https://medium.com/we-are-orb/linear-regression-in-python-without-scikit-learn-50aef4b8d122.

![Univariate Linear Regression](result-plots/univariate_linear_regression.svg)
