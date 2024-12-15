<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Loi chuc ngay moi vui ve</title>
    <style>
      body {
        font-family: Arial, sans-serif;
        background-color: #fef3f3;
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
        margin: 0;
        overflow: hidden;
      }
      .container {
        text-align: center;
        background-color: #fff;
        padding: 30px;
        border-radius: 15px;
        box-shadow: 0px 0px 15px rgba(0, 0, 0, 0.2);
        width: 320px;
        position: relative;
        z-index: 1;
        overflow: hidden;
      }
      h1 {
        color: #ff69b4;
        font-size: 24px;
        margin-bottom: 10px;
      }
      p {
        color: #333;
        font-size: 18px;
        margin-bottom: 20px;
      }
      .heart {
        color: #ff69b4;
        font-size: 50px;
        animation: float 2s ease-in-out infinite;
      }
      /* Heart floating effect */
      @keyframes float {
        0%,
        100% {
          transform: translateY(0);
        }
        50% {
          transform: translateY(-15px);
        }
      }
      /* Falling hearts */
      .falling-hearts {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        overflow: hidden;
        pointer-events: none;
      }
      .heart-shape {
        position: absolute;
        width: 20px;
        height: 20px;
        background-color: #ff69b4;
        transform: rotate(45deg);
        animation: fall 3s linear infinite;
        border-radius: 3px;
      }
      .heart-shape:before,
      .heart-shape:after {
        content: "";
        position: absolute;
        width: 20px;
        height: 20px;
        background-color: #ff69b4;
        border-radius: 50%;
      }
      .heart-shape:before {
        top: -10px;
        left: 0;
      }
      .heart-shape:after {
        left: 10px;
        top: 0;
      }
      /* Falling animation */
      @keyframes fall {
        0% {
          transform: translateY(-50px) rotate(45deg);
          opacity: 1;
        }
        100% {
          transform: translateY(400px) rotate(45deg);
          opacity: 0;
        }
      }
    </style>
  </head>
  <body>
    <div class="container">
      <h1>Chúc Cậu làm việc vui vẻ nheeeee!</h1>
      <p>
        Chúc cậu làm việc một ngày tràn đầy năng lượng, luôn vui vẻ và hehee nhớ
        tới tớ nheeeee, hk đc quên tớ âu á nhe <span class="heart">❤️</span>
      </p>
      <!-- Falling hearts effect -->
      <div class="falling-hearts">
        <div class="heart-shape" style="left: 10%; animation-delay: 0s"></div>
        <div class="heart-shape" style="left: 30%; animation-delay: 0.5s"></div>
        <div class="heart-shape" style="left: 50%; animation-delay: 1s"></div>
        <div class="heart-shape" style="left: 70%; animation-delay: 1.5s"></div>
        <div class="heart-shape" style="left: 90%; animation-delay: 2s"></div>
      </div>
    </div>
  </body>
</html>
