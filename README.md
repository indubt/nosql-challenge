# nosql-challenge
This repo contains Module 12 NOSQL Challenge Analysis.

Below steps are performed as requested. Repo contains 2 files 
1. NoSQL_setup.ipynb - contains the initial setup of mongo import, data clean up

    a. Import the data provided in the establishments.json file from your Terminal. Name the database uk_food and the collection establishments. Copy the text you used to import your data from your Terminal to a markdown cell in your notebook.

    b. Within your notebook, import the libraries you need: PyMongo and Pretty Print (pprint).

    c. Create an instance of the Mongo Client.

    d. Confirm that you created the database and loaded the data properly

    e. List the databases you have in MongoDB. Confirm that uk_food is listed.

    f. List the collection(s) in the database to ensure that establishments is there.

    g. Find and display one document in the establishments collection using find_one and display with pprint.

    h. Assign the establishments collection to a variable to prepare the collection for use.

    i. An exciting new halal restaurant just opened in Greenwich, but hasn't been rated yet. The magazine has asked you to include it in your analysis. Add the Penang Flavours information to the database.
    Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields.

    j. Update the new restaurant with the BusinessTypeID you found.
    k. The magazine is not interested in any establishments in Dover, so check how many documents contain the Dover Local Authority. Then, remove any establishments within the Dover Local Authority from the database, and check the number of documents to ensure they were deleted.

    l. Some of the number values are stored as strings, when they should be stored as numbers.

    m. Use update_many to convert latitude and longitude to decimal numbers.
    
    n. Use update_many to convert RatingValue to integer numbers.

2. NoSQL_analysis.ipynb - answers the questions asked in the challenge. The files are self explanatory.
    
Use the following questions to explore the database, and find the answers, so you can provide them to the magazine editors.

Unless otherwise stated, for each question:

    a. Use count_documents to display the number of documents contained in the result.

    b. Display the first document in the results using pprint.

    c. Convert the result to a Pandas DataFrame, print the number of rows in the DataFrame, and display the first 10 rows.

1. Which establishments have a hygiene score equal to 20?

2. Which establishments in London have a RatingValue greater than or equal to 4?

Hint: The London Local Authority has a longer name than "London" so you will need to use $regex as part of your search.

3. What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?

Hint: You will need to compare the geocode to find the nearest locations. Search within 0.01 degree on either side of the latitude and longitude.

4. How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.

Hint: You will need to use the aggregation method to answer this.



