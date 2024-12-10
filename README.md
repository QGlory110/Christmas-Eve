<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ĐÔNG ÊM ĐỀM 🎄❄✨</title>
  <style>
    /* Nền Gradient Lung Linh */
    body {
      background: radial-gradient(circle at top, #001d3d, #003566, #0077b6, #03045e);
      color: white;
      font-family: "Arial", sans-serif;
      margin: 0;
      padding: 0;
      overflow: hidden;
    }

    /* Tiêu đề chính */
    h1 {
      position: absolute;
      top: 20px;
      text-align: center;
      width: 100%;
      font-size: 3rem;
      text-shadow: 2px 2px 20px #ffd700;
      animation: glow 2s infinite alternate;
    }

    @keyframes glow {
      from {
        text-shadow: 0 0 20px #ff4500, 0 0 30px #ffd700, 0 0 40px #fff;
      }
      to {
        text-shadow: 0 0 30px #ffecb3, 0 0 40px #ffd700, 0 0 50px #fff;
      }
    }

    /* Container hộp quà */
    .gift-container {
      display: flex;
      justify-content: center;
      align-items: flex-end;
      gap: 20px;
      height: 100vh;
    }

    /* Hiệu ứng hộp quà */
    .gift {
      text-align: center;
      position: relative;
    }

    .gift-box {
      width: 60px;
      height: 60px;
      background-color: red;
      border-radius: 10px;
      box-shadow: 0 0 10px #ffd700;
      animation: giftFlicker 2s infinite alternate;
    }

    .ribbon {
      position: absolute;
      top: 50%;
      left: 50%;
      width: 6px;
      height: 6px;
      background-color: gold;
      transform: translate(-50%, -50%) rotate(45deg);
    }

    @keyframes giftFlicker {
      0%, 100% {
        opacity: 1;
      }
      50% {
        opacity: 0.5;
      }
    }

    /* Hiệu ứng tuyết rơi */
    .snowflake {
      position: absolute;
      color: white;
      opacity: 0.8;
      animation: snow linear infinite;
    }

    /* Chuyển động tuyết xoay */
    @keyframes snow {
      0% {
        transform: translateX(0) translateY(-100px) rotate(0deg);
        opacity: 0;
      }
      50% {
        opacity: 1;
      }
      100% {
        transform: translateX(calc(50px - 50px * var(--direction))) translateY(100vh) rotate(360deg);
        opacity: 0;
      }
    }

    /* Sao nhấp nháy */
    .star-twinkle {
      position: absolute;
      background-color: white;
      border-radius: 50%;
      box-shadow: 0 0 10px white;
      animation: twinkle 2s infinite alternate;
    }

    @keyframes twinkle {
      from {
        text-shadow: 0 0 10px #ffd700, 0 0 20px #ffd700, 0 0 30px #fff;
      }
      to {
        text-shadow: 0 0 20px #ffecb3, 0 0 30px #ffd700, 0 0 40px #fff;
      }
    }

  </style>
</head>
<body>
  <h1>🎅 MERRY CHRISTMAS🎄❄✨🎁</h1>

  <!-- Container hộp quà -->
  <div class="gift-container" id="gift-container"></div>

  <!-- Nhạc nền -->
  <audio autoplay loop>
    <source src="https://www.bensound.com/bensound-music/bensound-thejazzpiano.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
  </audio>

  <script>
    // Tạo hộp quà
    function createGift(container) {
      const gift = document.createElement("div");
      gift.className = "gift";

      // Hộp quà
      const giftBox = document.createElement("div");
      giftBox.className = "gift-box";

      // Ruy băng
      const ribbon = document.createElement("div");
      ribbon.className = "ribbon";
      giftBox.appendChild(ribbon);

      gift.appendChild(giftBox);
      container.appendChild(gift);
    }

    // Tạo tuyết rơi
    function createSnowflakes() {
      for (let i = 0; i < 100; i++) {
        const snowflake = document.createElement("div");
        snowflake.className = "snowflake";
        snowflake.style.left = Math.random() * window.innerWidth + "px";
        snowflake.style.animationDuration = Math.random() * 5 + 5 + "s";
        snowflake.style.fontSize = Math.random() * 15 + 10 + "px";
        snowflake.style.animationDelay = Math.random() * 5 + "s";
        snowflake.style.setProperty("--direction", Math.random() < 0.5 ? -1 : 1);
        snowflake.innerHTML = "❄";
        document.body.appendChild(snowflake);
      }
    }

    // Tạo sao nhấp nháy
    function createTwinklingStars() {
      for (let i = 0; i < 50; i++) {
        const star = document.createElement("div");
        star.className = "star-twinkle";
        star.style.left = Math.random() * window.innerWidth + "px";
        star.style.top = Math.random() * window.innerHeight / 2 + "px";
        star.style.width = star.style.height = Math.random() * 3 + 2 + "px";
        document.body.appendChild(star);
      }
    }

 

    // Hiệu ứng tuyết và sao
    createSnowflakes();
    createTwinklingStars();
  </script>
</body>
</html>
