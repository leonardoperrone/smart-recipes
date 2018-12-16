# Smart Recipes

# Abstract

In this project we would like to see which components of a recipe affect most the sentiment of the users giving feedback on the recipe. Such factors may include among others:  
- the time to prepare and cook the meal  
- the type of the cuisine  
- the level of difficulty of preparing the meal  

We are going to explore relationships between such features and suggest strategies of publishing a recipe in order to attract users and receive positive feedback, potentially including users who might not even attempted to prepare the recipe.


# Research questions

1) Does less preparation and cooking time result in a good review from users?
2) Does the level of healthiness attract people on preparing this meal or not?
3) How does the cuisine type reflect on the tendency of people trying this recepie ? (would people tend to try non-local food)
4) How does the effect of the first review on the remaining ones?
5) How does the sentiment of the users change over time regarding one recipe?
6) Do meals serving many people get a better review ?

# Dataset
For this project we will use the `Recipes` (https://stanford.io/2CVAwix) dataset. The dataset is in a HTML format so it will need to be parsed accordingly to extract the data. To make things more complicated, the dataset contains recipes from multiple websites, each of those having their own layout and formatting, which will require a different parsing logic for each. In order to simplify the task, but avoid losing too much valuable information, we are going to choose a number of websites which contain the most recipes. Focusing on the websites with the most recipes will also help to keep our analysis less prone to outliers, as we assume that those top websites have greater and more diverse user base.

### Data
The `Recipes` dataset contains links to recipe pages. The recipes themselves consist of steps, ingredients and quantities of the ingredients needed. This information, once parsed, gives information about what ingredients compose the recipe, as well as other attributes which may influence the reviews, such as preparation time and difficulty. The websites also capture reviews posted by readers. Our ulimate goal is to find correlations between the recipe attributes and the number of good and bad reviews.

### Preprocessing:
1. Parse the html data
2. Extract recipe attributes and reviews
3. Find a common data format for all websites included in the study
4. Convert key attributes into a common format
5. Text cleaning : tokenization , removal of stop words , lemmatization and converting into appropriate format for analysis

### Analysis: (Milestone 3)
The analysis will include a thorough study of the features against each other to see their effect on the sentiment of the user. The analysis will be focused on two parts:
1. Analyzing features that are extracted from the website including : cooking and preparation times of a meal,review posting dates , nutritional compostion of the meal ... The analysis will see the direct effect of these features on the sentiment of the users through different visualizations that will show both the them seperatley and combined together.
2. Analyzing the textual component of the reviews. This will help us labeling the datasets that don't have a rating as we can use fast-text to label the dataset. Also we can extract features such as the positive and negative words, the length of the review and the repetition of words in the reviews and use them with the features above to observe the infer the relation to the sentiment of the user.

# Directory structure:
There are two main notebooks :
1. Preprocessing.ipynb : contains initial attempt of cleaning the dataset. (SAME AS MILESTONE 2)
2. Smart Recipes.ipynb : contains the website scrapping procedure. (SAME AS MILESTONE 2)
3. Data_prep_augment.ipynb : Contains all the cleaning of the dataset and text processing of reviews and ingredients.
As well contains complenting the datasets using unsupervised learning. (NEW FOR MILESTONE 3)
4. analysis.ipynb : contains analysis of all features and correlations between these features and the sentiment of the users. (NEW FOR MILESTONE 3)

# Internal Milestones up to Project Milestone 2
- **Nov. 4th:** Deliver README with project details.
- **Nov. 11th:** Explore the recipe set and create a proper dataset by scraping the html pages.
- **Nov. 15th:** Have cleaned sets. Extract proper data from both and map ingredients to recipes.
- **Nov. 18th:** Obtain a set that is ready to be utilized for analysis.
- **Nov. 25th:** Create meaningful plots and visual summaries of the data.


# Differences between Milestone 2 and Milestone 3: (NEED TO GRADE)
A) All the updates below can be found under Data_prep_augment.ipynb :
1. Transforming ingredients into vector embeddings. Then clustering these embeddings to obtain a food class for each ingredient. Using the food classes as features, representing the ingredients of the recipe.
2. Using an average of word embeddings for user reviews on all recipe dataset. Then train a logistic regression model on those embeddings. Using this model to predict ratings for food.com dataset.
3. Unifiying the two datasets : All_recipe.com and Food.com

B) All the updates below can be found under analysis.ipynb :

1. Plots having relation between : cooking time , prepration time , nutrition compositon, ingredient compostion , and graph degree of ingredients linked together against recipe rating (denotes user's sentiment) 

C) Report:
a report summing up all the project

# Contributions:
1) Omar Mehio : web scrapers, data cleaning of all three datasets , feature engineering(word embeddings , kmeans clustering , logistic regression , unifying datasets) , analysis plots ( graph plots, prepration and cooking times plots, food composition plots )
2) Attila Bekker : report and intial analysis of the distributions of the data
3) Leonardo Perrone : analysis of nutrition composition and intial analysis of the distributions of the data


# Questions for TA
None at the moment
