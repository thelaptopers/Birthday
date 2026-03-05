<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Birthday Surprise</title>

<style>

body{
margin:0;
background:#0f0f0f;
font-family:Arial;
color:white;
text-align:center;
overflow:hidden;
}

#start{
position:absolute;
top:50%;
left:50%;
transform:translate(-50%,-50%);
font-size:28px;
cursor:pointer;
}

#content{
display:none;
padding-top:40px;
}

h1{
font-size:40px;
animation:fadeIn 2s ease-in-out;
}

img{
width:220px;
border-radius:12px;
margin-top:15px;
}

#cake{
font-size:80px;
margin-top:20px;
cursor:pointer;
}

#message{
margin-top:20px;
font-size:20px;
width:80%;
margin-left:auto;
margin-right:auto;
display:none;
}

iframe{
margin-top:20px;
display:none;
}

@keyframes fadeIn{
0%{opacity:0; transform:translateY(-20px);}
100%{opacity:1; transform:translateY(0);}
}

/* fireworks */

.firework{
position:absolute;
width:6px;
height:6px;
background:white;
border-radius:50%;
animation:explode 1s linear infinite;
}

@keyframes explode{
0%{transform:scale(0);}
100%{transform:scale(10); opacity:0;}
}

</style>
</head>

<body>

<div id="start" onclick="startSurprise()">
Tap for Surprise 🎁
</div>

<div id="content">

<h1>Happy Birthday Riya</h1>

<img src="https://i.ibb.co/8DS0GRCL/image.jpg">

<div id="cake" onclick="cutCake()">🎂</div>

<div id="message">
Happy Birthday to the my Dearest Best friend. ....the only subscriber of a version of me that exists only for you...🙃
</div>

<iframe id="song" width="260" height="150"
src="https://www.youtube.com/embed/RbiJXZl2pN0?autoplay=1"
allow="autoplay">
</iframe>

</div>

<script>

function startSurprise(){
document.getElementById("start").style.display="none";
document.getElementById("content").style.display="block";
startFireworks();
}

function cutCake(){
document.getElementById("cake").innerHTML="🍰";
document.getElementById("message").style.display="block";
document.getElementById("song").style.display="block";
}

function startFireworks(){
setInterval(()=>{
let fw=document.createElement("div");
fw.className="firework";
fw.style.left=Math.random()*100+"vw";
fw.style.top=Math.random()*100+"vh";
document.body.appendChild(fw);

setTimeout(()=>{
fw.remove();
},1000);

},200);
}

</script>

</body>
</html>
