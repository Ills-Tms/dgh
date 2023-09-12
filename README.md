# dgh
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dice Roller</title>
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
        }

        /* Styles for the dots (pips) on the dice */
        .dot {
            width: 30%;
            height: 30%;
            background-color: #000;
            border-radius: 50%;
            margin: 5%;
        }
    </style>
</head>
<body>
    <div class="dice-container" id="diceContainer"></div>
    <button id="addDiceButton">Add Dice</button>

    <script>
        // Function to create a new die
        function createDie() {
            const diceContainer = document.getElementById("diceContainer");
            const die = document.createElement("div");
            die.className = "dice";

            // Create six dots (pips) to represent the die's appearance
            for (let i = 0; i < 6; i++) {
                const dot = document.createElement("div");
                dot.className = "dot";
                die.appendChild(dot);
            }

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
