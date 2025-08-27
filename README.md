# 10m-txgraaahyao-anniversarykub
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Happy Anniversary 💖</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Comic Sans MS', cursive, sans-serif;
      background: linear-gradient(135deg, #ffdde1, #ee9ca7);
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
    }
    h1 {
      color: white;
      text-shadow: 2px 2px 5px rgba(0,0,0,0.3);
    }
    #game {
      position: relative;
      width: 100%;
      height: 70%;
      overflow: hidden;
    }
    .heart {
      position: absolute;
      font-size: 24px;
      cursor: pointer;
      user-select: none;
      animation: float 5s linear infinite;
    }
    @keyframes float {
      0% { transform: translateY(100vh); opacity: 1; }
      100% { transform: translateY(-10vh); opacity: 0; }
    }
    #letter {
      display: none;
      background: white;
      border-radius: 15px;
      padding: 20px;
      max-width: 400px;
      text-align: center;
      box-shadow: 0 5px 15px rgba(0,0,0,0.2);
      animation: fadeIn 2s;
    }
    #letter img {
      width: 100%;
      border-radius: 10px;
      margin-top: 15px;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: scale(0.8); }
      to { opacity: 1; transform: scale(1); }
    }
  </style>
</head>
<body>
  <h1>💘 Click 10 hearts to open your gift 💘</h1>
  <div id="game"></div>
  <div id="letter">
    <h2>30aug 10m txgraaahyao luv chu 3000 💖</h2>
    <p>Happy Anniversary! 🎉</p>
    <img src="https://raw.githubusercontent.com/yourusername/yourrepo/main/yourimage.jpg" alt="Us">
  </div>

  <!-- เพลง Wish - blackbear -->
  <iframe width="0" height="0" src="https://www.youtube.com/embed/Y3Gs7Jx4i0k?autoplay=1&loop=1&playlist=Y3Gs7Jx4i0k" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

  <script>
    const game = document.getElementById("game");
    const letter = document.getElementById("letter");
    let count = 0;

    function createHeart() {
      const heart = document.createElement("div");
      heart.classList.add("heart");
      heart.innerHTML = "❤️";
      heart.style.left = Math.random() * 90 + "vw";
      heart.style.fontSize = Math.random() * 20 + 20 + "px";
      game.appendChild(heart);

      heart.addEventListener("click", () => {
        heart.remove();
        count++;
        if (count >= 10) {
          game.style.display = "none";
          letter.style.display = "block";
        }
      });

      setTimeout(() => heart.remove(), 5000);
    }

    setInterval(createHeart, 800);
  </script>
</body>
</html>
