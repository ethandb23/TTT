 <h1>Tic Tac Toe App</h1>
    <p>This was a project that involved building a tic tac toe app using HTML, CSS, and JavaScript. This project was completed as part of my coursework in web development during General Assembly's Software Engineering Immersive course and allowed me to practice my skills in front-end development. The app features a user-friendly interface with customizable player names and icons, as well as sound effects triggered by moves and winning the game. Overall, this project was a great way to gain hands-on experience with front-end development and allowed me to apply the concepts and skills I learned in class to a real-world project.</p>

<h2>Getting Started</h2>
<p>Clone the GitHub repository to your local machine by executing the following command in your terminal:</p>
<pre><code>git clone https://github.com/ethandb23/TTT</code></pre>
<p>Open the project folder in your preferred code editor. You can use any code editor such as Visual Studio Code, Atom, or Sublime Text.</p>
<p>Install any necessary dependencies by running the following command in your terminal:</p>
<pre><code>npm install</code></pre>
<p>This will install any required packages and dependencies required to run the project.</p>
<p>To build and start the application, run the following command in your terminal:</p>
<pre><code>npm start</code></pre>
<p>This will compile the code and start a local server at <a href="http://localhost:3000/">http://localhost:3000/</a>.</p>
<p>Finally, open your preferred web browser and navigate to <a href="http://localhost:3000/">http://localhost:3000/</a>. This will open the index.html file and display the application.</p>

<h2>About the Project</h2>
<p>This was a solo project completed during a 1-week sprint.</p>
<h3>Technologies Used</h3>
<ul>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
  <li>Node</li>
  <li>CodePen</li>
</ul>

<h3>Big Goals</h3>
<ul>
  <li>Build a web application from scratch, without a starter codebase</li>
  <li>Use your programming skills to work out the game logic for a simple game like Tic Tac Toe</li>
  <li>Separate HTML, CSS, and JavaScript files in your application</li>
  <li>Build an application to a specification that someone else gives you</li>
  <li>Build a dynamic game that allows two players to compete from the same computer</li>
  <li>Craft a README.md file that explains your app to the world</li>
</ul>

