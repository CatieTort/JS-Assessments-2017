### Javascript Course Assessment

## Week 4 Assessment

Try your best to answer each question on your own before looking up the answer online. Once you're done writing your first answer, you can google the question and write the best answer you find.

#### 1. SQL stands for Structured Query Language. In your own words (no need to write a googled answer), what role does SQL play in a full-stack web application? How does this relate to MVC organization?

SQL is part of the Model layer in the MVC organization, the database that saves information for your app to use.

#### 2. Here is a basic SQL query. What are the various parts of this statement doing? (Comment the code to explain each piece)

     SELECT
      name,
      breed,
      vaccinations,
      age * 15 AS equivalent_human_age,
  //requesting a selection of the listed fields, age has an additional condition where is searches the values of equivalent_human_age and grabs any that have the value of 15
    FROM
  // this is the table where all the fields requested above are located  
      mydogs
    WHERE
      equivalent_human_age > 20
  //this is a condition that is requesting the query to select all the values greater than 20   
    ORDER BY
      equivalent_human_age DESC
  //this takes all the equivalent_human_age and sorts them in descending order  


#### 3. What is a foreign key?

// Your Answer: The foreign key is a unique identifier that is used to connect tables. In most cases the id of one table is the foreign key of another table.


// Googled Answer: A FOREIGN KEY is a key used to link two tables together.

A FOREIGN KEY is a field (or collection of fields) in one table that refers to the PRIMARY KEY in another table.

The table containing the foreign key is called the child table, and the table containing the candidate key is called the referenced or parent table.


#### 4. What is this Sequelize code doing? Comment the code to explain each piece.

    ComicBook
      .all({limit: 2})
    // this is taking the ComicBook table and limiting it to the first two rows  
      .then(function(comics){
      let mapped = comics.map(function(cb){
         return cb.get()
      })
  //the comics array (I know it's an array because of the .map() method) is put into a function that maps through the elements and returns them and saves it into the mapped variable.  
      console.log(mapped)
  //this will console.log the result of the function inside the mapped variable    
    })


 //Your Answer: Sequelize is Selecting 2 comics from the ComicBook table, each comic is an array and the comic is put into a variable that will display what is inside each array.


 //Googled Answer: Logs all the records in the ComicBook table but limits to 2 instances.


#### 5. Try to explain the role of an ORM in a full-stack application. Include at least two benefits of implementing an ORM.

//Your Answer: an ORM is the translator between the code that runs the business logic and the database. It is very helpful in a full-stack application because it allows you to have functions run using information from your database(s) or add new information to your database(s) based on the user interaction.


 //Googled Answer: Here are some advantages of ORM over traditional query approach:

Developers can only focus on business logic rather than writing interfaces between code and db.
Reduces development time and costs by avoiding redundant codes
Capable of connecting to different databases, which comes handy during switching from one db to the other.
Helps to effectively query from multiple tables similar to SQL JOIN—ORM takes the responsibility of converting the object-oriented query approach to SQL queries.

#### 6. Write a command to alter the TABLE water_monsters in the monster DATABASE to name it "sea_monsters" instead.(assume we are using a postgres database)

 //Your Answer: UPDATE monsters SET sea_monsters WHERE water_monsters


 //Googled Answer: ALTER TABLE water_monsters RENAME sea_monsters (my answer reset a field name)


 #### 7. What does CRUD stand for? And what do we use CRUD actions for?

 //Your Answer: CRUD stands for Create, Read, Update and Destroy. We use these actions within a database on the data and tables that are located there.


 //Googled Answer: In computer programming, create, read, update, and delete[1] (as an acronym CRUD) are the four basic functions of persistent storage.[2] Alternate words are sometimes used when defining the four basic functions of CRUD, such as retrieve instead of read, modify instead of update, or destroy instead of delete.

 The acronym CRUD refers to all of the major functions that are implemented in relational database applications. Each letter in the acronym can map to a standard SQL statement, HTTP method (this is typically used to build RESTful APIs[4]) or DDS operation


 #### 8. When working with Sequelize, how do we make changes on a table or database level? Give a code example along with your answer.

 You can use .create() then fill in all the fields with values for the new instance.

      let mouse = animal.create({
          code: 'blue',
          name: 'Frank',
          lastMeal: 'cheese'
        })
        .then(function(){
          return animal.save()
          })
          .catch(function(err){
          })

 #### 9. During the review we came across the idea of primitives types in Javascript but didn't really get to go into detail about them, other than the fact that they sometimes behave differently than objects and arrays. Do 5 min of research about primitives and record your findings here:

 //Googled Answer Except for null and undefined, all primitive values have object equivalents that wrap around the primitive values. You can run built-in methods on Number and String primitives.


#### 10. Friday's lesson was difficult because Sequelize updated its syntax. What did you think about this problem, and how might you deal with breaking updates like this in the future?


 //Your Answer: In a perfect world when Sequelize was updated they should have provided good docs to explain the changes. It was frustrating at times but going through the different error messages and trying different things as well as googling the error messages seemed to help some.


 //Googled Answer: Through the documentation of the new version implement the new syntax. Or revert to a previous version, altho that will stop working eventually.
