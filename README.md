# Airlines Customer Satisfaction 
This data given by an airline organization. It includes customer feedback on various aspects of their service and flight data.
The main goal of this project is to predict whether future customers will be satisfied based on these details. Additionally, the airline aims to identify which service aspects need improvement to increase customer satisfaction.
We will also utilize clustering algorithms to group the feedback based on the similarities or differences between the selected variables.

The dataset used in here obtained from Kaggle. 

<a href= 'https://www.kaggle.com/code/tugbakayaa/airlines-customer-satisfaction/notebook' target=_blank>You can find detailed information about the data here and see my notebook.</a>

# ---

We approached this project through two main categories: supervised and unsupervised learning.

In the *supervised learning* phase, we used Random Forest Classifier to train a model that predicted customer satisfaction levels. This method helped us classify customers based on their feedback and identify factors influencing their satisfaction. 

We implemented a machine learning pipeline to streamline our workflow. This pipeline effectively integrated multiple steps, including data preprocessing and model training, into a cohesive process.
The selected model was trained on the training dataset, allowing it to learn the underlying patterns and relationships within the data. Following the training, we made predictions on new, unseen data, enabling us to assess the model's performance and its ability to generalize to future customer satisfaction scenarios.
We evaluated the model's performance using a confusion matrix.

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|--------|
| 0     | 0.94      | 0.94   | 0.94     | 11882  |
| 1     | 0.95      | 0.95   | 0.95     | 14016  |
| **Accuracy**       |           |        | **0.94**     | **25898**  |
| Macro Avg | 0.94      | 0.94   | 0.94     | 25898  |
| Weighted Avg | 0.94      | 0.94   | 0.94     | 25898  |

The model achieved an overall accuracy of **94%**, indicating strong performance in predicting customer satisfaction.

To further enhance model performance, we performed hyperparameter tuning. This process involved optimizing the parameters that are not learned from the data during training. These parameters play a crucial role in influencing the learning process and can significantly impact the model's effectiveness.
The best score achieved after hyperparameter tuning was approximately **0.9425**, reflecting a high level of accuracy in predicting customer satisfaction.


In the *unsupervised learning* phase, we focused on clustering algorithms to group customer feedback into distinct clusters. 
We selected relevant features and standardized the data using StandardScaler. We calculated inertia values for KMeans clustering across different cluster numbers, observing a decreasing trend that indicated better-defined groupings with more clusters. We then applied Principal Component Analysis (PCA) to reduce dimensionality, retaining four principal components that explained approximately 72.90% of the variance. Finally, we recalculated inertia values using the PCA-transformed data to identify optimal clustering configurations.

## Conclusion
The classification algorithm provided more direct and quantifiable results, making it the more effective approach for predicting customer satisfaction in this project.



