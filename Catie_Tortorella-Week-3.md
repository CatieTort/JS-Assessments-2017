### Javascript Course Assessment

## Week 3 Assessment

Try your best to answer each question on your own before looking up the answer online. Once you're done writing your first answer, you can google the question and write the best answer you find.

#### 1. Here is a list of pros and cons to using the React library to build your application -- but some of them are false. Remove the false statements from the list:

- React is a modern, efficient answer to complex UI applications
- React is a flexible library that plays the role of V in an MVC framework


 #### 2. What are "smart" and "dumb" components? Explain the difference and also add why we bother to make the distinction between them.


 //Your Answer: Smart components are components that have code that does something, for example a Smart component could hold a function that checks if a user clicked on a button and display what change in state that should occur. Dumb components only display the JSX that is stated in the code.


 //Googled Answer: Dumb Components
Dumb components are also called ‘presentational’ components because their only responsibility is to present something to the DOM. Once that is done, the component is done with it. No keeping tabs on it, no checking in once in a while to see how things are going. Nope. Put the info on the page and move on.

The components themselves only have a render() method (they don’t need any others) and are often just Javascript functions. They don’t have internal state to manage. They wouldn’t know how to change the data they are presenting if they were asked. Ignorance is bliss.

Smart Components
Smart components (or container components) on the other hand have a different responsibility. Because they have the burden of being smart, they are the ones that keep track of state and care about how the app works.

Using the container design pattern, the container components are separated from the presentational components and each handles their own side of things. The container components do the heavy lifting and pass the data down to the presentational components as props.


#### 3. Write a simple component that simply prints "I am a dumb component" to the screen. Be sure to include all necessary imports, exports, etc...

import React, {Component} from 'react';

class Dummy extends Component {
  render (){
    return(
      <h1>I am a dumb component</h1>
      )
  }
}

export default Dummy


#### 4. When we use "yarn add ..." in the terminal - what is yarn doing? And what file will always be automatically updated after we add a package with yarn?


 //Your Answer: yarn add creates the node modules that are dependencies within the React app


 //Googled Answer: Installs a package and any packages that it depends on.
Adding dependencies
In general, a package is simply a folder with code and a package.json file that describes the contents. When you want to use another package, you first need to add it to your dependencies. This means running yarn add [package-name] to install it into your project.




#### 5. There are three mistakes in this code that would cause it to break our application. Find the mistakes and fix them:

    import React, { Component } from 'react';

    class Recipes extends Component {
      constructor(props){
        super(props)
        this.state = {
          recipes:
            {name: 'Meatballs'},
            {name: 'Mac & Cheese'}

        }
      }

        let recipes = this.state.recipes.map(function(recipe){
          return(
            <li key={recipe.name}>{recipe.name}</li>
          )
        })

      render() {

        return (

          <ul>
            {recipes}
          </ul>
        );
      }
    }

    export default Recipes;

#### 6. Name three input types. (NOTE: text is the default type - so it doesn't count in this case)

 //Your Answer: Number, image, button


 //Googled Answer: button, checkbox, color, date, datetime-local, email, file, hidden, image, month, number, password, radio, range, reset, search, submit, tel, time, url, week


 #### 7. How would you explain state to a friend who doesn't know code?

 //Your Answer: state is when you as a user does something to the page; click on a button or like a photo for example and something happens without the whole page changing.


 //Googled Answer: State commonly refers to either the present condition of a system or entity. That's pretty much what it means in a computing context: the data that defines the condition of some object or system.


 #### 8. What is the difference between component state and props? Your answer should include a short explanation of both.

    Component state is defined and lives in the app.js file it is the static state that it starts in. State can be changed but a function must be run in order to change the state.

    Props is the way that components outside of the app.js file can access the state within the app.js file. Once they can access the state they can run functions to change the state but it doesn't change the initial defined value.


 #### 9. Name three benefits of testing and TDD:


 //Your Answer: Test driven development is helpful because you can create tests that will make sure your code works and help you to make sure to add all elements a user will need to interact with your app. It also helps other developers able to understand what your code does based on the tests that you want it to pass.


 //Googled Answer: Focus: You're more productive while coding, and TDD helps keep that productivity high by narrowing your focus. You'll write one failing test, and focus solely on that to get it passing. It forces you to think about smaller chunks of functionality at a time rather than the application as a whole, and you can then incrementally build on a passing test, rather than trying to tackle the bigger picture from the get-go, which will probably result in more bugs, and therefore a longer development time.

Dependencies:
Will your new code have any dependencies? When writing your tests, you'll be able to mock these out without really worrying about what they are doing behind the scenes, which lets you focus on the logic within the class you're writing. An additional benefit is that the dependencies you mock would potentially be faster when running the tests, and not bring additional dependencies to your test suite, in the form of filesystems, networks, databases etc.

Fewer Bugs:
TDD results in more tests, which can often result in longer test run times. However, with better code coverage, you save time down the line that would be spent fixing bugs that have popped up and need time to figure out. This is not to say that you might be able to think of every test case, but if a bug does come up, you can still write a test first before attempting to fix the problem, to ensure that the bug won't come up again. This also helps define what the bug actually is, as you always need reproducible steps.


#### 10. List two helpful testing matchers and two helpful enzyme simulators that we can use when writing our tests:


 //Your Answer: expect and .toEqual() are both helpful matchers in Jest. expect tells jest what to look for usually a variable that you define in the test and .toEqual() sets what the expect should equal in your code.

 enzyme allows us to mount our code and run the tests a helpful simulator would be click, hover or input which will simulate events that happen on the page so we can run more realistic tests.


 //Googled Answer:  

 The simplest way to test a value is with exact equality.

test('two plus two is four', () => {
  expect(2 + 2).toBe(4);
});

In this code, expect(2 + 2) returns an "expectation" object. You typically won't do much with these expectation objects except call matchers on them. In this code, .toBe(4) is the matcher. When Jest runs, it tracks all the failing matchers so that it can print out nice error messages for you.

If you want to check the value of an object, use toEqual instead:

test('object assignment', () => {
  const data = {one: 1};
  data['two'] = 2;
  expect(data).toEqual({one: 1, two: 2});
});
toEqual recursively checks every field of an object or array.

Enzyme simulate: https://github.com/airbnb/enzyme/blob/master/docs/api/ShallowWrapper/simulate.md
