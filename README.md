# LE-GBA23
Le jeu culture générale 
<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<meta name="theme-color" content="#070707">
<meta name="description" content="GBA – Grand Quiz Côte d'Ivoire : testez vos connaissances sur la culture, l'histoire, le sport et les guerres mondiales.">
<title>GBA – Grand Quiz Côte d'Ivoire</title>
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-XXXXXXXXXXXXXXXX" crossorigin="anonymous"></script>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Playfair+Display:ital,wght@0,700;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
:root{--or:#F47920;--ve:#009A44;--go:#C9A84C;--bg:#070707;--c1:#111;--c2:#1A1A1A;--tx:#E8E4DC;--g1:#444;--g2:#888;--W:520px}
*,*::before,*::after{margin:0;padding:0;box-sizing:border-box;-webkit-tap-highlight-color:transparent}
html,body{width:100%;height:100%;overflow:hidden;background:var(--bg);color:var(--tx);font-family:'DM Sans',sans-serif}
#app{position:fixed;inset:0;overflow:hidden}
#app::before{content:'';position:absolute;inset:0;pointer-events:none;z-index:0;background:repeating-linear-gradient(60deg,transparent,transparent 50px,rgba(244,121,32,.018) 50px,rgba(244,121,32,.018) 51px),repeating-linear-gradient(-60deg,transparent,transparent 50px,rgba(0,154,68,.018) 50px,rgba(0,154,68,.018) 51px)}
.pg{position:absolute;inset:0;z-index:1;overflow-y:auto;overflow-x:hidden;-webkit-overflow-scrolling:touch;display:none;background:var(--bg)}
.pg.show{display:block;animation:pgIn .35s cubic-bezier(.25,.46,.45,.94) both}
.pg.out{animation:pgOut .28s cubic-bezier(.55,0,1,.45) both}
@keyframes pgIn{from{opacity:0;transform:translateX(36px)}to{opacity:1;transform:none}}
@keyframes pgOut{from{opacity:1;transform:none}to{opacity:0;transform:translateX(-36px)}}
.pg::-webkit-scrollbar{width:3px}.pg::-webkit-scrollbar-track{background:transparent}.pg::-webkit-scrollbar-thumb{background:rgba(255,255,255,.1);border-radius:2px}
.pgi{max-width:var(--W);margin:0 auto;padding:22px 18px 100px}
/* BUTTONS */
.btn{display:block;width:100%;padding:16px;font-family:'Bebas Neue',sans-serif;font-size:20px;letter-spacing:4px;border:none;border-radius:12px;cursor:pointer;transition:transform .14s,box-shadow .14s;text-align:center}
.btn:active{transform:scale(.97)}
.btn-or{background:linear-gradient(135deg,var(--or),#c44a00);color:#fff;box-shadow:0 6px 26px rgba(244,121,32,.38)}
.btn-or:hover{box-shadow:0 10px 34px rgba(244,121,32,.55)}
.btn-out{background:transparent;border:1.5px solid rgba(255,255,255,.14);color:var(--tx);box-shadow:none}
.btn-out:hover{border-color:var(--or);color:var(--or)}
.btn-sm{font-size:15px;letter-spacing:3px;padding:12px}
.btn-bk{display:inline-flex;align-items:center;justify-content:center;background:var(--c1);border:1px solid rgba(255,255,255,.08);border-radius:10px;width:38px;height:38px;cursor:pointer;font-size:18px;color:var(--tx);flex-shrink:0}
/* CARDS */
.card{background:var(--c1);border:1.5px solid rgba(255,255,255,.07);border-radius:13px;padding:18px 16px}
/* PILLS */
.pill{display:inline-flex;align-items:center;gap:5px;background:var(--c2);border:1px solid rgba(255,255,255,.07);border-radius:20px;padding:5px 12px;font-size:12px}
.pill .v{font-weight:600;color:var(--go)}
.bdg-or{display:inline-flex;align-items:center;gap:5px;background:rgba(244,121,32,.1);border:1px solid rgba(244,121,32,.25);color:var(--or);border-radius:20px;padding:3px 10px;font-size:11px;letter-spacing:1px;text-transform:uppercase}
.bdg-go{display:inline-flex;align-items:center;gap:5px;background:rgba(201,168,76,.1);border:1px solid rgba(201,168,76,.25);color:var(--go);border-radius:20px;padding:3px 10px;font-size:11px;letter-spacing:1px;text-transform:uppercase}
/* PROGRESS */
.pbw{height:3px;background:rgba(255,255,255,.07);border-radius:2px;margin-bottom:18px;overflow:hidden}
.pbf{height:100%;background:linear-gradient(90deg,var(--or),var(--ve));border-radius:2px;transition:width .55s ease}
/* QUESTION IMAGE */
.qimg{width:100%;height:175px;border-radius:12px;overflow:hidden;position:relative;background:var(--c2);margin-bottom:13px;border:1px solid rgba(255,255,255,.07);display:none}
.qimg.vis{display:block}
.qimg img{position:absolute;inset:0;width:100%;height:100%;object-fit:cover;opacity:0;transition:opacity .55s}
.qimg img.ok{opacity:1}
.shim{position:absolute;inset:0;background:linear-gradient(90deg,var(--c2) 25%,rgba(255,255,255,.04) 50%,var(--c2) 75%);background-size:200% 100%;animation:shim 1.3s infinite}
.shim.off{display:none}
.emoj{position:absolute;inset:0;display:flex;align-items:center;justify-content:center;font-size:52px;opacity:.14;pointer-events:none}
.cred{position:absolute;bottom:0;right:0;background:rgba(0,0,0,.5);color:rgba(255,255,255,.28);font-size:8px;padding:2px 7px;border-radius:4px 0 0 0}
@keyframes shim{0%{background-position:200% 0}100%{background-position:-200% 0}}
/* TIMER */
.trow{display:flex;align-items:center;gap:10px;margin-bottom:13px}
.tarc{width:44px;height:44px;flex-shrink:0}
.tarc circle{fill:none;stroke-width:3.5}
.tarc .tbg{stroke:rgba(255,255,255,.07)}
.tarc .tfg{stroke:var(--or);stroke-linecap:round;transition:stroke-dashoffset 1s linear,stroke .3s}
.tlbl{font-family:'Bebas Neue',sans-serif;font-size:28px;color:var(--or);line-height:1}
/* TEXT OPTIONS */
.og-t{display:grid;grid-template-columns:1fr 1fr;gap:9px;margin-bottom:13px}
@media(max-width:380px){.og-t{grid-template-columns:1fr}}
.ob{background:var(--c1);border:1.5px solid rgba(255,255,255,.08);border-radius:10px;padding:12px 13px;text-align:left;color:var(--tx);font-family:'DM Sans',sans-serif;font-size:13px;cursor:pointer;transition:all .17s;display:flex;align-items:center;gap:9px}
.ol{width:26px;height:26px;border-radius:6px;flex-shrink:0;background:rgba(255,255,255,.06);display:flex;align-items:center;justify-content:center;font-size:11px;font-weight:700;color:var(--g1);transition:all .17s}
.ob:hover:not(:disabled){border-color:rgba(244,121,32,.4);background:rgba(244,121,32,.05)}
.ob:hover:not(:disabled) .ol{background:rgba(244,121,32,.2);color:var(--or)}
.ob.ok{border-color:var(--ve)!important;background:rgba(0,154,68,.12)!important;animation:pop .3s}
.ob.ok .ol{background:var(--ve)!important;color:#fff!important}
.ob.ko{border-color:#E53935!important;background:rgba(229,57,53,.08)!important}
.ob.ko .ol{background:#E53935!important;color:#fff!important}
/* PHOTO OPTIONS */
.og-p{display:grid;grid-template-columns:1fr 1fr;gap:9px;margin-bottom:13px}
.po{position:relative;border-radius:12px;overflow:hidden;border:2px solid rgba(255,255,255,.08);aspect-ratio:1;background:var(--c2);cursor:pointer;transition:all .2s}
.po:hover:not(.off){border-color:var(--or);transform:scale(1.03);box-shadow:0 6px 18px rgba(244,121,32,.3)}
.po img{position:absolute;inset:0;width:100%;height:100%;object-fit:cover;opacity:0;transition:opacity .45s}
.po img.ok{opacity:1}
.psh{position:absolute;inset:0;background:linear-gradient(90deg,var(--c2) 25%,rgba(255,255,255,.05) 50%,var(--c2) 75%);background-size:200% 100%;animation:shim 1.3s infinite}
.psh.off{display:none}
.pei{position:absolute;inset:0;display:flex;align-items:center;justify-content:center;font-size:30px;opacity:.22;pointer-events:none}
.plb{position:absolute;bottom:0;left:0;right:0;background:linear-gradient(to top,rgba(0,0,0,.88),transparent);color:#fff;font-size:11px;font-weight:500;padding:17px 8px 7px;text-align:center}
.pbg{position:absolute;top:7px;left:7px;width:24px;height:24px;border-radius:7px;background:rgba(0,0,0,.65);display:flex;align-items:center;justify-content:center;font-family:'Bebas Neue',sans-serif;font-size:13px;color:rgba(255,255,255,.8)}
.po.ok{border-color:var(--ve)!important;animation:pop .3s}
.po.ok::after{content:'';position:absolute;inset:0;background:rgba(0,154,68,.18)}
.po.ok .plb{background:linear-gradient(to top,rgba(0,110,44,.9),transparent)}
.po.ko{border-color:#E53935!important}
.po.ko::after{content:'';position:absolute;inset:0;background:rgba(229,57,53,.1)}
.po.off{cursor:default;pointer-events:none}
/* EXPLANATION + WIKI LINK */
.exp{background:var(--c2);border-left:3px solid var(--go);border-radius:0 10px 10px 0;padding:12px 15px;font-size:13px;color:#C0B8A8;line-height:1.65;margin:11px 0;display:none;animation:fadeUp .33s ease}
.exp.vis{display:block}
.exp strong{color:var(--go)}
.wiki-link{display:inline-flex;align-items:center;gap:7px;margin-top:9px;padding:7px 14px;background:rgba(201,168,76,.1);border:1px solid rgba(201,168,76,.28);border-radius:20px;color:var(--go);font-size:12px;font-weight:500;text-decoration:none;transition:all .2s}
.wiki-link:hover{background:rgba(201,168,76,.2);transform:translateX(3px)}
/* AUTO-NEXT */
.an-lbl{font-size:10px;color:var(--g1);text-align:right;margin-bottom:3px;display:none;letter-spacing:.5px}
.an-lbl.vis{display:block}
.an-bar{height:2px;background:rgba(255,255,255,.07);border-radius:2px;overflow:hidden;margin-bottom:12px;display:none}
.an-bar.vis{display:block}
.an-fil{height:100%;width:100%;background:linear-gradient(90deg,var(--go),var(--or));border-radius:2px}
/* RESULT RING */
.rring{width:155px;height:155px;margin:0 auto 20px;position:relative}
.rring svg{transform:rotate(-90deg)}
.rsc{position:absolute;inset:0;display:flex;flex-direction:column;align-items:center;justify-content:center}
.rsn{font-family:'Bebas Neue',sans-serif;font-size:52px;color:var(--go);line-height:1}
.rsd{font-size:12px;color:var(--g1)}
/* RECAP DOTS */
.recap{display:flex;flex-wrap:wrap;gap:5px;justify-content:center;margin:12px 0 20px}
.rdot{width:22px;height:22px;border-radius:50%}
.rdot.ok{background:var(--ve)}
.rdot.ko{background:#E53935}
/* HOME */
.logo-ring{width:108px;height:108px;border-radius:50%;background:conic-gradient(var(--or) 33%,#fff 33% 66%,var(--ve) 66%);display:flex;align-items:center;justify-content:center;margin:0 auto 16px;animation:pulse 3s infinite}
.logo-in{width:80px;height:80px;border-radius:50%;background:var(--bg);display:flex;align-items:center;justify-content:center;font-family:'Bebas Neue',sans-serif;font-size:27px;color:var(--go);letter-spacing:2px}
.hstat{text-align:center;flex:1}
.hstat .hn{font-family:'Bebas Neue',sans-serif;font-size:27px;color:var(--go)}
.hstat .hl{font-size:10px;color:var(--g1);text-transform:uppercase;letter-spacing:1px}
/* MODE CARDS */
.mcard{display:flex;align-items:center;gap:14px;background:var(--c1);border:2px solid rgba(255,255,255,.08);border-radius:14px;padding:17px 15px;cursor:pointer;transition:all .2s;margin-bottom:11px}
.mcard:hover,.mcard:active{border-color:var(--or);background:rgba(244,121,32,.06)}
.mcard .mico{font-size:34px;flex-shrink:0}
.mcard .mtit{font-family:'Bebas Neue',sans-serif;font-size:20px;letter-spacing:2px;margin-bottom:3px}
.mcard .mdes{font-size:12px;color:var(--g2);line-height:1.5}
.mcard .marr{margin-left:auto;font-size:20px;color:var(--g1);flex-shrink:0}
/* ADS */
.ad-box{width:100%;border-radius:11px;overflow:hidden;border:1px solid rgba(255,255,255,.05);background:linear-gradient(135deg,rgba(244,121,32,.04),rgba(0,154,68,.04));display:flex;flex-direction:column;align-items:center;justify-content:center;gap:5px;padding:13px;margin:13px 0;position:relative;min-height:78px}
.ad-box .albl{position:absolute;top:5px;right:7px;font-size:8px;color:var(--g1);letter-spacing:1px;text-transform:uppercase}
.ad-box .aico{font-size:18px}
.ad-box .atxt{font-size:11px;color:var(--g2);text-align:center;line-height:1.5}
.ad-box a{font-size:11px;font-weight:600;color:var(--or);border:1px solid rgba(244,121,32,.35);border-radius:20px;padding:4px 13px;text-decoration:none;margin-top:2px;cursor:pointer}
.ad-stick{position:fixed;bottom:0;left:0;right:0;z-index:999;background:rgba(7,7,7,.96);backdrop-filter:blur(8px);border-top:1px solid rgba(255,255,255,.06);padding:7px 16px 9px;display:flex;align-items:center;justify-content:center}
.ad-stick-in{max-width:var(--W);width:100%;position:relative;display:flex;align-items:center;justify-content:center;min-height:42px}
.ad-x{position:absolute;top:-22px;right:0;width:20px;height:20px;border-radius:50%;background:var(--c2);border:1px solid rgba(255,255,255,.1);cursor:pointer;display:flex;align-items:center;justify-content:center;font-size:9px;color:var(--g2)}
/* AD INTER */
.ad-ib{background:var(--c2);border:1px solid rgba(255,255,255,.07);border-radius:15px;padding:26px 18px;min-height:170px;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:8px;margin-bottom:18px;text-align:center;width:100%}
.sk-bar{height:3px;background:rgba(255,255,255,.07);border-radius:2px;overflow:hidden;margin-bottom:8px;width:100%}
.sk-fil{height:100%;background:var(--go);border-radius:2px;width:0}
/* ANIMATIONS */
@keyframes pop{0%{transform:scale(1)}50%{transform:scale(1.025)}100%{transform:scale(1)}}
@keyframes fadeUp{from{opacity:0;transform:translateY(8px)}to{opacity:1;transform:none}}
@keyframes pulse{0%,100%{box-shadow:0 0 36px rgba(244,121,32,.28)}50%{box-shadow:0 0 65px rgba(244,121,32,.58)}}
</style>
</head>
<body>
<div id="app">

<!-- ▐▌▐▌▐▌  PAGE 1 — ACCUEIL  ▐▌▐▌▐▌ -->
<div class="pg" id="p-home">
  <div class="pgi" style="text-align:center;min-height:100vh;display:flex;flex-direction:column;align-items:center;justify-content:center">

    <div class="ad-box" style="width:100%;margin-bottom:20px">
      <span class="albl">Annonce</span>
      <div class="aico">📢</div>
      <div class="atxt">Espace Google AdSense — Activez pour monétiser</div>
      <a href="https://adsense.google.com" target="_blank" rel="noopener">Activer AdSense →</a>
    </div>

    <div class="logo-ring"><div class="logo-in">GBA</div></div>
    <div style="font-family:'Playfair Display',serif;font-style:italic;font-size:15px;color:var(--go);letter-spacing:2px;margin-bottom:4px">Grand Quiz de la</div>
    <div style="font-family:'Bebas Neue',sans-serif;font-size:clamp(42px,11vw,78px);letter-spacing:8px;line-height:1;background:linear-gradient(135deg,var(--or),var(--go),var(--ve));-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;margin-bottom:4px">CÔTE D'IVOIRE</div>
    <div style="font-size:10px;color:var(--g1);letter-spacing:3px;text-transform:uppercase;margin-bottom:26px">Culture · Histoire · Guerres · Rap · Photos</div>

    <div style="display:flex;gap:9px;width:100%;max-width:var(--W);margin-bottom:26px">
      <div class="card hstat" style="flex:1"><div class="hn" id="st-q">41</div><div class="hl">Questions</div></div>
      <div class="card hstat" style="flex:1"><div class="hn">9</div><div class="hl">Catégories</div></div>
      <div class="card hstat" style="flex:1"><div class="hn">2</div><div class="hl">Modes</div></div>
    </div>

    <div style="width:100%;max-width:var(--W)">
      <button class="btn btn-or" onclick="nav('p-mode')">JOUER MAINTENANT →</button>
    </div>

  </div>
</div>

<!-- ▐▌▐▌▐▌  PAGE 2 — CHOIX DU MODE  ▐▌▐▌▐▌ -->
<div class="pg" id="p-mode">
  <div class="pgi">

    <div style="display:flex;align-items:center;gap:12px;margin-bottom:22px;padding-top:6px">
      <button class="btn-bk" onclick="back()">←</button>
      <div>
        <div style="font-family:'Bebas Neue',sans-serif;font-size:23px;letter-spacing:3px">CHOISIR UN MODE</div>
        <div style="font-size:11px;color:var(--g2)">Sélectionne comment jouer</div>
      </div>
    </div>

    <div class="mcard" onclick="startGame('txt')">
      <div class="mico">📝</div>
      <div>
        <div class="mtit">QUIZ TEXTE</div>
        <div class="mdes">4 réponses en texte — questions aléatoires sur tous les thèmes CI et mondiaux.</div>
        <span style="display:inline-block;margin-top:5px;background:rgba(0,154,68,.12);border:1px solid rgba(0,154,68,.3);color:var(--ve);border-radius:20px;padding:2px 10px;font-size:10px">✓ CLASSIQUE</span>
      </div>
      <div class="marr">›</div>
    </div>

    <div class="mcard" onclick="startGame('pic')">
      <div class="mico">📸</div>
      <div>
        <div class="mtit">QUIZ PHOTOS</div>
        <div class="mdes">Clique sur la bonne photo parmi 4 images ! Monuments, personnages, batailles…</div>
        <span style="display:inline-block;margin-top:5px;background:rgba(201,168,76,.12);border:1px solid rgba(201,168,76,.3);color:var(--go);border-radius:20px;padding:2px 10px;font-size:10px">⭐ NOUVEAU</span>
      </div>
      <div class="marr">›</div>
    </div>

    <div class="ad-box">
      <span class="albl">Annonce</span>
      <div class="aico">💡</div>
      <div class="atxt">Google AdSense — Bannière 320×100<br>Gagnez de l'argent à chaque visite</div>
      <a href="https://adsense.google.com" target="_blank" rel="noopener">Créer mon compte</a>
    </div>

    <div style="background:var(--c2);border-radius:12px;padding:13px">
      <div style="font-size:10px;color:var(--g2);text-transform:uppercase;letter-spacing:1px;margin-bottom:8px">CATÉGORIES</div>
      <div id="cat-chips" style="display:flex;flex-wrap:wrap;gap:6px"></div>
    </div>

  </div>
</div>

<!-- ▐▌▐▌▐▌  PAGE 3 — QUESTION  ▐▌▐▌▐▌ -->
<div class="pg" id="p-q">
  <div class="pgi">

    <div style="display:flex;align-items:center;justify-content:space-between;margin-bottom:13px;gap:8px">
      <div style="display:flex;gap:7px">
        <div class="pill">✅ <span class="v" id="q-sc">0</span></div>
        <div class="pill">🔥 <span class="v" id="q-st">0</span></div>
      </div>
      <div class="pill">❓ <span class="v" id="q-nm">1/10</span></div>
    </div>

    <div class="pbw"><div class="pbf" id="q-pb" style="width:0%"></div></div>

    <div style="display:flex;gap:6px;flex-wrap:wrap;margin-bottom:7px">
      <div class="bdg-or" id="q-cat">—</div>
      <div class="bdg-go" id="q-mbd" style="display:none">📸 PHOTOS</div>
    </div>
    <div style="font-size:10px;color:var(--g1);letter-spacing:2px;text-transform:uppercase;margin-bottom:7px" id="q-lbl">QUESTION 1</div>

    <!-- image (mode texte) -->
    <div class="qimg" id="q-img">
      <div class="shim" id="q-sh"></div>
      <div class="emoj" id="q-ei"></div>
      <img id="q-imgel" src="" alt="">
      <div class="cred" id="q-cr"></div>
    </div>

    <div style="font-family:'Playfair Display',serif;font-size:clamp(15px,3.5vw,21px);line-height:1.5;margin-bottom:15px" id="q-txt">…</div>

    <div class="trow">
      <svg class="tarc" viewBox="0 0 44 44">
        <circle class="tbg" cx="22" cy="22" r="18"/>
        <circle class="tfg" id="q-tc" cx="22" cy="22" r="18" stroke-dasharray="113" stroke-dashoffset="0"/>
      </svg>
      <span class="tlbl" id="q-tl">20</span>
    </div>

    <div class="og-t" id="q-ot"></div>
    <div class="og-p" id="q-op" style="display:none"></div>

    <div class="exp" id="q-exp"></div>

    <div class="an-lbl" id="q-al">SUIVANTE DANS <span id="q-ac">4</span>s…</div>
    <div class="an-bar" id="q-ab"><div class="an-fil" id="q-af"></div></div>

    <button class="btn btn-out btn-sm" id="q-bn" onclick="nextQ()" style="display:none">SUIVANT →</button>

  </div>
</div>

<!-- ▐▌▐▌▐▌  PAGE 4 — PUB INTERSTITIELLE  ▐▌▐▌▐▌ -->
<div class="pg" id="p-ad">
  <div class="pgi" style="display:flex;flex-direction:column;align-items:center;justify-content:center;min-height:100vh;text-align:center">
    <div style="font-size:11px;color:var(--g1);letter-spacing:2px;text-transform:uppercase;margin-bottom:13px">⏸ PAUSE PUB</div>

    <div class="ad-ib" style="max-width:var(--W)">
      <ins class="adsbygoogle" style="display:block;width:100%;min-height:100px"
           data-ad-client="ca-pub-XXXXXXXXXXXXXXXX"
           data-ad-slot="0000000000"
           data-ad-format="auto"
           data-full-width-responsive="true"></ins>
      <div class="aico">📢</div>
      <div style="font-family:'Bebas Neue',sans-serif;font-size:19px;letter-spacing:3px;color:var(--go)">ESPACE PUBLICITAIRE</div>
      <div style="font-size:11px;co
