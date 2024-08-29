# Module 21 — Deep Learning Challenge

## Overview

Nonprofit foundations receive thousands of applications throughout the year for various grants they offer. These foundations often request a wide array of information, hoping it will provide deeper insights into the applicants. Grants can be awarded to a single large applicant, a few substantial ones, or several smaller candidates, depending on the grant's size and goals. However, the volume of information and the sheer number of applicants can pose significant challenges for foundations. Like individuals, foundations are limited by time and can only process so much information at once.

Imagine a foundation like Alphabet Soup, which has previously funded 34,000 organizations. The number of grant applications they receive—and must ultimately decline—is staggering. Each selection can feel like a game of chance, where even the most well-prepared applicants might not succeed. The challenge of this module was to improve the foundation's chances of identifying successful candidates by uncovering patterns hidden within the data.

## Results

### Data Processing

1. **What variable(s) are the target(s) for your model?**

   The target variable is `IS_SUCCESSFUL`. By analyzing successful projects and building a neural network based on what made them successful, Alphabet Soup can support their decision-making process.

2. **What variable(s) are the features for your model?**

   The feature variables include the former applicants’ affiliated industry, government classification, grant purpose, type of organization, whether they remain active, income bracket, potential special considerations, and the amount of their funding request.

3. **What variables are not included in the features for your model?**

   The variables `NAME` and `EIN` are not included as features in the model.

### Compiling, Training, and Evaluating the Model

1. **How many neurons, layers, and activation functions did you select for your neural network model, and why?**

   In the Google Colab environment, 80 neurons were selected for the first hidden layer, and 30 neurons for the second hidden layer. There were two hidden layers in total, utilizing two types of activation functions. These choices were made because transforming the data into dummy variables expanded the number of columns, requiring the neural network to account for a greater number of combinations.

2. **Were you able to achieve the target model performance?**

   After 100 epochs, the model achieved an accuracy of 72.64% with a loss of 0.55.

3. **Did additional modifications improve model performance?**

   In the Jupyter notebook, an extra hidden layer with 20 neurons was added. However, this only slightly improved the accuracy to 72.68%, while maintaining a loss of 0.55.

## Summary

Attempting to improve the model by adding additional hidden layers, even sizable ones, did not seem to enhance its accuracy. One possible reason for this is the combination of all types of applicants in a single model. Large applicants and small applicants have fundamentally different organizational structures. Large applicants may have numerous staff, bureaucratic procedures, and supplemental forms of funding. Additionally, their goals might be supported by other organizations invested in their success. On the other hand, smaller applicants might lack this organizational structure and collective support but may have a highly committed staff focused on achieving a niche objective. Not accounting for these differences or developing a separate network that inherently understands these features could be affecting the model's results. These features could potentially be better captured by siloing them into different models based on organizational characteristics.
