<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy Birthday Gotoo💋💋 ❤️</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
  font-family: 'Segoe UI', sans-serif;
}

body{
  background: linear-gradient(135deg,#ff758c,#ff7eb3);
  color:white;
  text-align:center;
  overflow-x:hidden;
}

/* Floating hearts */
.heart{
  position:fixed;
  bottom:-10px;
  font-size:20px;
  animation: floatUp 6s linear infinite;
  opacity:0.8;
}

@keyframes floatUp{
  0%{transform:translateY(0);opacity:1;}
  100%{transform:translateY(-120vh);opacity:0;}
}

/* Main content */
.container{
  padding:40px 20px;
  animation: fadeIn 2s ease;
}

@keyframes fadeIn{
  from{opacity:0;transform:translateY(30px);}
  to{opacity:1;transform:translateY(0);}
}

h1{
  font-size:2.6em;
}

h2{
  margin:15px 0 25px;
  font-weight:normal;
}

.card{
  background:rgba(255,255,255,0.18);
  border-radius:20px;
  padding:25px;
  margin:20px auto;
  max-width:700px;
  backdrop-filter: blur(10px);
}

p{
  font-size:1.1em;
  line-height:1.7;
}

/* Image gallery */
.gallery{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(140px,1fr));
  gap:15px;
  margin-top:20px;
}

.gallery img{
  width:100%;
  border-radius:15px;
  transition:transform 0.4s;
}

.gallery img:hover{
  transform:scale(1.08);
}

/* Footer */
footer{
  margin:30px 0;
  font-size:1em;
}
</style>
</head>

<body>

<!-- Floating hearts -->
<script>
for(let i=0;i<25;i++){
  let h=document.createElement("div");
  h.className="heart";
  h.innerHTML="❤️";
  h.style.left=Math.random()*100+"vw";
  h.style.animationDuration=4+Math.random()*4+"s";
  document.body.appendChild(h);
}
</script>

<div class="container">
  <h1>Happy Birthday 🎂</h1>
  <h2>Gotooo🐣🎀💋 ❤️</h2>

  <div class="card">
    <p>
      Today is special because **you** were born ❤️  
      You are my happiness, my comfort, and my favorite person.
      <br><br>
      Every smile of yours makes my world brighter.
      I promise to stand by you in every phase of life.
      <br><br>
      May your life always be filled with love, laughter, and dreams coming true.
      <br><br>
      <strong>I love you forever 💖</strong>
    </p>
  </div>

  <div class="card">
    <h2>Our Memories 📸</h2>
    <div class="gallery">
      <!-- Replace image names later -->
      <img src="photo1.jpg">
      <img src="photo2.jpg">
      <img src="photo3.jpg">
    </div>
    <p style="margin-top:10px;font-size:0.9em;">
      (I’ll add our photos here soon ❤️)
    </p>
  </div>

  <footer>
    — With love, <strong>Hemen</strong> 💕  
    <br>25 December
  </footer>
</div>

</body>
</html>
