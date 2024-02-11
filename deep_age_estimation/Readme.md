# Deep Age Estimation Using ResNet50 Architecture
In order to improve the services, the owner of the store decided to personalized their services based on the age of the customer.

**The Objective** is to build a deep age estimation model for the customer face data.

**Stack:** `pandas` `TensorFlow` `Keras` `ResNet50`

## Conclusion

In conclusion, the findings from the Exploratory Data Analysis (EDA) phase provided valuable insights into the dataset's age distribution and characteristics. The average age of approximately 31.2 years, a standard deviation of 17.1 years, and quartile information highlighted the dataset's diversity. The presence of images with obstructed faces like blocked part of face, brightnes, etc adds a complexity to the age detection task.

Moving to the output of the model training phase, several key observations guide the model development process. The inverse relationship between learning rate and overfitting suggests a delicate balance in training hyperparameters. In other words, lower learning rate resulting overfitting and vice versa. The impact of batch size on training speed emphasizes the trade-off between computational efficiency and model generalization. Introducing dropout after the ResNet backbone emerges as a beneficial strategy to enhance model performance (lower mean absolute error on validation data). But remain overfitting issues.

The best Mean Absolute Error (MAE) achieved in trial 3 further underscores the significance of these considerations. In conclusion, ResNet50 has proven to be a valuable backbone for age estimation models. However, the exploration of alternative image preprocessing techniques such as Pillow, OpenCV, and other model architectural remains crucial.

## Attachments

Face Data
![Face Data](https://github.com/nashihabdul/data_science_projects/blob/main/deep_age_estimation/face_data.png)

Age Distribution
![Age Distribution](https://github.com/nashihabdul/data_science_projects/blob/main/deep_age_estimation/age_distribution.png)
