<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Randomized Dice</title>
    <style>
        /* Styles for the dice container */
        .dice-container {
            display: flex;
            flex-wrap: wrap;
        }

        /* Styles for the individual dice */
        .dice {
            width: 80px;
            height: 80px;
            background-color: white;
            border: 1px solid #000;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            padding: 5px;
            border-radius: 10px;
            margin: 10px;
            font-size: 24px;
            font-weight: bold;
            align-items: center;
            justify-content: center;
        }
    </style>
</head>
<body>
    <div class="dice-container" id="diceContainer"></div>
    <button id="addDiceButton">Add Dice</button>

    <script>
        // Function to generate a random number between 1 and 6
        function getRandomNumber() {
            return Math.floor(Math.random() * 6) + 1;
        }

        // Function to create a new die with a random number
        function createDie() {
            const diceContainer = document.getElementById("diceContainer");
            const die = document.createElement("div");
            die.className = "dice";
            die.textContent = getRandomNumber(); // Set the random number as text

            diceContainer.appendChild(die);
        }

        // Add 10 dice initially
        for (let i = 0; i < 10; i++) {
            createDie();
        }

        // Add a die on button click
        const addDiceButton = document.getElementById("addDiceButton");
        addDiceButton.addEventListener("click", createDie);
    </script>
</body>
</html>
 
