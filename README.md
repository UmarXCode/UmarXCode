<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Muhammad Umar Shah | Python Developer</title>

<style>
:root{
    --bg:#07111f;
    --bg2:#0d1a2d;
    --card:rgba(255,255,255,.07);
    --card2:rgba(255,255,255,.04);
    --text:#f5f8ff;
    --muted:#aebbd0;
    --line:rgba(255,255,255,.13);
    --accent:#72b7ff;
    --accent2:#a8d5ff;
    --shadow:0 20px 70px rgba(0,0,0,.30);
}
body.light{
    --bg:#f4f8fc;
    --bg2:#eaf1f8;
    --card:rgba(255,255,255,.78);
    --card2:rgba(255,255,255,.55);
    --text:#102238;
    --muted:#5d6c7f;
    --line:rgba(16,34,56,.13);
    --accent:#2375c7;
    --accent2:#67aef0;
    --shadow:0 20px 60px rgba(38,73,108,.12);
}
body.ocean{
    --bg:#031d25;
    --bg2:#07313b;
    --card:rgba(255,255,255,.07);
    --card2:rgba(255,255,255,.04);
    --text:#efffff;
    --muted:#a9c9ce;
    --line:rgba(255,255,255,.13);
    --accent:#5dd5d0;
    --accent2:#a0f2e9;
    --shadow:0 20px 70px rgba(0,0,0,.32);
}

*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{
    font-family:Inter,Segoe UI,Arial,sans-serif;
    background:
      radial-gradient(circle at 15% 10%,color-mix(in srgb,var(--accent) 18%,transparent),transparent 28%),
      radial-gradient(circle at 85% 30%,color-mix(in srgb,var(--accent2) 12%,transparent),transparent 25%),
      var(--bg);
    color:var(--text);
    line-height:1.7;
    overflow-x:hidden;
    transition:.45s ease;
}
a{color:inherit;text-decoration:none}
.container{width:min(1120px,92%);margin:auto}

.bg-grid{
    position:fixed;inset:0;pointer-events:none;opacity:.12;z-index:-2;
    background-image:linear-gradient(var(--line) 1px,transparent 1px),
                     linear-gradient(90deg,var(--line) 1px,transparent 1px);
    background-size:55px 55px;
    mask-image:linear-gradient(to bottom,black,transparent 90%);
}
.orb{
    position:fixed;width:320px;height:320px;border-radius:50%;
    filter:blur(70px);opacity:.14;pointer-events:none;z-index:-1;
    background:var(--accent);animation:float 12s ease-in-out infinite;
}
.orb.one{left:-150px;top:25%}
.orb.two{right:-160px;top:65%;animation-delay:-5s}
@keyframes float{50%{transform:translate(45px,-35px) scale(1.08)}}

nav{
    position:fixed;top:0;left:0;right:0;z-index:50;
    backdrop-filter:blur(18px);
    background:color-mix(in srgb,var(--bg) 75%,transparent);
    border-bottom:1px solid var(--line);
}
.nav-inner{height:72px;display:flex;align-items:center;justify-content:space-between}
.logo{font-weight:900;letter-spacing:2px}
.logo span{color:var(--accent)}
.nav-links{display:flex;gap:22px;font-size:14px;color:var(--muted)}
.nav-links a{transition:.25s}
.nav-links a:hover{color:var(--accent)}
.theme-box{display:flex;gap:7px}
.theme-box button{
    border:1px solid var(--line);background:var(--card);
    color:var(--text);border-radius:50%;width:30px;height:30px;
    cursor:pointer;transition:.25s;
}
.theme-box button:hover{transform:translateY(-2px);border-color:var(--accent)}

