<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tic Tac Toe</title>
    <link rel="stylesheet" href="tictac.css">
</head>
<body>
    <div class="container">
        <h1>Tic Tac Toe</h1>
        <div id="board" class="board">
            <div class="cell" onclick="makeMove(0)"></div>
            <div class="cell" onclick="makeMove(1)"></div>
            <div class="cell" onclick="makeMove(2)"></div>
            <div class="cell" onclick="makeMove(3)"></div>
            <div class="cell" onclick="makeMove(4)"></div>
            <div class="cell" onclick="makeMove(5)"></div>
            <div class="cell" onclick="makeMove(6)"></div>
            <div class="cell" onclick="makeMove(7)"></div>
            <div class="cell" onclick="makeMove(8)"></div>
        </div>
        <button onclick="resetBoard()">Reset</button>
        <p id="message"></p>
    </div>
    <script src="tictac.js"></script>
</body>
</html>
