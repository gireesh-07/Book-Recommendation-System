# **Book-Recommendation-System**
## **Introduction**
With an increasing amount of information on the internet and a considerable increase in the number of users, it is essential for companies to search, map, and offer relevant information based on the preferences of users. An important functional means of providing personalized service to users is Recommendation System. This system uses algorithms and data analysis techniques to suggest items,content, or services that should be of interest to customers based on their past choices or by analyzing the preferences of similar users. They recommend the products which are currently trending or highly rated and they can also recommend the products which bring maximum profit to the company.
## **Objective**
The main objective of this project is to create a Book recommendation system that predicts best user interests and recommend the suitable/appropriate books to them, using various approaches. This would help us in providing better recommendation item to a right specific user.
## **Dataset Information**
We have three dataset:
### **Books**
- ISBN: International Standard Book Number unique to each edition of the book
- Book-Title: Title of the book
- Book-Author: Author of the book(incase of several authors only the first is provided)
- Year-of-Publication: The year in which the particular edition of the book was published
- Publisher:Name of the Book Publishing company
- Image-URL-S: URL link to a small version of the book cover displayed on the Amazon website
- Image-URL-M: URL link to Medium version image of the book cover displayed on the Amazon website
- Image-URL-L: URL link to Large sized image of the book cover displayed on the Amazon website
### **Ratings**
- User-ID: as mentioned above
- ISBN: as mentioned above
- Book-Rating: The rating given by the user (identified by User-ID) for the book (identified by ISBN). It is either explicit,expressed on a scale from 1-10 (higher values denoting higher appreciation), or implicit,expressed by 0
### **Users**
- User-ID: A unique identification number for each user
- Location:It contains city,state and country to which the user belongs ,separated by commas
- Age:The age of the user
## **Steps Involved**
- *Data Preprocessing*: This step basically includes data cleaning and feature engineering. Checked for null values, duplicates and dropped them. As some years seemed to be odd in 'Year of Publication' column, replaced them with null values and imputed them with mode. Also replaced all the null values with median for 'Age' column.
- *Merging of datasets*: In this project, recommender systems were built utilizing only explicit ratings (only the rated books obtained from both books and ratings dataset collectively). So finally, a new dataframe by merging the books dataset ,explicit ratings dataset and users dataset.
- *Feature Extraction*: Created new columns such as 'age_group' by binning the 'Age' column into 4 groups and extracted the country name from the 'Location' column. Also added new columns 'Average Rating' and 'Total no. of users rated for the book' for further understanding and calculation.
- *Exploratory Data Analysis*: Performed univariate analysis on numeric and categorical features and recorded the top findings.
- *Implementation of various Recommender System approaches*
## **Approaches Used**
1. **Popularity Based recommendation system**:  <br>
Used the Weighted average rating approach to get the top books.
2. **Collaborative Filtering Based recommendation system**: <br>
Used the Memory Based approach - KNN and Cosine Similarity
## **Conclusion**
- Harlequin is the top most publisher that has published most number of books, followed by Silhouette. We can observe Harlequin publisher's marking better performance than any other publishers
- Most number of books are published in the year 2002 because this value is imputed ad mode
- In explicit ratings, most of the users rated 8 for books
- "The Lovely Bones: A novel" is the top rated book among all the books. But this is not based on some recommendation system as they are top 10 books as per ratings
- Most of the users are 'Youth' category i.e, aged between 15 and 35
- The book Harry Potter and the Goblet of Fire (Book 4) is the top recommended book according to Popularity Based recommendation system
- Model built using collaborative filtering technique with cosine similarity has been observed to be performing better than other two models
