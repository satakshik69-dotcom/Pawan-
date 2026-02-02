<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Valentine 💖</title>
<style>
body{
  background: linear-gradient(135deg,#ff9a9e,#fad0c4);
  height:100vh;
  display:flex;
  justify-content:center;
  align-items:center;
  font-family: Arial, sans-serif;
}
.box{
  background:white;
  padding:30px;
  border-radius:20px;
  text-align:center;
  box-shadow:0 10px 25px rgba(0,0,0,.2);
}
button{
  padding:12px 25px;
  font-size:18px;
  border:none;
  border-radius:25px;
  cursor:pointer;
  margin:10px;
}
#yes{background:#ff4d6d;color:white;}
#no{background:#ccc;position:absolute;}
.hearts{
  font-size:40px;
  animation:float 1.5s infinite;
}
@keyframes float{
  0%{transform:translateY(0)}
  50%{transform:translateY(-20px)}
  100%{transform:translateY(0)}
}
</style>
</head>
<body>

<div class="box" id="q">
  <h1>Will you be my Valentine? 💘</h1>
  <button id="yes" onclick="yesClick()">Yes 💖</button>
  <button id="no" onmouseover="moveNo()">No 😅</button>
</div>

<script>
function yesClick(){
  document.body.innerHTML=
  '<div class="box"><h1>Yayyy!! 💕</h1><p>You made my day 💖</p><div class="hearts">💘 💖 💝 💞 💓</div></div>';
}
function moveNo(){
  const n=document.getElementById("no");
  n.style.left=Math.random()*80+"vw";
  n.style.top=Math.random()*80+"vh";
}
</script>

</body>
</html>
