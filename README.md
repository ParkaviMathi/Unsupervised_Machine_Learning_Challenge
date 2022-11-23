# Unsupervised_Machine_Learning_Challenge

## Myopia Clusters
### Background
We are on the data science team of a medical research company that’s interested in finding better ways to predict myopia, or nearsightedness. Our team has tried—and failed—to improve their classification model when training on the whole dataset. However, they believe that there might be distinct groups of patients that would be better to analyse separately. So, our supervisor has asked us to explore this possibility by using unsupervised learning.
We have been provided with raw data, so we’ll first need to process it to fit the machine learning models. We will use several clustering algorithms to explore whether the patients can be placed into distinct groups. Then, we’ll create a visualisation to share our findings with our team and other key stakeholders.


This activity is broken down into four parts:
Part 1: Preparing the Data
Part 2: Applying Dimensionality Reduction
Part 3: Performing a Cluster Analysis with K-means
Part 4: Making a Recommendation



### Part 1: Preparing the Data
myopia.csv is read into a Pandas DataFrame.
The "MYOPIC" column is removed from the dataset.
Note: The target column is needed for supervised machine learning, but it will make an unsupervised model biased. After all, the target column is effectively providing clusters already!
Our dataset is standardised so that columns that contain larger values do not influence the outcome more than columns with smaller values.

### Part 2: Applying Dimensionality Reduction

Dimensionality reduction is performed with PCA. How did the number of the features change?
Rather than specifying the number of principal components when we instantiate the PCA model, the desired explained variance is stated. For example, say that a dataset has 100 features. Using PCA(n_components=0.99) creates a model that will preserve approximately 99% of the explained variance, whether that means reducing the dataset to 80 principal components or 3. For this assignment, 90% of the explained variance is preserved in dimensionality reduction.

Further the dataset dimensions are reduced with t-SNE and the results are visually inspected. To do this, t-SNE is run on the principal components, which is the output of the PCA transformation.

A scatter plot of the t-SNE output is created. Are there distinct clusters?

### Part 3: Performing a Cluster Analysis with K-means
An elbow plot is created to identify the best number of clusters.
A for loop is used to determine the inertia for each k between 1 through 10.

The elbow of the plot is determined, and at which value of k it appears.

### Part 4: Makeing a Recommendation
Based on our findings, a brief (one or two sentences) recommendation is written for our supervisor in our Jupyter Notebook. Can the patients be clustered? If so, into how many clusters?
