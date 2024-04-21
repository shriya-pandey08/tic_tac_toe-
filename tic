let currentPlayer = 'X';
let board = ['', '', '', '', '', '', '', '', ''];
let gameOver = false;

const winningCombinations = [
    [0, 1, 2],
    [3, 4, 5],
    [6, 7, 8],
    [0, 3, 6],
    [1, 4, 7],
    [2, 5, 8],
    [0, 4, 8],
    [2, 4, 6]
];

const boardCells = document.querySelectorAll('.cell');
const messageElement = document.getElementById('message');

function makeMove(index) {
    if (!gameOver && board[index] === '') {
        board[index] = currentPlayer;
        boardCells[index].innerText = currentPlayer;
        
        if (checkWin()) {
            messageElement.innerText = `${currentPlayer} wins!`;
            gameOver = true;
        } else if (checkDraw()) {
            messageElement.innerText = "It's a draw!";
            gameOver = true;
        } else {
            currentPlayer = currentPlayer === 'X' ? 'O' : 'X';
            messageElement.innerText = `Player ${currentPlayer}'s turn`;
        }
    }
}

function checkWin() {
    return winningCombinations.some(combination => {
        return combination.every(index => {
            return board[index] === currentPlayer;
        });
    });
}

function checkDraw() {
    return board.every(cell => cell !== '');
}

function resetBoard() {
    board = ['', '', '', '', '', '', '', '', ''];
    currentPlayer = 'X';
    gameOver = false;
    messageElement.innerText = `Player ${currentPlayer}'s turn`;
    boardCells.forEach(cell => {
        cell.innerText = '';
    });
}
