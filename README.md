BREAST CANCER PREDICTION WITH MACHINE LEARNING

A mammogram is an x-ray picture of the breast. It can be used to check for breast cancer
in women who have no signs or symptoms of the disease. It can also be used if you have a lump or
other sign of breast cancer.
Screening mammography is the type of mammogram that checks you when you have no
symptoms. It can help reduce the number of deaths from breast cancer among women ages 40 to
70.
But it can also have drawbacks. Mammograms can sometimes find something that looks
abnormal but isn't cancer. This leads to further testing and can cause you anxiety. Sometimes
mammograms can miss cancer when it is there. It also exposes you to radiation.
You should talk to your doctor about the benefits and drawbacks of mammograms.
Together, you can decide when to start and how often to have a mammogram. Now while its
difficult to figure out for physicians by seeing only images of x-ray that weather the tumor is toxic
or not training a machine learning model according to the identification of tumour can be of
great help.

PROBLEM STATEMENT & DISCUSSION

Breast Cancer is one of the leading cancers developed in many countries including India. Though
the endurance rate is high – with early diagnosis 97% women can survive for more than 5 years.
Statistically, the death toll due to this disease has increased drastically in last few decades. The
main issue pertaining to its cure is early recognition. Hence, apart from medicinal solutions some Data
Science solution needs to be integrated for resolving the death causing issue.
1)This analysis aims to observe which features are most helpful in predicting malignant or benign
cancer
2)See general trends that may aid us in model selection and hyper parameter selection.
3)The goal is to classify whether the breast cancer is benign or malignant.
4) To achieve this, I have used machine learning classification methods to fit a function that can
predict the discrete class of new input.

Dataset and Data Description:

The Breast Cancer data used in this study were obtained from the Kaggle, The
dataset used in this story is publicly available and was created by Dr. William H. Wolberg,
physician at the University Of Wisconsin Hospital at Madison, Wisconsin, USA. To create the

dataset Dr. Wolberg used fluid samples, taken from patients with solid breast masses and an easy-
to-use graphical computer program called Xcyt, which is capable of perform the analysis of

cytological features based on a digital scan. The program uses a curve-fitting algorithm, to compute
ten features from each one of the cells in the sample, than it calculates the mean value, extreme
value and standard error of each feature for the image, returning a 30 real-valuated vector

➢ Variables/ Features Information:
1. ID number
2. Diagnosis (M = malignant, B = benign) 3–32)

Ten real-valued features are computed for each cell nucleus:

1. radius (mean of distances from center to points on the perimeter)
2. texture (standard deviation of gray-scale values)
3. perimeter
4. area
5. smoothness (local variation in radius lengths)
6. compactness (perimeter2 / area — 1.0)
7. concavity (severity of concave portions of the contour)
8. concave points (number of concave portions of the contour)
9. symmetry
10. fractal dimension (“coastline approximation” — 1)
The mean, standard error and “worst” or largest (mean of the three largest values) of these features were
computed for each image, resulting in 30 features. For instance, field 3 is Mean Radius, field 13 is Radius
SE, field 23 is Worst Radius.

Data Preprocessing:
Data preprocessing is indeed a critical step in the machine learning pipeline. It involves cleaning, transforming, and organizing the raw data to make it suitable for training machine learning models. In our study, we've mentioned some key steps in the data preprocessing process:
Handling Missing Values: 
Fortunately, in our dataset, there were no null or missing values. However, in real-world scenarios, dealing with missing values is a common challenge. Techniques like imputation or removing rows/columns with missing data can be employed.
Converting Labels to Categorical Variables: The "Diagnosis" variable, which is the label, was converted into categorical variables by classifying them into respective classes. This is typically done to ensure the machine learning model treats the labels as discrete categories rather than continuous values.

Feature Selection: Feature selection is the process of choosing the most relevant features from the available dataset. This step can help improve model performance and reduce overfitting by focusing only on the most important attributes.

Data Balancing: 
Unbalanced data is a common issue, especially in classification problems where one class has significantly more samples than the others. To address this, data balancing techniques are used to ensure that the model doesn't Favor the majority class and learns from all classes equally. Techniques like oversampling, under sampling, like using synthetic data generation methods (e.g., SMOTE - Synthetic Minority Over-sampling Technique) can be employed to achieve balanced data.
After data preprocessing, the resulting dataset will be more suitable for training a machine learning model, and the model's accuracy and efficiency are likely to improve. It is important to note that the specific data preprocessing techniques used may vary depending on the nature of the data and the machine learning task at hand.

Model Selection:
Model selection is the process of choosing the best machine learning model from a set of candidate models for a given training dataset. Sufficient data is essential for effective model selection, and the required data amount may be substantial, especially for complex problems.
In the ideal scenario, the dataset is split into training (80%) and test (20%) sets. Candidate models are trained on the training set and evaluated on a separate validation set. The model with the highest accuracy score on the validation set is selected as the final model. The performance of the chosen model is then assessed on the test set to provide an unbiased estimate of its effectiveness.
In this study, different machine learning models were assessed, and the "Logistic Regression" and "Decision Tree Classifier" models achieved the highest accuracy scores for classification. Consequently, the "Logistic Regression" model was chosen as the final model for classification.

Conclusion:

The statistical analysis indicates that certain factors, namely "area_mean," "concavity_worst," "radius_mean," "concavity_mean," "area_se," "perimeter_worst," "concave points_mean," "radius_worst," "concave points_worst," and "area_worst," outperformed other factors in predicting the diagnosis of breast cancer.
Using the Logistic Regression model, we achieved an accuracy of 96.50% in diagnosing breast cancer as Malignant or Benign. This accuracy rate showcases the model's effectiveness in classifying breast cancer cases.


