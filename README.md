<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Abia | 14 Years of Magic ✨</title>

<style>
:root{
--accent:#ff4f9a;
--bg-dark:#0f1020;
--glass:rgba(255,255,255,.18);
--blur:blur(18px);
}

/* Reset */
*{margin:0;padding:0;box-sizing:border-box;font-family:Inter,system-ui,sans-serif;}
html{scroll-behavior:smooth;}
body{background:radial-gradient(circle at top,#2a2f6b,#0f1020);color:white;overflow-x:hidden;}

/* Preloader */
#preloader{
position:fixed;top:0;left:0;width:100%;height:100%;
background:#0f1020;display:flex;justify-content:center;align-items:center;z-index:9999;
}
.loader{
width:70px;height:70px;border:8px solid rgba(255,255,255,.2);
border-top-color:var(--accent);border-radius:50%;animation:spin 1s linear infinite;
}
@keyframes spin{to{transform:rotate(360deg);}}

/* Navbar */
nav{
position:sticky;top:0;z-index:1000;background:rgba(15,16,32,.85);
backdrop-filter:blur(10px);display:flex;justify-content:space-between;align-items:center;
padding:14px 25px;
}
nav h1{font-size:1.2rem;}
nav a{color:#fff;margin-left:18px;text-decoration:none;opacity:.8;}
nav a:hover{opacity:1;}

/* Hero */
.hero{
min-height:90vh;display:flex;flex-direction:column;justify-content:center;align-items:center;text-align:center;
padding:20px;
}
.hero h2{font-size:3rem;background:linear-gradient(90deg,#ff4f9a,#ffc371);-webkit-background-clip:text;color:transparent;}
.hero p{opacity:.85;margin-top:15px;max-width:600px;line-height:1.5rem;}

/* Stats */
.stats{
display:grid;grid-template-columns:repeat(auto-fit,minmax(150px,1fr));gap:20px;
max-width:800px;margin:40px auto;
}
.stat{
background:var(--glass);backdrop-filter:var(--blur);border-radius:20px;padding:25px;text-align:center;
transition:all 0.5s;
}
.stat h3{font-size:2rem;color:var(--accent);transition:all 0.5s;}
.stat:hover{transform:scale(1.05);box-shadow:0 10px 25px rgba(0,0,0,.5);}

/* Sections */
section{padding:80px 20px;max-width:1100px;margin:auto;opacity:0;transform:translateY(50px);transition:all .8s ease;}
section.visible{opacity:1;transform:translateY(0);}
.card{background:var(--glass);backdrop-filter:var(--blur);border-radius:25px;padding:30px;margin-top:30px;}

/* Tabs */
.tabs{display:flex;gap:10px;flex-wrap:wrap;margin-top:20px;}
.tabs button{
background:none;border:1px solid #fff;color:#fff;padding:10px 20px;border-radius:30px;cursor:pointer;
transition:.3s;
}
.tabs button.active{background:#fff;color:#000;}

/* Timeline */
.timeline{border-left:3px solid var(--accent);padding-left:25px;margin-top:20px;}
.timeline div{margin-bottom:25px;position:relative;}
.timeline div::before{
content:"";position:absolute;left:-11px;top:0;width:20px;height:20px;background:var(--accent);border-radius:50%;
}

/* Badges */
.badges{display:grid;grid-template-columns:repeat(auto-fit,minmax(120px,1fr));gap:15px;margin-top:20px;}
.badge{padding:15px;border-radius:15px;background:linear-gradient(135deg,#ff4f9a,#ff8ccf);text-align:center;transition:0.3s;}
.badge:hover{transform:scale(1.1);box-shadow:0 0 20px rgba(255,255,255,0.7);}

/* Toast */
.toast{
position:fixed;bottom:20px;right:20px;background:#fff;color:#000;padding:15px 20px;border-radius:15px;display:none;
}

/* Buttons */
.btn{margin-top:20px;background:var(--accent);border:none;padding:12px 30px;border-radius:30px;color:#fff;cursor:pointer;transition:.3s;}
.btn:hover{transform:scale(1.1);}

/* Input */
input{padding:12px;border-radius:20px;border:none;margin-top:10px;width:220px;text-align:center;}

/* Confetti */
.fx{position:fixed;top:-20px;font-size:18px;animation:fall linear infinite;}
@keyframes fall{to{transform:translateY(120vh) rotate(360deg);opacity:0;}}

/* Fireworks */
.firework{
position:absolute;width:6px;height:6px;border-radius:50%;background:var(--accent);
animation:explode 1s linear forwards;
}
@keyframes explode{
0%{transform:scale(1);opacity:1;}
100%{transform:scale(3) translate(var(--x), var(--y));opacity:0;}
}

/* Dark Mode */
.dark{background:radial-gradient(circle at top,#0f1020,#1a1a2e);}
</style>
</head>

<body>

<!-- Preloader -->
<div id="preloader"><div class="loader"></div></div>

<!-- Navbar -->
<nav>
<h1>Abia ✨</h1>
<div>
<a href="#hero">Home</a>
<a href="#about">About</a>
<a href="#journey">Journey</a>
<a href="#achievements">Achievements</a>
<a href="#message">Message</a>
</div>
<button class="btn" onclick="toggleDark()">🌙 Mode</button>
</nav>

<!-- Hero Section -->
<section class="hero" id="hero">
<h2 id="typing"></h2>
<p>Welcome to your magical 14th birthday experience, Abia! 🎉</p>
<button class="btn" onclick="fireworks(event)">Celebrate 🎆</button>
</section>

<!-- Stats -->
<div class="stats">
<div class="stat"><h3>14</h3><p>Years of Magic</p></div>
<div class="stat"><h3>∞</h3><p>Dreams Ahead</p></div>
<div class="stat"><h3>100%</h3><p>Special</p></div>
</div>

<!-- About -->
<section id="about">
<h2>About Abia</h2>
<div class="card">
<p>Abia is a kind, bright, and amazing soul whose journey has just begun. This is a digital celebration of all the love and light she brings to the world.</p>
<div class="progress"><span id="prog"></span></div>
<button class="btn" onclick="grow()">See Growth</button>
</div>
</section>

<!-- Journey Timeline -->
<section id="journey">
<h2>Year 14 Journey</h2>
<div class="card timeline">
<div>🌸 Confidence Growth</div>
<div>✨ Dreams Expansion</div>
<div>💖 Kindness Deepened</div>
</div>
</section>

<!-- Achievements -->
<section id="achievements">
<h2>Achievements</h2>
<div class="card badges">
<div class="badge">Kind Soul 💕</div>
<div class="badge">Bright Smile 🌸</div>
<div class="badge">Strong Heart ✨</div>
<div class="badge">Unique Mind 💫</div>
</div>
</section>

<!-- Message -->
<section id="message">
<h2>Birthday Message</h2>
<div class="card">
<p>Happy 14th Birthday, Abia! Your journey is full of love, growth, and magic. Keep shining always.</p>
<button class="btn" onclick="notify()">Send Love 💖</button>
</div>
</section>

<div class="toast" id="toast">💖 Love sent!</div>

<script>
/* Preloader */
window.addEventListener("load",()=>{document.getElementById("preloader").style.display="none";});

/* Typing Effect */
const text="Happy 14th Birthday Abia 🎉✨";let i=0;
setInterval(()=>{if(i<text.length)document.getElementById("typing").innerHTML+=text[i++]},100);

/* Scroll Reveal */
const sections=document.querySelectorAll("section");
window.addEventListener("scroll",()=>{
sections.forEach(s=>{if(s.getBoundingClientRect().top<window.innerHeight-100)s.classList.add("visible");});
});

/* Progress Bar */
function grow(){document.getElementById("prog").style.width="100%";}

/* Toast */
function notify(){const t=document.getElementById("toast");t.style.display="block";setTimeout(()=>t.style.display="none",3000);}

/* Confetti */
setInterval(()=>{
let e=document.createElement("div");e.className="fx";e.innerHTML=["🎉","✨","💖","🌸","🎂","💫"][Math.floor(Math.random()*6)];
e.style.left=Math.random()*100+"vw";e.style.animationDuration=(3+Math.random()*4)+"s";document.body.appendChild(e);
setTimeout(()=>e.remove(),7000);
},250);

/* Dark Mode */
function toggleDark(){document.body.classList.toggle("dark");}

/* Fireworks */
function fireworks(e){
for(let i=0;i<20;i++){
let f=document.createElement("div");f.className="firework";
let angle=Math.random()*2*Math.PI;
let radius=100+Math.random()*50;
f.style.setProperty('--x',`${radius*Math.cos(angle)}px`);
f.style.setProperty('--y',`${radius*Math.sin(angle)}px`);
f.style.left=e.clientX+'px';
f.style.top=e.clientY+'px';
document.body.appendChild(f);
setTimeout(()=>f.remove(),1000);
}
}
</script>

</body>
</html>
