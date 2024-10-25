The Naive Bayes method is a classification technique based on Bayes' Theorem. It assumes that features in the dataset are independent with each other, which would make the prediction efficient and straightforward. Naive Bayes models calculate the conditional probability of each class based on input features, and then predict the class with the highest probability.
## Fundamental Method
### Prior Probability
$$
P(Y=c_k) = \frac{\Sigma_{i=1}^N\ I(y_i=c_k)}{N}
$$
### Conditional Probability
$$
\begin{aligned}
P(X=x|Y=c_k) &= P(X^{(1)}=x^{(1)},...,X^{(n)}=x^{(n)}|Y=c_k) \\
&= \Pi _{j=1}^n P(X^{(j)}=x^{(j)}|Y=c_k)
\end{aligned}
$$
### Posterior Probability
$$
P(Y=c_k|X=x) = \frac{P(X=x|Y=c_k)P(Y=c_k)}{\Sigma _{k=1}^{K}P(X=x|Y=c_k)P(Y=c_k)}
$$
### Naive Bayes Classifier
$$
y = f(x) = argmax_{c_k}P(Y=c_k)\Pi _{j=1}^n P(X^{(j)}=x^{(j)}|Y=c_k)
$$
