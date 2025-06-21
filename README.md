<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Buenos días mi amor</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(to top right, #ffdde1, #ee9ca7);
      height: 100vh;
      overflow: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      font-family: 'Segoe UI', sans-serif;
      position: relative;
    }

    h1 {
      font-size: 2.5rem;
      color: #fff;
      text-shadow: 2px 2px 5px #c0392b;
      animation: fadeIn 2s ease-in-out;
      z-index: 1;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-30px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .heart {
      position: absolute;
      bottom: 0; /* <-- Aparecen desde abajo */
      width: 20px;
      height: 20px;
      background-color: red;
      transform: rotate(45deg);
      animation: float 6s linear forwards;
    }

    .heart::before,
    .heart::after {
      content: "";
      position: absolute;
      width: 20px;
      height: 20px;
      background-color: red;
      border-radius: 50%;
    }

    .heart::before {
      top: -10px;
      left: 0;
    }

    .heart::after {
      left: -10px;
      top: 0;
    }

    @keyframes float {
      0% {
        transform: translateY(0) rotate(45deg);
        opacity: 1;
      }
      100% {
        transform: translateY(-100vh) rotate(45deg);
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <h1>Buenos días mi amor <br>mi bella <br>ADRIANA ELVIRA CALLA VARGAS 💖</h1>

  <!-- Corazones generados con JavaScript -->
  <script>
    function createHeart() {
      const heart = document.createElement('div');
      heart.className = 'heart';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDuration = 3 + Math.random() * 3 + 's';
      document.body.appendChild(heart);
      setTimeout(() => heart.remove(), 6000);
    }

    setInterval(createHeart, 300);
  </script>
</body>
</html>