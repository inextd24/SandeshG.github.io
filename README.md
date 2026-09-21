<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Sandesh Gandhgule — 3D Visualiser Portfolio & Resume.">
<title>SANDESH GANDHGULE | 3D VISUALISER — PORTFOLIO & RESUME</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600&family=Playfair+Display:wght@500;600&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
:root{--gold:#d4af37;--bg:#090909;--surface:#111;--text:#fff;--muted:#aaa59b;--line:rgba(255,255,255,.11)}
*{box-sizing:border-box}html{scroll-behavior:smooth}body{margin:0;background:var(--bg);color:var(--text);font-family:Poppins,sans-serif}body.lock{overflow:hidden}a{color:inherit}button{font-family:inherit}
header{position:fixed;top:0;left:0;right:0;z-index:1000;display:flex;justify-content:space-between;align-items:center;padding:22px 7%;transition:.3s}header.scrolled{background:rgba(8,8,8,.92);backdrop-filter:blur(15px);padding:14px 7%;border-bottom:1px solid var(--line)}.logo{font:500 28px 'Playfair Display';letter-spacing:4px;color:var(--gold)}nav{display:flex;gap:24px}nav a{font-size:11px;color:#bbb;text-decoration:none}nav a:hover{color:var(--gold)}
.hero{min-height:100vh;position:relative;display:flex;align-items:flex-end;overflow:hidden}.hero-media,.hero-media:after{position:absolute;inset:0}.hero-media img{width:100%;height:100%;object-fit:cover;filter:brightness(.65)}.hero-media:after{content:"";background:linear-gradient(to top,rgba(0,0,0,.96),rgba(0,0,0,.18) 60%,rgba(0,0,0,.35))}.hero-content{position:relative;z-index:2;width:86%;max-width:1300px;margin:auto;padding-bottom:10vh}.eyebrow,.section-no,.category{font-size:10px;letter-spacing:2.5px;text-transform:uppercase;color:var(--gold)}.hero h1{font:500 clamp(54px,8vw,112px)/.9 'Playfair Display';letter-spacing:-3px;margin:18px 0}.hero h1 span{color:var(--gold)}.hero p{max-width:620px;color:#d0cdc6;font-size:14px;line-height:1.8}.actions{display:flex;gap:10px;flex-wrap:wrap;margin-top:28px}.btn{display:inline-flex;padding:13px 22px;border:1px solid var(--line);font-size:10px;letter-spacing:1px;text-transform:uppercase;text-decoration:none;cursor:pointer;transition:.3s}.btn.primary{background:var(--gold);border-color:var(--gold);color:#080808}.btn:hover{transform:translateY(-2px);border-color:var(--gold)}
.section{padding:110px 7%}.dark{background:#101010}.head{display:flex;justify-content:space-between;align-items:end;gap:40px;margin-bottom:42px}.head h2{font:500 clamp(42px,5vw,68px)/1 'Playfair Display';margin:12px 0 0}.intro{max-width:520px;color:var(--muted);font-size:13px;line-height:1.8}
.filters{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:38px}.filter{background:transparent;border:1px solid var(--line);color:#aaa;padding:10px 15px;font-size:10px;letter-spacing:1px;text-transform:uppercase;cursor:pointer;border-radius:3px}.filter:hover,.filter.active{background:var(--gold);border-color:var(--gold);color:#080808}
.grid{display:grid;grid-template-columns:repeat(3,1fr);gap:20px}.project{cursor:pointer}.project.hide{display:none}.card{position:relative;min-height:380px;overflow:hidden;background:var(--surface);border:1px solid rgba(255,255,255,.04)}.card img,.card video{width:100%;height:100%;min-height:380px;object-fit:cover;display:block;transition:.7s}.card:after{content:"";position:absolute;inset:0;background:linear-gradient(to top,rgba(0,0,0,.94),transparent 66%);pointer-events:none}.card:hover img,.card:hover video{transform:scale(1.045);filter:brightness(.7)}.count{position:absolute;z-index:2;right:15px;top:15px;padding:7px 11px;border:1px solid rgba(212,175,55,.7);border-radius:20px;background:rgba(0,0,0,.7);color:var(--gold);font-size:10px}..single{position:absolute;z-index:2;left:15px;top:15px;background:rgba(0,0,0,.62);padding:6px 9px;color:#ddd;font-size:9px;letter-spacing:1px;text-transform:uppercase}.overlay{position:absolute;z-index:2;left:0;right:0;bottom:0;padding:70px 24px 24px}.overlay h3{font:500 25px 'Playfair Display';margin:7px 0}.meta{font-size:11px;color:#bbb}.arrow{margin-top:11px;color:var(--gold);font-size:11px}.wide{grid-column:span 2}.wide .card,.wide .card img{min-height:500px}
.featured{position:relative;overflow:hidden;cursor:pointer}.featured img{width:100%;height:min(70vh,720px);object-fit:cover;display:block;transition:.8s}.featured:hover img{transform:scale(1.025);filter:brightness(.75)}.featured .overlay{padding:100px 5% 38px}.featured h3{font:500 clamp(36px,5vw,62px) 'Playfair Display';margin:8px 0}
/* PROJECT DETAIL */
.detail{display:none;position:fixed;inset:0;z-index:1800;background:rgba(5,5,5,.98);overflow:auto;padding:90px 7% 50px}.detail.open{display:block}.detail-inner{max-width:1400px;margin:auto}.detail-top{display:flex;justify-content:space-between;gap:30px;margin-bottom:32px}.detail-top h2{font:500 clamp(40px,5vw,72px)/1 'Playfair Display';margin:10px 0}.detail-desc{max-width:700px;color:var(--muted);font-size:13px;line-height:1.8}.close-detail{width:45px;height:45px;background:transparent;border:1px solid var(--line);color:var(--gold);font-size:27px;cursor:pointer}.close-detail:hover{background:var(--gold);color:#000}.detail-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:14px}.detail-item{position:relative;overflow:hidden;cursor:pointer;background:#111}.detail-item img{width:100%;aspect-ratio:16/10;object-fit:cover;display:block;transition:.5s}.detail-item:hover img{transform:scale(1.025);filter:brightness(.78)}.caption{position:absolute;left:0;right:0;bottom:0;padding:38px 18px 15px;background:linear-gradient(transparent,rgba(0,0,0,.9));font-size:11px;color:#ddd}
/* LIGHTBOX */
.lightbox{display:none;position:fixed;z-index:2200;inset:0;background:rgba(0,0,0,.985);align-items:center;justify-content:center;padding:20px}.lightbox.open{display:flex}.lb-content{width:min(1250px,94vw);height:min(92vh,900px);display:flex;flex-direction:column;align-items:center}.lb-head{width:100%;display:flex;justify-content:space-between;margin-bottom:10px}.lb-title{font:500 21px 'Playfair Display'}.lb-counter{color:var(--gold);font-size:12px}.lb-main{position:relative;flex:1;min-height:0;width:100%;display:flex;align-items:center;justify-content:center}.lb-main img{max-width:88%;max-height:100%;object-fit:contain;border-radius:5px;box-shadow:0 25px 70px #000;transition:.2s}.lb-close,.lb-prev,.lb-next{position:absolute;z-index:3;color:var(--gold);cursor:pointer;user-select:none}.lb-close{top:15px;right:25px;font-size:42px}.lb-prev,.lb-next{top:50%;transform:translateY(-50%);font-size:45px;padding:18px}.lb-prev{left:0}.lb-next{right:0}.lb-caption{margin:10px 0;color:var(--gold);font-size:13px}.thumbs{width:100%;display:flex;gap:8px;overflow-x:auto;padding:8px 2px}.thumb{width:78px;height:52px;flex:0 0 auto;object-fit:cover;opacity:.4;border:1px solid transparent;border-radius:4px;cursor:pointer}.thumb.active{opacity:1;border-color:var(--gold)}
/* OTHER SECTIONS */
.services{display:grid;grid-template-columns:repeat(4,1fr);border-top:1px solid var(--line);border-left:1px solid var(--line)}.service{min-height:250px;padding:30px;border-right:1px solid var(--line);border-bottom:1px solid var(--line)}.service:hover{background:#151515}.service h3{font:500 24px 'Playfair Display';margin:55px 0 12px}.service p,.process p,.about p{color:var(--muted);font-size:12px;line-height:1.8}.processes{display:grid;grid-template-columns:repeat(5,1fr);border-top:1px solid var(--line)}.process{padding:28px 18px;border-right:1px solid var(--line)}.process h3{font:500 22px 'Playfair Display';margin:35px 0 8px}.about{display:grid;grid-template-columns:.8fr 1.2fr;gap:90px}.about blockquote{font:500 clamp(38px,4vw,58px)/1 'Playfair Display';margin:0}.about blockquote span{color:var(--gold)}.tags{display:flex;gap:7px;flex-wrap:wrap;margin-top:24px}.tags span{border:1px solid var(--line);padding:8px 11px;color:#aaa;font-size:9px;text-transform:uppercase;letter-spacing:1px}.reel{position:relative;min-height:70vh;overflow:hidden}.reel video{width:100%;height:70vh;object-fit:cover;filter:brightness(.5)}.reel-overlay{position:absolute;inset:0;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center}.reel-overlay h2{font:500 clamp(42px,6vw,78px)/.96 'Playfair Display';max-width:850px}.contact{text-align:center;padding:140px 7%;background:radial-gradient(circle,rgba(212,175,55,.08),transparent 35%),#090909}.contact h2{font:500 clamp(45px,7vw,90px)/.95 'Playfair Display';margin:12px 0 25px}.contact p{max-width:560px;margin:auto;color:var(--muted);font-size:13px}footer{text-align:center;padding:28px;background:#070707;color:#666;font-size:11px}.whatsapp{position:fixed;z-index:1200;right:20px;bottom:20px;width:52px;height:52px;display:flex;align-items:center;justify-content:center;border-radius:50%;background:#25d366;text-decoration:none;font-size:22px}
@media(max-width:1050px){.grid{grid-template-columns:repeat(2,1fr)}.services{grid-template-columns:repeat(2,1fr)}.processes{grid-template-columns:repeat(2,1fr)}.about{grid-template-columns:1fr;gap:45px}}
@media(max-width:700px){header{padding:18px 5%}nav{gap:11px}nav a{font-size:9px}.hero-content{width:90%;padding-bottom:70px}.hero h1{font-size:50px}.section{padding:80px 5%}.head{display:block}.intro{margin-top:18px}.grid{grid-template-columns:1fr}.wide{grid-column:auto}.wide .card,.wide .card img{min-height:380px}.card,.card img,.card video{min-height:330px}.detail{padding:85px 5% 35px}.detail-grid{grid-template-columns:1fr}.detail-top{gap:12px}.close-detail{width:40px;height:40px}.services,.processes{grid-template-columns:1fr}.process{border-right:0;border-bottom:1px solid var(--line)}.lb-content{width:100%;height:90vh}.lb-main img{max-width:94%}.lb-prev,.lb-next{font-size:30px;padding:10px}.lb-prev{left:-5px}.lb-next{right:-5px}}

/* ===== INEXT PREMIUM PROJECT REFINEMENTS ===== */
.project-card{
    border-radius:2px;
    isolation:isolate;
}
.project-card::before{
    content:"";
    position:absolute;
    inset:0;
    z-index:1;
    border:1px solid rgba(212,175,55,0);
    transition:.45s ease;
    pointer-events:none;
}
.project-card:hover::before{
    border-color:rgba(212,175,55,.42);
}
.project-card-media,
.project-card.video-card video{
    transition:transform 1s cubic-bezier(.2,.7,.2,1),filter .7s ease;
}
.project-card:hover .project-card-media,
.project-card.video-card:hover video{
    transform:scale(1.035);
}
.project-overlay{
    padding:95px 27px 27px;
}
.project-title{
    font-size:28px;
    letter-spacing:-.3px;
}
.project-meta{
    display:flex;
    align-items:center;
    gap:9px;
}
.project-meta::before{
    content:"";
    width:20px;
    height:1px;
    background:var(--gold);
    display:inline-block;
}
.visual-count{
    letter-spacing:1.1px;
    backdrop-filter:blur(8px);
}
.single-badge{
    border:1px solid rgba(255,255,255,.16);
    backdrop-filter:blur(8px);
}
.project-arrow{
    opacity:.75;
    transition:.3s;
}
.project-card:hover .project-arrow{
    opacity:1;
    transform:translateX(4px);
}
.project-detail{
    background:
        radial-gradient(circle at 75% 0%,rgba(212,175,55,.055),transparent 28%),
        rgba(5,5,5,.985);
}
.detail-inner{
    max-width:1500px;
}
.detail-top{
    padding-bottom:28px;
    border-bottom:1px solid var(--line);
}
.detail-top h2{
    letter-spacing:-1.5px;
}
.detail-gallery{
    margin-top:28px;
}
.detail-gallery-item{
    border:1px solid rgba(255,255,255,.06);
}
.detail-gallery-caption{
    letter-spacing:.2px;
}
.detail-gallery-item::after{
    content:"VIEW";
    position:absolute;
    right:14px;
    top:14px;
    padding:6px 8px;
    border:1px solid rgba(212,175,55,.45);
    color:var(--gold);
    background:rgba(0,0,0,.55);
    font-size:8px;
    letter-spacing:1.5px;
    opacity:0;
    transition:.3s;
}
.detail-gallery-item:hover::after{opacity:1}

.project-detail .detail-label::after{
    content:"  /  PROJECT GALLERY";
    color:#666;
    letter-spacing:1.5px;
}

.lightbox{
    background:rgba(2,2,2,.985);
    backdrop-filter:blur(10px);
}
.lightbox-header{
    padding:0 4px;
}
.lightbox-title{
    letter-spacing:.2px;
}
.lightbox-main{
    background:radial-gradient(circle,rgba(255,255,255,.035),transparent 60%);
}
#lightbox-img{
    max-width:90%;
}
.thumbnail-strip{
    scrollbar-width:thin;
}
.thumbnail{
    border-radius:2px;
}
.thumbnail.active{
    box-shadow:0 0 0 1px rgba(212,175,55,.25);
}
.video-card::after{
    background:
        linear-gradient(to top,rgba(0,0,0,.94),transparent 62%),
        linear-gradient(transparent,rgba(0,0,0,.12));
}
.video-card::before{
    content:"▶";
    position:absolute;
    z-index:4;
    top:50%;
    left:50%;
    width:54px;
    height:54px;
    margin:-27px 0 0 -27px;
    display:flex;
    align-items:center;
    justify-content:center;
    border:1px solid rgba(212,175,55,.7);
    border-radius:50%;
    color:var(--gold);
    background:rgba(0,0,0,.45);
    backdrop-filter:blur(8px);
    font-size:15px;
    padding-left:2px;
    transition:.35s;
}
.video-card:hover::before{
    transform:scale(1.08);
    background:rgba(212,175,55,.9);
    color:#080808;
}
@media(max-width:700px){
    .project-overlay{padding:80px 20px 20px}
    .project-title{font-size:24px}
    .detail-gallery-item::after{display:none}
}


/* ===== PERSONAL PORTFOLIO OVERRIDES ===== */
.hero h1 span{display:inline-block}
.logo{font-size:22px;letter-spacing:2.5px}
.about strong{color:#fff;font-weight:500}
.resume-note{margin-top:18px;color:var(--muted);font-size:12px;line-height:1.8}
</style>
</head>
<body>
<header id="header"><div class="logo"><a href="#top">SANDESH</a></div><nav><a href="#work">Portfolio</a><a href="#resume">Resume</a><a href="#about">About</a><a href="#contact">Contact</a></nav></header>

<section class="hero" id="top"><div class="hero-media"><img src="RE_01_NB.png" alt="Sandesh Gandhgule — 3D Visualiser"></div><div class="hero-content"><div class="eyebrow">3D VISUALISER · ARCHITECTURAL VISUALIZATION</div><h1>Sandesh <span>Gandhgule.</span><br>3D Visualiser.</h1><p>I create high-fidelity architectural visuals, interiors, exteriors, elevations and cinematic walkthroughs that turn design concepts into clear, realistic experiences.</p><div class="actions"><a class="btn primary" href="#work">View Portfolio</a><a class="btn primary" href="#resume">View Resume</a></div></div></section>

<section class="section" id="work"><div class="head"><div><div class="section-no">01 / Portfolio</div><h2>Selected Work</h2></div><div class="intro">A selection of my architectural visualization work. Each project remains grouped as a complete visual package, whether it contains one render or a full set of views.</div></div>
<div class="featured" data-project-id="featured" data-title="Modern Residential Architecture" data-type="Residential Elevation" data-description="Exterior architectural visualization and elevation presentation." data-gallery='[{"src":"RE_01_F.png","caption":"Front Elevation"},{"src":"FRS.jpg","caption":"Perspective View"},{"src":"opt ss 2.jpg","caption":"Elevation Detail"},{"src":"opt ss.jpg","caption":"Alternative View"}]'><img src="DA 1.jpg" alt="Modern Residential Architecture"><div class="overlay"><div class="category">Featured Project</div><h3>Modern Residential Architecture</h3><div class="meta">Exterior Visualization · 04 Visuals</div><div class="arrow">View project →</div></div></div></section>

<section class="section dark"><div class="head"><div><div class="section-no">02 / Portfolio</div><h2>My Visual Work</h2></div><div class="intro">Browse my work by category. Multiple renders from the same project stay together, while individual visual studies remain independent.</div></div>
<div class="filters"><button class="filter active" data-filter="all">All</button><button class="filter" data-filter="residential">Residential</button><button class="filter" data-filter="commercial">Commercial</button><button class="filter" data-filter="front">Front Elevations</button><button class="filter" data-filter="interior">Interiors</button><button class="filter" data-filter="exterior">Exteriors</button><button class="filter" data-filter="walkthrough">Walkthroughs</button><button class="filter" data-filter="plans">2D / 3D</button></div>
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
</div></section>

<section class="section" id="resume"><div class="head"><div><div class="section-no">03 / Resume</div><h2>Skills & Capabilities</h2></div><div class="intro">My core areas of work as a 3D visualiser, covering architectural elevations, interiors, exteriors, planning visuals and cinematic presentations.</div></div><div class="services"><div class="service"><div class="section-no">01</div><h3>3D Architectural Visualization</h3><p>Residential elevations, façades, perspectives, day/night views and presentation-ready architectural visuals.</p></div><div class="service"><div class="section-no">02</div><h3>Interior & Exterior</h3><p>Detailed interior and exterior visualization with materials, lighting, furniture, landscape and atmosphere.</p></div><div class="service"><div class="section-no">03</div><h3>Elevation & Planning</h3><p>Front, side and perspective elevation studies along with 2D / 3D planning presentation visuals.</p></div><div class="service"><div class="section-no">04</div><h3>Cinematic Walkthroughs</h3><p>Architectural and interior walkthrough films for presentations, portfolios and project communication.</p></div></div></section>

<section class="reel"><video src="vi.mp4" autoplay muted loop playsinline></video><div class="reel-overlay"><div class="eyebrow">SHOWREEL · 3D VISUALIZATION</div><h2>My work, presented through images, spaces and motion.</h2><a class="btn primary" href="#contact">Get In Touch</a></div></section>

<section class="section dark"><div class="head"><div><div class="section-no">04 / Workflow</div><h2>How I Work</h2></div><div class="intro">A structured visualization workflow keeps the design intent clear while developing polished, realistic final visuals.</div></div><div class="processes"><div class="process"><span class="section-no">01</span><h3>Discover</h3><p>Drawings, references, requirements and visual direction.</p></div><div class="process"><span class="section-no">02</span><h3>Model</h3><p>Develop the architectural form and spatial framework.</p></div><div class="process"><span class="section-no">03</span><h3>Visualize</h3><p>Materials, lighting, environment and camera composition.</p></div><div class="process"><span class="section-no">04</span><h3>Refine</h3><p>Review, feedback and controlled visual refinements.</p></div><div class="process"><span class="section-no">05</span><h3>Deliver</h3><p>High-resolution stills, animations and presentation assets.</p></div></div></section>

<section class="section" id="about"><div class="section-no">05 / About Me</div><div class="about"><blockquote>Visualising <span>architecture</span> with clarity and detail.</blockquote><div><p>I am <strong>Sandesh Gandhgule</strong>, a 3D visualiser focused on architectural visualization, interior and exterior presentation, elevations and cinematic walkthroughs.</p><p>My portfolio brings together residential, commercial and interior visualization work, presented as project-based galleries so the complete visual story of each project can be explored.</p><div class="tags"><span>3D Visualisation</span><span>Architecture</span><span>Interiors</span><span>Exteriors</span><span>Elevations</span><span>Walkthroughs</span></div></div></div></section>

<section class="contact" id="contact"><div class="section-no">06 / Contact</div><h2>Let’s Work Together.</h2><p>For architectural visualization, 3D elevation, interior/exterior visualization or walkthrough projects, get in touch with me.</p><div class="actions" style="justify-content:center"><a class="btn primary" href="https://wa.me/918459441620">WhatsApp</a><a class="btn" href="https://instagram.com/inext_designs">Instagram</a><a class="btn" href="mailto:your@email.com">Email</a></div></section>
<footer>© 2026 <strong>SANDESH GANDHGULE</strong> — 3D VISUALISER · PORTFOLIO & RESUME</footer><a class="whatsapp" href="https://wa.me/918459441620" aria-label="WhatsApp">💬</a>

<!-- PROJECT DETAIL -->
<div class="detail" id="detail" aria-hidden="true"><div class="detail-inner"><div class="detail-top"><div><div class="category" id="detail-type"></div><h2 id="detail-title"></h2><div class="detail-desc" id="detail-desc"></div></div><button class="close-detail" id="close-detail">×</button></div><div class="detail-grid" id="detail-grid"></div></div></div>

<!-- LIGHTBOX -->
<div class="lightbox" id="lightbox" aria-hidden="true"><div class="lb-content"><div class="lb-head"><div class="lb-title" id="lb-title"></div><div class="lb-counter" id="lb-counter"></div></div><div class="lb-main"><span class="lb-prev" id="lb-prev">❮</span><img id="lb-img" src="" alt=""><span class="lb-next" id="lb-next">❯</span></div><div class="lb-caption" id="lb-caption"></div><div class="thumbs" id="thumbs"></div></div><span class="lb-close" id="lb-close">×</span></div>

<script>
const header=document.getElementById('header');
window.addEventListener('scroll',()=>header.classList.toggle('scrolled',scrollY>30));

const filters=document.querySelectorAll('.filter');
const projects=document.querySelectorAll('.project');
filters.forEach(btn=>btn.addEventListener('click',()=>{filters.forEach(x=>x.classList.remove('active'));btn.classList.add('active');const f=btn.dataset.filter;projects.forEach(p=>p.classList.toggle('hide',f!=='all'&&!p.classList.contains(f)))}));

const detail=document.getElementById('detail'),detailTitle=document.getElementById('detail-title'),detailType=document.getElementById('detail-type'),detailDesc=document.getElementById('detail-desc'),detailGrid=document.getElementById('detail-grid');
const lightbox=document.getElementById('lightbox'),lbImg=document.getElementById('lb-img'),lbTitle=document.getElementById('lb-title'),lbCounter=document.getElementById('lb-counter'),lbCaption=document.getElementById('lb-caption'),thumbs=document.getElementById('thumbs');
let gallery=[],idx=0;
function readGallery(el){try{return JSON.parse(el.dataset.gallery||'[]')}catch(e){console.error('Invalid gallery:',el.dataset.title,e);return[]}}
function openProject(el){
 if(el.dataset.video){detailTitle.textContent=el.dataset.title;detailType.textContent=el.dataset.type;detailDesc.textContent=el.dataset.description;detailGrid.innerHTML='';const box=document.createElement('div');box.className='detail-item';box.style.gridColumn='1/-1';const v=document.createElement('video');v.src=el.dataset.video;v.controls=true;v.autoplay=true;v.playsInline=true;v.style.width='100%';v.style.maxHeight='78vh';v.style.background='#000';box.appendChild(v);detailGrid.appendChild(box);detail.classList.add('open');document.body.classList.add('lock');return}
 gallery=readGallery(el);if(!gallery.length)return;detailTitle.textContent=el.dataset.title;detailType.textContent=el.dataset.type;detailDesc.textContent=el.dataset.description;detailGrid.innerHTML='';gallery.forEach((g,i)=>{const box=document.createElement('div');box.className='detail-item';const img=document.createElement('img');img.src=g.src;img.alt=g.caption||el.dataset.title;img.loading=i?'lazy':'eager';img.onerror=()=>box.remove();const cap=document.createElement('div');cap.className='caption';cap.textContent=g.caption||'';box.append(img,cap);box.onclick=()=>openLightbox(gallery,i,el.dataset.title);detailGrid.appendChild(box)});detail.classList.add('open');detail.setAttribute('aria-hidden','false');document.body.classList.add('lock')}
function closeProject(){detail.classList.remove('open');detail.setAttribute('aria-hidden','true');detailGrid.innerHTML='';if(!lightbox.classList.contains('open'))document.body.classList.remove('lock')}
document.querySelectorAll('.project').forEach(p=>p.addEventListener('click',()=>openProject(p)));document.querySelector('.featured').addEventListener('click',function(){openProject(this)});document.getElementById('close-detail').onclick=closeProject;

function openLightbox(items,i,title){gallery=items;idx=i||0;lbTitle.textContent=title||'Project Gallery';thumbs.innerHTML='';gallery.forEach((g,n)=>{const t=document.createElement('img');t.className='thumb';t.src=g.src;t.alt=g.caption||'';t.onclick=e=>{e.stopPropagation();idx=n;updateLightbox()};thumbs.appendChild(t)});updateLightbox();lightbox.classList.add('open');lightbox.setAttribute('aria-hidden','false')}
function updateLightbox(){if(!gallery.length)return;const g=gallery[idx];lbImg.style.opacity=0;const pre=new Image();pre.onload=()=>{lbImg.src=g.src;lbImg.alt=g.caption||'';lbImg.style.opacity=1};pre.onerror=()=>{lbImg.src=g.src;lbImg.style.opacity=1};pre.src=g.src;lbCaption.textContent=g.caption||'';lbCounter.textContent=String(idx+1).padStart(2,'0')+' / '+String(gallery.length).padStart(2,'0');document.querySelectorAll('.thumb').forEach((t,n)=>t.classList.toggle('active',n===idx))}
function next(){if(gallery.length){idx=(idx+1)%gallery.length;updateLightbox()}}function prev(){if(gallery.length){idx=(idx-1+gallery.length)%gallery.length;updateLightbox()}}function closeLightbox(){lightbox.classList.remove('open');lightbox.setAttribute('aria-hidden','true');lbImg.src='';thumbs.innerHTML='';if(!detail.classList.contains('open'))document.body.classList.remove('lock')}
document.getElementById('lb-close').onclick=closeLightbox;document.getElementById('lb-next').onclick=e=>{e.stopPropagation();next()};document.getElementById('lb-prev').onclick=e=>{e.stopPropagation();prev()};lightbox.onclick=e=>{if(e.target===lightbox)closeLightbox()};
let touchX=0;lightbox.addEventListener('touchstart',e=>touchX=e.changedTouches[0].screenX,{passive:true});lightbox.addEventListener('touchend',e=>{const d=e.changedTouches[0].screenX-touchX;if(Math.abs(d)>50)d<0?next():prev()},{passive:true});
document.addEventListener('keydown',e=>{if(lightbox.classList.contains('open')){if(e.key==='Escape')closeLightbox();if(e.key==='ArrowRight')next();if(e.key==='ArrowLeft')prev()}else if(detail.classList.contains('open')&&e.key==='Escape')closeProject()});
</script>
</body>
</html>
