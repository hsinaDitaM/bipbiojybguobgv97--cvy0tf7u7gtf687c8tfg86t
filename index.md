<html>
<head>
  <title>Guess the Number</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #FFC8C8;
      text-align: center;
      margin-top: 100px;
    }
    html, body{
      background-color: #FFC8C8;
    }
    h1 {
      font-size: 4rem;
      color: #660000;
      text-shadow: 2px 2px #FF9999;
    }
    p {
      font-size: 2rem;
      color: #660000;
      text-shadow: 1px 1px #FF9999;
      margin-top: 50px;
    }
    input[type="text"] {
      padding: 10px;
      font-size: 2rem;
      border: 2px solid #660000;
      border-radius: 5px;
      margin-top: 30px;
    }
    button {
      padding: 10px;
      font-size: 2rem;
      background-color: #660000;
      color: #FFF;
      border: none;
      border-radius: 5px;
      margin-top: 30px;
      cursor: pointer;
    }
    button:hover {
      background-color: #FF9999;
      color: #660000;
      transition: background-color 0.5s ease;
    }
    p#result {
      font-size: 2rem;
      color: #660000;
      text-shadow: 1px 1px #FF9999;
      margin-top: 50px;
    }
  </style>
</head>
<body>
  <h1>Guess the Number</h1>
  <p>Try to guess the number between 1 and 100.</p>
  <input type="text" id="guess" placeholder="Enter your guess">
  <button onclick="checkGuess()">Submit</button>
  <p id="result"></p>

  <script>
    // Generate a random number between 1 and 100
    const randomNumber = Math.floor(Math.random() * 100) + 1;
    let attempts = 0;

    function checkGuess() {
      // Get the user's guess
      const guess = parseInt(document.getElementById("guess").value);

      // Increase the number of attempts
      attempts++;

      // Check if the guess is correct
      if (guess === randomNumber) {
        document.getElementById("result").innerHTML = `Congratulations! You guessed the number in ${attempts} attempts.`;
      } else if (guess < randomNumber) {
        document.getElementById("result").innerHTML = "Too low. Guess again.";
      } else {
        document.getElementById("result").innerHTML = "Too high. Guess again.";
      }
    }
  </script>
</body>
</html>