.hero{min-height:100vh;display:grid;place-items:center;padding:120px 0 70px}
.hero-grid{display:grid;grid-template-columns:1.25fr .75fr;gap:60px;align-items:center}
.eyebrow{
    display:inline-flex;align-items:center;gap:9px;
    padding:7px 13px;border:1px solid var(--line);border-radius:999px;
    background:var(--card);color:var(--accent);font-size:12px;
    text-transform:uppercase;letter-spacing:2px;font-weight:800;
}
.dot{width:7px;height:7px;background:var(--accent);border-radius:50%;box-shadow:0 0 18px var(--accent)}
h1{font-size:clamp(48px,7vw,86px);line-height:.95;margin:25px 0 20px;letter-spacing:-4px}
.gradient{
    background:linear-gradient(100deg,var(--text),var(--accent),var(--accent2));
    -webkit-background-clip:text;background-clip:text;color:transparent;
    background-size:220% auto;animation:shine 6s linear infinite;
}
@keyframes shine{to{background-position:220% center}}
.hero-role{font-size:clamp(20px,3vw,30px);color:var(--accent);font-weight:700}
.hero p{color:var(--muted);max-width:690px;margin-top:18px;font-size:17px}
.hero-buttons{display:flex;gap:12px;margin-top:30px;flex-wrap:wrap}
.btn{
    padding:12px 18px;border-radius:12px;border:1px solid var(--line);
    background:var(--card);font-weight:800;transition:.3s;
}
.btn.primary{background:var(--accent);color:#06111d;border-color:var(--accent)}
.btn:hover{transform:translateY(-4px);box-shadow:0 14px 35px color-mix(in srgb,var(--accent) 18%,transparent)}

.profile-card{
    padding:28px;border:1px solid var(--line);background:var(--card);
    border-radius:28px;box-shadow:var(--shadow);backdrop-filter:blur(20px);
    transform:rotate(2deg);transition:.5s;
}
.profile-card:hover{transform:rotate(0) translateY(-8px)}
.avatar{
    width:92px;height:92px;border-radius:24px;display:grid;place-items:center;
    background:linear-gradient(135deg,var(--accent),var(--accent2));
    color:#06111d;font-size:28px;font-weight:950;margin-bottom:22px;
}
.profile-card h3{font-size:24px}
.profile-card .mini{color:var(--muted);margin-top:4px}
.contact-list{margin-top:22px;display:grid;gap:13px}
.contact-item{display:flex;gap:11px;align-items:flex-start;color:var(--muted);font-size:14px}
.contact-item b{color:var(--text)}

section{padding:95px 0}
.section-head{margin-bottom:35px}
.kicker{color:var(--accent);font-size:12px;letter-spacing:3px;text-transform:uppercase;font-weight:900}
.section-head h2{font-size:clamp(32px,5vw,52px);line-height:1.1;margin-top:7px;letter-spacing:-2px}
.section-head p{color:var(--muted);max-width:700px;margin-top:10px}

.stats{display:grid;grid-template-columns:repeat(4,1fr);gap:16px;margin-top:25px}
.stat{
    padding:25px;border:1px solid var(--line);background:var(--card);
    border-radius:20px;transition:.35s;position:relative;overflow:hidden;
}
.stat:after{
    content:"";position:absolute;width:100px;height:100px;border-radius:50%;
    background:var(--accent);filter:blur(50px);opacity:.10;right:-35px;bottom:-35px;
}
.stat:hover{transform:translateY(-7px);border-color:var(--accent)}
.stat strong{font-size:32px;color:var(--accent);display:block}
.stat span{color:var(--muted);font-size:13px}

.about-box{
    padding:32px;border:1px solid var(--line);background:var(--card);
    border-radius:24px;box-shadow:var(--shadow)
}
.about-box p{color:var(--muted);font-size:17px}

.skills-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:16px}
.skill{
    padding:24px;border:1px solid var(--line);background:var(--card);
    border-radius:20px;transition:.35s;
}
.skill:hover{transform:translateY(-6px);border-color:var(--accent)}
.skill-top{display:flex;justify-content:space-between;gap:15px}
.skill-name{font-weight:800}
.level{color:var(--accent);font-size:12px;font-weight:800}
.bar{height:7px;background:var(--card2);border-radius:99px;margin-top:15px;overflow:hidden}
.bar i{display:block;height:100%;width:var(--w);background:linear-gradient(90deg,var(--accent),var(--accent2));border-radius:99px;transform-origin:left;animation:grow 1.3s ease both}
@keyframes grow{from{transform:scaleX(0)}to{transform:scaleX(1)}}

