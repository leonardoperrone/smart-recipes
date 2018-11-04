# Smart Recipes

# Abstract
The main idea behind this project is to optimize the utilization of the ingredients present in one’s fridge. This is accomplished by analyzing recipes, as well as food facts, and establish a type of distance between products, indicating that we can use different food items to prepare the same recipe. Using this, from a given input of products available at home, the program could suggest recipes, including new recipes derived by replacing some ingredients not presented in the input set of ingredients, with other similar ingredients that might be available to the user. 
Another optional implementation on top of the original purpose could be to give the user the option to turn recipes into gluten-free, pork-free, etc, in order to meet an individual’s dietary restrictions.This would help people waste less food due to the possible combinations of ingredients that they might not be aware of and educates them in associating specific ingredientes with similar ones.

# Research questions
What are the popular ingredients in recipes?

What are the most similar ingredients that could be switched together?

Can the recepies be clustered according to the cuisine (ex: italian recipes would be clustered together) ? And how would this influence the replacement of ingredients?

How would different word embeddings help in learning the mappings among recipes? 
What is the distribution of the frequency of ingredient words present in the data? Can we fit a distribution ? Can this distribution be used to learn a mapping between the ingredients?



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
