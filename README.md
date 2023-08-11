<!DOCTYPE html>
<html>
<head>
  <style>
    body {
      margin: 0;
      overflow: hidden;
      background-color: #0a0a0a;
    }

    .container {
      width: 100vw;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .shapes {
      animation: rotate 10s linear infinite;
    }

    @keyframes rotate {
      0% {
        transform: rotate(0deg);
      }
      100% {
        transform: rotate(360deg);
      }
    }

    .shape {
      width: 100px;
      height: 100px;
      background-color: #ff00ff;
      border-radius: 50%;
      position: absolute;
      mix-blend-mode: screen;
      opacity: 0.8;
    }

    .shape:nth-child(1) {
      animation: bounce 5s ease-in-out infinite alternate;
    }

    .shape:nth-child(2) {
      animation: bounce 5s ease-in-out 0.5s infinite alternate;
    }

    .shape:nth-child(3) {
      animation: bounce 5s ease-in-out 1s infinite alternate;
    }

    @keyframes bounce {
      0%, 100% {
        transform: translateY(0);
      }
      50% {
        transform: translateY(-40px);
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="shapes">
      <div class="shape"></div>
      <div class="shape"></div>
      <div class="shape"></div>
    </div>
  </div>
</body>
</html>
