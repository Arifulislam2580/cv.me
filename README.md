<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Ariful Islam — Software Developer & Documentary Video Editor</title>
<meta name="description" content="Hire Ariful Islam for web development, software projects and documentary-style video editing. Based in Dhaka, Bangladesh.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@500;700&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#0b0d12; --bg2:#11141b; --card:#161a23; --line:#262b37;
  --ink:#f2f3f5; --muted:#9aa1b2; --accent:#ffb547; --accent2:#4fd1c5;
  --todo:#3d3215; --todo-ink:#ffd27a; --radius:16px;
}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{background:var(--bg);color:var(--ink);font:16px/1.65 Inter,system-ui,sans-serif;-webkit-font-smoothing:antialiased;overflow-x:hidden}
a{color:inherit;text-decoration:none}
h1,h2,h3{font-family:"Space Grotesk",sans-serif;letter-spacing:-.02em;line-height:1.15}
.wrap{max-width:1080px;margin:0 auto;padding:0 22px}
.todo{background:var(--todo);color:var(--todo-ink);padding:1px 7px;border-radius:5px;font-size:.88em;font-weight:500}

/* NAV */
nav{position:fixed;inset:0 0 auto 0;z-index:50;transition:.3s}
nav.scrolled{background:rgba(11,13,18,.85);backdrop-filter:blur(12px);border-bottom:1px solid var(--line)}
nav .wrap{display:flex;align-items:center;justify-content:space-between;height:68px}
.logo{font-family:"Space Grotesk";font-weight:700;font-size:20px}
.logo b{color:var(--accent)}
.links{display:flex;align-items:center;gap:26px;font-size:15px}
.links a{color:var(--muted);transition:.2s}
.links a:hover{color:var(--ink)}
.btn{display:inline-flex;align-items:center;gap:8px;padding:13px 22px;border-radius:999px;font-weight:600;font-size:15px;border:1px solid var(--line);transition:transform .2s,box-shadow .2s,background .2s;cursor:pointer;background:none;color:var(--ink);font-family:inherit}
.btn:hover{transform:translateY(-2px)}
.btn.primary{background:var(--accent);color:#1a1205;border-color:var(--accent);box-shadow:0 8px 30px -8px rgba(255,181,71,.6)}
.btn.primary:hover{box-shadow:0 12px 36px -6px rgba(255,181,71,.75)}
.btn.ghost:hover{background:var(--card)}
.links .btn{padding:9px 18px;color:#1a1205}
.menu-btn{display:none;background:none;border:0;color:var(--ink);font-size:26px;cursor:pointer}
@media(max-width:820px){
  .links{position:fixed;top:68px;left:0;right:0;flex-direction:column;background:var(--bg2);padding:24px;gap:18px;border-bottom:1px solid var(--line);transform:translateY(-130%);transition:.3s}
  .links.open{transform:none}
  .menu-btn{display:block}
}

/* HERO */
header{position:relative;padding:150px 0 90px;overflow:hidden}
.glow{position:absolute;border-radius:50%;filter:blur(90px);opacity:.35;pointer-events:none}
.g1{width:460px;height:460px;background:var(--accent);top:-120px;right:-120px}
.g2{width:380px;height:380px;background:var(--accent2);bottom:-160px;left:-120px;opacity:.22}
.status{display:inline-flex;align-items:center;gap:9px;background:var(--card);border:1px solid var(--line);padding:7px 15px;border-radius:999px;font-size:14px;color:var(--muted);margin-bottom:26px}
.dot{width:9px;height:9px;border-radius:50%;background:#3ddc84;box-shadow:0 0 0 0 rgba(61,220,132,.7);animation:pulse 2s infinite}
@keyframes pulse{70%{box-shadow:0 0 0 10px rgba(61,220,132,0)}100%{box-shadow:0 0 0 0 rgba(61,220,132,0)}}
h1{font-size:clamp(40px,7.2vw,76px);font-weight:700;max-width:880px}
.grad{background:linear-gradient(90deg,var(--accent),#ff7a59 50%,var(--accent2));-webkit-background-clip:text;background-clip:text;color:transparent}
.lede{font-size:clamp(17px,2.2vw,20px);color:var(--muted);max-width:620px;margin:24px 0 36px}
.cta{display:flex;flex-wrap:wrap;gap:14px}
.trust{display:flex;flex-wrap:wrap;gap:28px;margin-top:56px;padding-top:28px;border-top:1px solid var(--line);color:var(--muted);font-size:14px}
.trust strong{display:block;color:var(--ink);font-family:"Space Grotesk";font-size:18px}

/* SECTIONS */
section{padding:96px 0}
.alt{background:var(--bg2)}
.label{display:inline-block;color:var(--accent);font-weight:600;font-size:13px;letter-spacing:.12em;text-transform:uppercase;margin-bottom:12px}
h2{font-size:clamp(30px,4.6vw,46px);max-width:700px}
.intro{color:var(--muted);max-width:620px;margin:14px 0 48px;font-size:17px}

/* SERVICES */
.services{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:18px}
.svc{background:var(--card);border:1px solid var(--line);border-radius:var(--radius);padding:30px 26px;transition:.3s;position:relative;overflow:hidden}
.svc:hover{transform:translateY(-6px);border-color:var(--accent)}
.svc .ico{width:52px;height:52px;border-radius:14px;display:grid;place-items:center;font-size:24px;background:rgba(255,181,71,.12);margin-bottom:20px}
.svc h3{font-size:21px;margin-bottom:10px}
.svc p{color:var(--muted);font-size:15px;margin-bottom:18px}
.svc a{color:var(--accent);font-weight:600;font-size:14px}
.svc a:hover{text-decoration:underline}

/* WORK */
.filters{display:flex;flex-wrap:wrap;gap:10px;margin-bottom:30px}
.chip{padding:8px 18px;border-radius:999px;border:1px solid var(--line);background:none;color:var(--muted);font:500 14px Inter;cursor:pointer;transition:.2s}
.chip.on,.chip:hover{background:var(--ink);color:var(--bg);border-color:var(--ink)}
.work{display:grid;grid-template-columns:repeat(auto-fill,minmax(310px,1fr));gap:20px}
.card{background:var(--card);border:1px solid var(--line);border-radius:var(--radius);overflow:hidden;transition:.3s;display:flex;flex-direction:column}
.card:hover{transform:translateY(-6px);box-shadow:0 24px 50px -20px rgba(0,0,0,.7);border-color:#3a4150}
.thumb{height:170px;position:relative;display:flex;align-items:flex-end;padding:18px;font-family:"Space Grotesk";font-weight:700;font-size:15px;letter-spacing:.04em}
.t1{background:linear-gradient(135deg,#ff9f43,#ee5253)}
.t2{background:linear-gradient(135deg,#0abde3,#10ac84)}
.t3{background:linear-gradient(135deg,#5f27cd,#341f97)}
.t4{background:linear-gradient(135deg,#576574,#222f3e)}
.t5{background:linear-gradient(135deg,#ff6b6b,#c44569)}
.thumb .badge{position:absolute;top:16px;left:16px;background:rgba(0,0,0,.35);backdrop-filter:blur(6px);padding:5px 12px;border-radius:999px;font:600 12px Inter}
.thumb .big{font-size:44px;position:absolute;right:20px;top:50%;transform:translateY(-50%);opacity:.9}
.body{padding:24px;display:flex;flex-direction:column;gap:10px;flex:1}
.body h3{font-size:20px}
.body p{color:var(--muted);font-size:15px}
.tags{display:flex;flex-wrap:wrap;gap:6px;margin-top:auto;padding-top:8px}
.tag{font-size:12px;padding:4px 10px;border-radius:999px;background:#202533;color:#c8cdd9}
.more{font-size:14px;font-weight:600;color:var(--accent);margin-top:6px}
.card.hide{display:none}

/* WHY */
.why{display:grid;grid-template-columns:1fr 1fr;gap:56px;align-items:center}
.points{display:grid;gap:18px}
.pt{display:flex;gap:16px;align-items:flex-start;background:var(--card);border:1px solid var(--line);border-radius:14px;padding:20px}
.pt span{flex:none;width:36px;height:36px;border-radius:10px;background:rgba(79,209,197,.14);color:var(--accent2);display:grid;place-items:center;font-weight:700}
.pt h3{font-size:17px;margin-bottom:4px}
.pt p{color:var(--muted);font-size:15px}
.skills{display:flex;flex-wrap:wrap;gap:10px;margin-top:26px}
.skills .tag{font-size:14px;padding:8px 14px;background:var(--card);border:1px solid var(--line)}
@media(max-width:820px){.why{grid-template-columns:1fr;gap:36px}}

/* PROCESS */
.steps{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:18px;counter-reset:s}
.step{border-top:3px solid var(--accent);padding-top:20px}
.step::before{counter-increment:s;content:"0" counter(s);font-family:"Space Grotesk";font-weight:700;font-size:36px;color:#2c3240;display:block;margin-bottom:6px}
.step h3{font-size:19px;margin-bottom:6px}
.step p{color:var(--muted);font-size:15px}

/* CONTACT */
.contact-box{background:linear-gradient(135deg,#1c1a14,#151922 60%,#10201f);border:1px solid var(--line);border-radius:28px;padding:clamp(36px,6vw,72px);text-align:center;position:relative;overflow:hidden}
.contact-box h2{margin:0 auto}
.contact-box .intro{margin:16px auto 34px}
.contact-box .cta{justify-content:center}
.socials{display:flex;justify-content:center;flex-wrap:wrap;gap:12px;margin-top:30px}
.socials a{padding:10px 18px;border:1px solid var(--line);border-radius:999px;color:var(--muted);font-size:14px;transition:.2s}
.socials a:hover{color:var(--ink);border-color:var(--ink)}
.toast{position:fixed;bottom:90px;left:50%;transform:translate(-50%,20px);background:var(--ink);color:var(--bg);padding:10px 18px;border-radius:10px;font-weight:600;font-size:14px;opacity:0;transition:.3s;pointer-events:none;z-index:60}
.toast.show{opacity:1;transform:translate(-50%,0)}

/* FLOATING HIRE */
.float{position:fixed;right:20px;bottom:20px;z-index:40;opacity:0;transform:translateY(20px);transition:.3s;pointer-events:none}
.float.show{opacity:1;transform:none;pointer-events:auto}

footer{padding:34px 0;text-align:center;color:var(--muted);font-size:14px;border-top:1px solid var(--line)}

/* REVEAL */
.reveal{opacity:0;transform:translateY(28px);transition:opacity .7s ease,transform .7s ease}
.reveal.in{opacity:1;transform:none}
@media (prefers-reduced-motion:reduce){.reveal{opacity:1;transform:none}*{animation:none!important;transition:none!important}}
</style>
</head>
<body>

<nav id="nav"><div class="wrap">
  <a class="logo" href="#top">Ariful<b>.</b></a>
  <button class="menu-btn" id="menuBtn" aria-label="Open menu">☰</button>
  <div class="links" id="links">
    <a href="#services">Services</a>
    <a href="#work">Work</a>
    <a href="#why">About</a>
    <a href="#process">Process</a>
    <a class="btn primary" href="#contact">Hire Me</a>
  </div>
</div></nav>

<header id="top">
  <div class="glow g1"></div><div class="glow g2"></div>
  <div class="wrap" style="position:relative">
    <div class="status"><span class="dot"></span>Available for new projects</div>
    <h1>I build <span class="grad">websites & software</span> and edit videos that tell your story.</h1>
    <p class="lede">Hi, I'm Ariful Islam, a developer and documentary video editor from Dhaka. I help businesses and creators launch clean, working web apps and engaging video content.</p>
    <div class="cta">
      <a class="btn primary" href="#contact">Start a project →</a>
      <a class="btn ghost" href="#work">See my work</a>
    </div>
    <div class="trust">
      <div><strong>Web & Software</strong>Python · JavaScript · PHP · C/C++/C#</div>
      <div><strong>Video Production</strong>DaVinci Resolve · CapCut Pro · DSLR</div>
      <div><strong>Team Leader</strong>Led client project for Laobaan Bangladesh</div>
    </div>
  </div>
</header>

<section id="services" class="alt"><div class="wrap">
  <span class="label reveal">Services</span>
  <h2 class="reveal">What I can do for you</h2>
  <p class="intro reveal">Pick one service or combine them. For example, a business website plus a short documentary video about your brand.</p>
  <div class="services">
    <div class="svc reveal"><div class="ico">💻</div><h3>Web Development</h3><p>Business websites, portfolios and web apps with databases, built to work well on phones.</p><a href="#contact" data-service="Web Development">Get a quote →</a></div>
    <div class="svc reveal"><div class="ico">⚙️</div><h3>Custom Software</h3><p>Inventory systems, management tools and scripts in Python, PHP, C++ or C# to automate your work.</p><a href="#contact" data-service="Custom Software">Get a quote →</a></div>
    <div class="svc reveal"><div class="ico">🎬</div><h3>Video Editing</h3><p>Documentary-style edits, YouTube videos and brand stories, with clean cuts, colour and pacing.</p><a href="#contact" data-service="Video Editing">Get a quote →</a></div>
    <div class="svc reveal"><div class="ico">🖼️</div><h3>Thumbnail Design</h3><p>Eye-catching YouTube thumbnails with cinematic compositions, made to earn clicks honestly.</p><a href="#contact" data-service="Thumbnail Design">Get a quote →</a></div>
  </div>
</div></section>

<section id="work"><div class="wrap">
  <span class="label reveal">Portfolio</span>
  <h2 class="reveal">Selected work</h2>
  <p class="intro reveal">Real projects I've built and edited, with my role and the tools I used.</p>
  <div class="filters reveal">
    <button class="chip on" data-f="all">All</button>
    <button class="chip" data-f="dev">Development</button>
    <button class="chip" data-f="video">Video</button>
    <button class="chip" data-f="research">Research</button>
  </div>
  <div class="work">
    <article class="card reveal" data-c="dev">
      <div class="thumb t1"><span class="badge">Client project · Team Lead</span><span class="big">📦</span>SMARTSTOCK</div>
      <div class="body">
        <h3>SmartStock: Inventory System with AI Chatbot</h3>
        <p>A product and stock management web app built for Laobaan Bangladesh LTD. I led a three-person team from requirements to delivery.</p>
        <div class="tags"><span class="tag">PHP</span><span class="tag">MySQL</span><span class="tag">JavaScript</span><span class="tag">AI Chatbot</span></div>
        <span class="more"><span class="todo">Add demo / GitHub link</span></span>
      </div>
    </article>
    <article class="card reveal" data-c="video">
      <div class="thumb t5"><span class="badge">YouTube · Editor & Designer</span><span class="big">🎥</span>HISHAB TV</div>
      <div class="body">
        <h3>Hishab TV: Entrepreneur Documentaries</h3>
        <p>Documentary-style videos about Bangladeshi entrepreneurs: concept, DSLR shooting, editing and thumbnail design.</p>
        <div class="tags"><span class="tag">DaVinci Resolve</span><span class="tag">CapCut Pro</span><span class="tag">Thumbnails</span></div>
        <span class="more"><span class="todo">Add channel link</span></span>
      </div>
    </article>
    <article class="card reveal" data-c="research">
      <div class="thumb t3"><span class="badge">Thesis · In progress</span><span class="big">🛡️</span>SDN SECURITY</div>
      <div class="body">
        <h3>ML for Early Detection of SDN Controller Hijacking</h3>
        <p>Research comparing Random Forest and LSTM models that track trust over time to catch network attacks earlier.</p>
        <div class="tags"><span class="tag">Machine Learning</span><span class="tag">LSTM</span><span class="tag">Network Security</span></div>
      </div>
    </article>
    <article class="card reveal" data-c="dev">
      <div class="thumb t2"><span class="badge">Compiler Design</span><span class="big">🧩</span>LEXER</div>
      <div class="body">
        <h3>Lexical Analyzer in Python</h3>
        <p>A complete lexer that breaks source code into tokens, delivered with a test suite and a technical report.</p>
        <div class="tags"><span class="tag">Python</span><span class="tag">Compilers</span><span class="tag">Testing</span></div>
        <span class="more"><span class="todo">Add GitHub link</span></span>
      </div>
    </article>
    <article class="card reveal" data-c="dev">
      <div class="thumb t4"><span class="badge">Operating Systems</span><span class="big">✈️</span>SCHEDULER</div>
      <div class="body">
        <h3>Airport Ground Scheduling Simulation</h3>
        <p>Compared FCFS, SJN, SRT, Round Robin and Priority scheduling, with deadlock analysis using the Banker's Algorithm.</p>
        <div class="tags"><span class="tag">CPU Scheduling</span><span class="tag">Deadlocks</span></div>
      </div>
    </article>
  </div>
</div></section>

<section id="why" class="alt"><div class="wrap why">
  <div>
    <span class="label reveal">About me</span>
    <h2 class="reveal">A developer who also thinks like a storyteller</h2>
    <p class="intro reveal" style="margin-bottom:0">I'm a Computer Science & Engineering student at IUBAT (graduating 2027) and a working video editor. Code and film need the same skill: a clear structure, no wasted parts, and polish in the details.</p>
    <div class="skills reveal">
      <span class="tag">Python</span><span class="tag">JavaScript</span><span class="tag">PHP</span><span class="tag">MySQL</span><span class="tag">C / C++ / C#</span><span class="tag">HTML & CSS</span><span class="tag">Machine Learning</span><span class="tag">DaVinci Resolve</span><span class="tag">CapCut Pro</span>
    </div>
  </div>
  <div class="points">
    <div class="pt reveal"><span>✓</span><div><h3>Clear communication</h3><p>I reply in English or Bengali and keep you updated at every step.</p></div></div>
    <div class="pt reveal"><span>✓</span><div><h3>Leadership experience</h3><p>I've led a team on a real industry project and organised university events as an Ambassador Team lead.</p></div></div>
    <div class="pt reveal"><span>✓</span><div><h3>Two skills, one person</h3><p>Need a website and a promo video? You get both without managing two freelancers.</p></div></div>
  </div>
</div></section>

<section id="process"><div class="wrap">
  <span class="label reveal">How it works</span>
  <h2 class="reveal">Simple process, no surprises</h2>
  <p class="intro reveal">From first message to final delivery in four steps.</p>
  <div class="steps">
    <div class="step reveal"><h3>Tell me your idea</h3><p>Send a message with what you need, your deadline and your budget.</p></div>
    <div class="step reveal"><h3>Get a plan & quote</h3><p>I reply with a clear scope, timeline and price before any work starts.</p></div>
    <div class="step reveal"><h3>I build & update you</h3><p>You see progress along the way and can request changes early.</p></div>
    <div class="step reveal"><h3>Delivery & support</h3><p>You get the final files or live site, plus help after launch.</p></div>
  </div>
</div></section>

<section id="contact" style="padding-top:20px"><div class="wrap">
  <div class="contact-box reveal">
    <div class="glow g1" style="opacity:.18"></div>
    <span class="label">Let's talk</span>
    <h2>Have a project in mind?</h2>
    <p class="intro" id="contactText">Tell me what you need. I usually reply within 24 hours.</p>
    <div class="cta">
      <button class="btn primary" id="copyEmail" data-email="your@email.com">✉️ Copy my email</button>
      <a class="btn ghost" href="#" id="waLink">💬 WhatsApp <span class="todo">add number</span></a>
    </div>
    <p style="margin-top:16px;color:var(--muted);font-size:14px">Email: <span class="todo">your@email.com</span></p>
    <div class="socials">
      <a href="https://github.com/Arifulislam2580">GitHub</a>
      <a href="#">LinkedIn <span class="todo">link</span></a>
      <a href="#">YouTube <span class="todo">link</span></a>
      <a href="#">Fiverr / Upwork <span class="todo">optional</span></a>
    </div>
  </div>
</div></section>

<footer>© 2026 Ariful Islam · Dhaka, Bangladesh · <a href="#top" style="color:var(--accent)">Back to top ↑</a></footer>

<a class="btn primary float" id="floatBtn" href="#contact">Hire Me</a>
<div class="toast" id="toast">Copied!</div>

<script>
const nav=document.getElementById('nav'),floatBtn=document.getElementById('floatBtn');
addEventListener('scroll',()=>{
  nav.classList.toggle('scrolled',scrollY>30);
  const c=document.getElementById('contact').getBoundingClientRect().top;
  floatBtn.classList.toggle('show',scrollY>600&&c>innerHeight);
},{passive:true});

const links=document.getElementById('links');
document.getElementById('menuBtn').onclick=()=>links.classList.toggle('open');
links.querySelectorAll('a').forEach(a=>a.onclick=()=>links.classList.remove('open'));

const io=new IntersectionObserver(es=>es.forEach(e=>{if(e.isIntersecting){e.target.classList.add('in');io.unobserve(e.target)}}),{threshold:.12});
document.querySelectorAll('.reveal').forEach(el=>io.observe(el));

document.querySelectorAll('.chip').forEach(ch=>ch.onclick=()=>{
  document.querySelectorAll('.chip').forEach(x=>x.classList.remove('on'));ch.classList.add('on');
  const f=ch.dataset.f;
  document.querySelectorAll('.card').forEach(c=>c.classList.toggle('hide',f!=='all'&&c.dataset.c!==f));
});

document.querySelectorAll('[data-service]').forEach(a=>a.addEventListener('click',()=>{
  document.getElementById('contactText').textContent='Interested in '+a.dataset.service+'? Tell me about your project. I usually reply within 24 hours.';
}));

const toast=document.getElementById('toast');
function showToast(t){toast.textContent=t;toast.classList.add('show');setTimeout(()=>toast.classList.remove('show'),1800)}
document.getElementById('copyEmail').onclick=async e=>{
  const em=e.currentTarget.dataset.email;
  try{await navigator.clipboard.writeText(em);showToast('Email copied: '+em)}catch(_){showToast(em)}
};
</script>
</body>
</html>
