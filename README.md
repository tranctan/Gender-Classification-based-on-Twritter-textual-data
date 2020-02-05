# Gender Classification based on Twitter Profile Data

<p align="center">
  <img width="460" height="300" src="https://seeklogo.com/images/T/twitter-logo-C591CF37A1-seeklogo.com.png">
</p>

This dataset is obtained from [Kaggle](https://www.kaggle.com/crowdflower/twitter-user-gender-classification).

As described:

The dataset contains 20,000 rows, each with a user name, a random tweet, account profile and image, location, and even link and sidebar color.

This data set was used to train a [CrowdFlower AI gender predictor](https://www.figure-eight.com/using-machine-learning-to-predict-gender/). You can read all about the project here. Contributors were asked to simply view a Twitter profile and judge whether the user was a male, a female, or a brand (non-individual). The dataset contains 20,000 rows, each with a user name, a random tweet, account profile and image, location, and even link and sidebar color.

Within this work, i implemented a notebook going through 5 steps:
1. Understanding Dataset
2. Cleaning Dataset
3. Visualizing Dataset
4. Classification Modeling

Regarding the scope, i mainly drop features and records that seemed not to contribute to the target, for simplicity. There are two main types of feautres within this dataset: Textual data (`text` and `description`) and non-textual data (other features including categorical and numerical type).

For textual data:
- I mainly cleaned it using regex and Python string methods.
- I employed TF-IDF as a transformation to represent the textual data as feature vectors for the models.
- I trained the models with only `text` feature at first, then concatenated `description` and re-trained the models. The result showed a significant improvments.

For non-textual data:
- I used label count encoding for categorical features (kudos to [wrosinski](https://wrosinski.github.io/fe_categorical_encoding/)), as their number unique values is huge, which is not represented well using ordinary one-hot encoding.
- All other numerical features are kept unchanged.

For more details, please reference the .ipynb file. Any comments or feedbacks are welcome I always love sharing knowledge and learning from you.