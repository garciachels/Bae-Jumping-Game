# Bae-Jumping-Game
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<title>Shanae aka Bae 💖</title>

<style>
  body {
    background: #111;
    color: white;
    font-family: Arial, sans-serif;
    text-align: center;
    margin: 0;
    padding: 20px;
  }

  h1 {
    margin-bottom: 5px;
  }

  #score, #highScore {
    font-size: 18px;
    margin: 4px 0;
  }

  #game {
    width: 90%;
    max-width: 600px;
    height: 220px;
    background: #222;
    margin: 20px auto;
    position: relative;
    overflow: hidden;
    border: 3px solid white;
    touch-action: manipulation;
  }

  /* ❤️ HEART PLAYER */
  #player {
    width: 40px;
    height: 40px;
    position: absolute;
    bottom: 0;
    left: 60px;
    background: red;
    transform: rotate(-45deg);
    transition: transform 0.1s;
  }

  #player::before,
  #player::after {
    content: "";
    width: 40px;
    height: 40px;
    background: red;
    border-radius: 50%;
    position: absolute;
  }

  #player::before {
    top: -20px;
    left: 0;
  }

  #player::after {
    left: 20px;
    top: 0;
  }

  /* 💕 Pulse while jumping */
  .pulse {
    animation: pulse 0.4s infinite alternate;
  }

  @keyframes pulse {
    from { transform: rotate(-45deg) scale(1); }
    to { transform: rotate(-45deg) scale(1.15); }
  }

  /* 💀 Broken heart */
  .broken {
    animation: break 0.6s forwards;
  }

  @keyframes break {
    to {
      transform: rotate(-45deg) scale(0);
      opacity: 0;
    }
  }

  /* Obstacles */
  .obstacle {
    width: 30px;
    height: 45px;
    background: #ef4444;
    position: absolute;
    bottom: 0;
    right: -40px;
  }

  /* Restart Button */
  #restartBtn {
    display: none;
    margin-top: 15px;
    padding: 10px 20px;
    font-size: 16px;
    background: #ef4444;
    color: white;
    border: none;
    border-radius: 6px;
    cursor: pointer;
  }

  #restartBtn:hover {
    background: #dc2626;
  }
</style>
</head>

<body>

<h1>Shanae aka Bae 💖</h1>
<div id="score">Score: 0</div>
<div id="highScore">High Score: 0</div>

<div id="game">
  <div id="player"></div>
</div>

<button id="restartBtn">Try Again</button>

<script>
  const game = document.getElementById("game");
  const player = document.getElementById("player");
  const scoreDisplay = document.getElementById("score");
  const highScoreDisplay = document.getElementById("highScore");
  const restartBtn = document.getElementById("restartBtn");

  let isJumping = false;
  let position = 0;
  let velocity = 0;
  let gravity = 0.9;
  let speed = 5;
  let score = 0;
  let gameOver = false;

  let highScore = localStorage.getItem("highScore") || 0;
  highScoreDisplay.textContent = "High Score: " + highScore;

  /* JUMP */
  function jump() {
    if (isJumping || gameOver) return;
    isJumping = true;
    velocity = 15;
    player.classList.add("pulse");
  }

  /* GAME LOOP */
  function update() {
    if (gameOver) return;

    velocity -= gravity;
    position += velocity;

    if (position <= 0) {
      position = 0;
      isJumping = false;
      player.classList.remove("pulse");
    }

    player.style.bottom = position + "px";
    requestAnimationFrame(update);
  }

  update();

  /* CONTROLS */
  document.addEventListener("keydown", e => {
    if (e.code === "Space") jump();
  });

  game.addEventListener("click", jump);
  game.addEventListener("touchstart", e => {
    e.preventDefault();
    jump();
  });

  /* OBSTACLES */
  function createObstacle() {
    if (gameOver) return;

    const obstacle = document.createElement("div");
    obstacle.classList.add("obstacle");
    game.appendChild(obstacle);

    let obstaclePos = game.clientWidth;

    const move = setInterval(() => {
      if (gameOver) {
        clearInterval(move);
        obstacle.remove();
        return;
      }

      obstaclePos -= speed;
      obstacle.style.right = obstaclePos + "px";

      const p = player.getBoundingClientRect();
      const o = obstacle.getBoundingClientRect();

      if (
        p.right > o.left &&
        p.left < o.right &&
        p.bottom > o.top
      ) {
        endGame();
        clearInterval(move);
      }

      if (obstaclePos < -40) {
        clearInterval(move);
        obstacle.remove();
      }
    }, 20);

    score++;
    scoreDisplay.textContent = "Score: " + score;
    speed += 0.15;

    setTimeout(createObstacle, 1400);
  }

  createObstacle();

  /* GAME OVER */
  function endGame() {
    gameOver = true;
    player.classList.remove("pulse");
    player.classList.add("broken");
    restartBtn.style.display = "inline-block";

    if (score > highScore) {
      highScore = score;
      localStorage.setItem("highScore", highScore);
      highScoreDisplay.textContent = "High Score: " + highScore;
    }
  }

  /* RESTART */
  restartBtn.addEventListener("click", () => {
    document.querySelectorAll(".obstacle").forEach(o => o.remove());
    score = 0;
    speed = 5;
    position = 0;
    velocity = 0;
    gameOver = false;
    isJumping = false;

    scoreDisplay.textContent = "Score: 0";
    player.style.bottom = "0px";
    player.className = "";
    restartBtn.style.display = "none";

    createObstacle();
    update();
  });
</script>

</body>
</html>
