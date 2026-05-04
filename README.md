<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Saad — Full Stack AI Developer</title>
<link rel="preconnect" href="https://fonts.googleapis.com"/>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,400;1,9..144,300;1,9..144,400&family=Cabinet+Grotesk:wght@400;500;700;800;900&family=Geist+Mono:wght@300;400;500&display=swap" rel="stylesheet"/>
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --c0:#FAFAF8;
  --c1:#F4F3EE;
  --c2:#E8E6DC;
  --c3:#C8C4B4;
  --c4:#8C8878;
  --c5:#3C3A34;
  --c6:#1A1916;
  --ink:#0F0E0C;
  --acc:#C8622A;
  --acc2:#1A6B55;
  --acc3:#2D4A8A;
  --fd:'Fraunces',serif;
  --fg:'Cabinet Grotesk',sans-serif;
  --fm:'Geist Mono',monospace;
}
html{scroll-behavior:smooth}
body{
  background:var(--c0);
  color:var(--ink);
  font-family:var(--fg);
  font-size:16px;
  line-height:1.6;
  -webkit-font-smoothing:antialiased;
  overflow-x:hidden;
}
body::before{
  content:'';
  position:fixed;inset:0;
  background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.025'/%3E%3C/svg%3E");
  pointer-events:none;z-index:999;
}
.page{max-width:1080px;margin:0 auto;padding:0 48px}
@media(max-width:640px){.page{padding:0 22px}}

/* NAV */
nav{
  display:flex;align-items:center;justify-content:space-between;
  padding:30px 0;border-bottom:1px solid var(--c2);
}
.nav-logo{
  font-family:var(--fd);font-size:22px;font-weight:400;
  font-style:italic;color:var(--ink);letter-spacing:-.01em;
}
.nav-logo em{font-style:normal;color:var(--acc)}
.nav-links{display:flex;gap:32px;list-style:none}
.nav-links a{
  font-family:var(--fm);font-size:11px;letter-spacing:.12em;
  text-transform:uppercase;color:var(--c4);text-decoration:none;transition:color .2s;
}
.nav-links a:hover{color:var(--ink)}
@media(max-width:560px){.nav-links{gap:18px}.nav-links a{font-size:10px;letter-spacing:.08em}}

/* HERO */
.hero{
  padding:96px 0 80px;display:grid;
  grid-template-columns:1fr 320px;gap:60px;align-items:end;
}
@media(max-width:820px){.hero{grid-template-columns:1fr;gap:48px}}
.hero-eyebrow{
  display:inline-flex;align-items:center;gap:10px;
  font-family:var(--fm);font-size:11px;letter-spacing:.14em;
  text-transform:uppercase;color:var(--acc2);margin-bottom:28px;
}
.hero-eyebrow::before{content:'';display:block;width:28px;height:1px;background:var(--acc2)}
.hero-name{
  font-family:var(--fd);font-size:clamp(68px,10vw,116px);
  font-weight:300;line-height:.88;letter-spacing:-.04em;color:var(--ink);
}
.hero-name .it{font-style:italic;color:var(--acc)}
.hero-role{
  font-family:var(--fg);font-size:clamp(15px,1.8vw,19px);
  font-weight:500;color:var(--c4);letter-spacing:-.01em;
  margin-top:22px;margin-bottom:28px;
}
.hero-desc{font-size:15px;color:var(--c5);line-height:1.82;max-width:480px}
.hero-cta{display:flex;gap:12px;margin-top:40px;flex-wrap:wrap}
.btn{
  display:inline-flex;align-items:center;gap:8px;padding:13px 26px;
  border-radius:100px;font-size:13px;font-weight:700;
  font-family:var(--fg);text-decoration:none;letter-spacing:.01em;
  transition:all .22s cubic-bezier(.4,0,.2,1);cursor:pointer;border:none;
}
.btn-dark{background:var(--ink);color:var(--c0)}
.btn-dark:hover{background:var(--c6);transform:translateY(-2px);box-shadow:0 8px 28px rgba(15,14,12,.16)}
.btn-outline{background:transparent;color:var(--ink);border:1.5px solid var(--c3)}
.btn-outline:hover{border-color:var(--ink);transform:translateY(-2px)}

