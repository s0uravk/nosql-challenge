# nosql-challenge

![no-sql-image](https://bairesdev.mo.cloudinary.net/blog/2021/06/nosql.jpg)

The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. I've been contracted by the editors of a food magazine, Eat Safe, Love, to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.

Part 1: Database and Jupyter Notebook Set Up and Update the Database.
Used 'NoSQL_setup_starter.ipynb' for this section of the challenge. This section emphasizes CRUD (Create, Update, Read, Delete)operations in NoSQL  using the Python library Pymongo.

This script imports the data from the establishment.json file in the Resources folder. Then, it creates a connection with the MongoDB server running on the local machine. Data is then shown from the collection named 'establishments' in Database 'uk_food'. Then it inserts an item into the table using the insert query and then checks if the item is inserted into the collection. The next query shows the selected fields from a document where a field has a specified value. Then, a field is been updated for the newly added document using the $set statement. Then the the query finds all the documents having the LocalAuthorityName field with the value 'Dover' and deletes all those documents. Then, it changes the datatype of longitude and latitude to Double. Furthermore, the 'RatingValue' field is set to None if the value is a string in a specified list, which is then set to datatype int and the final result is printed using pprint statement.

Part 2: Exploratory Analysis.
Use NoSQL_analysis_starter.ipynb for this section of the challenge. This section emphasizes fetching the data based on some criteria and converting it into Pandas Dataframes.

To begin with, a connection is made with the MongoDB database, and establishment collection is used in the uk_food database. First, the query retrieves establishments having a hygiene score equal to 20, which then gets converted into pandas dataframe. For the second dataframe, documents with the 'LocalAuthorityName' field containing 'London' in its values who has 'RatingValue' greater than or equal to 4 are fetched. Moving forward, data is retrieved for the top 5 establishments with a RatingValue rating value of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours" and converted into a dataframe. And for the final dataframe, the number of establishments in each Local Authority area has a hygiene score of 0.
