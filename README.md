# Smart Recipes

# Abstract

In this project we would like to see which components of a recipe affect most the sentiment of the users giving feedback on the recipe. Such factors may include : the time to prepare and cook the meal, the type of the cuisine, the level of difficulty of preparing the meal and many more. We would like to explore relationships between such features and maybe suggest for chefs ways of presenting a recipe to attract users to give positive feedback. (People who may not be even trying recepie)


# Research questions

1) Does less preparation and cooking time result in a good review from users?
2) Does the level of healthiness attract people on preparing this meal or not?
3) How does the cuisine type reflect on the tendency of people trying this recepie ? (would people tend to try non-local food)
4) How does the effect of the first review on the remaining ones?
5) How does the sentiment of the users change over time regarding one recipe?
6) Do meals serving many people get a better review ?



# Dataset
For this project we will use the Recipes (https://stanford.io/2CVAwix) and Food Facts (https://bit.ly/2RtmPv4) dataset. The former dataset is in a HTML form so it will be parse accordingly to extract the needed data, while the latter dataset is in a CSV form which will enable the team to manipulate the data directly but storing the CSV file possibly into pandas DataFrames. 

The Recipes dataset contains many links to recipe pages. The recipes have steps, ingredients and quantities of the ingredients needed. This information, once parsed, gives information about what ingredients compose every recipe. The other set, as mentioned before, is about food facts and it contains more than 680k items. It has information about food items in several languages, so it will need to cleaned up and either be translated to english or filtered for english content. This is done so that both sets have the same spelling for the ingredients/food items.
More steps of the actual processing and ML models are provided below.

### Preprocessing:
1. Parse the html data
2. Extract tokens from the recipes
3. Stem the extracted tokens
4. Keep words that are food types (ex: fruits and vegetables ...) using wordnet (Named Entity Recognition)
5. Map the extracted ingredients into a list and give each recipe a unique id
6. Transform recipes into word embeddings
7. Visualizations: word clouds and bar plots

### Models:
1. Use k-mean clustering to cluster recipes together
2. Visualize the clusters, can be used as a metric to evaluate other models
3. Baseline model: K-Nearest Neighbour  
4. Latent semantic analysis
5. GloVe

**NOTE:** the previous models will use the word embeddings to learn a mapping to replace ingredients. We will use cosine-similarity and L2 norm of the embeddings to replace the vectors. 

### Evaluation:

This is a very difficult task as this task should be human understandable and requires human intervention. However what we propose is to use the clusters formed previously and see if the proposed ingredient belong to one cluster or not. 

# Internal Milestones up to Project Milestone 2

By:
- **Nov. 4th:** Deliver README with project details.
- **Nov. 11th:**  Identify useful data out of the food facts set. Explore the recipe set and create a proper dataset from the html pages (Step 1-2).
- **Nov. 15th:** Have cleaned sets. Extract proper data from both and map ingredients to recipes. (Step 3-5)
- **Nov. 18th:** Obtain a set that is ready to be utilized for analysis. (Step 6)
- **Nov. 24th:** Create meaningful plots and visual summaries of the data. (Step 7)



# Questions for TAa
//TODO
