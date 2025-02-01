'use strict';
//in JavaScript, we can actually select this Element based on this class.
//class name likhlei element ta select hoye jay
/*
console.log(document.querySelector('.message').textContent);
document.querySelector('.message').textContent = '🎉 Correct Number!';
//if it was an ID instead of a class, we would use the #
// use the . if it is a class
//this querySelector is basically a method that's available on the document object .
//result of querySelector is an element.
//first select the Element then on that Element,
we can read the textContent property.
And so that's why we use another . here
and remember when we have multiple . operators,
they are executed from left to right.
/// .querySelector dile pura element tai print hobe ar .textContent hocche text ta print hobe!
amra querySelector dile message class tha ke acces korsi than textContent use kore text takeh access korsi.

// structure: document.queryselector('.className').textContent
//DOM stands for Document Object Model, and it is,
basically, a structured representation of HTML documents.
The DOM allows us to use JavaScript to access HTML elements
and styles in order to manipulate them.
//we will be able to change text,  change HTML attributes and also change
CSS styles from our JavaScript.
////So we can say that DOM is basically a CONNECTION POINT
between HTML documents and JavaScript code.
//Now, the DOM is automatically created by the browser as soon as the HTML page loads.
//it's stored in a tree structure ,each HTML element is one object.


//document is a special object that we have access to, in JavaScript 
this object serves as an entry point into the DOM.
-the query selector method is available on the document object.
-the first child element of document is usually the HTML element, because that's 
usually the root element in all HTML documents
-html er child HEAD, BODY
-head er child title
-body er child section, section child p element. eigula shob element 
- a Dom tree actually has more than just element nodes.
It also has nodes for all the text itself,
comments and other stuff, because basically the rule is that
whatever is in the HTML document also has to be in the DOM.
-the DOM really is a complete representation of the HTML document
-DOM ARE NOT PART OF JAVASCRIPT.
-the DOM and DOM methods
are actually part of something called the web APIs,Application Programming Interface. 

So the web APIs are like libraries that browsers implement
and that we can access from our JavaScript code


///////Selecting and Manipulating Elements
SETTING text
document.querySelector('.message').textContent = '🎉 Correct Number!';
//span is an HTML tag used to group and apply styles to inline-level element

document.querySelector('.number').textContent = 13;
document.querySelector('.score').textContent = 10;
//with an input field,to get the actual value,we use the value property.
document.querySelector('.guess').value = 23;
console.log(document.querySelector('.guess').value);





*/

let secretNumber = Math.trunc(Math.random() * 20) + 1;
let score = 20;
let highscore = 0;

const displayMessage = function (message) {
  document.querySelector('.message').textContent = message;
};

document.querySelector('.check').addEventListener('click', function () {
  const guess = Number(document.querySelector('.guess').value);
  console.log(guess, typeof guess);

  // When there is no input
  if (!guess) {
    // document.querySelector('.message').textContent = '⛔️ No number!';
    displayMessage('⛔️ No number!');

    // When player wins
  } else if (guess === secretNumber) {
    // document.querySelector('.message').textContent = '🎉 Correct Number!';
    displayMessage('🎉 Correct Number!');
    document.querySelector('.number').textContent = secretNumber;

    document.querySelector('body').style.backgroundColor = '#60b347';
    document.querySelector('.number').style.width = '30rem';

    if (score > highscore) {
      highscore = score;
      document.querySelector('.highscore').textContent = highscore;
    }

    // When guess is wrong
  } else if (guess !== secretNumber) {
    if (score > 1) {
      // document.querySelector('.message').textContent =
      // guess > secretNumber ? '📈 Too high!' : '📉 Too low!';
      displayMessage(guess > secretNumber ? '📈 Too high!' : '📉 Too low!');
      score--;
      document.querySelector('.score').textContent = score;
    } else {
      // document.querySelector('.message').textContent = '💥 You lost the game!';
      displayMessage('💥 You lost the game!');
      document.querySelector('.score').textContent = 0;
    }
  }

  //   // When guess is too high
  // } else if (guess > secretNumber) {
  //   if (score > 1) {
  //     document.querySelector('.message').textContent = '📈 Too high!';
  //     score--;
  //     document.querySelector('.score').textContent = score;
  //   } else {
  //     document.querySelector('.message').textContent = '💥 You lost the game!';
  //     document.querySelector('.score').textContent = 0;
  //   }

  //   // When guess is too low
  // } else if (guess < secretNumber) {
  //   if (score > 1) {
  //     document.querySelector('.message').textContent = '📉 Too low!';
  //     score--;
  //     document.querySelector('.score').textContent = score;
  //   } else {
  //     document.querySelector('.message').textContent = '💥 You lost the game!';
  //     document.querySelector('.score').textContent = 0;
  //   }
  // }
});

document.querySelector('.again').addEventListener('click', function () {
  score = 20;
  secretNumber = Math.trunc(Math.random() * 20) + 1;

  // document.querySelector('.message').textContent = 'Start guessing...';
  displayMessage('Start guessing...');
  document.querySelector('.score').textContent = score;
  document.querySelector('.number').textContent = '?';
  document.querySelector('.guess').value = '';

  document.querySelector('body').style.backgroundColor = '#222';
  document.querySelector('.number').style.width = '15rem';
});

///////////////////////////////////////
// Coding Challenge #1

/* 
Implement a game rest functionality, so that the player can make a new guess! Here is how:

1. Select the element with the 'again' class and attach a click event handler
2. In the handler function, restore initial values of the score and secretNumber variables
3. Restore the initial conditions of the message, number, score and guess input field
4. Also restore the original background color (#222) and number width (15rem)

GOOD LUCK 😀
*/
