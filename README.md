<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Sandesh Gandhgule — 3D Visualiser Portfolio, Resume & Showreel.">
<meta name="theme-color" content="#080808">
<title>SANDESH GANDHGULE — 3D VISUALISER</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600&family=Playfair+Display:wght@500;600&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">

<style>
:root{
  --gold:#d4af37;
  --gold-soft:#ead58a;
  --bg:#080808;
  --surface:#101010;
  --surface-2:#151515;
  --text:#f4f2ed;
  --muted:#99958c;
  --muted-2:#69665f;
  --line:rgba(255,255,255,.105);
  --line-gold:rgba(212,175,55,.28);
  --ease:cubic-bezier(.2,.7,.2,1);
  --max:1500px;
}
*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{
  margin:0;background:var(--bg);color:var(--text);
  font-family:Poppins,sans-serif;
  overflow-x:hidden;
}
body.lock{overflow:hidden}
a{color:inherit}
button{font:inherit}
::selection{background:var(--gold);color:#080808}
::-webkit-scrollbar{width:7px}
::-webkit-scrollbar-track{background:#080808}
::-webkit-scrollbar-thumb{background:#34322c}
::-webkit-scrollbar-thumb:hover{background:var(--gold)}

.cursor-dot{
  position:fixed;width:7px;height:7px;border-radius:50%;
  background:var(--gold);pointer-events:none;z-index:5000;
  transform:translate(-50%,-50%);opacity:0;transition:opacity .2s;
}
@media(pointer:fine){.cursor-dot{opacity:1}}

header{
  position:fixed;top:0;left:0;right:0;z-index:1000;
  display:flex;justify-content:space-between;align-items:center;
  padding:24px 6.5%;transition:.45s var(--ease);
}
header.scrolled{
  padding:15px 6.5%;
  background:rgba(7,7,7,.82);
  backdrop-filter:blur(18px);
  -webkit-backdrop-filter:blur(18px);
  border-bottom:1px solid var(--line);
}
.logo{
  font:500 20px 'Playfair Display',serif;
  letter-spacing:3px;color:var(--gold);text-decoration:none;
}
.logo span{color:#fff}
nav{display:flex;gap:28px;align-items:center}
nav a{
  position:relative;font-size:10px;color:#aaa69e;
  letter-spacing:1.4px;text-transform:uppercase;text-decoration:none;
  padding:7px 0;
}
nav a:after{
  content:"";position:absolute;left:0;bottom:0;width:0;height:1px;
  background:var(--gold);transition:.35s var(--ease);
}
nav a:hover{color:#fff}
nav a:hover:after{width:100%}

.hero{
  min-height:100svh;position:relative;display:flex;
  align-items:flex-end;overflow:hidden;
}
.hero-media,.hero-media:after{position:absolute;inset:0}
.hero-media img{
  width:100%;height:100%;object-fit:cover;
  filter:brightness(.58);transform:scale(1.02);
  animation:heroIn 1.6s var(--ease) both;
}
.hero-media:after{
  content:"";
  background:
    linear-gradient(90deg,rgba(0,0,0,.5),transparent 60%),
    linear-gradient(to top,rgba(0,0,0,.98),rgba(0,0,0,.08) 66%,rgba(0,0,0,.38));
}
@keyframes heroIn{from{opacity:.3;transform:scale(1.08)}to{opacity:1;transform:scale(1.02)}}
.hero-content{
  position:relative;z-index:2;width:87%;max-width:var(--max);
  margin:auto;padding:0 0 9.5vh;
}
.eyebrow,.section-no,.category{
  font-size:9px;letter-spacing:2.8px;text-transform:uppercase;
  color:var(--gold);
}
.hero .eyebrow{margin-bottom:18px}
.hero h1{
  font:500 clamp(56px,9.2vw,148px)/.84 'Playfair Display',serif;
  letter-spacing:-5px;margin:0 0 25px;max-width:1250px;
}
.hero h1 span{color:var(--gold)}
.hero-sub{
  max-width:650px;color:#d0cdc6;font-size:13px;
  line-height:1.9;margin:0;
}
.hero-line{
  display:flex;align-items:center;gap:16px;margin-top:34px;
  color:#aaa69e;font-size:9px;letter-spacing:2px;text-transform:uppercase;
}
.hero-line:before{content:"";width:45px;height:1px;background:var(--gold)}

.actions{display:flex;gap:10px;flex-wrap:wrap;margin-top:28px}
.btn{
  display:inline-flex;align-items:center;justify-content:center;
  min-height:43px;padding:12px 20px;
  border:1px solid var(--line);font-size:9px;letter-spacing:1.6px;
  text-transform:uppercase;text-decoration:none;cursor:pointer;
  transition:.35s var(--ease);
}
.btn.primary{background:var(--gold);border-color:var(--gold);color:#080808}
.btn:hover{transform:translateY(-3px);border-color:var(--gold)}
.btn.ghost:hover{background:rgba(212,175,55,.07)}

.scroll-mark{
  position:absolute;right:6.5%;bottom:38px;z-index:3;
  writing-mode:vertical-rl;color:#77736b;font-size:8px;
  letter-spacing:2px;text-transform:uppercase;
}
.scroll-mark:before{content:"";display:block;width:1px;height:38px;background:var(--gold);margin:0 auto 10px}

.section{padding:125px 6.5%}
.section-inner{max-width:var(--max);margin:auto}
.dark{background:#0e0e0e}
.head{
  display:flex;justify-content:space-between;align-items:end;
  gap:60px;margin-bottom:48px;
}
.head h2{
  font:500 clamp(45px,6vw,82px)/.9 'Playfair Display',serif;
  letter-spacing:-2.5px;margin:13px 0 0;
}
.intro{
  max-width:500px;color:var(--muted);font-size:12px;
  line-height:1.95;margin-bottom:4px;
}
.numbered{
  display:flex;align-items:center;gap:14px;color:#5f5c56;
  font-size:8px;letter-spacing:2px;text-transform:uppercase;
}
.numbered:after{content:"";width:48px;height:1px;background:var(--line)}

.featured{
  position:relative;overflow:hidden;cursor:pointer;
  max-width:var(--max);margin:auto;
  border:1px solid rgba(255,255,255,.06);
}
.featured img{
  width:100%;height:min(73vh,760px);object-fit:cover;display:block;
  transition:1s var(--ease);filter:brightness(.78);
}
.featured:after{
  content:"";position:absolute;inset:0;
  background:linear-gradient(to top,rgba(0,0,0,.95),transparent 63%);
  pointer-events:none;
}
.featured:hover img{transform:scale(1.025);filter:brightness(.66)}
.featured .overlay{position:absolute;z-index:2;left:0;right:0;bottom:0;padding:110px 5% 38px}
.featured h3{
  font:500 clamp(36px,5.3vw,70px) 'Playfair Display',serif;
  letter-spacing:-1.5px;margin:9px 0;
}
.meta{font-size:10px;color:#bbb7ae;letter-spacing:.5px}
.arrow{margin-top:12px;color:var(--gold);font-size:10px;letter-spacing:1px;transition:.3s}
.featured:hover .arrow{transform:translateX(6px)}

.filters{
  display:flex;gap:7px;flex-wrap:wrap;margin-bottom:38px;
  position:sticky;top:76px;z-index:20;padding:8px 0;
  background:linear-gradient(#0e0e0e 75%,transparent);
}
.filter{
  background:rgba(255,255,255,.015);border:1px solid var(--line);
  color:#96928a;padding:10px 14px;font-size:8px;letter-spacing:1.4px;
  text-transform:uppercase;cursor:pointer;border-radius:0;
  transition:.3s var(--ease);
}
.filter:hover,.filter.active{
  background:var(--gold);border-color:var(--gold);color:#080808;
}

.grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
.project{cursor:pointer;animation:cardIn .7s var(--ease) both}
.project.hide{display:none}
@keyframes cardIn{from{opacity:0;transform:translateY(15px)}to{opacity:1;transform:none}}
.card{
  position:relative;min-height:390px;overflow:hidden;
  background:var(--surface);border:1px solid rgba(255,255,255,.055);
  isolation:isolate;
}
.card:before{
  content:"";position:absolute;inset:0;z-index:3;
  border:1px solid transparent;transition:.4s;pointer-events:none;
}
.card:hover:before{border-color:rgba(212,175,55,.45)}
.card img,.card video{
  width:100%;height:100%;min-height:390px;object-fit:cover;
  display:block;transition:1s var(--ease);
}
.card:after{
  content:"";position:absolute;inset:0;
  background:linear-gradient(to top,rgba(0,0,0,.95),transparent 65%);
  pointer-events:none;z-index:1;
}
.card:hover img,.card:hover video{transform:scale(1.045);filter:brightness(.72)}
.count,.single{
  position:absolute;z-index:4;top:14px;
  background:rgba(0,0,0,.55);backdrop-filter:blur(8px);
  color:#ddd;font-size:8px;letter-spacing:1.3px;text-transform:uppercase;
}
.count{right:14px;padding:7px 10px;border:1px solid rgba(212,175,55,.45);color:var(--gold)}
.single{left:14px;padding:7px 9px;border:1px solid rgba(255,255,255,.15)}
.overlay{position:absolute;z-index:2;left:0;right:0;bottom:0;padding:80px 22px 22px}
.overlay h3{
  font:500 25px 'Playfair Display',serif;
  letter-spacing:-.4px;margin:7px 0;
}
.project:hover .arrow{transform:translateX(5px)}
.wide{grid-column:span 2}
.wide .card,.wide .card img{min-height:500px}

.video-card:before{
  content:"▶";position:absolute;z-index:4;top:50%;left:50%;
  width:55px;height:55px;margin:-27px 0 0 -27px;
  display:flex;align-items:center;justify-content:center;
  border:1px solid rgba(212,175,55,.7);border-radius:50%;
  color:var(--gold);background:rgba(0,0,0,.45);
  backdrop-filter:blur(8px);font-size:14px;padding-left:2px;
  transition:.35s;pointer-events:none;
}
.video-card:hover:before{transform:scale(1.08);background:var(--gold);color:#080808}

.detail{
  display:none;position:fixed;inset:0;z-index:1800;
  background:rgba(4,4,4,.985);overflow:auto;
  padding:95px 6.5% 55px;
}
.detail.open{display:block}
.detail-inner{max-width:var(--max);margin:auto}
.detail-top{
  display:flex;justify-content:space-between;gap:30px;
  padding-bottom:30px;margin-bottom:30px;
  border-bottom:1px solid var(--line);
}
.detail-top h2{
  font:500 clamp(40px,5.5vw,76px)/.92 'Playfair Display',serif;
  letter-spacing:-2px;margin:11px 0;
}
.detail-desc{max-width:700px;color:var(--muted);font-size:12px;line-height:1.9}
.close-detail{
  flex:0 0 auto;width:46px;height:46px;background:transparent;
  border:1px solid var(--line);color:var(--gold);font-size:25px;cursor:pointer;
  transition:.3s;
}
.close-detail:hover{background:var(--gold);color:#000}
.detail-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:14px}
.detail-item{
  position:relative;overflow:hidden;cursor:pointer;
  background:#111;border:1px solid rgba(255,255,255,.06);
}
.detail-item img{
  width:100%;aspect-ratio:16/10;object-fit:cover;display:block;
  transition:.55s var(--ease);
}
.detail-item:hover img{transform:scale(1.025);filter:brightness(.8)}
.caption{
  position:absolute;left:0;right:0;bottom:0;
  padding:45px 18px 15px;
  background:linear-gradient(transparent,rgba(0,0,0,.9));
  font-size:9px;color:#ddd;letter-spacing:.3px;
}
.detail-item:after{
  content:"VIEW";position:absolute;right:13px;top:13px;
  padding:6px 8px;border:1px solid rgba(212,175,55,.45);
  color:var(--gold);background:rgba(0,0,0,.55);
  font-size:7px;letter-spacing:1.5px;opacity:0;transition:.3s;
}
.detail-item:hover:after{opacity:1}

.lightbox{
  display:none;position:fixed;z-index:2200;inset:0;
  background:rgba(0,0,0,.99);backdrop-filter:blur(12px);
  align-items:center;justify-content:center;padding:20px;
}
.lightbox.open{display:flex}
.lb-content{
  width:min(1300px,95vw);height:min(93vh,920px);
  display:flex;flex-direction:column;align-items:center;
}
.lb-head{width:100%;display:flex;justify-content:space-between;margin-bottom:10px}
.lb-title{font:500 21px 'Playfair Display',serif}
.lb-counter{color:var(--gold);font-size:10px;letter-spacing:1px}
.lb-main{
  position:relative;flex:1;min-height:0;width:100%;
  display:flex;align-items:center;justify-content:center;
  background:radial-gradient(circle,rgba(255,255,255,.035),transparent 60%);
}
.lb-main img{
  max-width:90%;max-height:100%;object-fit:contain;
  box-shadow:0 25px 70px #000;transition:.2s;
}
.lb-close,.lb-prev,.lb-next{
  position:absolute;z-index:3;color:var(--gold);cursor:pointer;user-select:none;
}
.lb-close{top:14px;right:24px;font-size:42px}
.lb-prev,.lb-next{top:50%;transform:translateY(-50%);font-size:42px;padding:18px}
.lb-prev{left:0}.lb-next{right:0}
.lb-caption{margin:10px 0;color:var(--gold);font-size:11px}
.thumbs{
  width:100%;display:flex;gap:8px;overflow-x:auto;padding:8px 2px;
  scrollbar-width:thin;
}
.thumb{
  width:78px;height:52px;flex:0 0 auto;object-fit:cover;
  opacity:.4;border:1px solid transparent;border-radius:2px;cursor:pointer;
}
.thumb.active{opacity:1;border-color:var(--gold);box-shadow:0 0 0 1px rgba(212,175,55,.25)}

.resume-grid{
  display:grid;grid-template-columns:1.05fr 1.95fr;gap:18px;
}
.profile-panel,.skills-panel{
  border:1px solid var(--line);background:#0d0d0d;padding:35px;
}
.profile-panel h3,.skills-panel h3{
  font:500 28px 'Playfair Display',serif;margin:12px 0 15px;
}
.profile-panel p,.skill p,.about p{
  color:var(--muted);font-size:12px;line-height:1.9;
}
.profile-mark{
  font:500 clamp(45px,6vw,78px) 'Playfair Display',serif;
  color:var(--gold);line-height:.85;margin-bottom:30px;
}
.skill-list{
  display:grid;grid-template-columns:repeat(2,1fr);
  border-top:1px solid var(--line);border-left:1px solid var(--line);
}
.skill{
  min-height:190px;padding:24px;border-right:1px solid var(--line);
  border-bottom:1px solid var(--line);
}
.skill-no{color:var(--gold);font-size:8px;letter-spacing:2px}
.skill h4{font:500 21px 'Playfair Display',serif;margin:34px 0 8px}
.resume-note{margin-top:18px;color:var(--muted);font-size:11px;line-height:1.8}

.showreel{
  position:relative;min-height:78vh;overflow:hidden;
  border-top:1px solid var(--line);border-bottom:1px solid var(--line);
}
.showreel video{width:100%;height:78vh;object-fit:cover;filter:brightness(.43)}
.showreel:after{
  content:"";position:absolute;inset:0;
  background:linear-gradient(to top,rgba(0,0,0,.8),rgba(0,0,0,.08));
}
.reel-overlay{
  position:absolute;z-index:2;inset:0;display:flex;
  flex-direction:column;align-items:center;justify-content:center;
  text-align:center;padding:30px;
}
.reel-overlay h2{
  font:500 clamp(45px,7vw,95px)/.88 'Playfair Display',serif;
  letter-spacing:-3px;max-width:1000px;margin:18px 0 30px;
}

.processes{
  display:grid;grid-template-columns:repeat(5,1fr);
  border-top:1px solid var(--line);border-left:1px solid var(--line);
}
.process{
  padding:28px 20px;min-height:210px;
  border-right:1px solid var(--line);border-bottom:1px solid var(--line);
}
.process h3{font:500 22px 'Playfair Display',serif;margin:35px 0 8px}
.process p{color:var(--muted);font-size:11px;line-height:1.8}

.about{
  display:grid;grid-template-columns:.85fr 1.15fr;gap:100px;
  max-width:var(--max);margin:0 auto;
}
.about blockquote{
  font:500 clamp(40px,5vw,70px)/.94 'Playfair Display',serif;
  letter-spacing:-2px;margin:0;
}
.about blockquote span{color:var(--gold)}
.about strong{color:#fff;font-weight:500}
.tags{display:flex;gap:7px;flex-wrap:wrap;margin-top:24px}
.tags span{
  border:1px solid var(--line);padding:8px 11px;color:#aaa;
  font-size:8px;text-transform:uppercase;letter-spacing:1px;
}

.contact{
  text-align:center;padding:165px 7%;
  background:
    radial-gradient(circle at center,rgba(212,175,55,.09),transparent 34%),
    #080808;
}
.contact h2{
  font:500 clamp(52px,8vw,110px)/.88 'Playfair Display',serif;
  letter-spacing:-4px;margin:15px 0 25px;
}
.contact p{max-width:560px;margin:auto;color:var(--muted);font-size:12px;line-height:1.9}
.contact .actions{justify-content:center}

footer{
  display:flex;justify-content:space-between;gap:20px;
  padding:28px 6.5%;background:#060606;color:#5e5b55;font-size:9px;
  letter-spacing:1px;text-transform:uppercase;
}
.whatsapp{
  position:fixed;z-index:1200;right:22px;bottom:22px;
  width:50px;height:50px;display:flex;align-items:center;justify-content:center;
  border-radius:50%;background:#25d366;color:#fff;text-decoration:none;
  font-size:21px;box-shadow:0 12px 35px rgba(0,0,0,.4);
  transition:.3s;
}
.whatsapp:hover{transform:translateY(-4px) scale(1.04)}

.reveal{opacity:0;transform:translateY(25px);transition:opacity .8s var(--ease),transform .8s var(--ease)}
.reveal.visible{opacity:1;transform:none}

@media(max-width:1100px){
  .grid{grid-template-columns:repeat(2,1fr)}
  .resume-grid{grid-template-columns:1fr}
  .processes{grid-template-columns:repeat(2,1fr)}
  .about{grid-template-columns:1fr;gap:45px}
}
@media(max-width:700px){
  header{padding:17px 5%}
  header.scrolled{padding:13px 5%}
  .logo{font-size:17px;letter-spacing:2px}
  nav{gap:13px}
  nav a{font-size:8px;letter-spacing:.8px}
  nav a:nth-child(3){display:none}
  .hero-content{width:90%;padding-bottom:70px}
  .hero h1{font-size:52px;letter-spacing:-2.5px}
  .hero-sub{font-size:11px}
  .scroll-mark{display:none}
  .section{padding:82px 5%}
  .head{display:block;margin-bottom:35px}
  .head h2{font-size:48px}
  .intro{margin-top:18px}
  .featured img{height:62vh}
  .featured .overlay{padding:90px 22px 24px}
  .featured h3{font-size:38px}
  .filters{top:61px;overflow-x:auto;flex-wrap:nowrap;padding-bottom:10px}
  .filter{flex:0 0 auto}
  .grid{grid-template-columns:1fr}
  .wide{grid-column:auto}
  .card,.card img,.card video{min-height:340px}
  .wide .card,.wide .card img{min-height:340px}
  .overlay{padding:75px 18px 18px}
  .overlay h3{font-size:23px}
  .detail{padding:80px 5% 30px}
  .detail-grid{grid-template-columns:1fr}
  .detail-top{gap:12px}
  .detail-top h2{font-size:43px}
  .detail-item:after{display:none}
  .resume-grid{gap:12px}
  .profile-panel,.skills-panel{padding:25px}
  .skill-list{grid-template-columns:1fr}
  .processes{grid-template-columns:1fr}
  .process{border-right:1px solid var(--line)}
  .about blockquote{font-size:45px}
  .showreel,.showreel video{min-height:65vh;height:65vh}
  .reel-overlay h2{font-size:51px;letter-spacing:-2px}
  .contact{padding:120px 7%}
  .contact h2{font-size:58px;letter-spacing:-2px}
  footer{display:block;text-align:center;line-height:2}
  .lb-content{width:100%;height:90vh}
  .lb-main img{max-width:94%}
  .lb-prev,.lb-next{font-size:30px;padding:10px}
}
@media(prefers-reduced-motion:reduce){
  *,*:before,*:after{scroll-behavior:auto!important;animation:none!important;transition:none!important}
}
</style>
</head>

<body>
<div class="cursor-dot" id="cursor-dot"></div>

<header id="header">
  <a class="logo" href="#top">SANDESH <span>GANDHGULE</span></a>
  <nav>
    <a href="#work">Portfolio</a>
    <a href="#resume">Resume</a>
    <a href="#about">About</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<section class="hero" id="top">
  <div class="hero-media">
    <img src="RE_01_NB.png" alt="Sandesh Gandhgule — 3D Visualiser">
  </div>
  <div class="hero-content">
    <div class="eyebrow">3D VISUALISER · ARCHITECTURAL VISUALIZATION</div>
    <h1>SANDESH<br><span>GANDHGULE</span><br>3D VISUALISER.</h1>
    <p class="hero-sub">I create high-fidelity architectural visuals, interiors, exteriors, elevations and cinematic walkthroughs that turn design concepts into clear, realistic experiences.</p>
    <div class="actions">
      <a class="btn primary" href="#work">View Portfolio</a>
      <a class="btn ghost" href="#resume">View Resume</a>
    </div>
    <div class="hero-line">Portfolio · Resume · Showreel</div>
  </div>
  <div class="scroll-mark">Scroll to explore</div>
</section>

<section class="section" id="work">
  <div class="section-inner">
    <div class="head reveal">
      <div>
        <div class="section-no">01 / Portfolio</div>
        <h2>Selected Work</h2>
      </div>
      <div class="intro">A selection of my architectural visualization work. Each project remains grouped as a complete visual package, whether it contains one render or a full set of views.</div>
    </div>
<div class="featured" data-project-id="featured" data-title="Modern Residential Architecture" data-type="Residential Elevation" data-description="Exterior architectural visualization and elevation presentation." data-gallery='[{"src":"RE_01_F.png","caption":"Front Elevation"},{"src":"FRS.jpg","caption":"Perspective View"},{"src":"opt ss 2.jpg","caption":"Elevation Detail"},{"src":"opt ss.jpg","caption":"Alternative View"}]'><img src="DA 1.jpg" alt="Modern Residential Architecture"><div class="overlay"><div class="category">Featured Project</div><h3>Modern Residential Architecture</h3><div class="meta">Exterior Visualization · 04 Visuals</div><div class="arrow">View project →</div></div></div></section>
  </div>
</section>

<section class="section dark">
  <div class="section-inner">
    <div class="head reveal">
      <div>
        <div class="section-no">02 / Portfolio Archive</div>
        <h2>My Visual Work</h2>
      </div>
      <div class="intro">Browse my work by category. Multiple renders from the same project stay together, while individual visual studies remain independent.</div>
    </div>

    <div class="filters">
      <button class="filter active" data-filter="all">All</button>
      <button class="filter" data-filter="residential">Residential</button>
      <button class="filter" data-filter="commercial">Commercial</button>
      <button class="filter" data-filter="front">Front Elevations</button>
      <button class="filter" data-filter="interior">Interiors</button>
      <button class="filter" data-filter="exterior">Exteriors</button>
      <button class="filter" data-filter="walkthrough">Walkthroughs</button>
      <button class="filter" data-filter="plans">2D / 3D</button>
    </div>

    <div class="grid" id="grid">


<article class="project residential " data-title="Modern Residence 01" data-type="Residential Elevation" data-description="Residential exterior visualization package containing front, perspective and night views." data-gallery='[{"src":"RE_01_F.png","caption":"Front Elevation"},{"src":"RE_01_P1.jpg","caption":"Perspective View"},{"src":"RE_01_P3.jpg","caption":"Perspective View"},{"src":"RE_01_NB.png","caption":"Night View"},{"src":"RE_01_NB2.jpg","caption":"Night View"},{"src":"RE_01_N.jpg","caption":"Night View"}]'><div class="card"><img src="RE_01_P1.jpg" alt="Modern Residence 01"><span class="count">06 VISUALS</span><div class="overlay"><div class="category">Residential Elevation</div><h3>Modern Residence 01</h3><div class="meta">Exterior Visualization</div><div class="arrow">View project →</div></div></div></article>

<article class="project residential" data-title="Modern Residence 02" data-type="Residential Elevation" data-description="Residential elevation visualization package." data-gallery='[{"src":"RE_02_F.jpg","caption":"Front Elevation"},{"src":"RE_02_P1.jpg","caption":"Perspective View"},{"src":"RE_02_T.jpg","caption":"Elevation Detail"},{"src":"RE_02_N.jpg","caption":"Night View"}]'><div class="card"><img src="DA 1.jpg" alt="Modern Residence 02"><span class="count">04 VISUALS</span><div class="overlay"><div class="category">Residential Elevation</div><h3>Modern Residence 02</h3><div class="meta">Exterior Visualization</div><div class="arrow">View project →</div></div></div></article>

<article class="project residential" data-title="Modern Residence 03" data-type="Residential Elevation" data-description="Single hero visualization for a residential elevation." data-gallery='[{"src":"RE_03_F.jpg","caption":"Main Elevation"},{"src":"RE_03_P.jpg","caption":"Perspective View"},{"src":"RE_03_S.jpg","caption":"Perspective View"},{"src":"RE_03_H.png","caption":"Perspective View"}]'><div class="card"><img src="RE_03_F.jpg" alt="Modern Residence 03"><span class="count">04 VISUAL</span><div class="overlay"><div class="category">Residential Elevation</div><h3>Modern Residence 03</h3><div class="meta">Single Elevation Render</div><div class="arrow">View project →</div></div></div></article>

<article class="project residential" data-title="Modern Residence 04" data-type="Residential Elevation" data-description="Single hero visualization for a residential elevation." data-gallery='[{"src":"RE_04_PR.jpg","caption":"Main Elevation"},{"src":"RE_04_FV.jpg","caption":"Front View"},{"src":"RE_04_RV.jpg","caption":"Right View"},{"src":"RE_04_LV.jpg","caption":"Left View"},{"src":"RE_04_PL.jpg","caption":"Perspective Left View"},{"src":"RE_04_D.jpg","caption":"Day View"},{"src":"RE_04_N.png","caption":"Night View"},{"src":"RE_04_CC.jpg","caption":"Color Combinations"}]'><div class="card"><img src="RE_04_PR.jpg" alt="Modern Residence 04"><span class="count">08 VISUAL</span><div class="overlay"><div class="category">Residential Elevation</div><h3>Modern Residence 04</h3><div class="meta">Single Elevation Render</div><div class="arrow">View project →</div></div></div></article>

<article class="project residential" data-title="Modern Residence 05" data-type="Residential Elevation" data-description="Single hero visualization for a residential elevation." data-gallery='[{"src":"BE_05_ P.jpg","caption":"Main Elevation"},{"src":"BE_05_F.jpg","caption":"Front View"},{"src":"BE_05_R.jpg","caption":"Right View"},{"src":"BE_05_N.jpg","caption":"Night View"},{"src":"BE_05_CC.jpg","caption":"Color Combinations"}]'><div class="card"><img src="BE_05_ P.jpg" alt="Modern Residence 05"><span class="count">05 VISUAL</span><div class="overlay"><div class="category">Residential Elevation</div><h3>Modern Residence 05</h3><div class="meta">Single Elevation Render</div><div class="arrow">View project →</div></div></div></article>

<article class="project residential" data-title="Modern Residence 06" data-type="Residential Elevation" data-description="Single hero visualization for a residential elevation." data-gallery='[{"src":"RE_06_P.jpg","caption":"Main Elevation"},{"src":"RE_06_F.jpg","caption":"Front View"},{"src":"RE_06_R.jpg","caption":"Right View"},{"src":"RE_06_D.jpg","caption":"Day View"},{"src":"RE_06_N.jpg","caption":"Night View"},{"src":"RE_06_CC.jpg","caption":"Color Combinations"}]'><div class="card"><img src="RE_06_P.jpg" alt="Modern Residence 06"><span class="count">07 VISUAL</span><div class="overlay"><div class="category">Residential Elevation</div><h3>Modern Residence 06</h3><div class="meta">Single Elevation Render</div><div class="arrow">View project →</div></div></div></article>
    
<article class="project front" data-title="Front Elevation 01" data-type="Front Elevation" data-description="Focused front-elevation presentation." data-gallery='[{"src":"NC_P.jpg","caption":"Perspective Elevation"},{"src":"NC_F.jpg","caption":"Front Elevation"},{"src":"NC_S.jpg","caption":"Side Elevation"},{"src":"NC_01.jpg","caption":"Perspective Elevation"},{"src":"NC_T.jpg","caption":"Top View"},{"src":"NC_N.jpg","caption":"Night Elevation"},{"src":"NC_cco.jpg","caption":"Option Elevation"}]'><div class="card"><img src="NC_P.jpg" alt="Front Elevation 01"><span class="single">Single Visual</span><span class="count">07 VISUAL</span><div class="overlay"><div class="category">Front Elevation</div><h3>Front Elevation 01</h3><div class="meta">Architectural Visualization</div><div class="arrow">View project →</div></div></div></article>

<article class="project front" data-title="Front Elevation 02" data-type="Front Elevation" data-description="Two-view front elevation visualization." data-gallery='[{"src":"S_perspective.jpg","caption":"Front Perspective"},{"src":"S_front.jpg","caption":"Front Elevation"},{"src":"S_side.jpg","caption":"Side Elevation"},{"src":"S_back.jpg","caption":"Back Perspective"},{"src":"S_night.jpg","caption":"Night View"},{"src":"S_view.jpg","caption":"Optional Elevation"},{"src":"S_cc.jpg","caption":"Color Combinations"}]'><div class="card"><img src="S_perspective.jpg" alt="Front Elevation 02"><span class="count">07 VISUALS</span><div class="overlay"><div class="category">Front Elevation</div><h3>Front Elevation 02</h3><div class="meta">Exterior Visualization</div><div class="arrow">View project →</div></div></div></article>

<article class="project commercial" data-title="Commercial Architecture 01" data-type="Commercial Elevation" data-description="Commercial architectural visualization package." data-gallery='[{"src":"CR1.jpg","caption":"Perspective View"},{"src":"CR2.jpg","caption":"Eagel Eye View"},{"src":"CR3.jpg","caption":"Main Entrance"},{"src":"CR5.jpg","caption":"Entrance 2"},{"src":"CR2n.jpg","caption":"Night View"},{"src":"CR N.png","caption":"Night View2"},{"src":"CR6.jpg","caption":"Exterior Detail"}]'><div class="card"><img src="CR1.jpg" alt="Commercial Architecture 01"><span class="count">08 VISUALS</span><div class="overlay"><div class="category">Commercial Elevation</div><h3>Commercial Architecture 01</h3><div class="meta">Exterior Visualization</div><div class="arrow">View project →</div></div></div></article>

<article class="project commercial" data-title="Commercial Architecture 02" data-type="Commercial Elevation" data-description="Commercial architectural visualization package." data-gallery='[{"src":"CR_02_F.jpg","caption":"Front View"},{"src":"CR_02_P.jpg","caption":"Perspective View 01"},{"src":"CR_02_P2.jpg","caption":"Perspective View 02"},{"src":"CR_02_N.jpg","caption":"Night View"},{"src":"CR_02_OA.jpg","caption":"Optional View"}]'><div class="card"><img src="CR_02_F.jpg" alt="Commercial Architecture 02"><span class="count">05 VISUALS</span><div class="overlay"><div class="category">Commercial Elevation</div><h3>Commercial Architecture 02</h3><div class="meta">Exterior Visualization</div><div class="arrow">View project →</div></div></div></article>

<article class="project interior" data-title="Luxury Interior 01" data-type="Interior Visualization" data-description="Luxury interior package covering living, dining and kitchen spaces." data-gallery='[{"src":"IDL_201.jpg","caption":"Living / Lounge Area"},{"src":"IDL_202.jpg","caption":"Dining Area"},{"src":"IDL_203.jpg","caption":"Kitchen View"},{"src":"IDL_204.jpg","caption":"Kitchen Detail"}]'><div class="card"><img src="IDL_201.jpg" alt="Luxury Interior 01"><span class="count">04 VISUALS</span><div class="overlay"><div class="category">Interior</div><h3>Luxury Interior 01</h3><div class="meta">Interior Visualization</div><div class="arrow">View project →</div></div></div></article>

<article class="project interior" data-title="Luxury Interior 02" data-type="Interior Visualization" data-description="Luxury interior visualization package with multiple spatial views." data-gallery='[{"src":"IDL_101.jpg","caption":"Interior Overview"},{"src":"IDL_102.jpg","caption":"Living Room"},{"src":"IDL_103.jpg","caption":"Dining Area"},{"src":"IDL_104.png","caption":"Bar Area"},{"src":"IDL_105.jpg","caption":"Bar Area"},{"src":"IDL_106.png","caption":"Bar Area"}]'><div class="card"><img src="IDL_102.jpg" alt="Luxury Interior 02"><span class="count">06 VISUALS</span><div class="overlay"><div class="category">Interior</div><h3>Luxury Interior 02</h3><div class="meta">Interior Visualization</div><div class="arrow">View project →</div></div></div></article>

<article class="project interior" data-title="Luxury Interior 03" data-type="Interior Visualization" data-description="Bedroom and private interior visualization package." data-gallery='[{"src":"GLV.jpg","caption":"Bedroom / Lounge"},{"src":"bdr.jpg","caption":"Bedroom"},{"src":"BDM1.jpg","caption":"Bedroom Detail"},{"src":"BD3.jpg","caption":"Bedroom Perspective"}]'><div class="card"><img src="GLV.jpg" alt="Luxury Interior 03"><span class="count">04 VISUALS</span><div class="overlay"><div class="category">Interior</div><h3>Luxury Interior 03</h3><div class="meta">Interior Visualization</div><div class="arrow">View project →</div></div></div></article>

<article class="project exterior" data-title="Exterior Visualization 01" data-type="Exterior Visualization" data-description="Exterior architectural environment visualization." data-gallery='[{"src":"SS.jpg","caption":"Exterior Perspective"},{"src":"opt ss 2.jpg","caption":"Exterior View"}]'><div class="card"><img src="SS.jpg" alt="Exterior Visualization 01"><span class="count">02 VISUALS</span><div class="overlay"><div class="category">Exterior</div><h3>Exterior Visualization 01</h3><div class="meta">Architectural Environment</div><div class="arrow">View project →</div></div></div></article>

<article class="project plans" data-title="Sectional Presentation" data-type="2D / 3D" data-description="Architectural drawings and sectional visualization." data-gallery='[{"src":"FLOORP0.jpg","caption":"Floor Plan / Sectional 01"},{"src":"FLOORP1.jpg","caption":"Floor Plan / Sectional 02"},{"src":"FLOORP2.jpg","caption":"Floor Plan / Sectional 03"},{"src":"FLOORP3.jpg","caption":"Floor Plan / Sectional 04"}]'><div class="card"><img src="FLOORP0.jpg" alt="Sectional Presentation"><span class="count">04 VISUALS</span><div class="overlay"><div class="category">2D / 3D</div><h3>Sectional Presentation</h3><div class="meta">Architectural Drawings</div><div class="arrow">View project →</div></div></div></article>

<article class="project walkthrough" data-title="Architectural Walkthrough 01" data-type="Walkthrough" data-description="Cinematic architectural walkthrough presentation." data-video="vi.mp4"><div class="card"><video src="vi.mp4" autoplay muted loop playsinline></video><div class="overlay"><div class="category">Walkthrough</div><h3>Architectural Walkthrough 01</h3><div class="meta">Cinematic Presentation</div><div class="arrow">Play walkthrough →</div></div></div></article>

<article class="project walkthrough" data-title="Architectural Walkthrough 02" data-type="Walkthrough" data-description="Cinematic architectural walkthrough presentation." data-video="RS 2.mp4"><div class="card"><video src="RS 2.mp4" autoplay muted loop playsinline></video><div class="overlay"><div class="category">Walkthrough</div><h3>Architectural Walkthrough 02</h3><div class="meta">Cinematic Presentation</div><div class="arrow">Play walkthrough →</div></div></div></article>

<article class="project walkthrough" data-title="Interior Walkthrough" data-type="Interior Walkthrough" data-description="Cinematic interior walkthrough presentation." data-video="living wth 1.mp4"><div class="card"><video src="living wth 1.mp4" autoplay muted loop playsinline></video><div class="overlay"><div class="category">Walkthrough</div><h3>Interior Walkthrough</h3><div class="meta">Cinematic Interior Film</div><div class="arrow">Play walkthrough →</div></div></div></article>

    </div>
  </div>
</section>

<section class="section" id="resume">
  <div class="section-inner">
    <div class="head reveal">
      <div>
        <div class="section-no">03 / Resume</div>
        <h2>Profile & Capabilities</h2>
      </div>
      <div class="intro">A compact professional profile built around architectural visualization, interior and exterior presentation, elevations, planning visuals and cinematic walkthroughs.</div>
    </div>

    <div class="resume-grid reveal">
      <div class="profile-panel">
        <div class="profile-mark">SG</div>
        <div class="section-no">Professional Profile</div>
        <h3>3D Visualiser</h3>
        <p>I am <strong>Sandesh Gandhgule</strong>, a 3D visualiser focused on architectural visualization, interior and exterior presentation, elevations and cinematic walkthroughs.</p>
        <p>My portfolio brings together residential, commercial and interior visualization work, presented as project-based galleries so the complete visual story of each project can be explored.</p>
        <div class="resume-note">Portfolio areas: Residential · Commercial · Interiors · Exteriors · Elevations · Walkthroughs · 2D / 3D</div>
      </div>

      <div class="skills-panel">
        <div class="section-no">Core Skills</div>
        <h3>What I Create</h3>
        <div class="skill-list">
          <div class="skill">
            <div class="skill-no">01</div>
            <h4>3D Architectural Visualization</h4>
            <p>Residential elevations, façades, perspectives, day/night views and presentation-ready architectural visuals.</p>
          </div>
          <div class="skill">
            <div class="skill-no">02</div>
            <h4>Interior & Exterior</h4>
            <p>Detailed interior and exterior visualization with materials, lighting, furniture, landscape and atmosphere.</p>
          </div>
          <div class="skill">
            <div class="skill-no">03</div>
            <h4>Elevation & Planning</h4>
            <p>Front, side and perspective elevation studies along with 2D / 3D planning presentation visuals.</p>
          </div>
          <div class="skill">
            <div class="skill-no">04</div>
            <h4>Cinematic Walkthroughs</h4>
            <p>Architectural and interior walkthrough films for presentations, portfolios and project communication.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<section class="showreel">
  <video src="vi.mp4" autoplay muted loop playsinline></video>
  <div class="reel-overlay">
    <div class="eyebrow">SHOWREEL · 3D VISUALIZATION</div>
    <h2>Architecture, presented through images, spaces and motion.</h2>
    <a class="btn primary" href="#contact">Let’s Collaborate</a>
  </div>
</section>

<section class="section dark">
  <div class="section-inner">
    <div class="head reveal">
      <div>
        <div class="section-no">04 / Workflow</div>
        <h2>How I Work</h2>
      </div>
      <div class="intro">A structured visualization workflow keeps the design intent clear while developing polished, realistic final visuals.</div>
    </div>

    <div class="processes reveal">
      <div class="process"><span class="section-no">01</span><h3>Discover</h3><p>Drawings, references, requirements and visual direction.</p></div>
      <div class="process"><span class="section-no">02</span><h3>Model</h3><p>Develop the architectural form and spatial framework.</p></div>
      <div class="process"><span class="section-no">03</span><h3>Visualize</h3><p>Materials, lighting, environment and camera composition.</p></div>
      <div class="process"><span class="section-no">04</span><h3>Refine</h3><p>Review, feedback and controlled visual refinements.</p></div>
      <div class="process"><span class="section-no">05</span><h3>Deliver</h3><p>High-resolution stills, animations and presentation assets.</p></div>
    </div>
  </div>
</section>

<section class="section" id="about">
  <div class="section-inner">
    <div class="section-no">05 / About Me</div>
    <div class="about reveal">
      <blockquote>Visualising <span>architecture</span> with clarity and detail.</blockquote>
      <div>
        <p>I am <strong>Sandesh Gandhgule</strong>, a 3D visualiser focused on architectural visualization, interior and exterior presentation, elevations and cinematic walkthroughs.</p>
        <p>My portfolio brings together residential, commercial and interior visualization work, presented as project-based galleries so the complete visual story of each project can be explored.</p>
        <div class="tags">
          <span>3D Visualisation</span>
          <span>Architecture</span>
          <span>Interiors</span>
          <span>Exteriors</span>
          <span>Elevations</span>
          <span>Walkthroughs</span>
        </div>
      </div>
    </div>
  </div>
</section>

<section class="contact" id="contact">
  <div class="section-no">06 / Contact</div>
  <h2>Let’s Collaborate.</h2>
  <p>For architectural visualization, 3D elevation, interior/exterior visualization or walkthrough projects, get in touch with me.</p>
  <div class="actions">
    <a class="btn primary" href="https://wa.me/918459441620">WhatsApp</a>
    <a class="btn ghost" href="https://instagram.com/inext_designs">Instagram</a>
    <a class="btn ghost" href="mailto:your@email.com">Email</a>
  </div>
</section>

<footer>
  <div>© 2026 <strong>SANDESH GANDHGULE</strong></div>
  <div>3D VISUALISER · PORTFOLIO & RESUME</div>
</footer>

<a class="whatsapp" href="https://wa.me/918459441620" aria-label="WhatsApp">💬</a>

<!-- PROJECT DETAIL -->
<div class="detail" id="detail" aria-hidden="true">
  <div class="detail-inner">
    <div class="detail-top">
      <div>
        <div class="category" id="detail-type"></div>
        <h2 id="detail-title"></h2>
        <div class="detail-desc" id="detail-desc"></div>
      </div>
      <button class="close-detail" id="close-detail" aria-label="Close project">×</button>
    </div>
    <div class="detail-grid" id="detail-grid"></div>
  </div>
</div>

<!-- LIGHTBOX -->
<div class="lightbox" id="lightbox" aria-hidden="true">
  <div class="lb-content">
    <div class="lb-head">
      <div class="lb-title" id="lb-title"></div>
      <div class="lb-counter" id="lb-counter"></div>
    </div>
    <div class="lb-main">
      <span class="lb-prev" id="lb-prev">❮</span>
      <img id="lb-img" src="" alt="">
      <span class="lb-next" id="lb-next">❯</span>
    </div>
    <div class="lb-caption" id="lb-caption"></div>
    <div class="thumbs" id="thumbs"></div>
  </div>
  <span class="lb-close" id="lb-close">×</span>
</div>

<script>
const header=document.getElementById('header');
window.addEventListener('scroll',()=>header.classList.toggle('scrolled',scrollY>30),{passive:true});

const cursor=document.getElementById('cursor-dot');
if(cursor && window.matchMedia('(pointer:fine)').matches){
  window.addEventListener('mousemove',e=>{
    cursor.style.left=e.clientX+'px';
    cursor.style.top=e.clientY+'px';
  },{passive:true});
}

const filters=document.querySelectorAll('.filter');
const projects=document.querySelectorAll('.project');

filters.forEach(btn=>btn.addEventListener('click',()=>{
  filters.forEach(x=>x.classList.remove('active'));
  btn.classList.add('active');
  const f=btn.dataset.filter;
  projects.forEach((p,i)=>{
    const show=f==='all'||p.classList.contains(f);
    p.classList.toggle('hide',!show);
    if(show){
      p.style.animationDelay=(Math.min(i,8)*35)+'ms';
      p.classList.remove('reanimate');
      void p.offsetWidth;
      p.classList.add('reanimate');
    }
  });
}));

const detail=document.getElementById('detail');
const detailTitle=document.getElementById('detail-title');
const detailType=document.getElementById('detail-type');
const detailDesc=document.getElementById('detail-desc');
const detailGrid=document.getElementById('detail-grid');
const lightbox=document.getElementById('lightbox');
const lbImg=document.getElementById('lb-img');
const lbTitle=document.getElementById('lb-title');
const lbCounter=document.getElementById('lb-counter');
const lbCaption=document.getElementById('lb-caption');
const thumbs=document.getElementById('thumbs');

let gallery=[],idx=0;

function readGallery(el){
  try{return JSON.parse(el.dataset.gallery||'[]')}
  catch(e){console.error('Invalid gallery:',el.dataset.title,e);return[]}
}

function openProject(el){
  if(el.dataset.video){
    detailTitle.textContent=el.dataset.title;
    detailType.textContent=el.dataset.type;
    detailDesc.textContent=el.dataset.description;
    detailGrid.innerHTML='';
    const box=document.createElement('div');
    box.className='detail-item';
    box.style.gridColumn='1/-1';
    const v=document.createElement('video');
    v.src=el.dataset.video;
    v.controls=true;v.autoplay=true;v.playsInline=true;
    v.style.width='100%';v.style.maxHeight='78vh';v.style.background='#000';
    box.appendChild(v);
    detailGrid.appendChild(box);
    detail.classList.add('open');
    document.body.classList.add('lock');
    return;
  }

  gallery=readGallery(el);
  if(!gallery.length)return;

  detailTitle.textContent=el.dataset.title;
  detailType.textContent=el.dataset.type;
  detailDesc.textContent=el.dataset.description;
  detailGrid.innerHTML='';

  gallery.forEach((g,i)=>{
    const box=document.createElement('div');
    box.className='detail-item';
    const img=document.createElement('img');
    img.src=g.src;
    img.alt=g.caption||el.dataset.title;
    img.loading=i?'lazy':'eager';
    img.onerror=()=>box.remove();

    const cap=document.createElement('div');
    cap.className='caption';
    cap.textContent=g.caption||'';

    box.append(img,cap);
    box.onclick=()=>openLightbox(gallery,i,el.dataset.title);
    detailGrid.appendChild(box);
  });

  detail.classList.add('open');
  detail.setAttribute('aria-hidden','false');
  document.body.classList.add('lock');
}

function closeProject(){
  detail.classList.remove('open');
  detail.setAttribute('aria-hidden','true');
  detailGrid.innerHTML='';
  if(!lightbox.classList.contains('open'))document.body.classList.remove('lock');
}

document.querySelectorAll('.project').forEach(p=>p.addEventListener('click',()=>openProject(p)));
const featured=document.querySelector('.featured');
if(featured)featured.addEventListener('click',()=>openProject(featured));
document.getElementById('close-detail').onclick=closeProject;

function openLightbox(items,i,title){
  gallery=items;idx=i||0;
  lbTitle.textContent=title||'Project Gallery';
  thumbs.innerHTML='';

  gallery.forEach((g,n)=>{
    const t=document.createElement('img');
    t.className='thumb';
    t.src=g.src;
    t.alt=g.caption||'';
    t.onclick=e=>{
      e.stopPropagation();
      idx=n;
      updateLightbox();
    };
    thumbs.appendChild(t);
  });

  updateLightbox();
  lightbox.classList.add('open');
  lightbox.setAttribute('aria-hidden','false');
}

function updateLightbox(){
  if(!gallery.length)return;
  const g=gallery[idx];
  lbImg.style.opacity=0;
  const pre=new Image();

  pre.onload=()=>{
    lbImg.src=g.src;
    lbImg.alt=g.caption||'';
    lbImg.style.opacity=1;
  };
  pre.onerror=()=>{
    lbImg.src=g.src;
    lbImg.style.opacity=1;
  };
  pre.src=g.src;

  lbCaption.textContent=g.caption||'';
  lbCounter.textContent=String(idx+1).padStart(2,'0')+' / '+String(gallery.length).padStart(2,'0');
  document.querySelectorAll('.thumb').forEach((t,n)=>t.classList.toggle('active',n===idx));
}

function next(){
  if(gallery.length){idx=(idx+1)%gallery.length;updateLightbox()}
}
function prev(){
  if(gallery.length){idx=(idx-1+gallery.length)%gallery.length;updateLightbox()}
}
function closeLightbox(){
  lightbox.classList.remove('open');
  lightbox.setAttribute('aria-hidden','true');
  lbImg.src='';
  thumbs.innerHTML='';
  if(!detail.classList.contains('open'))document.body.classList.remove('lock');
}

document.getElementById('lb-close').onclick=closeLightbox;
document.getElementById('lb-next').onclick=e=>{e.stopPropagation();next()};
document.getElementById('lb-prev').onclick=e=>{e.stopPropagation();prev()};
lightbox.onclick=e=>{if(e.target===lightbox)closeLightbox()};

let touchX=0;
lightbox.addEventListener('touchstart',e=>touchX=e.changedTouches[0].screenX,{passive:true});
lightbox.addEventListener('touchend',e=>{
  const d=e.changedTouches[0].screenX-touchX;
  if(Math.abs(d)>50)d<0?next():prev();
},{passive:true});

document.addEventListener('keydown',e=>{
  if(lightbox.classList.contains('open')){
    if(e.key==='Escape')closeLightbox();
    if(e.key==='ArrowRight')next();
    if(e.key==='ArrowLeft')prev();
  }else if(detail.classList.contains('open')&&e.key==='Escape'){
    closeProject();
  }
});

const observer=new IntersectionObserver(entries=>{
  entries.forEach(entry=>{
    if(entry.isIntersecting){
      entry.target.classList.add('visible');
      observer.unobserve(entry.target);
    }
  });
},{threshold:.12});
document.querySelectorAll('.reveal').forEach(el=>observer.observe(el));
</script>
</body>
</html>
