# mykyta.github.io
<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mykyta Todorov – Bewerber Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=Bebas+Neue&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --red:#e8273a;
  --dark:#111;
  --light:#f5f4f0;
  --gray:#888;
  --border:#e2e2e2;
  --font:'Space Grotesk',sans-serif;
}
html{scroll-behavior:smooth}
body{font-family:var(--font);background:var(--light);color:var(--dark);overflow-x:hidden;font-size:15px}

/* ——— GRID BACKGROUND ——— */
body::before{
  content:'';position:fixed;inset:0;
  background-image:linear-gradient(rgba(0,0,0,0.04) 1px,transparent 1px),linear-gradient(90deg,rgba(0,0,0,0.04) 1px,transparent 1px);
  background-size:60px 60px;pointer-events:none;z-index:0;
}

/* ——— NAV ——— */
nav{
  position:fixed;top:0;width:100%;z-index:100;
  display:flex;justify-content:space-between;align-items:center;
  padding:18px 60px;
  background:rgba(245,244,240,0.92);
  backdrop-filter:blur(12px);
  border-bottom:1px solid var(--border);
}
.nav-logo{font-family:'Bebas Neue',sans-serif;font-size:1.3rem;letter-spacing:2px;color:var(--dark)}
.nav-logo span{color:var(--red)}
nav ul{list-style:none;display:flex;gap:36px;align-items:center}
nav a{text-decoration:none;font-size:0.72rem;letter-spacing:2px;text-transform:uppercase;font-weight:500;color:#555;transition:color 0.2s}
nav a:hover{color:var(--dark)}
.nav-cta{background:var(--red)!important;color:#fff!important;padding:9px 22px;font-size:0.72rem!important;letter-spacing:1px;transition:background 0.2s!important}
.nav-cta:hover{background:#c01e2e!important}

/* ——— RED SIDE LINE ——— */
.side-line{
  position:fixed;left:24px;top:0;bottom:0;width:1px;
  background:linear-gradient(180deg,transparent 10%,var(--red) 30%,var(--red) 70%,transparent 90%);
  z-index:50;opacity:0.25;
}
.side-dot{
  position:fixed;left:20px;width:9px;height:9px;
  border-radius:50%;background:var(--red);z-index:51;
  transition:top 0.3s ease;box-shadow:0 0 0 2px rgba(232,39,58,0.2);
}

/* ——— SECTION WRAPPER ——— */
section{position:relative;z-index:1}

/* ——— HERO ——— */
#hero{
  min-height:100vh;display:flex;align-items:center;
  padding:100px 60px 60px 100px;
}
.hero-inner{display:grid;grid-template-columns:1fr 320px;gap:60px;align-items:center;max-width:1200px;margin:0 auto;width:100%}
.hero-badge{
  display:inline-flex;align-items:center;gap:8px;
  font-size:0.68rem;letter-spacing:3px;text-transform:uppercase;font-weight:600;
  color:var(--gray);margin-bottom:28px;
}
.hero-badge::before{content:'';width:8px;height:8px;background:var(--red);border-radius:50%;animation:blink 1.5s ease-in-out infinite}
@keyframes blink{0%,100%{opacity:1}50%{opacity:0.3}}
.hero-name{line-height:0.92;margin-bottom:20px}
.hero-name .first{
  display:block;
  font-family:'Bebas Neue',sans-serif;
  font-size:clamp(4rem,9vw,7.5rem);
  color:var(--dark);
  -webkit-text-stroke:2px var(--dark);
  -webkit-text-fill-color:transparent;
  letter-spacing:2px;
}
.hero-name .last{
  display:block;
  font-family:'Bebas Neue',sans-serif;
  font-size:clamp(4rem,9vw,7.5rem);
  color:var(--dark);
  letter-spacing:2px;
  line-height:1;
}
.hero-divider{width:48px;height:3px;background:var(--red);margin-bottom:24px}
.hero-desc{font-size:1.05rem;line-height:1.7;color:#444;max-width:520px;margin-bottom:32px}
.hero-desc strong{color:var(--red);font-weight:600}
.hero-tags{display:flex;gap:10px;flex-wrap:wrap;margin-bottom:40px}
.hero-tag{
  display:inline-flex;align-items:center;gap:6px;
  font-size:0.7rem;letter-spacing:1.5px;text-transform:uppercase;font-weight:600;
  padding:7px 14px;border:1px solid var(--border);color:#555;
}
.hero-btns{display:flex;gap:14px;flex-wrap:wrap}
.btn-red{
  padding:14px 32px;background:var(--red);color:#fff;
  font-size:0.82rem;font-weight:600;letter-spacing:1px;
  border:none;cursor:pointer;transition:background 0.2s,transform 0.2s;text-decoration:none;display:inline-block;
}
.btn-red:hover{background:#c01e2e;transform:translateY(-2px)}
.btn-outline{
  padding:14px 32px;background:transparent;color:var(--dark);
  font-size:0.82rem;font-weight:600;letter-spacing:1px;
  border:1.5px solid var(--dark);cursor:pointer;transition:all 0.2s;text-decoration:none;display:inline-block;
}
.btn-outline:hover{background:var(--dark);color:#fff}

/* Snapshot card */
.snapshot-card{
  background:#fff;border:1px solid var(--border);padding:28px;
  box-shadow:0 4px 30px rgba(0,0,0,0.06);
}
.snapshot-label{font-size:0.65rem;letter-spacing:3px;color:var(--gray);text-transform:uppercase;margin-bottom:18px;font-weight:600}
.snapshot-row{display:flex;justify-content:space-between;align-items:center;padding:10px 0;border-bottom:1px solid #f0f0f0;font-size:0.78rem}
.snapshot-row:last-child{border-bottom:none}
.snap-key{letter-spacing:1.5px;text-transform:uppercase;color:var(--gray);font-weight:600;font-size:0.65rem}
.snap-val{font-weight:600;color:var(--dark)}
.snap-val.green{color:var(--red)}
.snapshot-tags{margin-top:20px;padding-top:16px;border-top:1px solid #f0f0f0}
.snapshot-tags .snap-key{margin-bottom:10px;display:block}
.tag-chips{display:flex;flex-wrap:wrap;gap:6px}
.chip{font-size:0.65rem;padding:4px 10px;background:var(--light);border:1px solid var(--border);color:#555;font-weight:500;letter-spacing:0.5px}

/* scroll indicator */
.scroll-hint{
  position:absolute;bottom:32px;left:50%;transform:translateX(-50%);
  display:flex;flex-direction:column;align-items:center;gap:8px;
  font-size:0.62rem;letter-spacing:3px;color:var(--gray);text-transform:uppercase;font-weight:600;
}
.scroll-arrow{width:1px;height:28px;background:var(--dark);position:relative;overflow:hidden}
.scroll-arrow::after{content:'';position:absolute;top:-100%;left:0;width:100%;height:100%;background:var(--red);animation:scrollDown 1.5s ease-in-out infinite}
@keyframes scrollDown{0%{top:-100%}100%{top:100%}}

/* ——— SECTIONS GENERAL ——— */
.section-wrap{max-width:1100px;margin:0 auto;padding:100px 60px}
.section-code{font-size:0.65rem;letter-spacing:3px;color:var(--gray);text-transform:uppercase;font-weight:600;margin-bottom:12px}
.section-heading{font-size:clamp(2rem,4vw,3rem);font-weight:700;line-height:1.1;margin-bottom:12px}
.section-heading span{color:var(--red)}
.section-sub{color:#666;line-height:1.7;max-width:480px;margin-bottom:48px}

/* ——— WERDEGANG ——— */
#werdegang{background:#fff;border-top:1px solid var(--border);border-bottom:1px solid var(--border)}
.timeline{display:flex;flex-direction:column;gap:0;max-width:620px}
.tl-item{display:flex;gap:24px;position:relative}
.tl-dot-col{display:flex;flex-direction:column;align-items:center;padding-top:18px}
.tl-dot{width:10px;height:10px;border-radius:50%;border:2px solid var(--border);background:#fff;flex-shrink:0;transition:border-color 0.3s}
.tl-dot.active{background:var(--red);border-color:var(--red)}
.tl-line{flex:1;width:1px;background:var(--border);margin-top:4px}
.tl-card{
  flex:1;border:1px solid var(--border);padding:20px 24px;margin-bottom:16px;
  cursor:pointer;transition:border-color 0.3s,box-shadow 0.3s;background:#fff;
}
.tl-card:hover{border-color:#ccc;box-shadow:0 2px 12px rgba(0,0,0,0.05)}
.tl-card.open{border-color:var(--dark)}
.tl-card-header{display:flex;justify-content:space-between;align-items:flex-start}
.tl-meta{font-size:0.68rem;letter-spacing:1px;color:var(--gray);margin-bottom:6px;display:flex;align-items:center;gap:8px}
.tl-badge{background:var(--red);color:#fff;font-size:0.58rem;letter-spacing:1px;padding:2px 7px;font-weight:700;text-transform:uppercase}
.tl-title{font-weight:700;font-size:1rem;margin-bottom:3px}
.tl-place{font-size:0.75rem;color:var(--gray)}
.tl-arrow{font-size:0.7rem;color:var(--gray);transition:transform 0.3s;flex-shrink:0;margin-top:4px}
.tl-card.open .tl-arrow{transform:rotate(180deg)}
.tl-body{max-height:0;overflow:hidden;transition:max-height 0.4s ease,padding 0.3s}
.tl-card.open .tl-body{max-height:200px;padding-top:14px}
.tl-body p{font-size:0.85rem;color:#555;line-height:1.7;border-top:1px solid #f0f0f0;padding-top:14px}

/* ——— SKILLS ——— */
#skills{background:var(--light)}
.skills-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:16px}
.skill-card{
  background:#fff;border:1px solid var(--border);padding:22px 20px;
  position:relative;overflow:hidden;transition:box-shadow 0.3s,transform 0.3s;cursor:default;
}
.skill-card:hover{box-shadow:0 6px 30px rgba(0,0,0,0.08);transform:translateY(-3px)}
.sk-type{font-size:0.6rem;letter-spacing:2px;text-transform:uppercase;color:var(--gray);font-weight:600;margin-bottom:10px}
.sk-icon{font-size:1.3rem;margin-bottom:8px}
.sk-name{font-weight:700;font-size:0.95rem;margin-bottom:8px}
.sk-bar-wrap{display:flex;align-items:center;gap:8px;margin-bottom:12px}
.sk-bar-label{font-size:0.6rem;letter-spacing:1px;text-transform:uppercase;color:var(--gray);font-weight:600;flex-shrink:0}
.sk-bar{flex:1;height:2px;background:#eee;position:relative;overflow:hidden}
.sk-bar-fill{height:100%;background:var(--red);width:0;transition:width 1s ease}
.sk-pct{font-size:0.72rem;font-weight:700;flex-shrink:0}
.sk-desc{font-size:0.78rem;color:#666;line-height:1.6}

/* ——— SPRACHEN ——— */
#sprachen{background:#fff;border-top:1px solid var(--border)}
.lang-list{max-width:540px;display:flex;flex-direction:column;gap:0;margin-bottom:36px}
.lang-row{display:grid;grid-template-columns:40px 140px 1fr 40px;align-items:center;gap:16px;padding:16px 0;border-bottom:1px solid #f5f5f5}
.lang-row:last-child{border-bottom:none}
.lang-code{font-size:0.72rem;font-weight:700;letter-spacing:2px;color:var(--gray)}
.lang-info .lang-name{font-weight:700;font-size:0.9rem}
.lang-info .lang-level{font-size:0.68rem;color:var(--gray);margin-top:2px}
.lang-bar{height:2px;background:#eee;position:relative;overflow:hidden;border-radius:0}
.lang-bar-fill{height:100%;width:0;transition:width 1.2s ease;border-radius:0}
.lang-pct{font-size:0.75rem;font-weight:700;text-align:right}
.lang-note{
  background:var(--light);border:1px solid var(--border);padding:22px 24px;
  max-width:540px;
}
.lang-note-code{font-size:0.62rem;letter-spacing:2px;color:var(--gray);margin-bottom:8px;font-weight:600}
.lang-note p{font-size:0.85rem;line-height:1.7;color:#444}
.lang-note strong{color:var(--dark)}
.lang-note em{color:var(--red);font-style:normal;font-weight:600}

/* ——— KONTAKT ——— */
#kontakt{background:var(--red);color:#fff}
#kontakt .section-wrap{display:grid;grid-template-columns:1fr 1fr;gap:60px;align-items:start}
#kontakt .section-code{color:rgba(255,255,255,0.6)}
#kontakt .section-heading{color:#fff;font-size:clamp(2rem,5vw,3.5rem);font-weight:800;line-height:1}
#kontakt .section-sub{color:rgba(255,255,255,0.8);max-width:400px}
.kontakt-info{display:flex;flex-direction:column;gap:16px;margin-top:8px}
.ki-row{display:flex;align-items:center;gap:14px}
.ki-icon{width:36px;height:36px;border:1px solid rgba(255,255,255,0.3);display:flex;align-items:center;justify-content:center;font-size:0.9rem;flex-shrink:0}
.ki-label{font-size:0.6rem;letter-spacing:2px;text-transform:uppercase;color:rgba(255,255,255,0.6);font-weight:600}
.ki-val{font-weight:600;font-size:0.9rem}
.ki-tags{margin-top:32px;padding-top:24px;border-top:1px solid rgba(255,255,255,0.2)}
.ki-tags-label{font-size:0.6rem;letter-spacing:2px;text-transform:uppercase;color:rgba(255,255,255,0.6);font-weight:600;margin-bottom:10px}
.ki-chip{display:inline-block;border:1px solid rgba(255,255,255,0.4);padding:5px 12px;font-size:0.68rem;letter-spacing:1px;margin:4px 4px 0 0;color:#fff}
.kontakt-form{background:#fff;padding:32px;color:var(--dark)}
.kf-label{font-size:0.62rem;letter-spacing:2px;text-transform:uppercase;color:var(--gray);font-weight:600;margin-bottom:6px;display:block}
.kf-label-row{font-size:0.65rem;letter-spacing:2px;color:rgba(255,255,255,0.5);font-weight:600;margin-bottom:14px}
.kf-input,.kf-textarea{
  width:100%;border:1px solid var(--border);padding:12px 14px;
  font-family:var(--font);font-size:0.9rem;color:var(--dark);
  background:#fff;outline:none;margin-bottom:14px;
  transition:border-color 0.2s;
}
.kf-input:focus,.kf-textarea:focus{border-color:var(--dark)}
.kf-textarea{resize:vertical;min-height:100px}
.kf-input::placeholder,.kf-textarea::placeholder{color:#bbb}
.btn-form{
  width:100%;padding:14px;background:var(--red);color:#fff;
  border:none;font-family:var(--font);font-size:0.82rem;font-weight:600;
  letter-spacing:1px;cursor:pointer;transition:background 0.2s;
  display:flex;align-items:center;justify-content:center;gap:8px;
}
.btn-form:hover{background:#c01e2e}
.form-success{display:none;text-align:center;padding:20px;color:var(--red);font-weight:600;font-size:0.9rem}

/* Footer */
.kontakt-footer{
  background:var(--red);border-top:1px solid rgba(255,255,255,0.15);
  padding:20px 60px;display:flex;justify-content:space-between;
  font-size:0.68rem;color:rgba(255,255,255,0.5);letter-spacing:1px;
}

/* ——— REVEAL ——— */
.reveal{opacity:0;transform:translateY(28px);transition:opacity 0.7s,transform 0.7s}
.reveal.visible{opacity:1;transform:none}

/* RESPONSIVE */
@media(max-width:900px){
  nav{padding:16px 24px}
  nav ul{display:none}
  .hero-inner{grid-template-columns:1fr;padding:0}
  #hero{padding:90px 24px 60px}
  .section-wrap{padding:70px 24px}
  .skills-grid{grid-template-columns:1fr 1fr}
  #kontakt .section-wrap{grid-template-columns:1fr}
  .kontakt-footer{padding:20px 24px;flex-direction:column;gap:4px}
}
@media(max-width:560px){
  .skills-grid{grid-template-columns:1fr}
  .lang-row{grid-template-columns:32px 110px 1fr 36px;gap:10px}
}
</style>
</head>
<body>

<div class="side-line"></div>
<div class="side-dot" id="side-dot"></div>

<!-- NAV -->
<nav>
  <div class="nav-logo">MT<span>.</span></div>
  <ul>
    <li><a href="#hero">Über mich</a></li>
    <li><a href="#werdegang">Werdegang</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#sprachen">Sprachen</a></li>
    <li><a href="#kontakt" class="nav-cta">Kontakt</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-inner">
    <div>
      <div class="hero-badge">● Offen für Ausbildung – Chemnitz, Deutschland</div>
      <h1 class="hero-name">
        <span class="first">Mykyta</span>
        <span class="last">Todorov</span>
      </h1>
      <div class="hero-divider"></div>
      <p class="hero-desc">
        Angehender <strong>Fachinformatiker</strong> für<br>
        Systemintegration & Anwendungsentwicklung.<br>
        Neugier in technische Kompetenz verwandeln.
      </p>
      <div class="hero-tags">
        <span class="hero-tag">⚙ Systemintegration</span>
        <span class="hero-tag">&lt;/&gt; Anwendungsentwicklung</span>
      </div>
      <div class="hero-btns">
        <a href="#kontakt" class="btn-red">Gespräch anfragen</a>
        <a href="#werdegang" class="btn-outline">Werdegang ansehen</a>
      </div>
    </div>
    <div class="snapshot-card reveal">
      <div class="snapshot-label">[Profil // Snapshot]</div>
      <div class="snapshot-row">
        <span class="snap-key">Schulbildung</span>
        <span class="snap-val">BBS Gerd Condé</span>
      </div>
      <div class="snapshot-row">
        <span class="snap-key">Standort</span>
        <span class="snap-val">Chemnitz, DE</span>
      </div>
      <div class="snapshot-row">
        <span class="snap-key">Sprachen</span>
        <span class="snap-val">5 Sprachen</span>
      </div>
      <div class="snapshot-row">
        <span class="snap-key">Verfügbar</span>
        <span class="snap-val green">Sofort</span>
      </div>
      <div class="snapshot-tags">
        <span class="snap-key">Kernkompetenzen</span>
        <div class="tag-chips">
          <span class="chip">Teamfähig</span>
          <span class="chip">Analytisch</span>
          <span class="chip">Lernbereit</span>
          <span class="chip">Kommunikativ</span>
        </div>
      </div>
    </div>
  </div>
  <div class="scroll-hint">
    <span>Scrollen</span>
    <div class="scroll-arrow"></div>
  </div>
</section>

<!-- WERDEGANG -->
<section id="werdegang">
  <div class="section-wrap">
    <div class="section-code reveal">[Section_02 // Werdegang]</div>
    <h2 class="section-heading reveal">Bildungs–<span>Reise</span></h2>
    <p class="section-sub reveal">Jeder Schritt war eine Lektion. Klicke auf einen Eintrag, um mehr zu erfahren.</p>
    <div class="timeline">

      <div class="tl-item">
        <div class="tl-dot-col"><div class="tl-dot active"></div><div class="tl-line"></div></div>
        <div class="tl-card reveal" onclick="toggleTl(this)">
          <div class="tl-card-header">
            <div>
              <div class="tl-meta"><span class="tl-badge">Aktuell</span> 📅 2025 – Aktuell</div>
              <div class="tl-title">BBS "Gerd Condé"</div>
              <div class="tl-place">📍 Chemnitz, Deutschland</div>
            </div>
            <div class="tl-arrow">▼</div>
          </div>
          <div class="tl-body"><p>Berufsschule mit Fokus auf IT-Systeme, Netzwerktechnik und Anwendungsentwicklung. Aktive Vorbereitung auf die Ausbildung zum Fachinformatiker für Systemintegration und Anwendungsentwicklung.</p></div>
        </div>
      </div>

      <div class="tl-item">
        <div class="tl-dot-col"><div class="tl-dot"></div><div class="tl-line"></div></div>
        <div class="tl-card reveal" onclick="toggleTl(this)">
          <div class="tl-card-header">
            <div>
              <div class="tl-meta">📅 2023 – 2025</div>
              <div class="tl-title">Dr.-Wilhelm-André-Gymnasium</div>
              <div class="tl-place">📍 Chemnitz, Deutschland</div>
            </div>
            <div class="tl-arrow">▼</div>
          </div>
          <div class="tl-body"><p>Allgemeinbildendes Gymnasium in Chemnitz. Stärkung analytischer und mathematischer Fähigkeiten. Erste Erfahrungen mit schulischen Projekten auf Deutsch.</p></div>
        </div>
      </div>

      <div class="tl-item">
        <div class="tl-dot-col"><div class="tl-dot"></div><div class="tl-line"></div></div>
        <div class="tl-card reveal" onclick="toggleTl(this)">
          <div class="tl-card-header">
            <div>
              <div class="tl-meta">📅 2022 – 2023</div>
              <div class="tl-title">Oberschule Gablenz</div>
              <div class="tl-place">📍 Chemnitz, Deutschland</div>
            </div>
            <div class="tl-arrow">▼</div>
          </div>
          <div class="tl-body"><p>Einstieg ins deutsche Schulsystem. Intensive Sprachförderung und schnelle Integration in den Unterricht trotz anfänglicher Sprachbarriere.</p></div>
        </div>
      </div>

      <div class="tl-item">
        <div class="tl-dot-col"><div class="tl-dot active"></div><div class="tl-line"></div></div>
        <div class="tl-card reveal" onclick="toggleTl(this)">
          <div class="tl-card-header">
            <div>
              <div class="tl-meta"><span class="tl-badge">Aktuell</span> 📅 2022 – Aktuell</div>
              <div class="tl-title">Chersoner Spezialschule Nr. 12 (Online)</div>
              <div class="tl-place">📍 Ukraine (Remote)</div>
            </div>
            <div class="tl-arrow">▼</div>
          </div>
          <div class="tl-body"><p>Parallele Schulbildung online auf Ukrainisch. Zeigt außergewöhnliche Selbstorganisation und die Fähigkeit, zwei Bildungssysteme gleichzeitig zu meistern.</p></div>
        </div>
      </div>

      <div class="tl-item">
        <div class="tl-dot-col"><div class="tl-dot"></div></div>
        <div class="tl-card reveal" onclick="toggleTl(this)">
          <div class="tl-card-header">
            <div>
              <div class="tl-meta">📅 2016 – 2022</div>
              <div class="tl-title">Chersoner Spezialschule Nr. 12</div>
              <div class="tl-place">📍 Cherson, Ukraine</div>
            </div>
            <div class="tl-arrow">▼</div>
          </div>
          <div class="tl-body"><p>Grundlegende Schulbildung in Cherson, Ukraine. Starkes Fundament in Mathematik, Naturwissenschaften und Sprachen. Frühe Entwicklung analytischen Denkens.</p></div>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="section-wrap">
    <div class="section-code reveal">[Section_03 // Kompetenzen]</div>
    <h2 class="section-heading reveal">Skill–<span>Architektur</span></h2>
    <p class="section-sub reveal">Hover über eine Karte, um den praktischen Kontext zu sehen — nicht nur das Was, sondern das Warum.</p>
    <div class="skills-grid">
      <div class="skill-card reveal">
        <div class="sk-type">Soft Skill</div>
        <div class="sk-icon">🤝</div>
        <div class="sk-name">Teamfähigkeit</div>
        <div class="sk-bar-wrap">
          <span class="sk-bar-label">Kompetenz</span>
          <div class="sk-bar"><div class="sk-bar-fill" data-w="95"></div></div>
          <span class="sk-pct" style="color:var(--red)">95%</span>
        </div>
        <div class="sk-desc">Durch Basketball und Fußball habe ich gelernt, wie man als Team funktioniert — Vertrauen, Kommunikation, gemeinsame Ziele.</div>
      </div>
      <div class="skill-card reveal" style="transition-delay:0.08s">
        <div class="sk-type">Core Skill</div>
        <div class="sk-icon">🔍</div>
        <div class="sk-name">Problemlösungskompetenz</div>
        <div class="sk-bar-wrap">
          <span class="sk-bar-label">Kompetenz</span>
          <div class="sk-bar"><div class="sk-bar-fill" data-w="88"></div></div>
          <span class="sk-pct" style="color:#2196f3">88%</span>
        </div>
        <div class="sk-desc">Analytisches Denken — Probleme in ihre Teile zerlegen, systematisch vorgehen, Lösungen entwickeln.</div>
      </div>
      <div class="skill-card reveal" style="transition-delay:0.16s">
        <div class="sk-type">Soft Skill</div>
        <div class="sk-icon">📋</div>
        <div class="sk-name">Organisationsfähigkeit</div>
        <div class="sk-bar-wrap">
          <span class="sk-bar-label">Kompetenz</span>
          <div class="sk-bar"><div class="sk-bar-fill" data-w="98"></div></div>
          <span class="sk-pct" style="color:#4caf50">98%</span>
        </div>
        <div class="sk-desc">Paralleles Führen von zwei Schulsystemen (Deutschland + Ukraine) erfordert höchste organisatorische Disziplin.</div>
      </div>
      <div class="skill-card reveal" style="transition-delay:0.24s">
        <div class="sk-type">Soft Skill</div>
        <div class="sk-icon">💬</div>
        <div class="sk-name">Verkaufsstärke</div>
        <div class="sk-bar-wrap">
          <span class="sk-bar-label">Kompetenz</span>
          <div class="sk-bar"><div class="sk-bar-fill" data-w="86"></div></div>
          <span class="sk-pct" style="color:#ff9800">86%</span>
        </div>
        <div class="sk-desc">Kommunikationsstärke und die Fähigkeit, Ideen überzeugend zu präsentieren — in Gesprächen und Präsentationen.</div>
      </div>
      <div class="skill-card reveal" style="transition-delay:0.08s">
        <div class="sk-type">Tech Interest</div>
        <div class="sk-icon">💻</div>
        <div class="sk-name">IT-Interesse</div>
        <div class="sk-bar-wrap">
          <span class="sk-bar-label">Kompetenz</span>
          <div class="sk-bar"><div class="sk-bar-fill" data-w="92"></div></div>
          <span class="sk-pct" style="color:var(--red)">92%</span>
        </div>
        <div class="sk-desc">Tiefes Interesse an Computersystemen, Netzwerken und Hardware. Motivation, diese Leidenschaft in ein professionelles Fundament zu verwandeln.</div>
      </div>
      <div class="skill-card reveal" style="transition-delay:0.16s">
        <div class="sk-type">Tech Interest</div>
        <div class="sk-icon">&lt;/&gt;</div>
        <div class="sk-name">Entwickler-Mindset</div>
        <div class="sk-bar-wrap">
          <span class="sk-bar-label">Kompetenz</span>
          <div class="sk-bar"><div class="sk-bar-fill" data-w="75"></div></div>
          <span class="sk-pct" style="color:#2196f3">75%</span>
        </div>
        <div class="sk-desc">Logisches Denken, das auch für die Anwendungsentwicklung relevant ist — Strukturen verstehen, Systeme aufbauen.</div>
      </div>
      <div class="skill-card reveal" style="transition-delay:0.24s">
        <div class="sk-type">Unique Strength</div>
        <div class="sk-icon">🌍</div>
        <div class="sk-name">Multikulturalität</div>
        <div class="sk-bar-wrap">
          <span class="sk-bar-label">Kompetenz</span>
          <div class="sk-bar"><div class="sk-bar-fill" data-w="98"></div></div>
          <span class="sk-pct" style="color:#4caf50">98%</span>
        </div>
        <div class="sk-desc">5 Sprachen, 3 Länder, diverse Kulturen. Diese Vielfalt macht mich zu einem besonderen Asset in internationalen Teams.</div>
      </div>
      <div class="skill-card reveal" style="transition-delay:0.32s">
        <div class="sk-type">Core Skill</div>
        <div class="sk-icon">⚡</div>
        <div class="sk-name">Lerngeschwindigkeit</div>
        <div class="sk-bar-wrap">
          <span class="sk-bar-label">Kompetenz</span>
          <div class="sk-bar"><div class="sk-bar-fill" data-w="94"></div></div>
          <span class="sk-pct" style="color:#ff9800">94%</span>
        </div>
        <div class="sk-desc">Innerhalb von 2 Jahren Deutsch von Null auf B2 gelernt und das deutsche Schulsystem gemeistert.</div>
      </div>
    </div>
  </div>
</section>

<!-- SPRACHEN -->
<section id="sprachen">
  <div class="section-wrap">
    <div class="section-code reveal">[Section_04 // Sprachkenntnisse]</div>
    <h2 class="section-heading reveal">Sprach–<span>Matrix</span></h2>
    <p class="section-sub reveal">5 Sprachen — ein Zeichen für Lernfähigkeit, Anpassung und interkulturelles Verständnis.</p>
    <div class="lang-list">
      <div class="lang-row reveal">
        <span class="lang-code">RU</span>
        <div class="lang-info"><div class="lang-name">Russisch</div><div class="lang-level">Muttersprache</div></div>
        <div class="lang-bar"><div class="lang-bar-fill" data-w="100" style="background:var(--red)"></div></div>
        <span class="lang-pct">100%</span>
      </div>
      <div class="lang-row reveal">
        <span class="lang-code">UA</span>
        <div class="lang-info"><div class="lang-name">Ukrainisch</div><div class="lang-level">Muttersprache</div></div>
        <div class="lang-bar"><div class="lang-bar-fill" data-w="100" style="background:var(--red)"></div></div>
        <span class="lang-pct">100%</span>
      </div>
      <div class="lang-row reveal">
        <span class="lang-code">DE</span>
        <div class="lang-info"><div class="lang-name">Deutsch</div><div class="lang-level">Fortgeschritten – B2</div></div>
        <div class="lang-bar"><div class="lang-bar-fill" data-w="80" style="background:#222"></div></div>
        <span class="lang-pct">80%</span>
      </div>
      <div class="lang-row reveal">
        <span class="lang-code">GB</span>
        <div class="lang-info"><div class="lang-name">Englisch</div><div class="lang-level">Gute Kenntnisse</div></div>
        <div class="lang-bar"><div class="lang-bar-fill" data-w="65" style="background:#222"></div></div>
        <span class="lang-pct">65%</span>
      </div>
      <div class="lang-row reveal">
        <span class="lang-code">FR</span>
        <div class="lang-info"><div class="lang-name">Französisch</div><div class="lang-level">Grundkenntnisse</div></div>
        <div class="lang-bar"><div class="lang-bar-fill" data-w="25" style="background:#aaa"></div></div>
        <span class="lang-pct">25%</span>
      </div>
    </div>
    <div class="lang-note reveal">
      <div class="lang-note-code">// Warum das wichtig ist</div>
      <p>Das Erlernen von 5 Sprachen ist kein Zufall — es ist Beweis für <strong>schnelle Mustererkennung</strong>, <strong>Ausdauer</strong> und die Fähigkeit, <em>komplexe Systeme zu verstehen</em>. Genau diese Fähigkeiten braucht ein guter Fachinformatiker.</p>
    </div>
  </div>
</section>

<!-- KONTAKT -->
<section id="kontakt">
  <div class="section-wrap">
    <div>
      <div class="section-code">[Section_05 // Kontakt]</div>
      <h2 class="section-heading" style="font-size:clamp(2.2rem,5vw,3.8rem);font-weight:800">Bereit für<br>das Gespräch.</h2>
      <p class="section-sub" style="color:rgba(255,255,255,0.8);margin-bottom:32px">Ich bin offen, motiviert und bereit — ein Gespräch könnte der erste Schritt zu einer erfolgreichen Zusammenarbeit sein.</p>
      <div class="kontakt-info">
        <div class="ki-row">
          <div class="ki-icon">✉</div>
          <div><div class="ki-label">Email</div><div class="ki-val">unikton44@gmail.com</div></div>
        </div>
        <div class="ki-row">
          <div class="ki-icon">📞</div>
          <div><div class="ki-label">Telefon</div><div class="ki-val">+49 0176 45994426</div></div>
        </div>
        <div class="ki-row">
          <div class="ki-icon">📍</div>
          <div><div class="ki-label">Standort</div><div class="ki-val">Steinwiese 22, Chemnitz</div></div>
        </div>
      </div>
      <div class="ki-tags">
        <div class="ki-tags-label">Ausbildungsinteresse</div>
        <span class="ki-chip">Fachinformatiker Systemintegration</span>
        <span class="ki-chip">Fachinformatiker Anwendungsentwicklung</span>
      </div>
    </div>
    <div>
      <div class="kontakt-form">
        <div class="kf-label-row" style="color:var(--gray);margin-bottom:20px">// Gesprächsanfrage</div>
        <div id="form-fields">
          <label class="kf-label">Ihr Name</label>
          <input class="kf-input" id="cf-name" placeholder="Max Mustermann" />
          <label class="kf-label">Unternehmen / Schule</label>
          <input class="kf-input" id="cf-company" placeholder="Musterfirma GmbH" />
          <label class="kf-label">Nachricht</label>
          <textarea class="kf-textarea" id="cf-msg" placeholder="Ich möchte Sie zu einem Vorstellungsgespräch einladen..."></textarea>
          <button class="btn-form" onclick="sendForm()">Gespräch anfragen →</button>
        </div>
        <div class="form-success" id="form-success">✓ Vielen Dank! Ich melde mich so schnell wie möglich.</div>
      </div>
    </div>
  </div>
</section>

<div class="kontakt-footer">
  <span>© 2025 Mykyta Todorov — Chemnitz, Deutschland</span>
  <span>Bewerber-Portfolio // Fachinformatiker</span>
</div>

<script>
// ——— Scroll reveal ———
const io = new IntersectionObserver(entries => {
  entries.forEach(e => { if(e.isIntersecting){e.target.classList.add('visible');io.unobserve(e.target)} });
},{threshold:0.12});
document.querySelectorAll('.reveal').forEach(el => io.observe(el));

// ——— Skill bars & lang bars on reveal ———
const barObs = new IntersectionObserver(entries => {
  entries.forEach(e => {
    if(!e.isIntersecting) return;
    e.target.querySelectorAll('.sk-bar-fill,.lang-bar-fill').forEach(bar => {
      bar.style.width = bar.dataset.w + '%';
    });
    barObs.unobserve(e.target);
  });
},{threshold:0.3});
document.querySelectorAll('.skill-card,.lang-row').forEach(el => barObs.observe(el));

// ——— Timeline toggle ———
function toggleTl(card){
  const isOpen = card.classList.contains('open');
  document.querySelectorAll('.tl-card.open').forEach(c => c.classList.remove('open'));
  if(!isOpen) card.classList.add('open');
}

// ——— Side dot scroll ———
window.addEventListener('scroll',()=>{
  const pct = window.scrollY/(document.body.scrollHeight-window.innerHeight);
  const dot = document.getElementById('side-dot');
  dot.style.top = (pct*90+5)+'vh';
});

// ——— Form submit ———
function sendForm(){
  const name = document.getElementById('cf-name').value.trim();
  const msg = document.getElementById('cf-msg').value.trim();
  if(!name||!msg) return;
  document.getElementById('form-fields').style.display='none';
  document.getElementById('form-success').style.display='block';
}
</script>
</body>
</html>