.timeline{position:relative;margin-top:20px}
.timeline:before{
    content:"";position:absolute;left:15px;top:0;bottom:0;width:1px;background:var(--line)
}
.experience{
    position:relative;padding:0 0 38px 52px;
}
.experience:last-child{padding-bottom:0}
.experience:before{
    content:"";position:absolute;left:9px;top:6px;width:13px;height:13px;
    border-radius:50%;background:var(--accent);box-shadow:0 0 0 6px color-mix(in srgb,var(--accent) 12%,transparent);
}
.exp-card{
    padding:25px;border:1px solid var(--line);background:var(--card);
    border-radius:20px;transition:.35s;
}
.exp-card:hover{transform:translateX(6px);border-color:var(--accent)}
.exp-top{display:flex;justify-content:space-between;gap:20px;flex-wrap:wrap}
.exp-card h3{font-size:21px}
.company{color:var(--accent);font-weight:800}
.date{color:var(--muted);font-size:13px}
.exp-role{margin-top:2px;font-weight:700}
.exp-card ul{margin:14px 0 0 18px;color:var(--muted)}
.exp-card li{margin:7px 0}

.edu-grid{display:grid;grid-template-columns:1fr 1fr;gap:18px}
.edu-card{
    padding:28px;border:1px solid var(--line);background:var(--card);
    border-radius:22px;transition:.35s;
}
.edu-card:hover{transform:translateY(-6px);border-color:var(--accent)}
.edu-year{color:var(--accent);font-size:13px;font-weight:900;letter-spacing:1px}
.edu-card h3{margin:7px 0 2px}
.edu-card p{color:var(--muted)}

.languages{display:flex;flex-wrap:wrap;gap:14px}
.lang{
    min-width:180px;padding:20px;border:1px solid var(--line);
    background:var(--card);border-radius:18px;
}
.lang b{display:block}.lang span{color:var(--accent);font-size:13px}

.no-project{
    padding:28px;border:1px dashed var(--line);border-radius:20px;
    color:var(--muted);background:var(--card2)
}

.contact-section{
    padding:60px 0 100px;
}
.contact-panel{
    padding:38px;border-radius:28px;border:1px solid var(--line);
    background:linear-gradient(135deg,var(--card),var(--card2));
    display:flex;justify-content:space-between;gap:30px;align-items:center;
}
.contact-panel h2{font-size:36px}
.contact-panel p{color:var(--muted);margin-top:8px}
footer{border-top:1px solid var(--line);padding:28px 0;color:var(--muted);font-size:13px}
.footer-inner{display:flex;justify-content:space-between;gap:20px;flex-wrap:wrap}

.reveal{opacity:0;transform:translateY(35px);transition:opacity .8s ease,transform .8s ease}
.reveal.show{opacity:1;transform:none}

@media(max-width:850px){
    .nav-links{display:none}
    .hero-grid{grid-template-columns:1fr;gap:35px}
    .profile-card{transform:none;max-width:600px}
    .stats{grid-template-columns:repeat(2,1fr)}
    .skills-grid,.edu-grid{grid-template-columns:1fr}
}
@media(max-width:520px){
    h1{letter-spacing:-2.5px}
    section{padding:70px 0}
    .stats{grid-template-columns:1fr 1fr;gap:10px}
    .stat{padding:18px}
    .stat strong{font-size:25px}
    .contact-panel{padding:26px;display:block}
    .contact-panel .btn{display:inline-block;margin-top:20px}
}
</style>

<style id="ultra-effects">
/* ===== EXTRA COLOR + MOTION LAYER ===== */
body{
    background:
      radial-gradient(circle at 10% 12%, rgba(0,225,255,.18), transparent 22%),
      radial-gradient(circle at 88% 18%, rgba(164,82,255,.18), transparent 22%),
      radial-gradient(circle at 70% 80%, rgba(0,255,170,.10), transparent 25%),
      var(--bg);
    background-attachment:fixed;
}
body:before{
    content:"";
    position:fixed;inset:-20%;z-index:-4;pointer-events:none;
    background:
      conic-gradient(from 0deg,
        transparent 0 18%,
        rgba(0,220,255,.08) 24%,
        transparent 32% 48%,
        rgba(150,70,255,.08) 56%,
        transparent 65% 82%,
        rgba(0,255,170,.06) 90%,
        transparent);
    filter:blur(35px);
    animation:megaSpin 25s linear infinite;
}
@keyframes megaSpin{to{transform:rotate(360deg)}}

