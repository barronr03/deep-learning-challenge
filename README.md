## OVERVIEW

* The purpose of this analysis is to develop a deep learning model using TensorFlow to predict the success of funding applications for Alphabet Soup, a charity organization. The goal is to create a model that can accurately classify whether a funding application will be successful or not based on various input features.

## RESULTS

 #### Data Preprocessing:

* Target Variable: The target variable for the model is the "IS_SUCCESSFUL" column, which indicates whether the funding application was successful or not.
* Feature Variables: The features for the model include various columns such as "APPLICATION_TYPE," "AFFILIATION," "CLASSIFICATION," "USE_CASE," "ORGANIZATION," "STATUS," "INCOME_AMT," "SPECIAL_CONSIDERATIONS," and "ASK_AMT." 
* Variables to be Removed: The "EIN" and "NAME" columns are removed from the input data as they are neither targets nor features.

 #### Compiling, Training, and Evaluating the Model:

* Neurons, Layers, and Activation Functions: The selected model architecture includes two hidden layers with 80 and 30 neurons, respectively. The activation function used for the hidden layers is "relu," which helps introduce non-linearity and captures complex patterns in the data. The output layer uses the "sigmoid" activation function to produce a binary classification result.
* Target Model Performance: The target model performance was set to achieve an accuracy higher than 75%, however the model don't reached the target:
    * loss: 0.5592 - accuracy: 0.7254 - 441ms/epoch - 2ms/step

#### Steps to Optimize Model Performance:
 * Several steps were taken to improve the model performance with little or no impact:
         * Droping columns as "STATUS" or "SPECIAL_CONSIDERATIONS" that didn't have a high differentiation in their answers.
         * Decreasing number of values for each bin.
         * Add more neurons to a hidden layer.
 * There was 3 alternatives taht slightly improves the performance of the model:
         * Add only ONE additional hidden layer because the addition of one more resulst in a little impact in the performance. 
         * The use of LeakyReLU instead of relu as activation function, that helps to improve the learning capability of the model, enabling better training and potentially better generalization. 
         * Add the number of epochs to 110.

   * loss: 0.5519 - accuracy: 0.7265 - 614ms/epoch - 2ms/step (the optimized model is better than the original one, achieving higher accuracy, lower loss, and faster training time, however the target was not reached despite the modifications of the model.

## SUMMARY

* The deep learning model developed for Alphabet Soup showed promising results in predicting the success of funding applications. By implementing various optimizations, such as adjusting the number of neurons, epochs, and learning rate, the model's performance was improved. However, despite these efforts, the final model achieved an accuracy of approximately 72-73%, which did not meet the target accuracy of 75%. Although the model did not reach the desired accuracy level, it still provides valuable insights into the factors influencing funding success and can be used as a starting point for further improvements or alternative modeling approaches

#### Recommendation

* To further enhance the model's performance, it is recommended to explore alternative model architectures or algorithms, ensemble methods, such as random forests, can be considered to combine multiple models and improve prediction accuracy. By experimenting with different model architectures and algorithms, Alphabet Soup can continue to refine their funding application prediction system and make more informed decisions regarding the allocation of resources to maximize the impact of their charitable activities.
