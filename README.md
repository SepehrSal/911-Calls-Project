# 911-Calls-Project
 In this capstone project we will be analyzing some 911 call data from Kaggle.

Steps in this project:

* Data and Setup
* Exploratory Data Analysis (EDA)
* Creating new features
* Scatter plots on maps

# Data and Setup

For this  project we will be analyzing some 911 call data from [Kaggle](https://www.kaggle.com/mchirico/montcoalert)

# Exploratory Data Analysis (EDA)

* calculating the top 5 zipcodes
* calculating the top 5 townships
* unique title codes

# Creating new features

* using lambda and split to extraxt the reasons for calls.

* countplot of 911 calls by Reason
 

![countplot](https://user-images.githubusercontent.com/121250443/210860135-8c5aee16-61ba-4c3e-97ae-869464570ed6.png)

* Creating new attributes like day of week and hour from time stamp using map()

df['Day of Week'] = df['timeStamp'].apply(lambda time: time.dayofweek)
dmap = {0:'Mon',1:'Tue',2:'Wed',3:'Thu',4:'Fri',5:'Sat',6:'Sun'}
df['Day of Week']=df['Day of Week'].map(dmap)

* fill in some month missing information by plotting the information and groupby

![filling](https://user-images.githubusercontent.com/121250443/210861491-c8a9a262-26f9-42e2-b79e-b175fcb46690.png)

* creating heatmaps with seaborn and our data. We'll first need to restructure the dataframe so that the columns become the Hours and the Index becomes the Day of the Week

![heatmap](https://user-images.githubusercontent.com/121250443/210861789-45263402-8052-45ba-b95c-1ed3918dafdd.png)


# Scatter plots on maps

* plot out the location of calls for fire Reason using lng and lat data


![newplot (3)](https://user-images.githubusercontent.com/121250443/210862520-5a91066b-23d0-4d8d-ab98-01daca4a17ae.png)






