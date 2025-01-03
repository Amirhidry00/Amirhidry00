<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Coin Manager</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f4f4f9;
            margin: 0;
            padding: 0;
        }
        .container {
            padding: 20px;
            max-width: 400px;
            margin: auto;
            background: white;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            margin-top: 50px;
        }
        h1 {
            color: #333;
        }
        .coins {
            font-size: 2em;
            margin: 20px 0;
        }
        .button {
            display: inline-block;
            margin: 5px;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            background-color: #4caf50;
            color: white;
            cursor: pointer;
        }
        .button.remove {
            background-color: #f44336;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Coin Manager</h1>
        <div id="coinDisplay" class="coins">💰 Coins: 0</div>
        <button class="button" onclick="addCoin()">Add Coin</button>
        <button class="button remove" onclick="removeCoin()">Remove Coin</button>
    </div>

    <script>
        let coins = 0;

        function updateDisplay() {
            document.getElementById('coinDisplay').textContent = `💰 Coins: ${coins}`;
        }

        function addCoin() {
            coins++;
            updateDisplay();
        }

        function removeCoin() {
            if (coins > 0) {
                coins--;
            } else {
                alert("No more coins to remove!");
            }
            updateDisplay();
        }

        updateDisplay();
    </script>
</body>
</html>
