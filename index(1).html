<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Advanced Tic Tac Toe</title>
    <style>
        /* General Styles */
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(to bottom, #6dd5ed, #2193b0);
            color: #fff;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            overflow: hidden;
        }

        .dark-mode {
            background: linear-gradient(to bottom, #2c3e50, #4ca1af);
            color: #ddd;
        }

        .container {
            text-align: center;
            padding: 20px;
            border-radius: 15px;
            background: rgba(0, 0, 0, 0.7);
            box-shadow: 0 8px 15px rgba(0, 0, 0, 0.3);
            max-width: 400px;
            width: 90%;
        }

        h1 {
            font-size: 2.5em;
            margin-bottom: 20px;
        }

        button {
            padding: 10px 20px;
            margin: 10px;
            font-size: 1em;
            border: none;
            border-radius: 5px;
            background-color: #f39c12;
            color: #fff;
            cursor: pointer;
            transition: transform 0.2s, background-color 0.3s;
        }

        button:hover {
            transform: scale(1.05);
            background-color: #e67e22;
        }

        .hidden {
            display: none;
        }

        .board {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            grid-gap: 10px;
            margin: 20px 0;
        }

        .cell {
            background: rgba(255, 255, 255, 0.9);
            color: #333;
            font-size: 2em;
            text-align: center;
            line-height: 100px;
            height: 100px;
            border-radius: 10px;
            cursor: pointer;
            transition: transform 0.2s, box-shadow 0.3s;
        }

        .cell:hover {
            transform: scale(1.1);
            box-shadow: 0 4px 10px rgba(255, 255, 255, 0.4);
        }

        .status {
            font-size: 1.2em;
            margin-top: 10px;
        }

        input[type="text"] {
            padding: 10px;
            margin: 10px 0;
            border-radius: 5px;
            border: 1px solid #ddd;
            font-size: 1em;
            width: 80%;
        }

        .savedGames {
            list-style: none;
            padding: 0;
        }

        .savedGames li {
            margin: 10px 0;
        }

        /* Score styling */
        .score {
            font-size: 1.2em;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <!-- Welcome Page -->
    <div id="welcomePage" class="container">
        <h1>Welcome to Tic Tac Toe!</h1>
        <p><strong>Created by Jat Maomo Tech</strong></p>
        <button onclick="showGameSetup()">Start Game</button>
        <button onclick="toggleTheme()">Light/Dark Mode</button>
        <h2>Saved Games</h2>
        <ul id="savedGamesList" class="savedGames"></ul>
    </div>

    <!-- Game Setup Page -->
    <div id="setupPage" class="container hidden">
        <h1>Game Setup</h1>
        <select id="player1Select">
            <option value="Maomo">Maomo</option>
            <option value="Dev Quat">Dev Quat</option>
            <option value="Maokad">Maokad</option>
            <option value="Bashiroh">Bashiroh</option>
            <option value="Jegas">Jegas</option>
        </select>
        <input type="text" id="newPlayerName" placeholder="Create a New Player">
        <button onclick="addPlayer()">Add Player</button>
        <select id="player2Select">
            <option value="Computer">Computer</option>
            <option value="Maomo">Maomo</option>
            <option value="Dev Quat">Dev Quat</option>
            <option value="Maokad">Maokad</option>
            <option value="Bashiroh">Bashiroh</option>
            <option value="Jegas">Jegas</option>
        </select>
        <button onclick="startGame()">Start</button>
        <button onclick="backToMenu()">Back to Menu</button>
    </div>

    <!-- Game Page -->
    <div id="gamePage" class="container hidden">
        <h1>Tic Tac Toe</h1>
        <div id="gameStatus" class="status">Player 1's turn</div>
        <div class="board">
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
        <div class="score">
            <p>Score: <span id="scorePlayer1">Player 1: 0</span> - <span id="scorePlayer2">Player 2: 0</span></p>
        </div>
        <button onclick="saveGame()">Save Game</button>
        <button onclick="resetGame()">restart</button>
        <button onclick="backToMenu()"> Menu</button>
    </div>

    <script>
        let currentPlayer = 1;
        let playerNames = ["Player 1", "Player 2"];
        let board = ['', '', '', '', '', '', '', '', ''];
        let gameOver = false;
        let isComputer = false;
        let scorePlayer1 = 0;
        let scorePlayer2 = 0;
        let savedGames = JSON.parse(localStorage.getItem('savedGames')) || [];

        function showGameSetup() {
            document.getElementById('welcomePage').classList.add('hidden');
            document.getElementById('setupPage').classList.remove('hidden');
            displaySavedGames();
        }

        function addPlayer() {
            const newPlayer = document.getElementById('newPlayerName').value.trim();
            if (newPlayer) {
                const player1Select = document.getElementById('player1Select');
                const player2Select = document.getElementById('player2Select');
                player1Select.innerHTML += `<option value="${newPlayer}">${newPlayer}</option>`;
                player2Select.innerHTML += `<option value="${newPlayer}">${newPlayer}</option>`;
                document.getElementById('newPlayerName').value = '';
                alert(`Player "${newPlayer}" added!`);
            }
        }

        function startGame() {
            const player1 = document.getElementById('player1Select').value;
            const player2 = document.getElementById('player2Select').value;
            playerNames = [player1, player2];
            isComputer = player2 === "Computer";
            document.getElementById('setupPage').classList.add('hidden');
            document.getElementById('gamePage').classList.remove('hidden');
            resetGame();
        }

        function backToMenu() {
            document.getElementById('setupPage').classList.add('hidden');
            document.getElementById('gamePage').classList.add('hidden');
            document.getElementById('welcomePage').classList.remove('hidden');
        }

        function makeMove(index) {
            if (gameOver || board[index] !== '') return;
            board[index] = currentPlayer === 1 ? 'X' : 'O';
            document.querySelectorAll('.cell')[index].textContent = board[index];
            checkWinner();
            if (!gameOver && isComputer && currentPlayer === 2) {
                setTimeout(makeComputerMove, 500);
            } else {
                currentPlayer = currentPlayer === 1 ? 2 : 1;
                updateStatus();
            }
        }

        function saveGame() {
            savedGames.push({ board: [...board], currentPlayer, playerNames, scorePlayer1, scorePlayer2 });
            localStorage.setItem('savedGames', JSON.stringify(savedGames));
            alert("Game saved!");
            displaySavedGames();
        }

        function checkWinner() {
            const winPatterns = [
                [0, 1, 2], [3, 4, 5], [6, 7, 8], // Horizontal
                [0, 3, 6], [1, 4, 7], [2, 5, 8], // Vertical
                [0, 4, 8], [2, 4, 6] // Diagonal
            ];

            for (let pattern of winPatterns) {                 
                const [a, b, c] = pattern;
                if (board[a] && board[a] === board[b] && board[a] === board[c]) {
                    gameOver = true;
                    document.getElementById('gameStatus').textContent = `${playerNames[currentPlayer - 1]} wins!`;
                    updateScore(currentPlayer);
                    return;
                }
            }

            // Check for a draw (no empty spaces left)
            if (!board.includes('')) {
                gameOver = true;
                document.getElementById('gameStatus').textContent = "It's a draw!";
            }
        }

                function updateScore(player) {
            if (player === 1) {
                scorePlayer1++;
                document.getElementById('scorePlayer1').textContent = `Player 1: ${scorePlayer1}`;
            } else {
                scorePlayer2++;
                document.getElementById('scorePlayer2').textContent = `Player 2: ${scorePlayer2}`;
            }
        }

        function resetGame() {
            board = ['', '', '', '', '', '', '', '', ''];
            gameOver = false;
            currentPlayer = 1;
            updateStatus();
            document.querySelectorAll('.cell').forEach(cell => cell.textContent = '');
        }

        function updateStatus() {
            document.getElementById('gameStatus').textContent = `${playerNames[currentPlayer - 1]}'s turn`;
        }

        function toggleTheme() {
            document.body.classList.toggle('dark-mode');
        }

        function makeComputerMove() {
            let availableMoves = board.map((cell, index) => cell === '' ? index : null).filter(index => index !== null);
            let randomMove = availableMoves[Math.floor(Math.random() * availableMoves.length)];
            makeMove(randomMove);
        }

        function displaySavedGames() {
            const savedGamesList = document.getElementById('savedGamesList');
            savedGamesList.innerHTML = '';
            savedGames.forEach((game, index) => {
                const gameItem = document.createElement('li');
                gameItem.textContent = `Game ${index + 1}: ${game.playerNames[0]} vs ${game.playerNames[1]} (Player 1: ${game.scorePlayer1}, Player 2: ${game.scorePlayer2})`;
                savedGamesList.appendChild(gameItem);
            });
        }
    </script>
</body>
</html>

