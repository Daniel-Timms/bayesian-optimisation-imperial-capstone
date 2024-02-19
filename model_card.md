# Model Card

See the [example Google model cards](https://modelcards.withgoogle.com/model-reports) for inspiration. 

## Model Description

**Input:** The model accepts multidimensional numerical data as input. This input typically represents the parameters or variables that are being optimized in the context of Bayesian optimisation. The exact nature of these inputs can vary widely depending on the specific application or optimization problem being addressed.

**Output:** The model outputs predictions of the objective function value associated with the given inputs. Additionally, it provides an estimate of the uncertainty (standard deviation) associated with these predictions, which is crucial for guiding the optimization process.

**Model Architecture:** The core of the model is a Gaussian Process Regressor equipped with a Cosine Similarity Kernel. This kernel measures the cosine distance between data points in the feature space, allowing the model to capture periodic patterns and similarities in the input space. The kernel's effectiveness is enhanced by hyperparameter tuning, particularly the length scale, which is optimized using grid search to find the setting that maximizes the log-marginal-likelihood of the model.

## Performance

The performance of the model was evaluated through iterative experimentation, with a focus on the improvement of the objective function over time. Performance metrics such as the reduction in prediction error and the efficiency of exploration vs. exploitation in the optimization process were key indicators. Graphical representations of the model's predictions, along with confidence intervals across the input space, provided a visual assessment of model performance and uncertainty estimation.

## Limitations

A notable limitation of this model is its tendency to underfit, especially in complex optimization landscapes with multiple local maxima or highly irregular surfaces. The Cosine Similarity Kernel, while adept at capturing periodicity, may not always adequately represent the underlying complexity of certain objective functions.

## Trade-offs

The use of the Cosine Similarity Kernel involves trade-offs that are particularly evident in its application to non-periodic or highly complex optimization problems. While it can effectively capture cyclical patterns, this specialization may limit its versatility across a broader range of optimization tasks. The model may exhibit performance issues when applied to data that do not exhibit the cyclical or repetitive patterns the kernel is designed to capture.
