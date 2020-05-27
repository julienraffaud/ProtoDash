# Efficient Data Representation by Selecting Prototypes with Importance Weights: An Implementation in PySpark

## Summary:

In this notebook I present a prototype selection algorithm proposed by Gurumoorthy, K. S. et al. ([1]) called ProtoDash, that is capable not only of selecting prototypes from a source dataset that are representative of a given target dataset, but can also assign non-negative weights to each one, thereby giving a sense of their relative importance in representing this target dataset. 

I implement the ProtoDash algorithm using PySpark, the Python API supporting Apache Spark, and in two experiments demonstrate its performance in application to a well-known large dataset: the MNIST Dataset of Handwritten Digits. In these experiments I show that the ProtoDash algorithm is capable of effectively representing an increasingly skewed target dataset based on a completely distinct and randomly sampled source dataset. Furthermore, I show that the algorithm's runtime in practice is largely driven by the computation of the mean inner product between the observations in the target and source datasets, with the actual selection of prototypes taking an increasingly small fraction of time as the dataset sizes increase by orders of magnitude.

## References

[1] Gurumoorthy, Karthik S., et al. "Efficient Data Representation by Selecting Prototypes with Importance Weights." 2019 IEEE International Conference on Data Mining (ICDM). IEEE, 2019. 

[2] Gretton, Arthur, et al. "A kernel method for the two-sample-problem." Advances in neural information processing systems. 2007.

[3] Kim, Been, Rajiv Khanna, and Oluwasanmi O. Koyejo. "Examples are not enough, learn to criticize! criticism for interpretability." Advances in neural information processing systems. 2016.

[4] Friedman, J., Hastie, T., & Tibshirani, R. (2001). The elements of statistical learning (Vol. 1, No. 10). New York: Springer series in statistics.

[5] The MNIST Database of Handwritten Digits: http://yann.lecun.com/exdb/mnist/

[6] Koh, P. W., & Liang, P. (2017, August). Understanding black-box predictions via influence functions. In Proceedings of the 34th International Conference on Machine Learning-Volume 70 (pp. 1885-1894). JMLR. org.

