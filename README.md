# Neural_Network_Charity_Analysis

## Overview of the analysis 
Using Machine Learning and Neural Networks for this project, features within this dataset were utilised to create a binary classifier using OneHot categorical encoding, to help predict whether applicants that are going to be funded by our charitable organisation (Alphabet Soup) are going to be successful in their venture or not. Such so, a dataset containing various measures on 34,000 organisations funded by Alaphabet Soup was utilised upon which the data was:
- Pre-processed 
- Compiled, trained, and then evaluated
- optimization of the model to obtain an accuracy of approx. 75% 

## Results 

### Data Pre-Processing 
In order to build our neura network around the data set provided, we must first go throug the steps of preprocessing our dat. This involves the following:
    - dropping irrelavent feilds that carry data of no meaning such as 'EIN' and 'NAME' 
    - finding the number if unique counts 
    - creating density plots for DIST.
    - creating a list of categorical variables 
    - encoding the data using OneHot ecoding 
    - Merging the encoded DataFrame with the existing one and and then dropping duplicates 
    - splitting our arrays
    - Creating Test and Training sets 
    - standardizing our data
    
### Compiling, training, and Evaluating 
The following neural network holds 2 hidden layers as well as an output layer. The first layer consisted of 80 neurons while the second consisted of 30. Furthermore, both hidden layesrs make use of the 'relu' activation fuction while the output apply apply a sigmoidal logic.

What variable(s) are considered the target(s) for your model?
    - IS_SUCCESSFUL colimn
What variable(s) are considered to be the features for your model?
    - all columns besides IS_SUCCESSFUL
What variable(s) are neither targets nor features, and should be removed from the input data?
    - all columns dropped during pre-processing such as 'EIN' and 'NAME'

Unofortunately the model did not achieve the targeted accuracy of 75% (only achieved a max of 69.95%) and so further optimization had to applied (i.e. refactor the code to decrease loss and increase accuracy). In order to do so, 3 seperate attempts were made at:
    - Adding more neurons to a hidden layer
    - Adding more layers 
    - Using different activation functions for the hidden layers
    
## Summary 
As the model did not hit the target accuracy of 75% reaching a max of 69.95% the three attempts listed above were undergone in order to try and amelorate the model:

### Adding more neurons to a hidden layer 
upon the addition of 20 mre neurons to hidden layer 1 we were able to increase the accuracy of our predictive model from 71.94% to 74.39%. This brings us closer to our goal of 75% but unfortunately wed have to round down keeping us at 74%.
### Adding more layers 
The addition of a third layer containing 10 neurons was slightly more successful yeilding a positive increase of the models accuracy from 72% to 74.46%, ufortunately this still falls short of our target score of 75% 

### Using different activation functions for the hidden layersa hidden layer
Finally, the use of a differnet activation function, in our case 'tanh' finally yeilded successful results increasing our models predictive accuracy from 72.07% to 74.55% which in this case for our purposes can be rounded up to 75%  

### Alternative model 
To conclude, we can alternate to using a more traditional Random Forest Clasifier. With less parameters to optimize it may be more advantageous to utilise owing to the lack of complexity and similar robustness as compared to the deep learning classification model