/* STAT CARD */
.stat-stack{
  display:flex;flex-direction:column;gap:1px;
  background:var(--c2);border:1px solid var(--c2);border-radius:18px;overflow:hidden;
}
.stat-row{
  background:var(--c0);padding:20px 24px;
  display:flex;align-items:baseline;justify-content:space-between;transition:background .18s;
}
.stat-row:hover{background:var(--c1)}
.stat-val{
  font-family:var(--fd);font-size:42px;font-weight:300;
  letter-spacing:-.03em;color:var(--ink);line-height:1;
}
.stat-val sup{font-size:18px;color:var(--acc);vertical-align:super}
.stat-key{
  font-family:var(--fm);font-size:10px;letter-spacing:.12em;
  text-transform:uppercase;color:var(--c4);text-align:right;line-height:1.5;
}

/* SECTION */
section{padding:80px 0;border-top:1px solid var(--c2)}
.sec-num{
  font-family:var(--fm);font-size:11px;color:var(--c3);
  letter-spacing:.1em;margin-bottom:10px;
}
.sec-title{
  font-family:var(--fd);font-size:clamp(34px,5vw,54px);
  font-weight:300;letter-spacing:-.03em;color:var(--ink);line-height:1;margin-bottom:48px;
}
.sec-title em{font-style:italic;color:var(--acc)}

