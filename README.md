<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday 🎂</title>

<style>

body{
margin:0;
font-family:Arial;
background:linear-gradient(135deg,#ff6a88,#ff99ac);
color:white;
text-align:center;
overflow:hidden;
}

.container{
padding:20px;
}

h1{
font-size:32px;
margin-top:30px;
animation: glow 2s infinite alternate;
}

@keyframes glow{
from{ text-shadow:0 0 10px white;}
to{ text-shadow:0 0 25px yellow;}
}

.slideshow{
width:90%;
max-width:320px;
margin:auto;
border-radius:20px;
overflow:hidden;
box-shadow:0 10px 30px rgba(0,0,0,0.4);
}

.slideshow img{
width:100%;
display:none;
}

button{
margin-top:20px;
padding:12px 25px;
border:none;
border-radius:12px;
font-size:16px;
background:white;
color:#ff4b7d;
cursor:pointer;
}

#msg{
margin-top:20px;
font-size:18px;
padding:10px;
}

.confetti{
position:fixed;
width:10px;
height:10px;
background:white;
top:-10px;
animation:fall linear infinite;
}

@keyframes fall{
to{
transform:translateY(110vh);
}
}

</style>
</head>

<body>

<div class="container">

<h1>🎂 Happy Birthday Bestie 🎂</h1>

<div class="slideshow">
<img src="PHOTO1.jpg">
<img src="PHOTO2.jpg">
<img src="PHOTO3.jpg">
<img src="PHOTO4.jpg">
</div>

<button onclick="showMessage()">Open Surprise 🎁</button>

<div id="msg"></div>

</div>

<audio autoplay loop>
<source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3">
</audio>

<script>

let index=0;
let images=document.querySelectorAll(".slideshow img");

function slideshow(){
images.forEach(img=>img.style.display="none");
index++;
if(index>images.length){index=1;}
images[index-1].style.display="block";
setTimeout(slideshow,2000);
}

slideshow();

function showMessage(){
document.getElementById("msg").innerHTML =
"💖 You are one of the most amazing people in my life. Thank you for all the memories and laughs. I hope your birthday is as awesome as you are! 🎉";
}

for(let i=0;i<40;i++){
let conf=document.createElement("div");
conf.className="confetti";
conf.style.left=Math.random()*100+"vw";
conf.style.animationDuration=(Math.random()*3+2)+"s";
conf.style.opacity=Math.random();
document.body.appendChild(conf);
}

</script>

</body>
</html>
