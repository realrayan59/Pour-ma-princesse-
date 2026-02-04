<!DOCTYPE html>  
<html lang="fr">  
<head>  
  <meta charset="UTF-8">  
  <title>Pour Kelly 💖</title>  
  <style>  
    body {  
      margin: 0;  
      height: 100vh;  
      background: linear-gradient(135deg, #ffb6c1, #ffc0cb);  
      display: flex;  
      justify-content: center;  
      align-items: center;  
      font-family: "Comic Sans MS", cursive, sans-serif;  
      overflow: hidden;  
    }  
  
    .card {  
      background: rgba(255, 255, 255, 0.9);  
      padding: 40px;  
      border-radius: 25px;  
      text-align: center;  
      box-shadow: 0 0 30px rgba(255, 105, 180, 0.6);  
      max-width: 500px;  
      z-index: 2;  
    }  
  
    h1 {  
      color: #e60073;  
      font-size: 28px;  
    }  
  
    .buttons {  
      margin-top: 30px;  
      display: flex;  
      justify-content: center;  
      gap: 20px;  
    }  
  
    button {  
      padding: 12px 22px;  
      font-size: 18px;  
      border: none;  
      border-radius: 20px;  
      cursor: pointer;  
      transition: 0.3s;  
    }  
  
    #yes {  
      background: #ff4d88;  
      color: white;  
    }  
  
    #yes:hover {  
      background: #e60073;  
      transform: scale(1.1);  
    }  
  
    #no {  
      background: #ffd6e5;  
      color: #cc0066;  
      position: relative;  
    }  
  
    .signature {  
      margin-top: 25px;  
      font-size: 20px;  
      color: #cc0066;  
    }  
  
    .heart {  
      position: absolute;  
      font-size: 24px;  
      animation: float 6s infinite ease-in;  
      opacity: 0.8;  
    }  
  
    @keyframes float {  
      0% {  
        transform: translateY(100vh) scale(0.5);  
        opacity: 0;  
      }  
      50% {  
        opacity: 1;  
      }  
      100% {  
        transform: translateY(-10vh) scale(1.2);  
        opacity: 0;  
      }  
    }  
  </style>  
</head>  
<body>  
  
  <div class="card" id="card">  
    <h1>  
      Veux-tu être ma Valentine<br>  
      s’il te plaît mon amour ? 💕  
    </h1>  
  
    <div class="buttons">  
      <button id="yes">Oui mon amour 💖</button>  
      <button id="no">Non 🙄</button>  
    </div>  
  
    <div class="signature">  
      Signé Rayan 💘  
    </div>  
  </div>  
  
  <script>  
    // Cœurs flottants  
    function createHeart() {  
      const heart = document.createElement("div");  
      heart.classList.add("heart");  
      heart.innerHTML = "💖";  
      heart.style.left = Math.random() * 100 + "vw";  
      heart.style.animationDuration = (4 + Math.random() * 4) + "s";  
      document.body.appendChild(heart);  
      setTimeout(() => heart.remove(), 8000);  
    }  
    setInterval(createHeart, 400);  
  
    // Bouton OUI  
    document.getElementById("yes").onclick = () => {  
      document.getElementById("card").innerHTML = `  
        <h1>J’ai gagné 😍💍</h1>  
        <p style="font-size:22px;color:#e60073;">  
          Je t’aime plus que tout Kelly 💖<br>  
          Ma Valentine pour toujours 🥹  
        </p>  
      `;  
    };  
  
    // Bouton NON qui fuit  
    const noBtn = document.getElementById("no");  
    noBtn.onmouseover = () => {  
      const x = Math.random() * 200 - 100;  
      const y = Math.random() * 200 - 100;  
      noBtn.style.transform = `translate(${x}px, ${y}px)`;  
    };  
  </script>  
  
</body>  
</html>  
