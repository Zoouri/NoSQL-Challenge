![Logo](ss/mongodb.png)

# NoSQL-Challenge :herb: :leaves:

*In this assignment, I will utilize my skills in MongoDB, import data, update the database, and perform exploratory analysis using Python and Jupyter Notebook.*


# Background

The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. You've been contracted by the editors of a food magazine, Eat Safe, Love, to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.

## Part 1: Database and Jupyter Notebook Set Up

### Import Data
The first step is to import the data provided in the `establishments.json` file into MongoDB. This is accomplished using the `mongoimport` command in the Terminal.

### Import Libraries
Once the data is imported, I imported the necessary libraries in our Jupyter Notebook. I imported `MongoClient` from PyMongo and `pprint` for pretty-printing.

### Create Mongo Client
Next, I created an instance of the MongoDB client using `MongoClient`. This allowed me to interact with the MongoDB server.

### Confirm Database and Data Loading
To ensure that the database and data were loaded properly, I listed the databases to confirm that `uk_food` is listed and then list the collections in the `uk_food` database to ensure that `establishments` is present. I also displayed one document from the `establishments` collection using `find_one` and `pprint`. Finally, I assigned the `establishments` collection to a variable for further use.

## Part 2: Update the Database

### Find and Update BusinessTypeID
The magazine editors have requested modifications to the database. I needed to find the `BusinessTypeID` for "Restaurant/Cafe/Canteen" and update a new restaurant, "Penang Flavours", with this `BusinessTypeID`.

### Remove Establishments from Dover
The magazine is not interested in any establishments in Dover, so I checked how many documents contained the Dover Local Authority. Then, I removed any establishments within the Dover Local Authority from the database and checked the number of documents to ensure they were deleted.

### Convert String Number Values
Some number values are stored as strings when they should be stored as numbers. I used `update_many` to convert latitude and longitude to decimal numbers and to convert `RatingValue` to integer numbers.

## Part 3: Exploratory Analysis

I used the provided `NoSQL_analysis_starter.ipynb` notebook for this section of the challenge. The notebook contains specific questions to answer, which will help provide insights for the magazine editors.

### Notes
I took into account some notes about the dataset, such as the meaning of `RatingValue` and the reverse nature of scores for Hygiene, Structural, and ConfidenceInManagement.

### Questions to Explore
I addressed specific questions provided in the notebook, such as identifying establishments with a hygiene score equal to 20, finding establishments in London with a `RatingValue` greater than or equal to 4, and so on.

### Instructions
For each question, I used `count_documents` to display the number of documents contained in the result, `pprint` to display the first document, and converted the result to a Pandas DataFrame to analyze the data further.


#### Technologies used
* Visual Studio Code 
* **MongoDB**
* **Python**


#### File list
* NoSQL_analysis.ipynb
* NoSQL_setup.ipynb
* css directory with styling
* Resources Folder containing required data
* Various Screen Shots in directory "ss"


Cover Photo Source: `https://www.google.com/imgres?q=mongodb%20logo&imgurl=https%3A%2F%2Fupload.wikimedia.org%2Fwikipedia%2Fcommons%2Fthumb%2F9%2F93%2FMongoDB_Logo.svg%2F2560px-MongoDB_Logo.svg.png&imgrefurl=https%3A%2F%2Fen.m.wikipedia.org%2Fwiki%2FFile%3AMongoDB_Logo.svg&docid=8ocQ0mdnMBW0JM&tbnid=8WhT_JV_5FLSuM&vet=12ahUKEwihwYjVpsGFAxWyyDgGHUAaAqcQM3oECBsQAA..i&w=2560&h=690&hcb=2&ved=2ahUKEwihwYjVpsGFAxWyyDgGHUAaAqcQM3oECBsQAA`