# Birthday
<!DOCTYPE html>
<html lang="mn">
<head>
<meta charset="UTF-8">
<title>🎉 Төрсөн өдрийн мэнд!</title>
<style>
  body {
    margin: 0;
    height: 100vh;
    background: radial-gradient(circle, #ffb6c1, #ff69b4);
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: Arial;
    overflow: hidden;
  }

  h1 {
    font-size: 50px;
    color: white;
    text-shadow: 0 0 10px #fff;
    animation: pop 1.5s infinite;
  }

  @keyframes pop {
    0% { transform: scale(1); }
    50% { transform: scale(1.15); }
    100% { transform: scale(1); }
  }

  .balloon {
    position: absolute;
    bottom: -100px;
    font-size: 40px;
    animation: fly 6s linear infinite;
  }

  @keyframes fly {
    from { transform: translateY(0); }
    to { transform: translateY(-120vh); }
  }
</style>
</head>
<body>

<h1>🎂 ТӨРСӨН ӨДРИЙН МЭНД 🎉<br>Надад хамгийн сайхан бүхнийг хүсье 💖</h1>

<script>
  const emojis = ["🎈","🎉","🎂","💖","✨"];
  setInterval(() => {
    const b = document.createElement("div");
    b.className = "balloon";
    b.style.left = Math.random() * 100 + "vw";
    b.innerText = emojis[Math.floor(Math.random() * emojis.length)];
    document.body.appendChild(b);
    setTimeout(() => b.remove(), 6000);
  }, 400);
</script>

</body>
</html>
