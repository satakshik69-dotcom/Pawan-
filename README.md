<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Valentine 💖</title>
  <style>
    body {
      background: pink;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      font-family: Arial, sans-serif;
      text-align: center;
    }

    h1 {
      font-size: 40px;
      color: #b30059;
    }

    button {
      font-size: 22px;
      padding: 12px 25px;
      margin: 10px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
    }

    #yes {
      background: red;
      color: white;
    }

    #no {
      background: white;
      color: black;
    }

    #message {
      margin-top: 20px;
      font-size: 26px;
      color: #800040;
    }

    #heart {
      font-size: 120px;
      display: none;
      animation: pop 0.6s ease-in-out infinite alternate;
    }

    @keyframes pop {
      from { transform: scale(1); }
      to { transform: scale(1.2); }
    }
  </style>
</head>
<body>

  <div>
    <h1>pawan will you be my Valentine? 💘</h1>
    <button id="yes">Yes 💖</button>
    <button id="no">No 🙃</button>

    <div id="message"></div>
    <div id="heart">❤️</div>
  </div>

  <script>
    let noMessages = ["Seriously? 😒", "No way 😤"];
    let noIndex = 0;

    document.getElementById("no").onclick = function () {
      document.getElementById("message").innerText = noMessages[noIndex];
      noIndex = (noIndex + 1) % noMessages.length;
    };

    document.getElementById("yes").onclick = function () {
      document.getElementById("message").innerText = "YAYYYY 💕 I knew it!!!";
      document.getElementById("heart").style.display = "block";
    };
  </script>

</body>
</html>