<ul>
  <li>Render a game board in the browser</li>
  <li>Switch turns between X and O (or whichever markers you select)</li>
  <li>Visually display which side won if a player gets three in a row, or show a draw if neither player wins</li>
  <li>Include separate HTML / CSS / JavaScript files</li>
  <li>Stick with KISS (Keep It Simple Stupid) and DRY (Don't Repeat Yourself) principles</li>
  <li>Use JavaScript for DOM manipulation</li>
  <li>Deploy your game online, where the rest of the world can access it</li>
  <li>You can use GitHub Pages for deploying your project</li>
  <li>Use semantic markup for HTML and CSS (adhere to best practices)</li>
  <li>Have well-formatted, and well-commented code</li>
</ul>

<p>User Stories:</p>

<ul>
  <li>As a user, I should be able to start a new tic tac toe game</li>
  <li>As a user, I should be able to click on a square to add X first and then O, and so on</li>
  <li>As a user, I should be shown a message after each turn for if I win, lose, tie or who's turn it is next</li>
  <li>As a user, I should not be able to click the same square twice</li>
  <li>As a user, I should be shown a message when I win, lose or tie</li>
  <li>As a user, I should not be able to continue playing once I win, lose, or tie</li>
  <li>As a user, I should be able to play the game again without refreshing the page</li>
</ul>

<p>Potential Extra Tic Tac Toe Features:</p>

<ul>
  <li>Keep track of multiple game rounds with a win, lose and tie counter</li>
  <li>Allow players to customize their tokens (X, O, name, picture, etc)</li>
  <li>Use localStorage to persist data locally to allow games to continue after page refresh or loss of internet connectivity</li>
  <li>Involve Audio in your game</li>
  <li>Create an AI opponent: teach JavaScript to play an unbeatable game against you</li>
  <li>Make your site fully responsive so that it is playable from a mobile phone</li>
  <li>Get inventive with your styling e.g. use hover effects or animations</li>
  <li>Allow 2 players to play online with each other using any means such as WebSockets, Firebase, or other 3rd-party services.</li>
</ul>



<h2>Planning</h2>
 
 
 <p>The planning stage for this was simple, as Tic Tac Toe is a very commonly known game. I did not require any sketches or wireframes in order to visualize the game board. I am an experienced tic-tac-toe player and had no problem imagining a board to begin with. I decided that functionality would be my initial focus. However, I did start with some basic pseudocode:</p>
    
    

 // Define the game board as a 2D array of empty squares
let board = [
  ['', '', ''],
  ['', '', ''],
  ['', '', '']
];





// Define the current player as X
let currentPlayer = 'X';





// Define a function to check if a player has won the game
function checkWin(player) {



// Check rows
  for (let row = 0; row < 3; row++) {
    if (board[row][0] === player && board[row][1] === player && board[row][2] === player) {
      return true;
    }
  }




// Check columns
  for (let col = 0; col < 3; col++) {
    if (board[0][col] === player && board[1][col] === player && board[2][col] === player) {
      return true;
    }
  }




// Check diagonals
  if (board[0][0] === player && board[1][1] === player && board[2][2] === player) {
    return true;
  }
  if (board[0][2] === player && board[1][1] === player && board[2][0] === player) {
    return true;
  }





  // If no winning condition is met, return false
  return false;
}



// Define a function to make a move on the board
function makeMove(row, col, player) {
 


// Check if the square is empty
  if (board[row][col] === '') {
  
  
  
// Set the square to the player's mark
    board[row][col] = player;
    


// Check if the player has won
    if (checkWin(player)) {
      console.log(player + ' wins!');
    } else {
      

// Switch to the other player
      currentPlayer = (currentPlayer === 'X') ? 'O' : 'X';
    }
  } else {
    console.log('That square is already taken!');
  }
}



// Start the game loop
    while (true) {
// Display the current board state
  console.log(board);


  
// Ask the current player to make a move
  let row = prompt('Enter row (0-2) for ' + currentPlayer + ':');
  let col = prompt('Enter column (0-2) for ' + currentPlayer + ':');
  </p>








<p>The callback parameter is assigned to the this.callback property, which means that it will be accessible as an instance property of the TicTacToe object.</p>
<p>Finally, an object called scores is created with two properties, X and O, both set to 0. This object will be used to keep track of the score of each player throughout the game.</p>



<h2>Code</h2>
<p>The first parameter, placeholder, is a reference to an HTML element that will serve as the container for the Tic Tac Toe game.</p>
<p>The second parameter, grid_size, is an integer value that represents the size of the grid to be used in the Tic Tac Toe game. This value will determine the number of rows and columns that will be used to construct the game board.</p>
<p>The third parameter, callback, is a function that will be called after each turn in the game. This function will receive information about the current state of the game as its argument.</p>

<pre><code>
TicTacToe.prototype.empty = function() {
    for(var i = 0; i < this.columns.length; i++) {
        this.columns[i].innerHTML = '';
        this.columns[i].classList.remove(this.marks.X);
        this.columns[i].classList.remove(this.marks.O);
    }
    this.marks.count = 0;
};
</code></pre>

<p>Inside the TicTacToe function, the this.placeholder property is set to the placeholder parameter, which means that the placeholder element will be accessible as an instance property of the TicTacToe object.</p>

<pre><code>
TicTacToe.prototype.reset = function() {
    this.empty();
    this.scores = {
        X: 0,
        O: 0
    };
};
</code></pre>




<p>The paint method is called on the object, passing in the grid_size parameter as an argument. This method will generate the HTML and CSS needed to construct the game board inside the placeholder element.</p>

<pre><code>
var placeholder = document.getElementById("placeholder");

var tictactoe = new TicTacToe(placeholder, 3, onResult);

function onResult(result, scores) {
    if(result == 'draw') {
        alert("It's a draw!");
    } else {
        alert(result + " wins!");
        updateScores(scores.X, scores.O);
    }
    tictactoe.empty();
}

function updateScores(X, O) {
    document.querySelector("#scoreboard #player1").innerHTML = X;
    document.querySelector("#scoreboard #player2").innerHTML = O;    
}

function restart(grid_size) {
    tictactoe.reset();
    updateScores(0, 0);
    if(grid_size) {
        tictactoe.paint(grid_size);
    }
}
</code></pre>


<p>The callback parameter is assigned to the this.callback property, which means that it will be accessible as an instance property of the TicTacToe object.</p>
<p>Finally, an object called scores is created with two properties, X and O, both set to 0. This object will be used to keep track of the score of each player throughout the game.</p>


<h2>Function Explanation</h2>
<ul>
    <li><code>TicTacToe.prototype.empty</code>: A prototype method of the TicTacToe function that clears the game board and sets the count property of the marks object to 0.</li>
    <li><code>TicTacToe.prototype.reset</code>: A prototype method of the TicTacToe function that resets the game board and the scores object to their initial states.</li>
    <li><code>onResult(result, scores)</code>: A callback function that takes in the outcome of the game (win or draw) and the scores of each player, respectively, and displays an alert message indicating which player won the game or if it ended in a draw. It then calls the <code>updateScores</code> function to update the score board and calls the <code>empty</code> method to clear the game


<p>This is a continuation of the previous code snippet where the empty and reset methods are defined as prototype methods of the TicTacToe function.</p>

<p>The empty method is called when a new game needs to be started or when the user clicks on the "New Game" button. This method iterates through all the columns of the game board and clears the contents of each cell by setting its innerHTML property to an empty string. It also removes the classes that were previously added to the cell to indicate which player marked it (X or O). Finally, it sets the count property of the marks object (which was not shown in this code snippet) to 0 to indicate that no cells have been marked yet.</p>

<p>The reset method is called when the user clicks on the "Reset Scores" button. This method simply calls the empty method to clear the game board and sets the scores object back to its initial state, with both X and O properties set to 0.</p>

<p>After defining these methods, the code initializes a new TicTacToe object with a placeholder element, a grid_size of 3, and a callback function called onResult.</p>

<p>The onResult function is the callback function that was passed to the TicTacToe object constructor. It takes in two parameters, result and scores, which represent the outcome of the game (win or draw) and the scores of each player, respectively. If the result is a draw, it displays an alert message indicating that the game ended in a draw. Otherwise, it displays an alert message indicating which player won the game and calls the updateScores function to update the score board. Finally, it calls the empty method to clear the game board for the next game.</p>

<p>The updateScores function updates the score board with the scores of each player. It selects the appropriate DOM elements using querySelector and updates their innerHTML properties with the corresponding scores.</p>

<p>The restart function is called when the user clicks on the "Restart" button. It calls the reset method to clear the game board and reset the scores. If a new grid_size parameter is passed in, it calls the paint method of the TicTacToe object to generate a new game board with the new size. Finally, it calls the updateScores function to update the score board with the new scores.</p>



<h2>Challenges</h2>
<p>One of the main challenges I encountered during the project was learning how to use JavaScript for the first time to create a functional app. To overcome this challenge, I spent a significant amount of time studying the basics of JavaScript, such as variables, loops, and conditional statements. I also spent time exploring various resources online to gain a deeper understanding of how JavaScript works and how it can be used to create web applications. Additionally, I experimented with creating small, standalone scripts to test out different ideas and approaches, which helped me to build my skills and confidence in using JavaScript.</p>


<h2>Wins</h2>

<p>A new project can be a daunting experience, especially when it involves building a functional application with styling. However, through dedication and persistence, I was able to achieve these two important milestones. One of the main wins of this project was building my first working app with styling. This required me to learn new techniques for designing and implementing user interfaces, including CSS styling and responsive design principles. By experimenting with different styling options and refining my approach through feedback and iteration, I was able to create a polished and visually appealing application.</p>

<p>Another significant achievement of this project was learning to build my first functional application. This required me to understand the fundamentals of programming, including data structures, control flow, and error handling. By breaking down the application into manageable parts and approaching each task systematically, I was able to make steady progress towards a fully functional product. This experience taught me valuable lessons about problem-solving, debugging, and testing, which will be useful in future projects. Overall, this project was a significant milestone in my journey as a developer, and I look forward to applying these skills and knowledge in future projects.</p>
<p>Through this project, I gained a deeper understanding of JavaScript. I also learned plenty of new CSS techniques and gained experience working on a solo project with a short timeframe. Overall, this project helped me to solidify my foundational skills in web development.</p>
<h2>Potential Improvements</h2>
<ul>
  <li><strong>Better styling:</strong> Improving the styling of the tic tac toe app can enhance the user experience and make it more visually appealing. This can include things like adding color schemes, choosing appropriate font styles, and incorporating images or icons to make the app more engaging. Furthermore, making the app responsive to different screen sizes and devices can help ensure that it looks good and functions well on a variety of platforms.</li>
  <li><strong>Computer opponent:</strong> Adding a computer opponent to the tic tac toe app can provide users with a single-player mode, where they can play against the computer instead of against another person. This can be a good way to allow users to practice their tic tac toe skills, without having to find someone to play with. Moreover, it can also provide an additional level of challenge for users who may find it too easy to win against a human opponent.</li>
  <li><strong>Sounds triggered by players making moves and winning the game:</strong> Incorporating sounds into the tic tac toe app can make the gameplay more engaging and exciting. For example, adding sounds that are triggered when players make moves can help users stay more engaged with the game, as it provides audio feedback to accompany their actions. Additionally, adding unique sounds that are triggered when a player wins the game can help add to the excitement and sense of accomplishment associated with winning.</li>
  <li><strong>Customizable player names and icons:</strong> Allowing users to customize their player names and icons can add a personal touch to the tic tac toe app. This can help users feel more connected to the game and create a sense of ownership over their gameplay experience. Additionally, it can provide a way for users to distinguish themselves from other players and make their gameplay experience more unique. By incorporating customizable player names and icons, users can feel more invested in the game and more likely to continue playing over time.</li>
</ul>
