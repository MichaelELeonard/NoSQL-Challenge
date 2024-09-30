<img src="Pics/Header1.png" width="900" height="500">

# NoSQL Challenge

[NoSQL Challenge Setup Code Link]( https://github.com/MichaelELeonard/nosql-challenge/blob/main/NoSQL_setup_working.ipynb)

[NoSQL Challenge Analysis Code Link]( https://github.com/MichaelELeonard/nosql-challenge/blob/main/NoSQL_analysis_working.ipynb)

<br>

## The Scenario
The UK Food Standards Agency evaluates various establishments across the United Kingdom and gives them a food hygiene rating. We have been contracted by the editors of a food magazine, Eat Safe, Love, to evaluate some of the ratings data to help their journalists and food critics decide where to focus future articles.

### Part 1: Database and Jupyter Notebook Set Up 
A json file of data was imported using the mongoimport command: 

<img src="Pics/SetUp1.png" width="805" height="20">

An instance of the MongoClient was established and a print statement was used to confirm that the ‘uk_food’ database had been successfully imported and was available.  

<img src="Pics/SetUp4.png" width="767" height="37">


‘Establishments’ was identified as the only collection in the ‘uk_food’ database.

<img src="Pics/SetUp6.png" width="166" height="40">



### Part 2: Update the Database
A new document entry for the restaurant ‘Penang Flavours’ was added to the existing ‘establishments’ collection.  
 
<img src="Pics/Update2.png" width="572" height="383">



We then needed to establish which ‘BusinessTypeID’ should be assigned to the ‘Penang Flavours’ to update it correctly.  We accomplished this by finding out what ID other establishments were assigned of the same business type and updating the ‘BusinessTypeID’ for ‘Penang Flavours’ with that same ID to ensure consistency within the collection.  

<img src="Pics/Update3.png" width="361" height="75">
<img src="Pics/Update4.png" width="576" height="379">



We needed to establish how many documents (restaurants) in the collection there were from the Dover Local Authority and remove them from the DataBase.  The Dover establishments were counted and returned a total of 994.  The Dover establishments were deleted and confirmed, returning a count of 0. 

<img src="Pics/Update5.png" width="49" height="30">
<img src="Pics/Update6.png" width="421" height="40">
<img src="Pics/Update7.png" width="45" height="32">




We then needed to do some cleaning and updating of the database to prepare it for analysis.  The geocode.longitude & geocode.latitude variables were cast to doubles, any non 1-5  Rating Values to Null, and RatingValues were cast to intergers.  The first five results in the database were checked to ensure that the changes were implemented correctly.

<img src="Pics/Update8.png" width="581" height="294">


### Part 3: Exploratory Analysis
There were four questions that were examined by the analysis portion of the NoSQL-Challenge.  These four questions included:
* Which establishments have a hygiene score equal to 20?
* Which establishments in London have a “RatingValue” greater than or equal to 4?
* What are the top 5 establishments with a “RatingValue” rating value of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
* How many establishments in each Local Authority area have a hygiene score of 0?
 
### Which establishments have a hygiene score equal to 20?

<img src="Pics/Analysis1.png" width="334" height="39">


### Which establishments in London have a “RatingValue” greater than or equal to 4?

<img src="Pics/Analysis2.png" width="572" height="38">



### What are the top 5 establishments with a “RatingValue” rating value of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?

<img src="Pics/Analysis3.png" width="499" height="356">

### How many establishments in each Local Authority area have a hygiene score of 0?

<img src="Pics/Analysis4.png" width="232" height="39">


