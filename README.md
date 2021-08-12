# Cover Type Classification

### Objective: 
Build a deep learning model using TensorFlow with Keras to predict the forest cover type from different cartographic variables.

### Given: 
1. Cover Types: ['Spruce/Fir', 'Lodgepole Pine','Ponderosa Pine', 'Cottonwood/Willow','Aspen', 'Douglas-fir', 'Krummholz']
2. A csv file ('cover_data.csv') that contains 581012 observations. Each observation has 55 columns (54 features and the last one being the class).

### Output: 
A good model and it's performance over epochs, classification-report etc.
     
### Conclusions: 
We see that Lodgepole Pine, Cottonwood Willow, Aspen, and Douglas-Fir suffer from a high percentage of mis-classifications. To investigate the possible causes, one can explore the following:

1. Check the proportion of observations for each cover-type. Imbalances in the dataset will affect classification.
2. Find the similarties among different cover-types (correlation, scatter-plots, etc.) These similarities might be one of the reasons the model might be tripping-up. There are ways to address it - one of it is to carefully remove all of the collinear variables, leaving only one.
3. Remove noise, inconsistent data and errors in training data - this should be done carefully with domain experts.
4. Try to use some other performance metric other than 'accuracy'. It fails to be a reliable metric when data in imbalanced. That is why we have other metrics such as Precision/Recall, F1-score etc.
5. Try resampling the data (undersample or oversample appropriately or stratified). Downsampling could be done with thresholding.

