<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Salma</title>

<style>

body{
margin:0;
height:100vh;
display:flex;
justify-content:center;
align-items:center;
font-family:Arial;
background:linear-gradient(135deg,#ff758c,#ff7eb3,#ffc3a0);
overflow:hidden;
}

.card{
background:white;
padding:50px;
border-radius:25px;
text-align:center;
box-shadow:0 20px 40px rgba(0,0,0,0.2);
animation:pop 1s ease;
}

h1{
font-size:50px;
color:#ff3e6c;
margin-bottom:10px;
animation:glow 2s infinite alternate;
}

p{
font-size:20px;
color:#444;
}

button{
margin-top:20px;
padding:12px 25px;
border:none;
border-radius:20px;
background:#ff3e6c;
color:white;
font-size:16px;
cursor:pointer;
}

.heart{
position:absolute;
color:#ff3e6c;
font-size:20px;
animation:float 6s linear infinite;
}

@keyframes pop{
0%{transform:scale(0)}
100%{transform:scale(1)}
}

@keyframes glow{
from{text-shadow:0 0 10px pink}
to{text-shadow:0 0 25px red}
}

@keyframes float{
0%{transform:translateY(0);opacity:1}
100%{transform:translateY(-100vh);opacity:0}
}

.cake{
font-size:60px;
margin:15px 0;
animation:bounce 2s infinite;
}

@keyframes bounce{
0%,100%{transform:translateY(0)}
50%{transform:translateY(-10px)}
}

</style>
</head>

<body>

<div class="card">

<h1>Happy Birthday Salma 🎉</h1>

<div class="cake">🎂</div>

<p>Wishing you happiness, success and a beautiful year ahead ❤️</p>

<button onclick="playMusic()">Play Birthday Music 🎵</button>

<audio id="music">
<source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
</audio>

</div>

<script>

function createHeart(){
const heart=document.createElement("div");
heart.classList.add("heart");
heart.innerHTML="❤";
heart.style.left=Math.random()*100+"vw";
heart.style.fontSize=(Math.random()*20+10)+"px";
document.body.appendChild(heart);

setTimeout(()=>{heart.remove()},6000);
}

setInterval(createHeart,300);

function playMusic(){
document.getElementById("music").play();
}

</script>

</body>
</html># -
