# Water Quality Analysis Using AI
This is a project our group, Peer Learning Group 4 worked on which focuses on using an AI model with TensorFlow/Keras for analyzing water quality data and predicting water quality. We predict the quality of water samples as either "Safe" or "Unsafe." Our model can generalize well on unseen data, thereby assisting in identifying potentially unsafe water samples.
Here is the link to the Colab Document (Version History also available in the doc): https://colab.research.google.com/drive/1SdaXB9Gk3GVVvcPaSjQ6X2tExeZBB_RB?usp=sharing
## Group Structure and Task Allocation

This project was completed as part of a collaborative effort among four members of a peer learning group. The responsibilities were divided as follows:

### Team Members and Roles
1. **Samuel Oluwajunwonlo Babalola**  
   - **Email**: [s.babalola@alustudent.com](mailto:s.babalola@alustudent.com)  
   - **Role**: Model Building (L1 Regularization and Adam Optimizer), Vanilla Model Implementation.  
   - **Contribution**: Samuel focused on building the model using L1 Regularization and the Adam optimizer. He also contributed significantly to the initial vanilla model development.

2. **Oche David Ankeli**  
   - **Email**: [o.ankeli@alustudent.com](mailto:o.ankeli@alustudent.com)  
   - **Role**: Model Building (L2 Regularization and RMSprop Optimizer), Error Analysis, Vanilla Model Implementation.  
   - **Contribution**: Oche worked on optimizing the model using L2 Regularization with the RMSprop optimizer, and the vanilla model Implementation. He also contributed to error analysis and validation, ensuring that the models were evaluated and compared comprehensively.

3. **Irakoze Jean Raisa**  
   - **Email**: [r.irakoze@alustudent.com](mailto:r.irakoze@alustudent.com)  
   - **Role**: Data Handling and Processing.  
   - **Contribution**: Jean was responsible for gathering, processing, and transforming the dataset into a suitable format for training. Her work ensured that the data fed into the models was clean and consistent.

4. **Aime Magnifique NDAYISHIMIYE**  
   - **Email**: [a.ndayishim@alustudent.com](mailto:a.ndayishim@alustudent.com)  
   - **Role**: Data Cleaning and Preprocessing.  
   - **Contribution**: Aime focused on data cleaning and preprocessing tasks, ensuring that all irrelevant data points were removed and missing values were handled, making the data more suitable for modeling.

## Summary of the Implementation Process

### 1. Data Preprocessing
The dataset was processed to handle missing values, remove duplicates, and normalize the numerical features. This step was crucial to ensure that the models were trained on clean data.  
- **Tasks**: Irakoze and Aime collaborated to handle missing values, standardize the numerical features, and encode the categorical variables.  
- The final dataset was split into training and test sets, maintaining a consistent ratio for model evaluation.

### 2. Model Implementation and Variations
Several variations of models were implemented using different regularization techniques and optimizers to identify the best-performing model for this project. These models were built and tuned based on accuracy, precision, recall, F1 score, and stability across training and validation sets.

- **Vanilla Model**:  
  The vanilla model served as a baseline, implemented by Samuel and Oche, with minimal configuration and no regularization. It was used to understand the dataset characteristics and set a reference for future improvements.

- **L1 Regularization with Adam Optimizer**:  
  Implemented by Samuel Babalola, this variation was aimed at reducing the impact of less important features by adding L1 regularization. The Adam optimizer was chosen for its adaptive learning rate capability. However, the results showed fluctuating loss values, indicating that L1 might not be the best regularization technique for this dataset.

- **L2 Regularization with RMSprop Optimizer**:  
  Implemented by Oche David Ankeli, this variation used L2 regularization to penalize large weights and improve generalization. RMSprop was selected for its ability to adapt the learning rate based on the moving average of squared gradients. This model showed superior performance in terms of both accuracy and stability, making it the preferred configuration for this project.

### 3. Error Analysis and Model Evaluation
The models were evaluated using key performance metrics like **accuracy, precision, recall, F1 score, and stability**. It was found that the **L2 Regularization model** outperformed the L1 variant, especially in terms of recall for the "Unsafe" class, which is critical for identifying unsafe water samples.

### 4. Concluding Remarks
After comparing multiple configurations, the **L2 Regularization model with RMSprop** was selected as the final model due to its higher recall, stability, and consistent performance across both training and validation sets. It is the most reliable model for predicting unsafe water samples, making it the best fit for this safety-critical application.

## Outcome of Different Implementations in Summary

| **Model**                          | **Accuracy** | **Precision** | **Recall (Unsafe)** | **F1 Score** | **Specificity** |
|------------------------------------|--------------|---------------|--------------------|-------------|----------------|
| Vanilla Model                      | 0.66         | 0.65          | 0.34               | 0.45        | 0.89           |
| L1 Regularization + Adam           | 0.68         | 0.65          | 0.33               | 0.44        | 0.89           |
| **L2 Regularization + RMSprop**    | **0.68**     | **0.70**      | **0.86**           | **0.77**    | **0.90**       |

### Final Recommendation
Based on the evaluation, the **L2 Regularization with RMSprop Optimizer** is recommended for deployment due to its superior performance in detecting unsafe water samples and overall model stability.
