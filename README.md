<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Mummy ❤️</title>

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family: "Segoe UI", sans-serif;
}

body{
height:100vh;
overflow:hidden;
background:linear-gradient(135deg,#ff758c,#ff7eb3);
display:flex;
justify-content:center;
align-items:center;
flex-direction:column;
color:white;
text-align:center;
}

/* Title */

h1{
font-size:3rem;
margin-bottom:30px;
text-shadow:0 0 15px white;
}

/* Random photo container */

.photos{
position:absolute;
width:100%;
height:100%;
top:0;
left:0;
z-index:1;
pointer-events:none;
}

.photos img{
position:absolute;
width:120px;
border-radius:15px;
box-shadow:0 0 15px rgba(255,255,255,0.7);
transform:rotate(calc(-20deg + 40deg * var(--r)));
animation:float 10s ease-in-out infinite;
}
}
  
.photos img:nth-child(1){animation-duration:25s;}
.photos img:nth-child(2){animation-duration:25s;}
.photos img:nth-child(3){animation-duration:25s;}
.photos img:nth-child(4){animation-duration:25s;}
.photos img:nth-child(5){animation-duration:25s;}
.photos img:nth-child(6){animation-duration:25s;}
.photos img:nth-child(7){animation-duration:25s;}

  @keyframes floatPhoto{

0%{
transform:translate(-10vw,100vh) rotate(-10deg);
}

100%{
transform:translate(110vw,-20vh) rotate(10deg);
}

}
/* Envelope */

.envelope{
width:160px;
height:110px;
background:white;
position:relative;
cursor:pointer;
border-radius:8px;
box-shadow:0 10px 25px rgba(0,0,0,0.3);
animation:heartbeat 1.2s infinite;
z-index:5;
}

/* Envelope triangle */

.envelope:before{
content:"";
position:absolute;
top:0;
left:0;
width:0;
height:0;
border-left:80px solid transparent;
border-right:80px solid transparent;
border-top:60px solid #ff5e78;
}

/* Heartbeat animation */

@keyframes heartbeat{
0%{transform:scale(1);}
25%{transform:scale(1.05);}
50%{transform:scale(0.95);}
75%{transform:scale(1.05);}
100%{transform:scale(1);}
}

/* Message modal */

.messageBox{
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
background:rgba(0,0,0,0.8);
display:flex;
justify-content:center;
align-items:center;
visibility:hidden;
opacity:0;
transition:0.4s;
z-index:10;
}

.messageBox.active{
visibility:visible;
opacity:1;
}

.message{
background:white;
color:#444;
padding:40px;
border-radius:15px;
max-width:500px;
text-align:center;
font-size:1.2rem;
line-height:1.6;
box-shadow:0 0 30px rgba(255,255,255,0.5);
}

/* Floating hearts */

.heart{
position:absolute;
bottom:-20px;
font-size:20px;
color:#fff;
animation:float 6s linear infinite;
opacity:0.8;
text-shadow:0 0 10px white;
}

@keyframes float{
0%{
transform:translateY(0) scale(1);
opacity:1;
}
100%{
transform:translateY(-110vh) scale(1.5);
opacity:0;
}
}

</style>
</head>

<body>

<h1>🎉 Happy Birthday Mummy 🎂</h1>

<div class="photos">

<!-- Replace with real photos -->

<img src="mum1.jpg" style="top:10%;left:5%;--r:0.2;">
<img src="mum2.jpg" style="top:70%;left:10%;--r:0.7;">
<img src="mum3.jpg" style="top:20%;left:80%;--r:0.4;">
<img src="mum4.jpg" style="top:60%;left:85%;--r:0.8;">
<img src="mum5.jpg" style="top:30%;left:20%;--r:0.3;">
<img src="mum6.jpg" style="top:50%;left:60%;--r:0.6;">
</div>

<!-- Envelope -->

<div class="envelope" onclick="openMessage()"></div>

<!-- Message -->

<div class="messageBox" id="messageBox">
<div class="message">
<h2>❤️ HBD LA MÉRE ❤️</h2>
<p>

Happy Birthday Mummy 🎂  

Thank you for all the love, and care.  
May this year bring you happiness, health, and riches.  

I love you so much ❤️

</p>
<br>
<button onclick="closeMessage()" style="padding:10px 20px;border:none;border-radius:8px;background:#ff5e78;color:white;font-size:16px;cursor:pointer;">
Close
</button>
</div>
</div>

<script>

/* open message */

function openMessage(){
document.getElementById("messageBox").classList.add("active");
}

/* close message */

function closeMessage(){
document.getElementById("messageBox").classList.remove("active");
}

/* create floating hearts */

function createHeart(){

const heart = document.createElement("div");
heart.classList.add("heart");
heart.innerHTML="❤";

heart.style.left = Math.random()*100 + "vw";
heart.style.fontSize = (15 + Math.random()*25) + "px";
heart.style.animationDuration = (4 + Math.random()*4) + "s";

document.body.appendChild(heart);

setTimeout(()=>{
heart.remove();
},7000)

}

setInterval(createHeart,300);

</script>

</body>
</html>

