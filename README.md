# Smart Recipes

# Abstract

In this project we would like to see which components of a recipe affect most the sentiment of the users giving feedback on the recipe. Such factors may include  
- the time to prepare and cook the meal  
- the type of the cuisine  
- the level of difficulty of preparing the meal  
and many more. We would like to explore relationships between such features and maybe suggest for chefs ways of presenting a recipe to attract users and receive positive feedback, potentially including users who might not even attempted to prepare the recipe.


# Research questions

1) Does less preparation and cooking time result in a good review from users?
2) Does the level of healthiness attract people on preparing this meal or not?
3) How does the cuisine type reflect on the tendency of people trying this recepie ? (would people tend to try non-local food)
4) How does the effect of the first review on the remaining ones?
5) How does the sentiment of the users change over time regarding one recipe?
6) Do meals serving many people get a better review ?

# Dataset
For this project we will use the `Recipes` (https://stanford.io/2CVAwix) dataset. The dataset is in a HTML format so it will need to be parsed accordingly to extract the data. To make things more complicated, the dataset contains recipes from multiple websites, each of those having their own layout and formatting, which will require a different parsing logic for each. In order to simplify the task, but avoid losing too much valuable information, we are going to choose a number of websites which contain the most recipes. Focusing on the websites with the most recipes will also help to keep our analysis less prone to outliers, as we assume that those websites have greater and more diverse user base.

### Data
The `Recipes` dataset contains links to recipe pages. The recipes themselves consist of steps, ingredients and quantities of the ingredients needed. This information, once parsed, gives information about what ingredients compose the recipe, as well as other attributes which may influence the reviews, such as preparation time and difficulty. The websites also capture reviews posted by readers. Our ulimate goal is to find correlations between the recipe attributes and the number of good and bad reviews.

### Preprocessing:
1. Parse the html data
2. Extract recipe attributes and reviews
3. Find a common data format for all websites included in the study
4. Convert key attributes into a common format
5. Stem the extracted tokens

# Internal Milestones up to Project Milestone 2
- **Nov. 4th:** Deliver README with project details.
- **Nov. 11th:** Explore the recipe set and create a proper dataset by scraping the html pages.
- **Nov. 15th:** Have cleaned sets. Extract proper data from both and map ingredients to recipes.
- **Nov. 18th:** Obtain a set that is ready to be utilized for analysis.
- **Nov. 25th:** Create meaningful plots and visual summaries of the data.

# Questions for TA
None at the moment