.color-wave{
    position:fixed;left:0;right:0;top:72px;height:2px;z-index:49;
    background:linear-gradient(90deg,#00e5ff,#7c4dff,#ff4fd8,#00ffae,#00e5ff);
    background-size:300% 100%;
    animation:colorRun 5s linear infinite;
    box-shadow:0 0 18px rgba(0,229,255,.65);
}
@keyframes colorRun{to{background-position:300% 0}}

.cursor-glow{
    position:fixed;width:280px;height:280px;border-radius:50%;
    pointer-events:none;z-index:0;
    background:radial-gradient(circle,rgba(0,225,255,.12),rgba(120,60,255,.06),transparent 68%);
    transform:translate(-50%,-50%);
    mix-blend-mode:screen;
}
.particle{
    position:fixed;width:3px;height:3px;border-radius:50%;
    pointer-events:none;z-index:-1;
    background:var(--accent);
    box-shadow:0 0 12px currentColor;
    animation:particleFloat linear infinite;
}
@keyframes particleFloat{
    from{transform:translateY(110vh) scale(.4);opacity:0}
    12%{opacity:.8}
    88%{opacity:.8}
    to{transform:translateY(-15vh) scale(1.3);opacity:0}
}

section{position:relative}
section:before{
    content:"";
    position:absolute;left:50%;top:15px;
    width:120px;height:2px;transform:translateX(-50%);
    background:linear-gradient(90deg,transparent,var(--accent),#b86cff,transparent);
    opacity:.35;
}
.kicker{
    text-shadow:0 0 18px color-mix(in srgb,var(--accent) 45%,transparent);
}
.section-head h2{
    background:linear-gradient(90deg,var(--text),var(--accent),#c58cff,var(--text));
    background-size:250% auto;
    -webkit-background-clip:text;background-clip:text;color:transparent;
    animation:headingFlow 8s linear infinite;
}
@keyframes headingFlow{to{background-position:250% center}}

.eyebrow{
    box-shadow:0 0 0 1px rgba(0,225,255,.05),0 0 28px rgba(0,225,255,.08);
    animation:softPulse 3s ease-in-out infinite;
}
@keyframes softPulse{
    50%{box-shadow:0 0 0 1px rgba(150,90,255,.14),0 0 35px rgba(0,225,255,.15)}
}

.profile-card,.about-box,.skill,.stat,.exp-card,.edu-card,.lang,.no-project,.contact-panel{
    position:relative;overflow:hidden;
}
.profile-card:before,.about-box:before,.skill:before,.stat:before,
.exp-card:before,.edu-card:before,.lang:before,.no-project:before,.contact-panel:before{
    content:"";
    position:absolute;inset:-1px;
    border-radius:inherit;
    padding:1px;
    background:linear-gradient(120deg,transparent 15%,rgba(0,225,255,.55),rgba(150,80,255,.65),rgba(255,70,210,.45),transparent 85%);
    -webkit-mask:linear-gradient(#000 0 0) content-box,linear-gradient(#000 0 0);
    -webkit-mask-composite:xor;
    mask-composite:exclude;
    opacity:0;
    transition:.45s ease;
    pointer-events:none;
}
.profile-card:hover:before,.about-box:hover:before,.skill:hover:before,.stat:hover:before,
.exp-card:hover:before,.edu-card:hover:before,.lang:hover:before,.no-project:hover:before,.contact-panel:hover:before{
    opacity:1;
}
.profile-card:after,.about-box:after,.skill:after,.stat:after,.exp-card:after,.edu-card:after,.lang:after,.contact-panel:after{
    content:"";
    position:absolute;top:-100%;left:-30%;width:35%;height:300%;
    transform:rotate(25deg);
    background:linear-gradient(90deg,transparent,rgba(255,255,255,.16),transparent);
    transition:.8s ease;
    pointer-events:none;
}
.profile-card:hover:after,.about-box:hover:after,.skill:hover:after,.stat:hover:after,
.exp-card:hover:after,.edu-card:hover:after,.lang:hover:after,.contact-panel:hover:after{
    left:110%;
}

.stat:nth-child(1) strong{color:#00d9ff;text-shadow:0 0 20px rgba(0,217,255,.35)}
.stat:nth-child(2) strong{color:#9b70ff;text-shadow:0 0 20px rgba(155,112,255,.35)}
.stat:nth-child(3) strong{color:#ff68cf;text-shadow:0 0 20px rgba(255,104,207,.35)}
.stat:nth-child(4) strong{color:#40e6a0;text-shadow:0 0 20px rgba(64,230,160,.35)}

.skill:nth-child(1) .bar i{background:linear-gradient(90deg,#00d9ff,#43a8ff)}
.skill:nth-child(2) .bar i{background:linear-gradient(90deg,#7d6cff,#b66cff)}
.skill:nth-child(3) .bar i{background:linear-gradient(90deg,#ff5ccf,#ff8b67)}
.skill:nth-child(4) .bar i{background:linear-gradient(90deg,#00e6a8,#5ff2c8)}
.skill:nth-child(5) .bar i{background:linear-gradient(90deg,#ffc857,#ff8d5c)}
.skill:nth-child(6) .bar i{background:linear-gradient(90deg,#4cd9ff,#6f7cff)}
.skill:nth-child(7) .bar i{background:linear-gradient(90deg,#ff6b9d,#c86bff)}

.hero-buttons .btn.primary{
    background:linear-gradient(100deg,#00d9ff,#6f5cff,#e45bff,#00d9ff);
    background-size:250% auto;
    color:white;border:0;
    animation:buttonFlow 5s linear infinite;
}
@keyframes buttonFlow{to{background-position:250% center}}

.avatar{
    background:conic-gradient(from 0deg,#00d9ff,#6f5cff,#ff62d0,#00e6a8,#00d9ff);
    background-size:200% 200%;
    animation:avatarFlow 5s linear infinite, avatarFloat 4s ease-in-out infinite;
    box-shadow:0 0 35px rgba(0,217,255,.25);
}
@keyframes avatarFlow{to{background-position:200% 100%}}
@keyframes avatarFloat{50%{transform:translateY(-7px) rotate(-2deg)}}

.timeline:before{
    background:linear-gradient(to bottom,#00d9ff,#7b5cff,#ff63d0,#00e6a8);
}
.experience:before{
    background:conic-gradient(#00d9ff,#7b5cff,#ff63d0,#00e6a8,#00d9ff);
    box-shadow:0 0 0 5px rgba(0,217,255,.09),0 0 18px rgba(123,92,255,.45);
    animation:dotSpin 3s linear infinite;
}
@keyframes dotSpin{to{transform:rotate(360deg)}}

.lang:nth-child(1){box-shadow:inset 0 -2px 0 #00d9ff}
.lang:nth-child(2){box-shadow:inset 0 -2px 0 #7b5cff}
.lang:nth-child(3){box-shadow:inset 0 -2px 0 #ff63d0}

::-webkit-scrollbar{width:9px}
::-webkit-scrollbar-track{background:var(--bg)}
::-webkit-scrollbar-thumb{
    border-radius:20px;
    background:linear-gradient(#00d9ff,#7b5cff,#ff63d0);
}
::selection{background:#7b5cff;color:white}

@media(max-width:850px){
    .color-wave{top:72px}
}
</style>

</head>

<body>
<div class="color-wave"></div>
<div class="cursor-glow" id="cursorGlow"></div>

<div class="bg-grid"></div>
<div class="orb one"></div>
<div class="orb two"></div>

<nav>
    <div class="container nav-inner">
        <a class="logo" href="#home">M<span>US</span></a>
        <div class="nav-links">
            <a href="#about">About</a>
            <a href="#skills">Skills</a>
            <a href="#tech">Tech</a>
            <a href="#experience">Experience</a>
            <a href="#education">Education</a>
            <a href="#languages">Languages</a>
            <a href="#contact">Contact</a>
        </div>
        <div class="theme-box" aria-label="Theme selector">
            <button onclick="setTheme('dark')" title="Dark">D</button>
            <button onclick="setTheme('light')" title="Light">L</button>
            <button onclick="setTheme('ocean')" title="Ocean">O</button>
        </div>
    </div>
</nav>

<main id="home">
<section class="hero">
    <div class="container hero-grid">
        <div class="reveal">
            <div class="eyebrow"><i class="dot"></i> Python Developer & Machine Learning Specialist</div>
            <h1><span class="gradient">MUHAMMAD<br>UMAR SHAH</span></h1>
            <div class="hero-role">Python Developer & Machine Learning Specialist</div>
<p style="margin-top:10px;color:var(--accent2);font-weight:800;">Python · Data Science · DSA · Pandas · NumPy · AI/ML · Django · SQL</p>
            <p>
                An ambitious Junior Content Writer with a solid foundation in HTML, CSS, and C++,
                complemented by expert proficiency in MS Office and typing skills. Seeking to
                contribute to content development and digital projects within a professional setting,
                leveraging technical expertise and writing capabilities for impactful results.
            </p>
            <div class="hero-buttons">
                <a class="btn primary" href="#experience">View Experience</a>
                <a class="btn" href="#contact">Contact Me</a>
            </div>
        </div>

        <aside class="profile-card reveal">
            <div class="avatar">MUS</div>
            <h3>Muhammad Umar Shah</h3>
            <div class="mini">Python Developer & Machine Learning Specialist</div>

            <div class="contact-list">
                <div class="contact-item"><span>☎</span><b>+92 3283117175</b></div>
                <div class="contact-item"><span>✉</span><b>umarshah9786@gmail.com</b></div>
                <div class="contact-item"><span>⌖</span><b>House No. 118 Amna Park Block B Multan Road, Lahore</b></div>
            </div>
        </aside>
    </div>
</section>

<section id="about">
    <div class="container">
        <div class="section-head reveal">
            <div class="kicker">Profile</div>
            <h2>About Me</h2>
        </div>

        <div class="about-box reveal">
            <p>
                An ambitious Junior Content Writer with a solid foundation in HTML, CSS, and C++,
                complemented by expert proficiency in MS Office and typing skills. Seeking to
                contribute to content development and digital projects within a professional setting,
                leveraging my technical expertise and writing capabilities for impactful results.
            </p>
        </div>

        <div class="stats">
            <div class="stat reveal"><strong>6 Months</strong><span>Python Developer experience mentioned at Arfa Kareem Tower</span></div>
            <div class="stat reveal"><strong>3 Months</strong><span>Practical application at Ideoversity</span></div>
            <div class="stat reveal"><strong>1+ Year</strong><span>Freelance experience on Fiverr & Upwork</span></div>
            <div class="stat reveal"><strong>2025–2029</strong><span>Bachelor of Data Science</span></div>
        </div>
    </div>
</section>

<section id="skills">
    <div class="container">
        <div class="section-head reveal">
            <div class="kicker">Expertise</div>
            <h2>Skills</h2>
            <p>Skills and proficiency levels exactly as listed in the CV.</p>
        </div>

        <div class="skills-grid">
            <div class="skill reveal"><div class="skill-top"><span class="skill-name">Content Writer</span><span class="level">Junior</span></div><div class="bar"><i style="--w:45%"></i></div></div>
            <div class="skill reveal"><div class="skill-top"><span class="skill-name">HTML & CSS</span><span class="level">Intermediate</span></div><div class="bar"><i style="--w:70%"></i></div></div>
            <div class="skill reveal"><div class="skill-top"><span class="skill-name">C++</span><span class="level">Intermediate</span></div><div class="bar"><i style="--w:70%"></i></div></div>
            <div class="skill reveal"><div class="skill-top"><span class="skill-name">Typing Master</span><span class="level">Expert</span></div><div class="bar"><i style="--w:95%"></i></div></div>
            <div class="skill reveal"><div class="skill-top"><span class="skill-name">Kali Linux</span><span class="level">Basic</span></div><div class="bar"><i style="--w:30%"></i></div></div>
            <div class="skill reveal"><div class="skill-top"><span class="skill-name">MS Office</span><span class="level">Expert</span></div><div class="bar"><i style="--w:95%"></i></div></div>
            <div class="skill reveal"><div class="skill-top"><span class="skill-name">JavaScript</span><span class="level">Basic</span></div><div class="bar"><i style="--w:30%"></i></div></div>
        </div>
    </div>
</section>


<section id="tech">
    <div class="container">
        <div class="section-head reveal">
            <div class="kicker">Technical Identity</div>
            <h2>Python • Data Science • AI/ML</h2>
            <p>Focused around the technical identity you specified: Python, Data Science, DSA, Pandas, NumPy, AI/ML, Django and SQL.</p>
        </div>

        <div class="skills-grid">
            <div class="skill reveal">
                <div class="skill-top"><span class="skill-name">Python</span><span class="level">Core</span></div>
                <div class="bar"><i style="--w:92%"></i></div>
            </div>
            <div class="skill reveal">
                <div class="skill-top"><span class="skill-name">Data Science</span><span class="level">Focus</span></div>
                <div class="bar"><i style="--w:88%"></i></div>
            </div>
            <div class="skill reveal">
                <div class="skill-top"><span class="skill-name">DSA / Data Structures</span><span class="level">Focus</span></div>
                <div class="bar"><i style="--w:86%"></i></div>
            </div>
            <div class="skill reveal">
                <div class="skill-top"><span class="skill-name">Pandas</span><span class="level">Focus</span></div>
                <div class="bar"><i style="--w:86%"></i></div>
            </div>
            <div class="skill reveal">
                <div class="skill-top"><span class="skill-name">NumPy</span><span class="level">Focus</span></div>
                <div class="bar"><i style="--w:84%"></i></div>
            </div>
            <div class="skill reveal">
                <div class="skill-top"><span class="skill-name">AI / Machine Learning</span><span class="level">Focus</span></div>
                <div class="bar"><i style="--w:82%"></i></div>
            </div>
            <div class="skill reveal">
                <div class="skill-top"><span class="skill-name">Django</span><span class="level">Backend</span></div>
                <div class="bar"><i style="--w:88%"></i></div>
            </div>
            <div class="skill reveal">
                <div class="skill-top"><span class="skill-name">SQL / Databases</span><span class="level">Core</span></div>
                <div class="bar"><i style="--w:82%"></i></div>
            </div>
        </div>
    </div>
</section>

<section id="experience">
    <div class="container">
        <div class="section-head reveal">
            <div class="kicker">Career</div>
            <h2>Work Experience</h2>
        </div>

        <div class="timeline">
            <article class="experience reveal">
                <div class="exp-card">
                    <div class="exp-top">
                        <div><h3>Arfa Kareem Tower</h3><div class="company">Python Developer (Senior)</div></div>
                        <div class="date">2024 – PRESENT</div>
                    </div>
                    <ul>
                        <li>Results-driven Python Developer with 6 months of experience in developing and maintaining web applications at Arfa Kareem Tower. Proficient in leveraging frameworks such as Django and Flask to deliver high-quality software solutions.</li>
                        <li>Seeking to contribute technical skills and a passion for problem-solving in a challenging environment, while continuously enhancing development practices and fostering collaboration within a dynamic team.</li>
                    </ul>
                </div>
            </article>

            <article class="experience reveal">
                <div class="exp-card">
                    <div class="exp-top">
                        <div><h3>Ideoversity</h3><div class="company">Python Developer (Junior)</div></div>
                        <div class="date">2024 – PRESENT</div>
                    </div>
                    <ul>
                        <li>Motivated Junior Python Developer with six months of combined experience, including three months of practical application and three months of internship at Ideoversity. Eager to leverage my skills in Python and web development to contribute to innovative projects.</li>
                        <li>Committed to continuous learning and collaboration within a dynamic team environment, aiming to deliver effective software solutions that address real-world challenges.</li>
                    </ul>
                </div>
            </article>

            <article class="experience reveal">
                <div class="exp-card">
                    <div class="exp-top">
                        <div><h3>Fiverr & Upwork</h3><div class="company">Python Developer (Expert)</div></div>
                        <div class="date">2024 – 2025</div>
                    </div>
                    <ul>
                        <li>Experienced Python Developer (Expert) with over one year of freelance experience on Fiverr and Upwork, specializing in building scalable web applications and APIs. Adept at collaborating with clients to deliver tailored solutions that meet their specific needs.</li>
                        <li>Seeking to leverage my technical expertise and proven track record of client satisfaction in a challenging development role, while continuing to enhance my skills and contribute to innovative projects.</li>
                    </ul>
                </div>
            </article>
        </div>
    </div>
</section>

<section id="education">
    <div class="container">
        <div class="section-head reveal">
            <div class="kicker">Academic Background</div>
            <h2>Education</h2>
        </div>

        <div class="edu-grid">
            <article class="edu-card reveal">
                <div class="edu-year">2025 – 2029</div>
                <h3>Superior University</h3>
                <p>Bachelor Of Data Science.</p>
            </article>

            <article class="edu-card reveal">
                <div class="edu-year">2023 – 2024</div>
                <h3>Superior College</h3>
                <p>Intermediate (ICS) In Physics.</p>
            </article>
        </div>
    </div>
</section>

<section id="languages">
    <div class="container">
        <div class="section-head reveal">
            <div class="kicker">Communication</div>
            <h2>Languages</h2>
        </div>

        <div class="languages">
            <div class="lang reveal"><b>English</b><span>Fluent</span></div>
            <div class="lang reveal"><b>Urdu</b><span>Fluent</span></div>
            <div class="lang reveal"><b>Japanese</b><span>Basic</span></div>
        </div>
    </div>
</section>

<section id="projects">
    <div class="container">
        <div class="section-head reveal">
            <div class="kicker">Portfolio</div>
            <h2>Projects</h2>
        </div>
        <div class="no-project reveal">
            The provided CV does not contain a Projects section, so no projects have been added here.
        </div>
    </div>
</section>

<section id="contact" class="contact-section">
    <div class="container">
        <div class="contact-panel reveal">
            <div>
                <div class="kicker">Get In Touch</div>
                <h2>Contact</h2>
                <p>Phone: +92 3283117175 · Email: umarshah9786@gmail.com</p>
                <p>House No. 118 Amna Park Block B Multan Road, Lahore</p>
            </div>
            <a class="btn primary" href="mailto:umarshah9786@gmail.com">Email Me</a>
        </div>
    </div>
</section>
</main>

<footer>
    <div class="container footer-inner">
        <span>© Muhammad Umar Shah</span>
        <span>Python Developer & Machine Learning Specialist</span>
    </div>
</footer>

<script>
function setTheme(theme){
    document.body.classList.remove('light','ocean');
    if(theme !== 'dark') document.body.classList.add(theme);
    localStorage.setItem('portfolio-theme',theme);
}
const savedTheme = localStorage.getItem('portfolio-theme');
if(savedTheme) setTheme(savedTheme);

const observer = new IntersectionObserver((entries)=>{
    entries.forEach(entry=>{
        if(entry.isIntersecting) entry.target.classList.add('show');
    });
},{threshold:.12});

document.querySelectorAll('.reveal').forEach(el=>observer.observe(el));
</script>

<script>
/* colorful floating particles */
(function(){
    const count = 42;
    for(let i=0;i<count;i++){
        const p=document.createElement("span");
        p.className="particle";
        p.style.left=(Math.random()*100)+"vw";
        p.style.animationDuration=(7+Math.random()*14)+"s";
        p.style.animationDelay=(-Math.random()*18)+"s";
        p.style.opacity=(.25+Math.random()*.7);
        const hue=Math.floor(Math.random()*360);
        p.style.background=`hsl(${hue} 90% 65%)`;
        p.style.color=`hsl(${hue} 90% 65%)`;
        document.body.appendChild(p);
    }
})();

/* mouse-follow color glow */
const glow=document.getElementById("cursorGlow");
window.addEventListener("mousemove",e=>{
    if(glow){
        glow.style.left=e.clientX+"px";
        glow.style.top=e.clientY+"px";
    }
});

/* subtle 3D tilt on larger screens */
document.querySelectorAll(".skill,.stat,.edu-card,.lang").forEach(card=>{
    card.addEventListener("mousemove",e=>{
        if(window.innerWidth<900) return;
        const r=card.getBoundingClientRect();
        const x=(e.clientX-r.left)/r.width-.5;
        const y=(e.clientY-r.top)/r.height-.5;
        card.style.transform=`perspective(700px) rotateX(${-y*5}deg) rotateY(${x*5}deg) translateY(-5px)`;
    });
    card.addEventListener("mouseleave",()=>{
        card.style.transform="";
    });
});
</script>

</body>
</html>
