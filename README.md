# Age-Gender-Ethnicity-Prediction

In this notebook, I'm going to do image classification and try to predict 3 different target variables: gender, ethnicity and age with 3 separate models. 

The data took from Kaggle and here's the [DIRECT LINK](https://https://www.kaggle.com/nipunarora8/age-gender-and-ethnicity-face-data-csv).


This dataset includes a CSV of facial images that are labeled on the basis of age, gender, and ethnicity.
The dataset includes 27305 rows and 5 columns.
The pictures are formated in 48X48 pixels in a grayscale.

There are three targets:

- Age: range from 1 to 116

- Ethnicity: 0 - White, 1 - Black, 2 - Asian, 3 - Indian, 4 - Other

- Gender: 0 - male, 1 - female


First, I'm going to deal with gender classification by using: 
- Simple fully connected network with hyperparameter search.

- Simple convolutional network.

- Data augmentation technique in try to improve the convolutional network.

Then, I will try to predict the ethnicity of the person in the image (which is harder because it's 5 classes) with the convolutional network.

At last, I will try to predict the age of the person in the image, which is a regression problem. I use:
- The convolutional network with the same architecture from earlier (almost).

- VGG19 architecture.

- Resnet50 architecture.



# Results Summary

### Gender:

- Fully connected layer model with 4 layers, 80 neurons each, Accuracy: 83.712%
- Convolutional model, Accuracy: 90.09%
- Convolutional model with data augmentation, Accuracy: 92.4 **best**

### Ethnicity:

- Convolutional model with data augmentation, F1 score: 82.54% **best**


### Age:

Note: With data augmentation Throughout.
- Convolutional model, MAE: 6.744
- VGG19, MAE: 5.921 **best**
- ResNet50, MAE: 6.3

