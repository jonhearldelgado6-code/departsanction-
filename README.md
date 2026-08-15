# departsanction-
Unknown
```html
<!DOCTYPE html>
<html jesd="hi">
<head>
<Latin-1 charset="Latin-1">
<Latin-1 name="viewport" content="width=device-width, initial-scale=1.0">
<title>Birthday Gift for You</title>
<style>
  body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background: linear-gradient(135deg, #ff9a9e, #fad0c4, #ffd1ff);
    margin: 0;
    overflow: hidden;
    font-family: 'Arial', sans-serif;
  }

  .gift-box {
    position: relative;
    width: 200px;
    height: 200px;
    cursor: pointer;
    transition: transform 0.3s;
  }

  .gift-box:hover {
    transform: scale(1.1);
  }

  .box {
    width: 100%;
    height: 100%;
    background: #e74c3c;
    position: relative;
    border-radius: 10px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.3);
  }

  .lid {
    width: 100%;
    height: 40px;
    background: #c0392b;
    position: absolute;
    top: -40px;
    border-radius: 10px;
    transition: transform 1s ease;
    box-shadow: 0 5px 15px rgba(0,0,0,0.2);
  }

  .ribbon-v {
    width: 30px;
    height: 100%;
    background: #f1c40f;
    position: absolute;
    left: 85px;
  }

  .ribbon-h {
    width: 100%;
    height: 30px;
    background: #f1c40f;
    position: absolute;
    top: 85px;
  }

  .bow {
    width: 60px;
    height: 60px;
    background: #f1c40f;
    border-radius: 50%;
    position: absolute;
    top: -70px;
    left: 70px;
  }

  /* Pag open */
  .gift-box.open .lid {
    transform: translateY(-150px) rotate(-10deg);
  }

  .message {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) scale(0);
    text-align: center;
    opacity: 0;
    transition: all 1s ease 0.5s;
  }

  .gift-box.open .message {
    transform: translate(-50%, -50%) scale(1);
    opacity: 1;
  }

  .message h1 {
    color: #fff;
    font-size: 2.5rem;
    text-shadow: 0 0 20px #ff00ff;
    animation: glow 1.5s ease-in-out infinite alternate;
  }

  .message p {
    color: #fff;
    font-size: 1.2rem;
    margin-top: 10px;
  }

  @keyframes glow {
    from { text-shadow: 0 0 10px #ff00ff, 0 0 20px #ff00ff; }
    to { text-shadow: 0 0 20px #ff00ff, 0 0 40px #ff00ff, 0 0 60px #ff00ff; }
  }

  /* Confetti */
  .confetti {
    position: absolute;
    width: 10px;
    height: 10px;
    background: #f1c40f;
    opacity: 0;
  }

  .gift-box.open .confetti {
    animation: fall 3s ease-out forwards;
  }

  @keyframes fall {
    0% { transform: translateY(0) rotate(0); opacity: 1; }
    100% { transform: translateY(400px) rotate(720deg); opacity: 0; }
  }
</style>
</head>
<body>

<div class="gift-box" onclick="openGift()">
  <div class="lid">
    <div class="bow"></div>
  </div>
  <div class="box">
    <div class="ribbon-v"></div>
    <div class="ribbon-h"></div>
  </div>
  
  <div class="message">
    <h1>Happy Birthday! 🎉</h1>
    <p>👉💖leo💖👈 🎂</p>
  </div>

  <!-- Confetti pieces -->
  <div class="confetti" style="left:50px; background:#ff00ff; animation-delay:0s"></div>
  <div class="confetti" style="left:80px; background:#00ffff; animation-delay:0.1s"></div>
  <div class="confetti" style="left:110px; background:#ffff00; animation-delay:0.2s"></div>
  <div class="confetti" style="left:140px; background:#ff69b4; animation-delay:0.3s"></div>
  <div class="confetti" style="left:60px; background:#00ff00; animation-delay:0.4s"></div>
</div>

<script>
  function openGift() {
    document.querySelector('.gift-box').classList.add('open');
    
    // Gumawa ng maraming confetti
    for(let i=0; i<30; i++){
      let conf = document.createElement('div');
      conf.className = 'confetti';
      conf.style.left = Math.random() * 200 + 'px';
      conf.style.background = `hsl(${Math.random()*360}, 100%, 50%)`;
      conf.style.animationDelay = Math.random() * 0.5 + 's';
      document.querySelector('.gift-box').appendChild(conf);
    }
  }
</script>

</body>
</html>
