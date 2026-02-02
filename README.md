# Valentine-s-
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Be My Valentine 💖</title>
<style>
body {
  font-family: Arial, sans-serif;
  text-align: center;
  background: linear-gradient(#ffd6e8, #fff);
  height: 100vh;
  margin: 0;
  overflow: hidden;
}
h1 { margin-top: 80px; }
button {
  padding: 15px 30px;
  font-size: 18px;
  border-radius: 30px;
  border: none;
  cursor: pointer;
}
#yes {
  background: #ff4d6d;
  color: white;
}
#no {
  position: absolute;
  background: #ccc;
}
.hidden { display: none; }
img {
  max-width: 80%;
  border-radius: 20px;
  margin-top: 20px;
}
</style>
</head>
<body>

<div id="page1">
  <h1>Will you be my Valentine? 💘</h1>
  <button id="yes" onclick="nextPage()">Yes ❤️</button>
  <button id="no">No ❌</button>
</div>

<div id="page2" class="hidden">
  <h1>I knew you’d say yes 😍</h1>
  <p>You’re my favorite person in the world.</p>
  <img src="your-photo.jpg" alt="Us ❤️"/>
</div>

<script>
const noBtn = document.getElementById("no");

noBtn.addEventListener("mouseover", moveNo);
noBtn.addEventListener("click", moveNo);

function moveNo() {
  const x = Math.random() * (window.innerWidth - 100);
  const y = Math.random() * (window.innerHeight - 100);
  noBtn.style.left = x + "px";
  noBtn.style.top = y + "px";
}

function nextPage() {
  document.getElementById("page1").classList.add("hidden");
  document.getElementById("page2").classList.remove("hidden");
}
</script>

</body>
</html>
