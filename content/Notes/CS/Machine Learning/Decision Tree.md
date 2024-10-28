Decision Tree is a family of machine learning methods for both regression and classification. Decision tree uses a tree structure, with inner nodes represent the tests of an attribute, branches represent the outcome of the tests and leaf nodes represent the final decision. Decision tree models are built by recursively splitting the data into subsets based on the feature that best seperates the classes. They are intuitive and efficient. Common models include ID3, C4.5 and CART. To moderate overfitting, pruning of the tree is commonly utilized.
## Feature Selection
### Information Gain
$$
g(D,A) = H(D) - H(D|A)
$$
where $H(D)$ is the entropy of dataset $D$ and $H(D|A)$ is the conditional entropy of $D$ under the condition $A$.
#### Information Gain Ratio
$$
g_R(D,A) = \frac{g(D,A)}{H_A(D)}
$$
where 
$$
H_A(D) = -\Sigma _{i=1} ^n \frac{|D_i|}{|D|}log\frac{|D_i|}{|D|}
$$
## Pruning
Minimize
$$
C_\alpha (T) = C(T) + \alpha |T|
$$
## CART
### Regression Tree
Least Squares Regression
### Classification Tree
Gini Index
### Pruning of CART
Use cross-validation.