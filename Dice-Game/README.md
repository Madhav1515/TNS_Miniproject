# Dice-Game
This simple web application generates two random dice rolls for two players and determines the winner based on the higher dice value. It's a fun and interactive way to simulate a dice game between two players.

Open the index.html file in a web browser.

Enjoy the dice game! Each time you refresh the page, it will generate new random dice rolls and display the winner.

Code Overview
The JavaScript code in script.js handles the logic for generating random dice rolls, updating the dice images, and determining the winner. Here's a brief overview:

### javascript
// Generate a random number between 1 and 6 for Player 1
var randomNumber1 = Math.floor(Math.random() * 6) + 1;

// Create the file path for the corresponding dice image
var randomDiceImage = "dice" + randomNumber1 + ".png";
var randomImageSource = "images/" + randomDiceImage;

// Update the first dice image on the web page
document.querySelectorAll("img")[0].setAttribute("src", randomImageSource);

// Generate a random number between 1 and 6 for Player 2
var randomNumber2 = Math.floor(Math.random() * 6) + 1;

// Create the file path for the corresponding dice image for Player 2
var randomImageSource2 = "images/dice" + randomNumber2 + ".png";

// Update the second dice image on the web page
document.querySelectorAll("img")[1].setAttribute("src", randomImageSource2);

// Determine the winner based on the dice rolls
if (randomNumber1 > randomNumber2) {
  document.querySelector("h1").innerHTML = "🚩 Player 1 Wins!";
} else if (randomNumber2 > randomNumber1) {
  document.querySelector("h1").innerHTML = "Player 2 Wins! 🚩";
} else {
  document.querySelector("h1").innerHTML = "Draw!";
}
