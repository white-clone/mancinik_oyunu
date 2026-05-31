<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mancınık Matematik Savaşı</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=MedievalSharp&family=Cinzel:wght@400;700;900&family=Lora:wght@400;600&display=swap');

  :root {
    --sky: #1a0a2e;
    --sky2: #16213e;
    --ground: #2d1b0e;
    --ground2: #3d2510;
    --stone: #8b7355;
    --stone-dark: #5c4a32;
    --gold: #d4a017;
    --gold2: #f0c040;
    --red: #c0392b;
    --green: #27ae60;
    --wood: #8b5e3c;
    --wood2: #a0714f;
    --hp-red: #e74c3c;
    --hp-green: #2ecc71;
    --text-light: #f5e6c8;
    --text-dim: #a89070;
    --castle-p1: #4a6fa5;
    --castle-p2: #a54a4a;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: var(--sky);
    font-family: 'Lora', serif;
    overflow: hidden;
    height: 100vh;
    display: flex;
    flex-direction: column;
    user-select: none;
  }

  /* ── STARS ── */
  #stars {
    position: fixed; top: 0; left: 0; width: 100%; height: 60%;
    pointer-events: none; z-index: 0;
  }

  /* ── GAME CANVAS AREA ── */
  #game-area {
    position: relative;
    width: 100%;
    height: 280px;
    flex-shrink: 0;
    background: linear-gradient(180deg, #0d0520 0%, #1a0a2e 40%, #16213e 100%);
    overflow: hidden;
    border-bottom: 3px solid var(--gold);
  }

  /* Moon */
  #moon {
    position: absolute; top: 20px; left: 50%;
    transform: translateX(-50%);
    width: 50px; height: 50px;
    background: radial-gradient(circle at 35% 35%, #ffe566, #f0c040);
    border-radius: 50%;
    box-shadow: 0 0 30px 10px rgba(240,192,64,0.3);
  }

  /* Ground */
  #ground {
    position: absolute; bottom: 0; left: 0; right: 0;
    height: 60px;
    background: linear-gradient(180deg, var(--ground2) 0%, var(--ground) 100%);
    border-top: 3px solid #5a3a1a;
  }

  /* Grass */
  #ground::before {
    content: '';
    position: absolute; top: -8px; left: 0; right: 0; height: 12px;
    background: repeating-linear-gradient(90deg, #2d6a2d 0px, #3a7a3a 10px, #2d6a2d 20px);
    border-radius: 4px 4px 0 0;
  }

  /* ── CATAPULT SVGs ── */
  .catapult {
    position: absolute;
    bottom: 52px;
    width: 100px;
    height: 80px;
  }
  #catapult1 { left: 40px; }
  #catapult2 { right: 40px; transform: scaleX(-1); }

  /* ── CASTLES ── */
  .castle {
    position: absolute;
    bottom: 58px;
    width: 90px;
    height: 120px;
  }
  #castle1 { left: 150px; }
  #castle2 { right: 150px; }

  /* ── HP BARS ── */
  .hp-bar-wrap {
    position: absolute;
    top: 10px;
    width: 160px;
  }
  #hp1-wrap { left: 10px; }
  #hp2-wrap { right: 10px; }
  .hp-label {
    font-family: 'Cinzel', serif;
    font-size: 11px;
    color: var(--gold2);
    text-shadow: 0 0 8px rgba(240,192,64,0.6);
    margin-bottom: 3px;
  }
  .hp-bar-bg {
    width: 100%; height: 14px;
    background: #1a0a0a;
    border: 2px solid var(--stone);
    border-radius: 3px;
    overflow: hidden;
  }
  .hp-bar-fill {
    height: 100%;
    background: linear-gradient(90deg, #e74c3c, #c0392b);
    transition: width 0.5s ease;
    border-radius: 2px;
  }
  .hp-text {
    font-size: 10px;
    color: var(--text-dim);
    margin-top: 2px;
  }

  /* ── PROJECTILE ── */
  #projectile {
    position: absolute;
    width: 22px; height: 22px;
    border-radius: 50%;
    background: radial-gradient(circle at 35% 35%, #888, #333);
    box-shadow: 0 0 8px rgba(0,0,0,0.6);
    display: none;
    z-index: 10;
  }

  /* ── EXPLOSION ── */
  #explosion {
    position: absolute;
    width: 60px; height: 60px;
    border-radius: 50%;
    display: none;
    z-index: 11;
    pointer-events: none;
  }

  /* ── TURN INDICATOR ── */
  #turn-indicator {
    position: absolute;
    top: 10px;
    left: 50%;
    transform: translateX(-50%);
    font-family: 'Cinzel', serif;
    font-size: 13px;
    color: var(--gold2);
    text-align: center;
    text-shadow: 0 0 10px rgba(240,192,64,0.7);
    background: rgba(0,0,0,0.5);
    padding: 4px 14px;
    border: 1px solid var(--gold);
    border-radius: 4px;
    white-space: nowrap;
  }

  /* ── QUIZ PANEL ── */
  #quiz-panel {
    flex: 1;
    background: linear-gradient(180deg, #0d0520 0%, #160830 100%);
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 16px 20px 10px;
    overflow-y: auto;
    position: relative;
  }

  #quiz-panel::before {
    content: '';
    position: absolute; top: 0; left: 0; right: 0; height: 3px;
    background: linear-gradient(90deg, transparent, var(--gold), transparent);
  }

  #q-category {
    font-family: 'Cinzel', serif;
    font-size: 11px;
    color: var(--gold);
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-bottom: 6px;
    opacity: 0.8;
  }

  #q-number {
    font-family: 'Cinzel', serif;
    font-size: 12px;
    color: var(--text-dim);
    margin-bottom: 8px;
  }

  #q-text {
    font-size: 15px;
    color: var(--text-light);
    text-align: center;
    max-width: 680px;
    line-height: 1.6;
    margin-bottom: 14px;
    text-shadow: 0 1px 4px rgba(0,0,0,0.5);
  }

  #q-type-badge {
    display: inline-block;
    font-size: 10px;
    font-family: 'Cinzel', serif;
    letter-spacing: 1px;
    padding: 2px 10px;
    border-radius: 12px;
    margin-bottom: 10px;
  }
  .badge-mc { background: #1a3a5c; color: #6ab4f5; border: 1px solid #2a5a8c; }
  .badge-tf { background: #1a3a1a; color: #6af56a; border: 1px solid #2a7a2a; }

  #options-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
    width: 100%;
    max-width: 620px;
    margin-bottom: 10px;
  }

  .opt-btn {
    background: linear-gradient(135deg, #1a0a2e, #2a1248);
    border: 2px solid var(--stone-dark);
    color: var(--text-light);
    font-family: 'Lora', serif;
    font-size: 13px;
    padding: 12px 16px;
    border-radius: 6px;
    cursor: pointer;
    text-align: left;
    transition: all 0.2s ease;
    position: relative;
    overflow: hidden;
  }
  .opt-btn::before {
    content: '';
    position: absolute; top: 0; left: -100%; width: 100%; height: 100%;
    background: linear-gradient(90deg, transparent, rgba(212,160,23,0.15), transparent);
    transition: left 0.3s;
  }
  .opt-btn:hover:not(:disabled)::before { left: 100%; }
  .opt-btn:hover:not(:disabled) {
    border-color: var(--gold);
    color: var(--gold2);
    transform: translateY(-2px);
    box-shadow: 0 4px 15px rgba(212,160,23,0.3);
  }
  .opt-btn:disabled { cursor: not-allowed; opacity: 0.7; }
  .opt-btn.correct {
    border-color: var(--hp-green) !important;
    background: linear-gradient(135deg, #0a2a0a, #1a4a1a) !important;
    color: #7aff7a !important;
  }
  .opt-btn.wrong {
    border-color: var(--hp-red) !important;
    background: linear-gradient(135deg, #2a0a0a, #4a1a1a) !important;
    color: #ff7a7a !important;
  }

  #feedback-msg {
    font-family: 'Cinzel', serif;
    font-size: 15px;
    text-align: center;
    min-height: 22px;
    margin-bottom: 6px;
    font-weight: 700;
    text-shadow: 0 0 10px currentColor;
  }
  .fb-correct { color: #5aff5a; }
  .fb-wrong { color: #ff5a5a; }

  #next-btn {
    display: none;
    font-family: 'Cinzel', serif;
    font-size: 13px;
    background: linear-gradient(135deg, var(--gold), #b8860b);
    color: #1a0a00;
    border: none;
    padding: 10px 32px;
    border-radius: 5px;
    cursor: pointer;
    font-weight: 700;
    letter-spacing: 1px;
    transition: all 0.2s;
    box-shadow: 0 3px 10px rgba(212,160,23,0.4);
  }
  #next-btn:hover { transform: translateY(-2px); box-shadow: 0 5px 18px rgba(212,160,23,0.6); }

  /* ── SCORE BAR ── */
  #score-bar {
    display: flex;
    justify-content: space-around;
    align-items: center;
    background: rgba(0,0,0,0.4);
    border-top: 2px solid var(--stone-dark);
    padding: 6px 20px;
    flex-shrink: 0;
  }
  .score-item {
    font-family: 'Cinzel', serif;
    font-size: 12px;
    color: var(--text-dim);
    text-align: center;
  }
  .score-item span {
    display: block;
    font-size: 18px;
    font-weight: 700;
  }
  #s1 span { color: var(--castle-p1); text-shadow: 0 0 10px var(--castle-p1); }
  #s2 span { color: var(--castle-p2); text-shadow: 0 0 10px var(--castle-p2); }
  #sq span { color: var(--gold2); }

  /* ── OVERLAY ── */
  #overlay {
    display: none;
    position: fixed; inset: 0;
    background: rgba(0,0,0,0.85);
    z-index: 100;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  #overlay.active { display: flex; }
  #overlay-box {
    background: linear-gradient(135deg, #0d0520, #1a0a2e);
    border: 3px solid var(--gold);
    border-radius: 12px;
    padding: 40px 60px;
    text-align: center;
    max-width: 500px;
    width: 90%;
    box-shadow: 0 0 60px rgba(212,160,23,0.3);
  }
  #overlay-title {
    font-family: 'Cinzel', serif;
    font-size: 28px;
    color: var(--gold2);
    text-shadow: 0 0 20px rgba(240,192,64,0.8);
    margin-bottom: 12px;
  }
  #overlay-sub {
    font-size: 16px;
    color: var(--text-light);
    margin-bottom: 24px;
    line-height: 1.6;
  }
  #overlay-btn {
    font-family: 'Cinzel', serif;
    font-size: 15px;
    background: linear-gradient(135deg, var(--gold), #b8860b);
    color: #1a0a00;
    border: none;
    padding: 12px 40px;
    border-radius: 6px;
    cursor: pointer;
    font-weight: 700;
    letter-spacing: 1px;
    transition: all 0.2s;
  }
  #overlay-btn:hover { transform: scale(1.05); }

  /* ── START SCREEN ── */
  #start-screen {
    display: flex;
    position: fixed; inset: 0;
    background: radial-gradient(ellipse at center, #1a0a2e 0%, #0a0515 100%);
    z-index: 200;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  #start-screen h1 {
    font-family: 'Cinzel', serif;
    font-size: clamp(24px, 5vw, 42px);
    color: var(--gold2);
    text-shadow: 0 0 30px rgba(240,192,64,0.6), 0 2px 0 #7a5000;
    margin-bottom: 8px;
    text-align: center;
  }
  #start-screen p {
    color: var(--text-dim);
    font-size: 14px;
    margin-bottom: 30px;
    text-align: center;
    max-width: 400px;
    line-height: 1.6;
  }
  .player-setup {
    display: flex;
    gap: 30px;
    margin-bottom: 28px;
    flex-wrap: wrap;
    justify-content: center;
  }
  .player-card {
    background: rgba(255,255,255,0.04);
    border: 2px solid var(--stone-dark);
    border-radius: 8px;
    padding: 20px 28px;
    text-align: center;
    min-width: 180px;
  }
  .player-card label {
    display: block;
    font-family: 'Cinzel', serif;
    font-size: 12px;
    letter-spacing: 2px;
    margin-bottom: 10px;
  }
  #p1-card label { color: #6ab4f5; }
  #p2-card label { color: #f56a6a; }
  .player-card input {
    background: rgba(0,0,0,0.4);
    border: 1px solid var(--stone);
    color: var(--text-light);
    font-family: 'Lora', serif;
    font-size: 14px;
    padding: 8px 12px;
    border-radius: 4px;
    width: 100%;
    outline: none;
    text-align: center;
  }
  .player-card input:focus { border-color: var(--gold); }
  #start-btn {
    font-family: 'Cinzel', serif;
    font-size: 16px;
    background: linear-gradient(135deg, var(--gold), #b8860b);
    color: #1a0a00;
    border: none;
    padding: 14px 50px;
    border-radius: 6px;
    cursor: pointer;
    font-weight: 900;
    letter-spacing: 2px;
    box-shadow: 0 0 30px rgba(212,160,23,0.4);
    transition: all 0.2s;
  }
  #start-btn:hover { transform: scale(1.05); box-shadow: 0 0 50px rgba(212,160,23,0.6); }

  /* ── DAMAGE FLOATER ── */
  .floater {
    position: absolute;
    font-family: 'Cinzel', serif;
    font-size: 20px;
    font-weight: 700;
    pointer-events: none;
    z-index: 20;
    animation: floatUp 1.2s forwards;
  }
  @keyframes floatUp {
    0% { opacity: 1; transform: translateY(0) scale(1.2); }
    100% { opacity: 0; transform: translateY(-60px) scale(0.8); }
  }

  /* Catapult animation */
  @keyframes launch {
    0% { transform: rotate(0deg); }
    30% { transform: rotate(-40deg); }
    100% { transform: rotate(0deg); }
  }
  .catapult-arm-animated { animation: launch 0.5s ease-out; }

  #catapult2-inner { transform: scaleX(-1); }
</style>
</head>
<body>

<!-- START SCREEN -->
<div id="start-screen">
  <div style="font-size:60px;margin-bottom:16px">⚔️</div>
  <h1>Mancınık Matematik Savaşı</h1>
  <p>Soruları doğru cevapla, rakip kaleye kaya fırlat!<br>İki oyunculu ortaçağ matematik düellosu.</p>
  <div class="player-setup">
    <div class="player-card" id="p1-card">
      <label>⚔ OYUNCU 1</label>
      <input id="p1-name" type="text" placeholder="Adını yaz..." maxlength="14" value="Şövalye">
    </div>
    <div class="player-card" id="p2-card">
      <label>🛡 OYUNCU 2</label>
      <input id="p2-name" type="text" placeholder="Adını yaz..." maxlength="14" value="Savaşçı">
    </div>
  </div>
  <button id="start-btn" onclick="startGame()">⚔ SAVAŞA BAŞLA ⚔</button>
</div>

<!-- OVERLAY (win/lose) -->
<div id="overlay">
  <div id="overlay-box">
    <div id="overlay-title"></div>
    <div id="overlay-sub"></div>
    <button id="overlay-btn" onclick="restartGame()">🔄 Yeniden Oyna</button>
  </div>
</div>

<!-- STARS -->
<canvas id="stars"></canvas>

<!-- GAME AREA -->
<div id="game-area">
  <!-- HP bars -->
  <div class="hp-bar-wrap" id="hp1-wrap">
    <div class="hp-label" id="hp1-name">Oyuncu 1</div>
    <div class="hp-bar-bg"><div class="hp-bar-fill" id="hp1-bar" style="width:100%"></div></div>
    <div class="hp-text" id="hp1-text">5 / 5 ❤</div>
  </div>
  <div class="hp-bar-wrap" id="hp2-wrap">
    <div class="hp-label" id="hp2-name">Oyuncu 2</div>
    <div class="hp-bar-bg"><div class="hp-bar-fill" id="hp2-bar" style="width:100%"></div></div>
    <div class="hp-text" id="hp2-text">5 / 5 ❤</div>
  </div>

  <div id="moon"></div>
  <div id="turn-indicator">Sıra: Oyuncu 1</div>

  <!-- Castle 1 (blue) -->
  <svg class="castle" id="castle1" viewBox="0 0 90 120" fill="none" xmlns="http://www.w3.org/2000/svg">
    <rect x="5" y="40" width="80" height="80" fill="#3a5a8a"/>
    <rect x="5" y="40" width="80" height="80" fill="url(#c1g)"/>
    <rect x="0" y="25" width="20" height="30" rx="2" fill="#4a6fa5"/>
    <rect x="35" y="20" width="20" height="35" rx="2" fill="#4a6fa5"/>
    <rect x="70" y="25" width="20" height="30" rx="2" fill="#4a6fa5"/>
    <rect x="2" y="22" width="6" height="8" fill="#1a0a2e"/>
    <rect x="10" y="22" width="6" height="8" fill="#1a0a2e"/>
    <rect x="37" y="17" width="6" height="8" fill="#1a0a2e"/>
    <rect x="47" y="17" width="6" height="8" fill="#1a0a2e"/>
    <rect x="72" y="22" width="6" height="8" fill="#1a0a2e"/>
    <rect x="80" y="22" width="6" height="8" fill="#1a0a2e"/>
    <rect x="30" y="75" width="30" height="45" fill="#2a4a7a"/>
    <rect x="38" y="55" width="14" height="14" rx="7" fill="#1a2a4a"/>
    <defs><linearGradient id="c1g" x1="0" y1="0" x2="90" y2="0"><stop offset="0" stop-color="#2a4a7a"/><stop offset="1" stop-color="#4a6fa5"/></linearGradient></defs>
  </svg>

  <!-- Castle 2 (red) -->
  <svg class="castle" id="castle2" viewBox="0 0 90 120" fill="none" xmlns="http://www.w3.org/2000/svg">
    <rect x="5" y="40" width="80" height="80" fill="#8a3a3a"/>
    <rect x="5" y="40" width="80" height="80" fill="url(#c2g)"/>
    <rect x="0" y="25" width="20" height="30" rx="2" fill="#a54a4a"/>
    <rect x="35" y="20" width="20" height="35" rx="2" fill="#a54a4a"/>
    <rect x="70" y="25" width="20" height="30" rx="2" fill="#a54a4a"/>
    <rect x="2" y="22" width="6" height="8" fill="#1a0a2e"/>
    <rect x="10" y="22" width="6" height="8" fill="#1a0a2e"/>
    <rect x="37" y="17" width="6" height="8" fill="#1a0a2e"/>
    <rect x="47" y="17" width="6" height="8" fill="#1a0a2e"/>
    <rect x="72" y="22" width="6" height="8" fill="#1a0a2e"/>
    <rect x="80" y="22" width="6" height="8" fill="#1a0a2e"/>
    <rect x="30" y="75" width="30" height="45" fill="#7a2a2a"/>
    <rect x="38" y="55" width="14" height="14" rx="7" fill="#2a1a1a"/>
    <defs><linearGradient id="c2g" x1="0" y1="0" x2="90" y2="0"><stop offset="0" stop-color="#a54a4a"/><stop offset="1" stop-color="#7a2a2a"/></linearGradient></defs>
  </svg>

  <!-- Catapult 1 -->
  <svg class="catapult" id="catapult1" viewBox="0 0 100 80" xmlns="http://www.w3.org/2000/svg">
    <rect x="10" y="55" width="80" height="10" rx="3" fill="#8b5e3c"/>
    <rect x="15" y="58" width="70" height="7" rx="2" fill="#a0714f"/>
    <circle cx="20" cy="65" r="10" fill="#555" stroke="#333" stroke-width="2"/>
    <circle cx="20" cy="65" r="5" fill="#444"/>
    <circle cx="80" cy="65" r="10" fill="#555" stroke="#333" stroke-width="2"/>
    <circle cx="80" cy="65" r="5" fill="#444"/>
    <rect x="45" y="40" width="8" height="20" rx="2" fill="#7a4f2e"/>
    <line x1="49" y1="42" x2="49" y2="40" stroke="#6a4020" stroke-width="2"/>
    <g id="arm1">
      <rect x="46" y="10" width="6" height="35" rx="3" fill="#a0714f" transform-origin="49 45" transform="rotate(-30,49,45)"/>
      <circle cx="34" cy="15" r="9" fill="radial-gradient(circle,#888,#333)" stroke="#222" stroke-width="2"/>
      <circle cx="34" cy="15" r="9" fill="#666"/>
    </g>
  </svg>

  <!-- Catapult 2 -->
  <svg class="catapult" id="catapult2" viewBox="0 0 100 80" xmlns="http://www.w3.org/2000/svg">
    <rect x="10" y="55" width="80" height="10" rx="3" fill="#8b5e3c"/>
    <rect x="15" y="58" width="70" height="7" rx="2" fill="#a0714f"/>
    <circle cx="20" cy="65" r="10" fill="#555" stroke="#333" stroke-width="2"/>
    <circle cx="20" cy="65" r="5" fill="#444"/>
    <circle cx="80" cy="65" r="10" fill="#555" stroke="#333" stroke-width="2"/>
    <circle cx="80" cy="65" r="5" fill="#444"/>
    <rect x="45" y="40" width="8" height="20" rx="2" fill="#7a4f2e"/>
    <g id="arm2">
      <rect x="46" y="10" width="6" height="35" rx="3" fill="#a0714f" transform-origin="49 45" transform="rotate(-30,49,45)"/>
      <circle cx="34" cy="15" r="9" fill="#666" stroke="#222" stroke-width="2"/>
    </g>
  </svg>

  <!-- Projectile -->
  <div id="projectile"></div>
  <div id="explosion"></div>

  <!-- Ground -->
  <div id="ground"></div>
</div>

<!-- QUIZ PANEL -->
<div id="quiz-panel">
  <div id="q-category">📜 Bölüm</div>
  <div id="q-number">Soru 1 / 20</div>
  <div id="q-type-badge" class="badge-mc">ÇOK SEÇENEKLI</div>
  <div id="q-text">Yükleniyor...</div>
  <div id="options-grid"></div>
  <div id="feedback-msg"></div>
  <button id="next-btn" onclick="nextQuestion()">Sonraki Soru →</button>
</div>

<!-- SCORE BAR -->
<div id="score-bar">
  <div class="score-item" id="s1"><span id="sc1">0</span><span style="font-size:10px;display:block;margin-top:2px">isabetli</span></div>
  <div class="score-item" id="sq"><span id="sqn">1/20</span>SORU</div>
  <div class="score-item" id="s2"><span id="sc2">0</span><span style="font-size:10px;display:block;margin-top:2px">isabetli</span></div>
</div>

<script>
// ────────────────────────────────
// STARS
// ────────────────────────────────
(function(){
  const c = document.getElementById('stars');
  c.width = window.innerWidth; c.height = window.innerHeight * 0.6;
  const ctx = c.getContext('2d');
  for(let i=0;i<180;i++){
    const x=Math.random()*c.width, y=Math.random()*c.height;
    const r=Math.random()*1.5+0.3;
    ctx.beginPath(); ctx.arc(x,y,r,0,Math.PI*2);
    ctx.fillStyle=`rgba(255,255,255,${Math.random()*0.8+0.2})`;
    ctx.fill();
  }
})();

// ────────────────────────────────
// QUESTIONS
// ────────────────────────────────
const questions = [
  // BÖLÜM 1 – Eşitlik ve İşlem Özellikleri
  {
    category: "Bölüm 1 – Eşitlik ve İşlem Özellikleri",
    type: "mc",
    text: "5 + (3 + 7) = (5 + 3) + 7 eşitliği hangi işlem özelliğini göstermektedir?",
    options: ["Değişme özelliği", "Birleşme özelliği", "Dağılma özelliği", "Etkisiz eleman"],
    correct: 1
  },
  {
    category: "Bölüm 1 – Eşitlik ve İşlem Özellikleri",
    type: "tf",
    text: "4 × (6 + 2) = 4×6 + 4×2 ifadesi doğrudur ve dağılma özelliğini kullanır.",
    options: ["✔ Doğru", "✘ Yanlış"],
    correct: 0
  },
  {
    category: "Bölüm 1 – Örüntüler",
    type: "mc",
    text: "3, 7, 11, 15, 19, ... örüntüsünde 6. terim kaçtır?",
    options: ["21", "23", "25", "27"],
    correct: 1
  },
  {
    category: "Bölüm 1 – Örüntüler",
    type: "mc",
    text: "3, 7, 11, 15, 19, ... örüntüsünün genel terim ifadesi nedir?",
    options: ["3n", "4n − 1", "n + 3", "3n + 1"],
    correct: 1
  },
  {
    category: "Bölüm 1 – Önermeler",
    type: "tf",
    text: "\"Ardışık iki tek sayının toplamı her zaman çifttir.\" Bu önerme doğrudur.",
    options: ["✔ Doğru", "✘ Yanlış"],
    correct: 0
  },
  // BÖLÜM 2 – Çarpanlar ve Bölünebilme
  {
    category: "Bölüm 2 – Çarpanlar ve Asal Çarpanlar",
    type: "mc",
    text: "36 sayısının asal çarpanlara ayrımı hangisidir?",
    options: ["2² × 3²", "2³ × 3", "2 × 3³", "4 × 9"],
    correct: 0
  },
  {
    category: "Bölüm 2 – Bölünebilme Kuralları",
    type: "tf",
    text: "180 sayısı 9'a tam bölünür.",
    options: ["✔ Doğru", "✘ Yanlış"],
    correct: 0
  },
  {
    category: "Bölüm 2 – Bölünebilme Kuralları",
    type: "mc",
    text: "252 sayısı aşağıdakilerden hangisine tam BÖLÜNMEZ?",
    options: ["2'ye", "3'e", "5'e", "6'ya"],
    correct: 2
  },
  {
    category: "Bölüm 2 – Bölünebilme Kuralları",
    type: "mc",
    text: "6'ya tam bölünebilmek için hangi iki kural birlikte sağlanmalıdır?",
    options: ["2 ve 3 kuralı", "3 ve 4 kuralı", "2 ve 5 kuralı", "4 ve 6 kuralı"],
    correct: 0
  },
  {
    category: "Bölüm 2 – Bölünebilme Kuralları",
    type: "tf",
    text: "315 sayısı 5'e tam bölünür.",
    options: ["✔ Doğru", "✘ Yanlış"],
    correct: 0
  },
  // BÖLÜM 3 – Cebirsel İfadeler
  {
    category: "Bölüm 3 – Cebirsel İfadeler",
    type: "mc",
    text: "Ahmet 3 kg elma (a TL/kg) ve 2 kg armut (b TL/kg) aldı. Toplam fiyatı ifade eden cebirsel ifade hangisidir?",
    options: ["3a − 2b", "3a + 2b", "5ab", "2a + 3b"],
    correct: 1
  },
  {
    category: "Bölüm 3 – Şekil Örüntüleri",
    type: "mc",
    text: "1, 4, 9, 16, ... şekil örüntüsünde n. adımdaki toplam kare sayısı nedir?",
    options: ["2n", "n²", "n + 3", "3n − 2"],
    correct: 1
  },
  {
    category: "Bölüm 3 – Şekil Örüntüleri",
    type: "tf",
    text: "1, 4, 9, 16, ... örüntüsünde her adımda eklenen kare sayısı tek sayılardır (1, 3, 5, 7, ...).",
    options: ["✔ Doğru", "✘ Yanlış"],
    correct: 0
  },
  // BÖLÜM 4 – Cebirsel İfadelerle İşlemler
  {
    category: "Bölüm 4 – Cebirsel İşlemler",
    type: "mc",
    text: "(3x + 5) + (2x − 1) işleminin sonucu nedir?",
    options: ["5x + 4", "5x + 6", "x + 4", "6x + 4"],
    correct: 0
  },
  {
    category: "Bölüm 4 – Cebirsel İşlemler",
    type: "mc",
    text: "4 · (2x − 3) işleminin sonucu nedir?",
    options: ["6x − 7", "8x − 12", "8x + 12", "2x − 12"],
    correct: 1
  },
  {
    category: "Bölüm 4 – Cebirsel İşlemler",
    type: "tf",
    text: "−(1/2) · (6x + 8) = −3x − 4 sonucunu verir.",
    options: ["✔ Doğru", "✘ Yanlış"],
    correct: 0
  },
  {
    category: "Bölüm 4 – Dikdörtgen Çevresi",
    type: "mc",
    text: "Uzun kenarı (2x + 3) cm, kısa kenarı x cm olan dikdörtgenin çevresi nedir?",
    options: ["3x + 3", "6x + 6", "4x + 6", "5x + 3"],
    correct: 1
  },
  // BÖLÜM 5 – Denklemler ve Eşitsizlikler
  {
    category: "Bölüm 5 – Denklemler",
    type: "mc",
    text: "Bir öğrencinin sınav notu, ödev notunun 3 katıdır. İkisinin toplamı 175'tir. Sınav notu kaçtır?",
    options: ["43,75", "87,5", "131,25", "100"],
    correct: 2
  },
  {
    category: "Bölüm 5 – Eşitsizlikler",
    type: "mc",
    text: "2x + 4 = 10 denkleminde x kaçtır?",
    options: ["2", "3", "4", "5"],
    correct: 1
  },
  {
    category: "Bölüm 5 – Eşitsizlikler",
    type: "mc",
    text: "Kare çerçeve için en fazla 48 cm tel kullanılacaktır. Kenar uzunluğu en fazla kaç cm olabilir?",
    options: ["8 cm", "10 cm", "12 cm", "16 cm"],
    correct: 2
  },
];

// ────────────────────────────────
// STATE
// ────────────────────────────────
let playerNames = ["Oyuncu 1","Oyuncu 2"];
let hp = [5, 5];
let scores = [0, 0];
let currentTurn = 0; // 0 = player1, 1 = player2
let currentQ = 0;
let answered = false;
let shuffled = [];
const MAX_HP = 5;

function shuffle(arr) {
  const a = [...arr];
  for(let i=a.length-1;i>0;i--){const j=Math.floor(Math.random()*(i+1));[a[i],a[j]]=[a[j],a[i]];}
  return a;
}

function startGame() {
  const n1 = document.getElementById('p1-name').value.trim() || "Şövalye";
  const n2 = document.getElementById('p2-name').value.trim() || "Savaşçı";
  playerNames = [n1, n2];
  document.getElementById('start-screen').style.display = 'none';
  shuffled = shuffle(questions);
  currentQ = 0; currentTurn = 0;
  hp = [MAX_HP, MAX_HP]; scores = [0,0];
  updateUI();
  loadQuestion();
}

function updateUI() {
  document.getElementById('hp1-name').textContent = playerNames[0];
  document.getElementById('hp2-name').textContent = playerNames[1];
  document.getElementById('hp1-bar').style.width = (hp[0]/MAX_HP*100)+'%';
  document.getElementById('hp2-bar').style.width = (hp[1]/MAX_HP*100)+'%';
  document.getElementById('hp1-text').textContent = hp[0]+' / '+MAX_HP+' ❤';
  document.getElementById('hp2-text').textContent = hp[1]+' / '+MAX_HP+' ❤';
  document.getElementById('sc1').textContent = scores[0];
  document.getElementById('sc2').textContent = scores[1];
  document.getElementById('turn-indicator').textContent = 'Sıra: ⚔ '+playerNames[currentTurn];
  document.getElementById('s1').querySelector('span').textContent = scores[0];
  document.getElementById('s2').querySelector('span').textContent = scores[1];
}

function loadQuestion() {
  if(currentQ >= shuffled.length) { endGame('draw'); return; }
  const q = shuffled[currentQ];
  answered = false;
  document.getElementById('feedback-msg').textContent = '';
  document.getElementById('feedback-msg').className = '';
  document.getElementById('next-btn').style.display = 'none';
  document.getElementById('q-category').textContent = '📜 ' + q.category;
  document.getElementById('q-number').textContent = 'Soru '+(currentQ+1)+' / '+shuffled.length;
  document.getElementById('sqn').textContent = (currentQ+1)+'/'+shuffled.length;

  const badge = document.getElementById('q-type-badge');
  if(q.type === 'mc') { badge.textContent = '🔵 ÇOK SEÇENEKLİ'; badge.className = 'q-type-badge badge-mc'; }
  else { badge.textContent = '🟢 DOĞRU / YANLIŞ'; badge.className = 'q-type-badge badge-tf'; }

  document.getElementById('q-text').textContent = q.text;

  const grid = document.getElementById('options-grid');
  grid.innerHTML = '';
  if(q.type === 'tf') grid.style.gridTemplateColumns = '1fr 1fr';
  else grid.style.gridTemplateColumns = '1fr 1fr';

  q.options.forEach((opt, i) => {
    const btn = document.createElement('button');
    btn.className = 'opt-btn';
    btn.textContent = (q.type === 'mc' ? String.fromCharCode(65+i)+') ' : '') + opt;
    btn.onclick = () => handleAnswer(i);
    grid.appendChild(btn);
  });
  updateUI();
}

function handleAnswer(chosen) {
  if(answered) return;
  answered = true;
  const q = shuffled[currentQ];
  const btns = document.querySelectorAll('.opt-btn');
  btns.forEach(b => b.disabled = true);
  btns[q.correct].classList.add('correct');

  const fb = document.getElementById('feedback-msg');
  if(chosen === q.correct) {
    btns[chosen].classList.add('correct');
    fb.textContent = '✅ Doğru! Rakip kaleye kaya fırlatıyorsun!';
    fb.className = 'fb-correct';
    scores[currentTurn]++;
    // Current player attacks the opponent
    const target = 1 - currentTurn;
    hp[target] = Math.max(0, hp[target] - 1);
    updateUI();
    animateProjectile(currentTurn, () => {
      if(hp[target] <= 0) { endGame(currentTurn); return; }
      showNextBtn();
    });
  } else {
    btns[chosen].classList.add('wrong');
    fb.textContent = '❌ Yanlış! Rakip sana kaya fırlatıyor!';
    fb.className = 'fb-wrong';
    // Opponent attacks current player
    const attacker = 1 - currentTurn;
    hp[currentTurn] = Math.max(0, hp[currentTurn] - 1);
    updateUI();
    animateProjectile(attacker, () => {
      if(hp[currentTurn] <= 0) { endGame(attacker); return; }
      showNextBtn();
    });
  }
}

function showNextBtn() {
  document.getElementById('next-btn').style.display = 'inline-block';
}

function nextQuestion() {
  currentQ++;
  currentTurn = 1 - currentTurn; // alternate turns
  if(currentQ >= shuffled.length) { endGame('draw'); return; }
  loadQuestion();
}

// ────────────────────────────────
// ANIMATION
// ────────────────────────────────
function animateProjectile(shooter, callback) {
  const gameArea = document.getElementById('game-area');
  const proj = document.getElementById('projectile');
  const rect = gameArea.getBoundingClientRect();

  // shooter 0 = left catapult fires right
  // shooter 1 = right catapult fires left
  let startX, startY, endX, endY;
  const areaH = gameArea.offsetHeight;

  if(shooter === 0) {
    startX = 80; startY = areaH - 120;
    endX = gameArea.offsetWidth - 170; endY = areaH - 100;
  } else {
    startX = gameArea.offsetWidth - 100; startY = areaH - 120;
    endX = 160; endY = areaH - 100;
  }

  proj.style.left = startX+'px';
  proj.style.top = startY+'px';
  proj.style.display = 'block';

  const duration = 900;
  const startTime = performance.now();
  const arcH = 80;

  function frame(now) {
    const t = Math.min(1, (now - startTime) / duration);
    const x = startX + (endX - startX) * t;
    const arc = -arcH * Math.sin(Math.PI * t);
    const y = startY + (endY - startY) * t + arc;
    proj.style.left = x+'px';
    proj.style.top = y+'px';
    if(t < 1) { requestAnimationFrame(frame); }
    else {
      proj.style.display = 'none';
      // Explosion
      const exp = document.getElementById('explosion');
      exp.style.left = (endX - 30)+'px';
      exp.style.top = (endY - 30)+'px';
      exp.style.display = 'block';
      exp.style.background = 'radial-gradient(circle, #ff9900, #ff4400, transparent)';
      exp.style.animation = 'none';
      exp.offsetWidth; // reflow
      exp.style.animation = 'floatUp 0.6s forwards';
      // Damage floater
      const f = document.createElement('div');
      f.className = 'floater';
      f.textContent = '-1 ❤';
      f.style.color = '#ff4444';
      f.style.left = endX+'px';
      f.style.top = (endY-20)+'px';
      gameArea.appendChild(f);
      setTimeout(()=>{ f.remove(); exp.style.display='none'; }, 1200);
      setTimeout(callback, 700);
    }
  }
  requestAnimationFrame(frame);
}

function endGame(winner) {
  const ov = document.getElementById('overlay');
  const title = document.getElementById('overlay-title');
  const sub = document.getElementById('overlay-sub');
  ov.classList.add('active');
  if(winner === 'draw') {
    title.textContent = '⚖ Beraberlik!';
    sub.innerHTML = `Tüm sorular bitti!<br>${playerNames[0]}: ${scores[0]} isabet<br>${playerNames[1]}: ${scores[1]} isabet`;
  } else {
    title.textContent = '🏆 ' + playerNames[winner] + ' Kazandı!';
    sub.innerHTML = `Rakip kale yıkıldı!<br>Doğru cevaplar: ${scores[winner]} / ${shuffled.length/2 | 0}+`;
  }
}

function restartGame() {
  document.getElementById('overlay').classList.remove('active');
  hp = [MAX_HP, MAX_HP]; scores = [0,0];
  currentQ = 0; currentTurn = 0;
  shuffled = shuffle(questions);
  updateUI();
  loadQuestion();
}
</script>
</body>
</html>
