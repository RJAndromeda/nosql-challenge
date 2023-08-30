## Module 12 Challenge: noSQL

Created and submitted as Challenge 12 for Monash University Data Analytics Boot Camp (August 2023).

## Table of Contents

## Tasks 

Part 1: Database and Jupyter Notebook Set Up: 
Use NoSQL_setup_starter.ipynb for this section of the challenge. Import the data, requisite libraries, create instance of Mongo Client, confirm and check database, prepare collection for use. See Jupyter Notebook starter for full details of setup.

Part 2: Update the Database
Use NoSQL_setup_starter.ipynb for this section of the challenge. Modify the database before analysis, including adding new establishment, removing Dover restaurants, and updating fields as required. See Jupyter Notebook starter for full details of setup.

Updated record included for Penang Flavours:

![image-20230827151553651](C:\Users\rhian\AppData\Roaming\Typora\typora-user-images\image-20230827151553651.png)

Remove Dover establishments:

![image-20230830174941435](C:\Users\rhian\AppData\Roaming\Typora\typora-user-images\image-20230830174941435.png)



## Part 3:

**Find out the following: Which establishments have a hygiene score equal to 20?** 

There are 41 establishments with a hygiene score equal to 20. See jupyter notebook, analysis starter, for full results.

**Which establishments in London have a RatingValue greater than or equal to 4?** 

There are 33 establishments with a Rating value of 4 or more. See jupyter notebook, analysis starter, for full results.

**What are the top 5 establishments with a RatingValue of '5', sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?** 

The top 5 establishments near Penang Flavours are as follows - and it can be noted that none are restaurants :

![image-20230830175956478](C:\Users\rhian\AppData\Roaming\Typora\typora-user-images\image-20230830175956478.png)

**How many establishments in each Local Authority area have a hygiene score of 0?** 

A rather large number of establishments had hygiene scores of 0. 55 Local Authority areas had records in this group, with the worst performing 10 as follows:

![image-20230830175650368](C:\Users\rhian\AppData\Roaming\Typora\typora-user-images\image-20230830175650368.png)

See jupyter notebook for full code. 



## Comments & References 

In addition to course materials, I have also reviewed the MongoDB manual, StackOverflow and other general information sources for problem-solving for particular errors in my code. To ensure that the RatingValue was correctly coerced into integer, and that the latitude and longitude were also converted to numbers, I investigated various approaches. The final solution came about with reference to:  #starball's discussion in Stackoverflow of $type, was most useful for establishing the conversions of both latitude and longitude, in combination with requisite reference to the MongoDB type documentation. Converting to integer and coercing the non-numeric values final solution came from the MongoDB manual & forum (see code for marked section). With thanks to Hussam to pointing out that I should check the unique values to see what needed to be coerced.

https://stackoverflow.com/questions/4973095/how-to-change-the-type-of-a-field and https://www.mongodb.com/docs/manual/reference/operator/query/type/


https://www.mongodb.com/docs/manual/reference/operator/aggregation/toDecimal/

https://www.mongodb.com/docs/manual/reference/operator/aggregation/convert/



August 2023.

