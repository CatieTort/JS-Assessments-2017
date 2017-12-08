### Javascript Course Assessment

## Week 1 Assessment

Try your best to answer each question on your own before looking up the answer online. Once you're done writing your first answer, you can google the question and write the best answer you find.

#### 1. Name some of the data types in Javascript.

  //Your Answer: 
        Data types are strings, numbers, booleans, arrays and objects in JavaScript. 
  
  //Googled Answer: 
        The latest ECMAScript standard defines seven data types:

        Six data types that are primitives:
        Boolean
        Null
        Undefined
        Number
        String
        Symbol (new in ECMAScript 6)
        and Object



#### 2. Describe what "if" does in Javascript.

  //Your Answer: 
        if is part of a conditional statement usually found within a function or loop in JavaScript. It takes a condition and         checks if the condition is true or false. if statements are usually combined with an else statement but does not               require one. You can have multiple if statements with different conditions.

        Ex: if (x > 9){
          return x + " is greater than 9"
        }else if (x < 9){
          return x + " is less than 9"
        }...
  
  //Googled Answer: 
      The if/else statement executes a block of code if a specified condition is true. If the condition is false, another           block of code can be executed. 


#### 3. Write a function that takes one number as a parameter and decides if that number is divisble by three or not. If it is, print the number and "is divisible by three". If it is not, print that the number "is not divisble by three".

    function byThree (x){
      if (x % 3 > 0){
        return x + " is not divisible by three";
      }else if (x % 3 === 0){
        return x + " is divisible by three";
      }else{
        return x + " cannot be divided by three";
      }
    };


#### 4. What is JSON?

  //Your Answer: 
      JSON is an acronymn for JavaScript Object Notation
  
  
  //Googled Answer: 
  
      JSON: JavaScript Object Notation.

      JSON is a syntax for storing and exchanging data.

#### 5. Write about yourself in an object, giving at least three properties of you. Then store your object in a variable with your name.

      var Catie = { 
         hairColor: "brown",
         hobbies: ["hiking", "reading", "cooking"],
         age: 30
      };


#### 6. What is a closure?

  //Your Answer:
      A closure is a way to access and use a local-scope or block-scope variable without reassigning the value within the           variable's scope. It is usually used by creating an annonomyus function within a named function.
  
  //Googled Answer: 
      A closure is an inner function that has access to the outer (enclosing) function's variables—scope chain. The closure         has three scope chains: it has access to its own scope (variables defined between its curly brackets), it has access to       the outer function's variables, and it has access to the global variables.

#### 7. What's the difference between =, ==, and === in JavaScript?

  //Your Answer: 
  
  = assigns value to something
  == compares like values but isn't super strict  ex: 5 == "5" would be true. 
  === compares values and is VERY strict  ex: 5 === 5 is true, but 5 === "5" is false.
  
  //Googled Answer:
  = (assignment oporator)
  == (equal to value)
  === (equal to value & equal to type)
  

#### 8. Create an array with at least 4 items inside it, then access two of the values and console.log() them. Try to access the two values in two different ways.

    var letsGoTo = ["Spain", "Italy", "Germany", "Australia"];
    
    console.log(letsGoTo[3], letsGoTo[2]);
    
    var firstTrip = letsGoTo.slice(0,2);
    
    console.log(firstTrip);

#### 9. Describe the different kinds of loops and why you would use them.

  //Your Answer: There are 3 different types of loops in JavaScript, Do while, while, and for loops. Do while takes a condition to start a while loop then the 
  
  
  //Googled Answer
  
#### 10. How would you explain "scope" in javascript?

  //Your Answer
  
  
  //Googled Answer
