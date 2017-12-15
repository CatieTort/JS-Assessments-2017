### Javascript Course Assessment

## Week 2 Assessment

Try your best to answer each question on your own before looking up the answer online. Once you're done writing your first answer, you can google the question and write the best answer you find.

#### 1. How do you link a css file to your html page?

 //Your Answer: In the head of your HTML file you need to put the code below to link your css file to your HTML.

 <link type="text/css" rel="stylesheet" href="filename.css">
 //type is the file type, rel is always stylesheet when referring to //css and then href is where to find the css file.

 //Googled Answer: To start with, open up your html document in Sublime Text. In the header section, add: <link rel="stylesheet" type="text/css" href="PATHTOCSSHERE">. You want to change "PATHTOCSSHERE" with the path to the css file you are trying to link the html page to.


 #### 2. What is a css class? How do you use declare one in html? How do you use it in css?


 //Your Answer: A css class is a way to specifically assign styles to parts of your HTML using a . and followed by a unique name. A class can be used multiple times. To declare a class in HTML inside the div tag or any tag that you are applying the class to you will need to put class="classname". In the css file you can use it to change any fonts, alignments, colors, backgrounds, borders etc. to the tag that is is declared in.

 //Googled Answer: In the CSS, a class selector is a name preceded by a full stop (“.”) You can also specify that only specific HTML elements should be affected by a class. To do this, start with the element name, then write the period (.) character, followed by the name of the class. HTML elements can also refer to more than one class.

 Ex: //in CSS
 .hometown {
    background-color: yellow;
}

//in html
<p class="hometown">This paragraph refers to two classes.</p>


#### 3. The class "heading-box" exists in our html file - write the css code that would:
  .heading-box{
##### 1) align this box to the center of its container,
      align-items: center;
##### 2) give it a black border that is 5px wide,
      border: solid black 5px;
##### 3) make its text appear in the center of the box
      text-align: center;
}

#### 4. What is Bootstrap? Explain a few reasons that you might choose to use it in a project?


 //Your Answer: Bootstrap is a css library that we can use in a project so that we do not need to code all of our css from scratch. It helps with nav bars, buttons, layout etc.


 //Googled Answer: Bootstrap is a free front-end framework for faster and easier web development. Bootstrap includes HTML and CSS based design templates for typography, forms, buttons, tables, navigation, modals, image carousels and many other, as well as optional JavaScript plugins.


#### 5. Name 4 semantic html tags.
<div></div> divider tag
<p></p> paragraph tag
<h1></h1> header type 1 tag
<a></a> anchor tag usually seen holding an href

#### 6. What is block scope that became available in ES6? Include how it differs from local and global scope, and what variables are block scoped.

 //Your Answer: block scope is when a function or variable is only available within the "block" of code. It is the same idea as local scope where the information is protected from other functions or variables changing the value, usually wrapped in a function.


 //Googled Answer: A variable can be either of global or local scope. A global variable is a variable declared in the main body of the source code, outside all functions, while a local variable is one declared within the body of a function or a block. Modern versions allow nested lexical scoping.

 #### 7. What is front end development? Can you identify any tools/skills that are uniquely required of front end developers?

 //Your Answer: Front end development is any coding/design that deals with the viewer/client side of the application you are making. Some skills that they need are ability to work with and write HTML, CSS, JavaScript, work with frameworks like Bootstrap and React, pull specific information from APIs to display on the page for users. They do not maintain servers and databases.


 //Googled Answer: A front-end web developer is responsible for implementing visual elements that users see and interact with in a web application.


 #### 8. Choose one of the new ES6 concepts we learned about this week (namely: block scope, classes, and string interpolation) and write example code that demonstrates the concept, with comments to explain what is going on.

 class Treehouse extends Backyard {
//A new class of Treehouse has been created that extends the //attributes of the class Backyard   
     constructor(){
  //constructor is a built-in function that is in all classes     
       super()
      //super is also a built-in function that allows us to add new //attributes to a class that extends another's attributes
       this.rooms = 2
       this.ropeSwing = true
       this.boysAllowed = false
       //this is referring to the Treehouse class and we have added //3 attributes that states there are 2 rooms, a rope swing //and no boys are allowed.
     }
 };

 var girlsOnly = new Treehouse()
//this var is allowing us to use the class in the rest of the application.

 #### 9. What is the difference between a div and a span?


 //Your Answer: div is a tag that creates a container to hold other tags or code can be any size and can be nested. A span tag is used in line elements of html and is used to apply something to what is inside the tag.


 //Googled Answer: The difference between span and div is that a span element is in-line and usually used for a small chunk of HTML inside a line (such as inside a paragraph) whereas a div (division) element is block-line (which is basically equivalent to having a line-break before and after it) and used to group larger chunks of code.

#### 10. How would you explain the idea of "inheritance" in object oriented programming?


 //Your Answer: Inheritance is in connection to classes where the attributes of the parent class are inherited by the child classes.

 //Googled Answer: Inheritance enables new classes to receive—or inherit—the properties and methods of existing classes.
