# Valentine Prank Website
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Valentine 💖</title>

  <style>
    body {
      margin: 0;
      height: 100vh;
      background: #ffd6e8;
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: Arial, sans-serif;
    }

    .container {
      text-align: center;
    }

    img {
      width: 200px;
    }

    h1 {
      color: #d63384;
      margin-top: 15px;
    }

    .buttons {
      margin-top: 25px;
      position: relative;
      height: 120px;
      width: 400px;
      margin-left: auto;
      margin-right: auto;
    }

    button {
      padding: 12px 32px;
      font-size: 18px;
      border-radius: 30px;
      border: none;
      cursor: pointer;
      position: absolute;
    }

    #yes {
      background: #ff4d88;
      color: white;
      left: 60px;
    }

    #no {
      background: white;
      color: black;
      border: 2px solid #ff4d88;
      left: 220px;
    }
  </style>
</head>

<body>

  <div class="container">
    <img src="https://media.giphy.com/media/JIX9t2j0ZTN9S/giphy.gif" alt="cute">
    <h1>Poonam, will you be my Valentine? 💘</h1>

    <div class="buttons">
      <button id="yes">Yes 💖</button>
      <button id="no">No 😏</button>
    </div>
  </div>

  <script>
    const noBtn = document.getElementById("no");

    // No button moves around on hover
    noBtn.addEventListener("mouseover", () => {
      const maxX = 320;
      const maxY = 80;

      const x = Math.random() * maxX;
      const y = Math.random() * maxY;

      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";
    });

    // Yes button click shows holding hands GIF
    document.getElementById("yes").addEventListener("click", () => {
      document.body.innerHTML = `
        <div style="text-align:center;">
          <h1 style="color:#d63384;font-size:48px;">YAY! 🎉</h1>
          <img src="https://media.giphy.com/media/l0HlOvJ7yaacpuSas/giphy.gif" width="320" alt="Holding Hands">
        </div>
      `;
    });
  </script>

</body>
</html>