/* EXPERTISE */
.exp-grid{
  display:grid;grid-template-columns:repeat(2,1fr);gap:1px;
  background:var(--c2);border:1px solid var(--c2);border-radius:20px;overflow:hidden;
}
@media(max-width:600px){.exp-grid{grid-template-columns:1fr}}
.exp-card{
  background:var(--c0);padding:34px 30px;transition:background .18s;
}
.exp-card:hover{background:var(--c1)}
.exp-num{
  font-family:var(--fd);font-size:11px;font-style:italic;
  color:var(--c3);margin-bottom:18px;
}
.exp-dot{
  width:38px;height:38px;border-radius:10px;
  display:flex;align-items:center;justify-content:center;
  font-size:17px;margin-bottom:18px;
}
.d1{background:#FEF3EC;border:1px solid #F5D0B5}
.d2{background:#ECF4F1;border:1px solid #B8E0D3}
.d3{background:#EEF1FA;border:1px solid #BEC8EC}
.d4{background:#FDF6EC;border:1px solid #EFD9B5}
.exp-title{
  font-size:17px;font-weight:800;color:var(--ink);
  letter-spacing:-.02em;margin-bottom:10px;
}
.exp-body{font-size:13.5px;color:var(--c4);line-height:1.75}

/* STACK */
.stack-tbl{width:100%;border-collapse:collapse}
.stack-tbl tr{border-bottom:1px solid var(--c2);transition:background .15s}
.stack-tbl tr:last-child{border-bottom:none}
.stack-tbl tr:hover{background:var(--c1)}
.stack-tbl td{padding:17px 0;vertical-align:middle}
.s-layer{
  font-family:var(--fm);font-size:11px;letter-spacing:.12em;
  text-transform:uppercase;color:var(--c4);width:130px;padding-right:28px;
}
.s-techs{display:flex;flex-wrap:wrap;gap:7px}
.s-pill{
  font-family:var(--fm);font-size:12px;color:var(--c5);
  background:var(--c1);border:1px solid var(--c2);
  padding:5px 13px;border-radius:100px;transition:all .15s;cursor:default;
}
.s-pill:hover{background:var(--ink);color:var(--c0);border-color:var(--ink)}

/* PROJECTS */
.proj-list{display:flex;flex-direction:column}
.proj-item{
  display:grid;grid-template-columns:72px 1fr 28px;
  gap:28px;align-items:start;padding:38px 0;
  border-bottom:1px solid var(--c2);
  text-decoration:none;color:inherit;transition:all .2s;
}
.proj-item:first-child{padding-top:0}
.proj-item:last-child{border-bottom:none;padding-bottom:0}
.proj-item:hover .p-name{color:var(--acc)}
.proj-item:hover .p-arrow{transform:translate(4px,-4px);opacity:1}
.p-idx{
  font-family:var(--fd);font-size:44px;font-weight:300;
  font-style:italic;color:var(--c2);line-height:1;margin-top:2px;transition:color .2s;
}
.proj-item:hover .p-idx{color:var(--c3)}
.p-label{
  display:inline-block;font-family:var(--fm);font-size:10px;
  letter-spacing:.12em;text-transform:uppercase;color:var(--acc2);
  background:#ECF4F1;border:1px solid #BCE0D4;
  padding:3px 10px;border-radius:100px;margin-bottom:12px;
}
.p-name{
  font-family:var(--fd);font-size:clamp(20px,2.8vw,30px);
  font-weight:400;letter-spacing:-.02em;color:var(--ink);
  margin-bottom:10px;transition:color .2s;line-height:1.1;
}
.p-desc{font-size:14px;color:var(--c4);line-height:1.75;max-width:540px;margin-bottom:16px}
.p-tags{display:flex;flex-wrap:wrap;gap:6px}
.p-tag{
  font-size:11px;font-family:var(--fm);color:var(--c4);
  border:1px solid var(--c2);padding:3px 10px;border-radius:4px;
}
.p-arrow{
  font-size:22px;color:var(--ink);opacity:.25;
  transition:all .2s;margin-top:6px;line-height:1;
}
@media(max-width:600px){
  .proj-item{grid-template-columns:44px 1fr 24px;gap:14px}
  .p-idx{font-size:30px}
}

/* SERVICES */
.svc-grid{
  display:grid;grid-template-columns:repeat(3,1fr);gap:1px;
  background:var(--c2);border:1px solid var(--c2);border-radius:20px;overflow:hidden;
}
@media(max-width:720px){.svc-grid{grid-template-columns:1fr 1fr}}
@media(max-width:480px){.svc-grid{grid-template-columns:1fr}}
.svc-cell{background:var(--c0);padding:30px 26px;transition:background .18s}
.svc-cell:hover{background:var(--c1)}
.svc-n{
  font-family:var(--fm);font-size:10px;color:var(--c3);
  letter-spacing:.1em;margin-bottom:16px;
}
.svc-bar{display:inline-block;width:24px;height:2px;border-radius:2px;margin-bottom:16px}
.b1{background:var(--acc)}.b2{background:var(--acc2)}.b3{background:var(--acc3)}
.b4{background:var(--acc)}.b5{background:var(--acc2)}.b6{background:var(--acc3)}
.svc-name{
  font-size:15px;font-weight:800;color:var(--ink);
  letter-spacing:-.02em;margin-bottom:8px;
}
.svc-desc{font-size:13px;color:var(--c4);line-height:1.7}

/* CONTACT */
.ct-wrap{
  display:grid;grid-template-columns:1fr 1fr;
  gap:72px;align-items:center;
}
@media(max-width:720px){.ct-wrap{grid-template-columns:1fr;gap:40px}}
.ct-heading{
  font-family:var(--fd);font-size:clamp(42px,6vw,68px);
  font-weight:300;letter-spacing:-.04em;line-height:.95;color:var(--ink);
}
.ct-heading em{font-style:italic;color:var(--acc)}
.ct-sub{font-size:15px;color:var(--c4);line-height:1.8;margin-top:20px;max-width:380px}
.ct-links{
  display:flex;flex-direction:column;gap:1px;
  background:var(--c2);border:1px solid var(--c2);border-radius:16px;overflow:hidden;
}
.ct-link{
  display:flex;align-items:center;justify-content:space-between;
  padding:20px 22px;background:var(--c0);text-decoration:none;transition:background .18s;gap:12px;
}
.ct-link:hover{background:var(--c1)}
.ct-ll{display:flex;align-items:center;gap:13px}
.ct-ico{
  width:36px;height:36px;border-radius:8px;
  background:var(--c1);border:1px solid var(--c2);
  display:flex;align-items:center;justify-content:center;font-size:15px;flex-shrink:0;
}
.ct-name{font-size:14px;font-weight:700;color:var(--ink);letter-spacing:-.01em}
.ct-val{font-family:var(--fm);font-size:11px;color:var(--c4);margin-top:2px}
.ct-arr{font-size:15px;color:var(--c3);transition:all .2s}
.ct-link:hover .ct-arr{color:var(--ink);transform:translate(3px,-3px)}

/* FOOTER */
footer{
  padding:32px 0;border-top:1px solid var(--c2);
  display:flex;align-items:center;justify-content:space-between;
  flex-wrap:wrap;gap:16px;
}
.foot-brand{
  font-family:var(--fd);font-size:18px;
  font-weight:400;font-style:italic;color:var(--ink);
}
.foot-brand em{font-style:normal;color:var(--acc)}
.foot-copy{font-family:var(--fm);font-size:11px;color:var(--c3);letter-spacing:.06em}

/* REVEAL */
.rv{
  opacity:0;transform:translateY(24px);
  transition:opacity .65s cubic-bezier(.4,0,.2,1),transform .65s cubic-bezier(.4,0,.2,1);
}
.rv.on{opacity:1;transform:none}
</style>
</head>
<body>

<div class="page">
  <nav>
    <div class="nav-logo">S<em>.</em>aad</div>
    <ul class="nav-links">
      <li><a href="#work">Work</a></li>
      <li><a href="#stack">Stack</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</div>

<!-- HERO -->
<div class="page">
  <div class="hero">
    <div class="hero-left rv">
      <div class="hero-eyebrow">Available for work &nbsp;·&nbsp; Lahore, PK</div>
      <h1 class="hero-name">
        Saad<br/>
        <span class="it">builds.</span>
      </h1>
      <p class="hero-role">Full Stack AI Developer &amp; Mobile Specialist</p>
      <p class="hero-desc">I design and engineer AI-powered mobile and web products — from architecture to App Store. 20+ years of shipping software that real people actually use.</p>
      <div class="hero-cta">
        <a class="btn btn-dark" href="mailto:your@email.com">Get in touch</a>
        <a class="btn btn-outline" href="#work">View work</a>
      </div>
    </div>
    <div class="rv">
      <div class="stat-stack">
        <div class="stat-row">
          <div class="stat-val">20<sup>+</sup></div>
          <div class="stat-key">Years of<br/>experience</div>
        </div>
        <div class="stat-row">
          <div class="stat-val">15<sup>+</sup></div>
          <div class="stat-key">Apps<br/>shipped</div>
        </div>
        <div class="stat-row">
          <div class="stat-val">3</div>
          <div class="stat-key">AI products<br/>in production</div>
        </div>
        <div class="stat-row">
          <div class="stat-val">∞</div>
          <div class="stat-key">Problems<br/>solved</div>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- EXPERTISE -->
<div class="page">
  <section>
    <div class="rv"><div class="sec-num">01 — Expertise</div>
    <h2 class="sec-title">What I do <em>best</em></h2></div>
    <div class="exp-grid rv">
      <div class="exp-card">
        <div class="exp-num">i.</div>
        <div class="exp-dot d1">📱</div>
        <div class="exp-title">Mobile Development</div>
        <div class="exp-body">Cross-platform apps with React Native &amp; Expo. Smooth 60fps animations, native-feel UX, and rock-solid performance on iOS and Android.</div>
      </div>
      <div class="exp-card">
        <div class="exp-num">ii.</div>
        <div class="exp-dot d2">🤖</div>
        <div class="exp-title">AI Integration</div>
        <div class="exp-body">OpenAI-powered features built into the product core — not bolted on. Real-time streaming, smart recommendations, intelligent automation.</div>
      </div>
      <div class="exp-card">
        <div class="exp-num">iii.</div>
        <div class="exp-dot d3">🌐</div>
        <div class="exp-title">Full Stack Web</div>
        <div class="exp-body">End-to-end MERN applications with clean APIs, scalable architecture, and production-grade backends built on Supabase and Node.js.</div>
      </div>
      <div class="exp-card">
        <div class="exp-num">iv.</div>
        <div class="exp-dot d4">🎯</div>
        <div class="exp-title">Product Engineering</div>
        <div class="exp-body">I think in outcomes, not tickets. Architecture, performance, UX flows — I own the whole thing, not just my slice of the code.</div>
      </div>
    </div>
  </section>
</div>

<!-- STACK -->
<div class="page">
  <section id="stack">
    <div class="rv"><div class="sec-num">02 — Stack</div>
    <h2 class="sec-title">Tech I <em>trust</em></h2></div>
    <div class="rv">
      <table class="stack-tbl">
        <tbody>
          <tr><td class="s-layer">Mobile</td><td><div class="s-techs"><span class="s-pill">React Native</span><span class="s-pill">Expo</span></div></td></tr>
          <tr><td class="s-layer">Frontend</td><td><div class="s-techs"><span class="s-pill">React</span><span class="s-pill">TypeScript</span><span class="s-pill">JavaScript</span></div></td></tr>
          <tr><td class="s-layer">Backend</td><td><div class="s-techs"><span class="s-pill">Node.js</span><span class="s-pill">Express.js</span></div></td></tr>
          <tr><td class="s-layer">Data / BaaS</td><td><div class="s-techs"><span class="s-pill">Supabase</span><span class="s-pill">MongoDB</span><span class="s-pill">MySQL</span><span class="s-pill">Firebase</span></div></td></tr>
          <tr><td class="s-layer">AI</td><td><div class="s-techs"><span class="s-pill">OpenAI API</span><span class="s-pill">LLM Integration</span><span class="s-pill">Streaming</span></div></td></tr>
          <tr><td class="s-layer">Payments</td><td><div class="s-techs"><span class="s-pill">Stripe</span></div></td></tr>
          <tr><td class="s-layer">DevOps</td><td><div class="s-techs"><span class="s-pill">Git</span><span class="s-pill">GitHub</span><span class="s-pill">CI/CD</span></div></td></tr>
        </tbody>
      </table>
    </div>
  </section>
</div>

<!-- PROJECTS -->
<div class="page">
  <section id="work">
    <div class="rv"><div class="sec-num">03 — Work</div>
    <h2 class="sec-title">Selected <em>projects</em></h2></div>
    <div class="proj-list rv">

      <a class="proj-item" href="#">
        <div class="p-idx">01</div>
        <div>
          <span class="p-label">Search &amp; Discovery</span>
          <div class="p-name">SnapFind</div>
          <div class="p-desc">A smart search and discovery app built for speed and precision. Real-time results, intelligent ranking, and a clean cross-platform UI engineered for high daily retention.</div>
          <div class="p-tags">
            <span class="p-tag">React Native</span><span class="p-tag">Supabase</span><span class="p-tag">Node.js</span><span class="p-tag">Expo</span>
          </div>
        </div>
        <div class="p-arrow">↗</div>
      </a>

      <a class="proj-item" href="#">
        <div class="p-idx">02</div>
        <div>
          <span class="p-label">AI · Health &amp; Fitness</span>
          <div class="p-name">FitPulse AI</div>
          <div class="p-desc">AI-powered fitness companion delivering personalized workout plans and coaching via OpenAI. Tracks health metrics daily and adapts to each user — real intelligence, not generic advice.</div>
          <div class="p-tags">
            <span class="p-tag">React Native</span><span class="p-tag">OpenAI API</span><span class="p-tag">Supabase</span><span class="p-tag">Expo</span><span class="p-tag">Streaming</span>
          </div>
        </div>
        <div class="p-arrow">↗</div>
      </a>

      <a class="proj-item" href="#">
        <div class="p-idx">03</div>
        <div>
          <span class="p-label">Full Stack · E-commerce</span>
          <div class="p-name">Food Delivery App</div>
          <div class="p-desc">Complete food ordering platform — restaurant listings, cart, live order tracking, Stripe payments, and an admin dashboard for operators. Built end-to-end, production-ready.</div>
          <div class="p-tags">
            <span class="p-tag">React Native</span><span class="p-tag">Node.js</span><span class="p-tag">MongoDB</span><span class="p-tag">Stripe</span><span class="p-tag">Firebase</span>
          </div>
        </div>
        <div class="p-arrow">↗</div>
      </a>
    </div>
  </section>
</div>

<!-- SERVICES -->
<div class="page">
  <section id="services">
    <div class="rv"><div class="sec-num">04 — Services</div>
    <h2 class="sec-title">How I can <em>help</em></h2></div>
    <div class="svc-grid rv">
      <div class="svc-cell">
        <div class="svc-n">01</div>
        <div class="svc-bar b1"></div>
        <div class="svc-name">Mobile App Development</div>
        <div class="svc-desc">React Native apps for iOS and Android — pixel-perfect UI, smooth performance, native integrations, App Store deployment.</div>
      </div>
      <div class="svc-cell">
        <div class="svc-n">02</div>
        <div class="svc-bar b2"></div>
        <div class="svc-name">Full Stack Web</div>
        <div class="svc-desc">End-to-end MERN applications. Clean APIs, scalable architecture, real-time features, production deployments.</div>
      </div>
      <div class="svc-cell">
        <div class="svc-n">03</div>
        <div class="svc-bar b3"></div>
        <div class="svc-name">AI Feature Integration</div>
        <div class="svc-desc">Chatbots, LLM pipelines, smart recommendations, and OpenAI-powered automation woven into your existing product.</div>
      </div>
      <div class="svc-cell">
        <div class="svc-n">04</div>
        <div class="svc-bar b4"></div>
        <div class="svc-name">Supabase Solutions</div>
        <div class="svc-desc">Auth, real-time databases, row-level security, edge functions, and storage — done correctly from day one.</div>
      </div>
      <div class="svc-cell">
        <div class="svc-n">05</div>
        <div class="svc-bar b5"></div>
        <div class="svc-name">UI/UX Optimization</div>
        <div class="svc-desc">Animation polish, load-time improvements, and interface refinements that improve retention and engagement.</div>
      </div>
      <div class="svc-cell">
        <div class="svc-n">06</div>
        <div class="svc-bar b6"></div>
        <div class="svc-name">API &amp; Integrations</div>
        <div class="svc-desc">Stripe, Firebase, REST APIs, webhooks, and real-time data pipelines — connected cleanly to your stack.</div>
      </div>
    </div>
  </section>
</div>

<!-- CONTACT -->
<div class="page">
  <section id="contact">
    <div class="rv"><div class="sec-num">05 — Contact</div></div>
    <div class="ct-wrap">
      <div class="rv">
        <h2 class="ct-heading">Let's<br/><em>work</em><br/>together.</h2>
        <p class="ct-sub">Open to freelance projects, remote roles, and ambitious collaborations. If you're building something real, let's talk.</p>
      </div>
      <div class="ct-links rv">
        <a class="ct-link" href="mailto:your@email.com">
          <div class="ct-ll"><div class="ct-ico">✉️</div><div><div class="ct-name">Email</div><div class="ct-val">your@email.com</div></div></div>
          <div class="ct-arr">↗</div>
        </a>
        <a class="ct-link" href="https://fiverr.com/yourprofile" target="_blank">
          <div class="ct-ll"><div class="ct-ico">💼</div><div><div class="ct-name">Fiverr</div><div class="ct-val">fiverr.com/yourprofile</div></div></div>
          <div class="ct-arr">↗</div>
        </a>
        <a class="ct-link" href="https://linkedin.com/in/yourprofile" target="_blank">
          <div class="ct-ll"><div class="ct-ico">🔗</div><div><div class="ct-name">LinkedIn</div><div class="ct-val">linkedin.com/in/yourprofile</div></div></div>
          <div class="ct-arr">↗</div>
        </a>
        <a class="ct-link" href="https://github.com/yourusername" target="_blank">
          <div class="ct-ll"><div class="ct-ico">🐙</div><div><div class="ct-name">GitHub</div><div class="ct-val">github.com/yourusername</div></div></div>
          <div class="ct-arr">↗</div>
        </a>
      </div>
    </div>
  </section>
</div>

<!-- FOOTER -->
<div class="page">
  <footer>
    <div class="foot-brand">S<em>.</em>aad</div>
    <div class="foot-copy">Full Stack AI Developer &nbsp;·&nbsp; © 2025 &nbsp;·&nbsp; Lahore, PK</div>
  </footer>
</div>

<script>
const els = document.querySelectorAll('.rv');
const io = new IntersectionObserver((entries) => {
  entries.forEach((e, i) => {
    if (e.isIntersecting) {
      setTimeout(() => e.target.classList.add('on'), i * 70);
      io.unobserve(e.target);
    }
  });
}, { threshold: 0.07 });
els.forEach(el => io.observe(el));
</script>
</body>
</html>
