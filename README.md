# BAYESIAN OPTIMISATION

## NON-TECHNICAL EXPLANATION OF YOUR PROJECT
Bayesian optimization is a powerful strategy for improving the performance of machine learning models. Think of it as a highly intelligent trial-and-error process, but instead of randomly guessing, it uses past experiments to make smarter choices about what to try next. This project focuses on applying Bayesian optimization to fine-tune the settings of a predictive model, akin to finding the perfect recipe that makes a dish taste just right. Our goal is to demonstrate how this method can lead to better predictions with less guesswork and fewer trials.

## DATA
Our exploration is grounded in a dataset provided by Imperial College London, comprising 8 distinct functions designed to simulate real-world scenarios. Each function represents a different challenge, testing our model's ability to predict outcomes accurately. This diverse set allows us to rigorously evaluate our model's effectiveness across various conditions, ensuring its applicability in real-life situations.

## MODEL 
We employed a Gaussian Process Regressor model with a Cosine Similarity Kernel for this project. Gaussian Processes provide a flexible approach to modeling unknown functions, making them ideal for situations where we have limited data but need to make informed predictions. The Cosine Similarity Kernel was chosen because it excels at identifying periodic patterns, which we hypothesized could be present in user responses to different website configurations.

## HYPERPARAMETER OPTIMSATION
Hyperparameters in our model include the length scale and scale of the Cosine Similarity Kernel, crucial for defining how the model interprets similarity between data points. We optimized these hyperparameters using a combination of grid search and Bayesian optimization techniques. Grid search provided a broad overview of the parameter space, while Bayesian optimization refined the search to hone in on the most promising configurations, balancing exploration of new parameters with exploitation of known good ones.

## RESULTS
The implementation of the Cosine Similarity Kernel resulted in noticeable improvements in model performance. This kernel facilitated a better generalisation and mitigated the risk of overfitting, which was a concern with the RBF kernel given the small and potentially noisy dataset. However, we often under-fit the data.

The Cosine Similarity Kernel, provided a fresh perspective that was more aligned with the data’s characteristics. This adjustment underscored the critical role of domain knowledge and iterative experimentation in machine learning endeavours.

![download]([/Users/danieltimms/Desktop/download.png](https://github.com/Daniel-Timms/bayesian-optimisation-imperial-capstone/blob/main/download.png)https://github.com/Daniel-Timms/bayesian-optimisation-imperial-capstone/blob/main/download.png)

