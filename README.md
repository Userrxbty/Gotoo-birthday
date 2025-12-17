<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy Birthday Tanisha ❤️</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:'Segoe UI',sans-serif;}
body{
  background:radial-gradient(circle at top,#ff9a9e,#ff2f6d,#120010);
  color:#fff;
  text-align:center;
  overflow-x:hidden;
}

/* Password screen */
#lock{
  position:fixed; inset:0;
  background:#000;
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:center;
  z-index:20;
}
#lock input{
  padding:12px;
  border:none;
  border-radius:10px;
  font-size:1em;
  margin-top:15px;
}
#lock button{
  margin-top:10px;
  padding:10px 25px;
  border:none;
  border-radius:20px;
  background:#ff4d6d;
  color:#fff;
  font-size:1em;
}

/* Intro */
#intro{
  position:fixed; inset:0;
  background:#000;
  display:flex;
  align-items:center;
  justify-content:center;
  z-index:10;
  animation:fadeOut 2s ease forwards;
  animation-delay:3s;
}
#intro h1{font-size:2.8em; animation:zoom 2s;}
@keyframes zoom{from{transform:scale(.3);opacity:0;}to{transform:scale(1);opacity:1;}}
@keyframes fadeOut{to{opacity:0;visibility:hidden;}}

/* Hearts */
.heart{
  position:fixed;
  bottom:-20px;
  font-size:22px;
  animation:floatUp linear infinite;
  filter:drop-shadow(0 0 10px pink);
}
@keyframes floatUp{to{transform:translateY(-120vh);}}

/* Content */
.container{padding:50px 20px;max-width:900px;margin:auto;}
.card{
  background:rgba(255,255,255,.15);
  border-radius:25px;
  padding:30px;
  margin:25px auto;
  backdrop-filter:blur(14px);
  box-shadow:0 0 30px rgba(255,0,100,.4);
}
.type{font-size:1.2em;min-height:60px;margin:20px 0;}

/* Slider */
.slider{overflow:hidden;border-radius:20px;}
.slides{display:flex;animation:slide 12s infinite;}
.slides img{width:100%;flex-shrink:0;}
@keyframes slide{
  0%{transform:translateX(0);}
  33%{transform:translateX(-100%);}
  66%{transform:translateX(-200%);}
}

/* Fireworks */
canvas{position:fixed;top:0;left:0;pointer-events:none;}
</style>
</head>

<body>

<!-- PASSWORD -->
<div id="lock">
  <h2>Enter Password ❤️</h2>
  <input type="password" id="pass" placeholder="Hint: her name + date">
  <button onclick="unlock()">Open</button>
</div>

<!-- INTRO -->
<div id="intro"><h1>For Tanisha ❤️</h1></div>

<!-- MUSIC -->
<audio id="music" loop>
  <source src="music.mp3" type="audio/mpeg">
</audio>

<canvas id="fire"></canvas>

<script>
function unlock(){
  if(document.getElementById("pass").value==="tanisha25"){
    document.getElementById("lock").style.display="none";
    document.getElementById("music").play();
  }else alert("Wrong password ❤️");
}

/* Hearts */
for(let i=0;i<35;i++){
 let h=document.createElement("div");
 h.className="heart";
 h.innerHTML="❤️";
 h.style.left=Math.random()*100+"vw";
 h.style.animationDuration=4+Math.random()*6+"s";
 document.body.appendChild(h);
}

/* Typewriter */
const text="Today the world became beautiful because you were born 💖";
let i=0;
function typeWriter(){
 if(i<text.length){
  document.getElementById("type").innerHTML+=text.charAt(i++);
  setTimeout(typeWriter,60);
 }
}
setTimeout(typeWriter,3500);

/* Fireworks */
const c=document.getElementById("fire"),x=c.getContext("2d");
c.width=innerWidth;c.height=innerHeight;
let p=[];
function boom(){
 p.push({x:Math.random()*c.width,y:Math.random()*c.height,r:0});
}
setInterval(boom,700);
function draw(){
 x.clearRect(0,0,c.width,c.height);
 p.forEach(b=>{b.r+=2;x.beginPath();x.arc(b.x,b.y,b.r,0,2*Math.PI);x.strokeStyle="pink";x.stroke();});
 requestAnimationFrame(draw);
}
draw();
</script>

<div class="container">
  <h1>Happy Birthday 🎂</h1>
  <h1>Tanisha ❤️</h1>

  <div class="type" id="type"></div>

  <div class="card">
    <p>
      You are my favorite feeling, my safest place, my forever person.
      I promise to love you louder on bad days and softer on tired ones.
      <br><br>
      <strong>Forever yours — Hemen 💖</strong>
    </p>
  </div>

  <div class="card">
    <h2>Our Moments 📸</h2>
    <div class="slider">
      <div class="slides">
        <img src="photo1.jpg">
        <img src="photo2.jpg">
        <img src="photo3.jpg">
      </div>
    </div>
  </div>

  <footer>25 December 🎉</footer>
</div>

</body>
</html>
