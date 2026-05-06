<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kobe · Crypto Trader & Analyst</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@300;400;600;700&family=IBM+Plex+Mono:wght@300;400;500&family=Noto+Serif+SC:wght@300;400;700&display=swap" rel="stylesheet">
<style>
  :root {
    --gold: #C9A84C;
    --gold-light: #E8C97A;
    --gold-dim: rgba(201,168,76,0.15);
    --bg: #080A0F;
    --bg2: #0D1017;
    --bg3: #111622;
    --text: #E8E2D6;
    --text-muted: #7A7568;
    --green: #00C896;
    --red: #FF4D6A;
    --border: rgba(201,168,76,0.18);
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'IBM Plex Mono', monospace;
    overflow-x: hidden;
    cursor: none;
  }

  /* ── Custom Cursor ── */
  #cursor {
    position: fixed; top: 0; left: 0; z-index: 9999;
    width: 12px; height: 12px;
    background: var(--gold);
    border-radius: 50%;
    pointer-events: none;
    mix-blend-mode: difference;
    transform: translate(-50%,-50%);
    transition: transform 0.1s, width 0.2s, height 0.2s;
  }
  #cursor-ring {
    position: fixed; top: 0; left: 0; z-index: 9998;
    width: 36px; height: 36px;
    border: 1px solid var(--gold);
    border-radius: 50%;
    pointer-events: none;
    transform: translate(-50%,-50%);
    transition: transform 0.25s ease, width 0.3s, height 0.3s, opacity 0.3s;
    opacity: 0.5;
  }

  /* ── Ticker Bar ── */
  .ticker-wrap {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    background: var(--bg2);
    border-bottom: 1px solid var(--border);
    height: 36px;
    overflow: hidden;
  }
  .ticker {
    display: flex; align-items: center;
    height: 100%;
    animation: tickerScroll 30s linear infinite;
    white-space: nowrap;
  }
  .ticker-item {
    display: inline-flex; align-items: center; gap: 8px;
    padding: 0 32px;
    font-size: 11px;
    letter-spacing: 0.08em;
    color: var(--text-muted);
  }
  .ticker-item .sym { color: var(--gold); font-weight: 500; }
  .ticker-item .up { color: var(--green); }
  .ticker-item .dn { color: var(--red); }
  @keyframes tickerScroll {
    0%   { transform: translateX(0); }
    100% { transform: translateX(-50%); }
  }

  /* ── Nav ── */
  nav {
    position: fixed; top: 36px; left: 0; right: 0; z-index: 100;
    display: flex; justify-content: space-between; align-items: center;
    padding: 0 48px;
    height: 64px;
    background: rgba(8,10,15,0.85);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
  }
  .nav-logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 22px; font-weight: 600;
    color: var(--gold);
    letter-spacing: 0.12em;
    text-transform: uppercase;
  }
  .nav-links { display: flex; gap: 36px; }
  .nav-links a {
    font-size: 11px; letter-spacing: 0.15em; text-transform: uppercase;
    color: var(--text-muted);
    text-decoration: none;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--gold); }

  /* ── Hero ── */
  #hero {
    position: relative;
    min-height: 100vh;
    display: flex; align-items: center; justify-content: center;
    padding-top: 100px;
    overflow: hidden;
  }

  canvas#bg-canvas {
    position: absolute; inset: 0;
    width: 100%; height: 100%;
    opacity: 0.6;
  }

  .hero-grid {
    position: absolute; inset: 0;
    background-image:
      linear-gradient(rgba(201,168,76,0.04) 1px, transparent 1px),
      linear-gradient(90deg, rgba(201,168,76,0.04) 1px, transparent 1px);
    background-size: 60px 60px;
    mask-image: radial-gradient(ellipse 80% 70% at 50% 50%, black 40%, transparent 100%);
  }

  .hero-content {
    position: relative; z-index: 2;
    text-align: center;
    max-width: 900px;
    padding: 0 24px;
  }

  .hero-label {
    font-size: 11px; letter-spacing: 0.3em; text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 24px;
    opacity: 0;
    animation: fadeUp 0.8s 0.3s forwards;
  }

  .hero-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(64px, 10vw, 120px);
    font-weight: 300;
    line-height: 0.95;
    letter-spacing: -0.02em;
    color: var(--text);
    opacity: 0;
    animation: fadeUp 0.9s 0.5s forwards;
  }
  .hero-name em {
    font-style: italic;
    color: var(--gold);
  }

  .hero-sub {
    font-family: 'Noto Serif SC', serif;
    font-size: clamp(14px, 2vw, 18px);
    color: var(--text-muted);
    margin-top: 28px;
    letter-spacing: 0.2em;
    opacity: 0;
    animation: fadeUp 0.9s 0.7s forwards;
  }

  .hero-divider {
    width: 1px; height: 60px;
    background: linear-gradient(to bottom, var(--gold), transparent);
    margin: 40px auto;
    opacity: 0;
    animation: fadeUp 0.9s 0.9s forwards;
  }

  .hero-stats {
    display: flex; justify-content: center; gap: 64px;
    opacity: 0;
    animation: fadeUp 0.9s 1.1s forwards;
  }
  .stat { text-align: center; }
  .stat-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 36px; font-weight: 600;
    color: var(--gold);
    display: block;
  }
  .stat-label {
    font-size: 10px; letter-spacing: 0.2em; text-transform: uppercase;
    color: var(--text-muted);
    margin-top: 6px;
  }

  .scroll-hint {
    position: absolute; bottom: 40px; left: 50%;
    transform: translateX(-50%);
    font-size: 10px; letter-spacing: 0.2em; text-transform: uppercase;
    color: var(--text-muted);
    display: flex; flex-direction: column; align-items: center; gap: 12px;
    opacity: 0;
    animation: fadeUp 1s 1.4s forwards;
  }
  .scroll-hint::after {
    content: '';
    width: 1px; height: 48px;
    background: linear-gradient(to bottom, var(--gold), transparent);
    display: block;
    animation: scrollPulse 2s infinite;
  }
  @keyframes scrollPulse {
    0%,100% { opacity: 1; transform: scaleY(1); }
    50% { opacity: 0.4; transform: scaleY(0.7); }
  }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  /* ── Section Base ── */
  section { padding: 120px 0; }

  .container {
    max-width: 1100px;
    margin: 0 auto;
    padding: 0 48px;
  }

  .section-label {
    font-size: 10px; letter-spacing: 0.35em; text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 16px;
    display: flex; align-items: center; gap: 16px;
  }
  .section-label::after {
    content: '';
    flex: 1; height: 1px;
    background: var(--border);
  }

  .section-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(36px, 5vw, 60px);
    font-weight: 300;
    line-height: 1.1;
    color: var(--text);
    margin-bottom: 64px;
  }

  /* ── About ── */
  #about {
    background: var(--bg2);
    border-top: 1px solid var(--border);
    border-bottom: 1px solid var(--border);
  }

  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: start;
  }

  .about-text p {
    font-size: 14px; line-height: 1.9;
    color: var(--text-muted);
    margin-bottom: 20px;
  }
  .about-text p strong { color: var(--text); font-weight: 500; }

  .about-right { display: flex; flex-direction: column; gap: 20px; }

  .about-card {
    background: var(--bg3);
    border: 1px solid var(--border);
    border-radius: 2px;
    padding: 24px 28px;
    position: relative;
    overflow: hidden;
    transition: border-color 0.3s;
  }
  .about-card::before {
    content: '';
    position: absolute; left: 0; top: 0; bottom: 0;
    width: 3px;
    background: var(--gold);
  }
  .about-card:hover { border-color: var(--gold); }
  .about-card-title {
    font-size: 11px; letter-spacing: 0.2em; text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 8px;
  }
  .about-card-val {
    font-family: 'Cormorant Garamond', serif;
    font-size: 22px; color: var(--text);
  }

  /* ── Strategy ── */
  #strategy { background: var(--bg); }

  .strategy-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2px;
  }

  .strat-card {
    background: var(--bg2);
    border: 1px solid var(--border);
    padding: 40px 32px;
    position: relative;
    overflow: hidden;
    transition: background 0.3s, transform 0.3s;
  }
  .strat-card:hover {
    background: var(--bg3);
    transform: translateY(-4px);
  }
  .strat-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 72px; font-weight: 700;
    color: var(--gold-dim);
    line-height: 1;
    position: absolute; top: 12px; right: 16px;
    pointer-events: none;
    transition: color 0.3s;
  }
  .strat-card:hover .strat-num { color: rgba(201,168,76,0.25); }
  .strat-icon { font-size: 28px; margin-bottom: 20px; }
  .strat-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: 22px; font-weight: 600;
    color: var(--text);
    margin-bottom: 12px;
  }
  .strat-desc {
    font-size: 12px; line-height: 1.8;
    color: var(--text-muted);
  }
  .strat-tag {
    display: inline-block;
    margin-top: 20px;
    padding: 4px 12px;
    border: 1px solid var(--border);
    font-size: 10px; letter-spacing: 0.15em;
    color: var(--gold);
    text-transform: uppercase;
  }

  /* ── Live Chart Section ── */
  #market {
    background: var(--bg2);
    border-top: 1px solid var(--border);
    border-bottom: 1px solid var(--border);
  }

  .chart-container {
    background: var(--bg3);
    border: 1px solid var(--border);
    border-radius: 2px;
    padding: 32px;
  }
  .chart-header {
    display: flex; justify-content: space-between; align-items: center;
    margin-bottom: 24px;
  }
  .chart-sym { font-size: 13px; letter-spacing: 0.1em; color: var(--gold); }
  .chart-price {
    font-family: 'Cormorant Garamond', serif;
    font-size: 32px; color: var(--green);
  }
  canvas#price-chart { width: 100%; height: 160px; display: block; }

  .market-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 16px;
    margin-top: 32px;
  }
  .mkt-card {
    background: var(--bg3);
    border: 1px solid var(--border);
    padding: 20px;
    transition: border-color 0.3s;
  }
  .mkt-card:hover { border-color: var(--gold); }
  .mkt-sym { font-size: 12px; letter-spacing: 0.1em; color: var(--gold); margin-bottom: 8px; }
  .mkt-price {
    font-family: 'Cormorant Garamond', serif;
    font-size: 22px; color: var(--text);
    margin-bottom: 4px;
  }
  .mkt-chg { font-size: 12px; }
  .mkt-chg.up { color: var(--green); }
  .mkt-chg.dn { color: var(--red); }

  /* ── Links / Connect ── */
  #connect { background: var(--bg); }

  .links-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 16px;
    max-width: 700px;
  }

  .link-card {
    display: flex; align-items: center; gap: 20px;
    background: var(--bg2);
    border: 1px solid var(--border);
    padding: 24px 28px;
    text-decoration: none;
    color: var(--text);
    transition: border-color 0.3s, transform 0.2s;
    position: relative;
    overflow: hidden;
  }
  .link-card::after {
    content: '→';
    position: absolute; right: 24px;
    font-size: 18px; color: var(--gold);
    opacity: 0;
    transform: translateX(-8px);
    transition: opacity 0.2s, transform 0.2s;
  }
  .link-card:hover {
    border-color: var(--gold);
    transform: translateX(4px);
  }
  .link-card:hover::after { opacity: 1; transform: translateX(0); }
  .link-icon { font-size: 28px; }
  .link-name { font-size: 13px; font-weight: 500; color: var(--text); letter-spacing: 0.05em; }
  .link-desc { font-size: 11px; color: var(--text-muted); margin-top: 3px; }

  /* ── Footer ── */
  footer {
    border-top: 1px solid var(--border);
    padding: 40px 48px;
    display: flex; justify-content: space-between; align-items: center;
    background: var(--bg2);
  }
  .footer-left {
    font-family: 'Cormorant Garamond', serif;
    font-size: 18px; color: var(--gold);
    letter-spacing: 0.1em;
  }
  .footer-right { font-size: 11px; color: var(--text-muted); letter-spacing: 0.1em; }

  /* ── Glow effect ── */
  .glow {
    position: absolute;
    border-radius: 50%;
    filter: blur(80px);
    pointer-events: none;
  }
  .glow-gold {
    width: 500px; height: 500px;
    background: radial-gradient(circle, rgba(201,168,76,0.08) 0%, transparent 70%);
    top: 20%; left: -100px;
  }
  .glow-green {
    width: 400px; height: 400px;
    background: radial-gradient(circle, rgba(0,200,150,0.06) 0%, transparent 70%);
    bottom: 10%; right: -80px;
  }

  /* responsive */
  @media (max-width: 768px) {
    nav { padding: 0 20px; }
    .nav-links { gap: 20px; }
    .container { padding: 0 20px; }
    .about-grid { grid-template-columns: 1fr; gap: 40px; }
    .strategy-grid { grid-template-columns: 1fr; }
    .market-grid { grid-template-columns: repeat(2, 1fr); }
    .links-grid { grid-template-columns: 1fr; }
    footer { flex-direction: column; gap: 16px; text-align: center; }
  }
</style>
</head>
<body>

<div id="cursor"></div>
<div id="cursor-ring"></div>

<!-- Ticker -->
<div class="ticker-wrap">
  <div class="ticker" id="ticker">
    <span class="ticker-item"><span class="sym">BTC/USDT</span> <span class="up" id="btc-p">103,842</span> <span class="up">▲ 2.41%</span></span>
    <span class="ticker-item"><span class="sym">ETH/USDT</span> <span class="up" id="eth-p">2,618</span> <span class="up">▲ 3.87%</span></span>
    <span class="ticker-item"><span class="sym">SOL/USDT</span> <span class="dn">151.40</span> <span class="dn">▼ 0.93%</span></span>
    <span class="ticker-item"><span class="sym">BNB/USDT</span> <span class="up">614.20</span> <span class="up">▲ 1.20%</span></span>
    <span class="ticker-item"><span class="sym">HYPE/USDT</span> <span class="up">28.45</span> <span class="up">▲ 5.64%</span></span>
    <span class="ticker-item"><span class="sym">SUI/USDT</span> <span class="up">3.812</span> <span class="up">▲ 7.14%</span></span>
    <span class="ticker-item"><span class="sym">DOGE/USDT</span> <span class="dn">0.1923</span> <span class="dn">▼ 1.38%</span></span>
    <!-- repeat for seamless loop -->
    <span class="ticker-item"><span class="sym">BTC/USDT</span> <span class="up">103,842</span> <span class="up">▲ 2.41%</span></span>
    <span class="ticker-item"><span class="sym">ETH/USDT</span> <span class="up">2,618</span> <span class="up">▲ 3.87%</span></span>
    <span class="ticker-item"><span class="sym">SOL/USDT</span> <span class="dn">151.40</span> <span class="dn">▼ 0.93%</span></span>
    <span class="ticker-item"><span class="sym">BNB/USDT</span> <span class="up">614.20</span> <span class="up">▲ 1.20%</span></span>
    <span class="ticker-item"><span class="sym">HYPE/USDT</span> <span class="up">28.45</span> <span class="up">▲ 5.64%</span></span>
    <span class="ticker-item"><span class="sym">SUI/USDT</span> <span class="up">3.812</span> <span class="up">▲ 7.14%</span></span>
    <span class="ticker-item"><span class="sym">DOGE/USDT</span> <span class="dn">0.1923</span> <span class="dn">▼ 1.38%</span></span>
  </div>
</div>

<!-- Nav -->
<nav>
  <div class="nav-logo">Kobe</div>
  <div class="nav-links">
    <a href="#about">About</a>
    <a href="#strategy">Strategy</a>
    <a href="#market">Market</a>
    <a href="#connect">Connect</a>
  </div>
</nav>

<!-- Hero -->
<section id="hero">
  <canvas id="bg-canvas"></canvas>
  <div class="hero-grid"></div>
  <div class="glow glow-gold"></div>
  <div class="glow glow-green"></div>

  <div class="hero-content">
    <div class="hero-label">Crypto Trader · Analyst · Content Creator</div>
    <h1 class="hero-name">
      Trade<br>with <em>Precision</em>
    </h1>
    <p class="hero-sub">加密货币研究者 · 量化策略探索者</p>
    <div class="hero-divider"></div>
    <div class="hero-stats">
      <div class="stat">
        <span class="stat-num">3+</span>
        <span class="stat-label">Years Trading</span>
      </div>
      <div class="stat">
        <span class="stat-num">50+</span>
        <span class="stat-label">Pairs Tracked</span>
      </div>
      <div class="stat">
        <span class="stat-num">24/7</span>
        <span class="stat-label">Bot Monitoring</span>
      </div>
    </div>
  </div>

  <div class="scroll-hint">scroll</div>
</section>

<!-- About -->
<section id="about">
  <div class="container">
    <div class="section-label">01 · About</div>
    <h2 class="section-title">Who I Am</h2>
    <div class="about-grid">
      <div class="about-text">
        <p>I'm <strong>Kobe</strong> — a cryptocurrency trader, market analyst, and automation builder with a sharp focus on quantitative signals and smart market structure.</p>
        <p>My edge lies in combining <strong>institutional-grade analysis</strong> — Smart Money Concepts, time-series momentum, and liquidity mechanics — with custom algorithmic tools built in Python.</p>
        <p>I run <strong>加密币Bot</strong>, an automated Telegram reporting system that delivers daily market insights, top gainer scans, and signal alerts. I also curate crypto content on Binance Square for traders who want signal over noise.</p>
        <p>Markets don't sleep. Neither does my bot.</p>
      </div>
      <div class="about-right">
        <div class="about-card">
          <div class="about-card-title">Telegram Bot</div>
          <div class="about-card-val">加密币Bot</div>
        </div>
        <div class="about-card">
          <div class="about-card-title">Content Platform</div>
          <div class="about-card-val">Binance Square</div>
        </div>
        <div class="about-card">
          <div class="about-card-title">Primary Markets</div>
          <div class="about-card-val">BTC · ETH · Altcoins</div>
        </div>
        <div class="about-card">
          <div class="about-card-title">Tech Stack</div>
          <div class="about-card-val">Python · ccxt · Bybit API</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Strategy -->
<section id="strategy">
  <div class="container">
    <div class="section-label">02 · Strategy</div>
    <h2 class="section-title">How I Trade</h2>
    <div class="strategy-grid">
      <div class="strat-card">
        <div class="strat-num">01</div>
        <div class="strat-icon">📈</div>
        <div class="strat-title">Time-Series Momentum</div>
        <div class="strat-desc">TSMOM signals identify sustained directional trends across multiple timeframes, filtering noise from real momentum shifts in price action.</div>
        <div class="strat-tag">TSMOM</div>
      </div>
      <div class="strat-card">
        <div class="strat-num">02</div>
        <div class="strat-icon">🎯</div>
        <div class="strat-title">RSI + ADX Confluence</div>
        <div class="strat-desc">Combining relative strength with trend strength indicators to only enter when both momentum and trend direction confirm the same thesis.</div>
        <div class="strat-tag">RSI · ADX</div>
      </div>
      <div class="strat-card">
        <div class="strat-num">03</div>
        <div class="strat-icon">⚖️</div>
        <div class="strat-title">Volatility-Scaled Sizing</div>
        <div class="strat-desc">Position sizes adjust dynamically to current market volatility — larger when conditions are calm, reduced during turbulent regimes.</div>
        <div class="strat-tag">Risk Management</div>
      </div>
      <div class="strat-card">
        <div class="strat-num">04</div>
        <div class="strat-icon">💧</div>
        <div class="strat-title">Liquidity Engineering</div>
        <div class="strat-desc">Mapping institutional liquidity pools, stop-loss clusters, and order block zones using SMC / ICT framework mechanics.</div>
        <div class="strat-tag">SMC · ICT</div>
      </div>
      <div class="strat-card">
        <div class="strat-num">05</div>
        <div class="strat-icon">🤖</div>
        <div class="strat-title">Automated Scanning</div>
        <div class="strat-desc">Custom Python bot scans for the top-5 altcoin gainers daily, generating Telegram alerts with key metrics and entry zones.</div>
        <div class="strat-tag">Automation</div>
      </div>
      <div class="strat-card">
        <div class="strat-num">06</div>
        <div class="strat-icon">🔄</div>
        <div class="strat-title">Delta-Neutral Arb</div>
        <div class="strat-desc">Spot-to-futures arbitrage using precisely defined principal allocations, hedge ratios, and multi-exchange execution to capture funding rate spreads.</div>
        <div class="strat-tag">Arbitrage</div>
      </div>
    </div>
  </div>
</section>

<!-- Market -->
<section id="market">
  <div class="container">
    <div class="section-label">03 · Market</div>
    <h2 class="section-title">Live Pulse</h2>

    <div class="chart-container">
      <div class="chart-header">
        <div class="chart-sym">BTC/USDT · 1H</div>
        <div class="chart-price" id="live-price">$103,842</div>
      </div>
      <canvas id="price-chart" height="160"></canvas>
    </div>

    <div class="market-grid">
      <div class="mkt-card">
        <div class="mkt-sym">BTC/USDT</div>
        <div class="mkt-price">$103,842</div>
        <div class="mkt-chg up">▲ 2.41%</div>
      </div>
      <div class="mkt-card">
        <div class="mkt-sym">ETH/USDT</div>
        <div class="mkt-price">$2,618</div>
        <div class="mkt-chg up">▲ 3.87%</div>
      </div>
      <div class="mkt-card">
        <div class="mkt-sym">SOL/USDT</div>
        <div class="mkt-price">$151.40</div>
        <div class="mkt-chg dn">▼ 0.93%</div>
      </div>
      <div class="mkt-card">
        <div class="mkt-sym">HYPE/USDT</div>
        <div class="mkt-price">$28.45</div>
        <div class="mkt-chg up">▲ 5.64%</div>
      </div>
    </div>
  </div>
</section>

<!-- Connect -->
<section id="connect">
  <div class="container">
    <div class="section-label">04 · Connect</div>
    <h2 class="section-title">Find Me</h2>
    <div class="links-grid">
      <a class="link-card" href="https://t.me/jiamibBot" target="_blank">
        <div class="link-icon">✈️</div>
        <div>
          <div class="link-name">加密币Bot · Telegram</div>
          <div class="link-desc">Daily signals, top gainers, market alerts</div>
        </div>
      </a>
      <a class="link-card" href="https://www.binance.com/en/square" target="_blank">
        <div class="link-icon">🟡</div>
        <div>
          <div class="link-name">Binance Square</div>
          <div class="link-desc">Crypto content, analysis & commentary</div>
        </div>
      </a>
      <a class="link-card" href="https://github.com/kobe836" target="_blank">
        <div class="link-icon">⚙️</div>
        <div>
          <div class="link-name">GitHub · kobe836</div>
          <div class="link-desc">Trading bots & open-source projects</div>
        </div>
      </a>
      <a class="link-card" href="mailto:hello@kobe836.github.io">
        <div class="link-icon">📩</div>
        <div>
          <div class="link-name">Email</div>
          <div class="link-desc">Collaboration & inquiries</div>
        </div>
      </a>
    </div>
  </div>
</section>

<footer>
  <div class="footer-left">Kobe · 加密币</div>
  <div class="footer-right">© 2026 · Trade Smart. Stay Sharp.</div>
</footer>

<script>
/* ── Cursor ── */
const cur = document.getElementById('cursor');
const ring = document.getElementById('cursor-ring');
let rx = 0, ry = 0, mx = 0, my = 0;
document.addEventListener('mousemove', e => { mx = e.clientX; my = e.clientY; cur.style.left = mx+'px'; cur.style.top = my+'px'; });
(function animateRing(){
  rx += (mx-rx)*0.12; ry += (my-ry)*0.12;
  ring.style.left = rx+'px'; ring.style.top = ry+'px';
  requestAnimationFrame(animateRing);
})();
document.querySelectorAll('a,.strat-card,.about-card,.mkt-card').forEach(el => {
  el.addEventListener('mouseenter', ()=>{ cur.style.width='20px'; cur.style.height='20px'; ring.style.width='56px'; ring.style.height='56px'; });
  el.addEventListener('mouseleave', ()=>{ cur.style.width='12px'; cur.style.height='12px'; ring.style.width='36px'; ring.style.height='36px'; });
});

/* ── Background canvas: animated candlestick-like lines ── */
const bgc = document.getElementById('bg-canvas');
const bgx = bgc.getContext('2d');
function resizeBg(){ bgc.width=window.innerWidth; bgc.height=window.innerHeight; }
resizeBg(); window.addEventListener('resize', resizeBg);

const lines = Array.from({length:18}, (_,i)=>({
  x: Math.random()*window.innerWidth,
  y: Math.random()*window.innerHeight,
  speed: 0.15+Math.random()*0.25,
  len: 60+Math.random()*120,
  dir: Math.random()>0.5?1:-1,
  alpha: 0.08+Math.random()*0.12,
  color: Math.random()>0.4?'201,168,76':'0,200,150'
}));

function drawBg(){
  bgx.clearRect(0,0,bgc.width,bgc.height);
  lines.forEach(l=>{
    l.y += l.speed*l.dir;
    if(l.y<-200||l.y>bgc.height+200){ l.y=l.dir>0?-50:bgc.height+50; l.x=Math.random()*bgc.width; }
    bgx.beginPath();
    bgx.moveTo(l.x, l.y);
    bgx.lineTo(l.x, l.y + l.len*l.dir);
    bgx.strokeStyle=`rgba(${l.color},${l.alpha})`;
    bgx.lineWidth=1;
    bgx.stroke();
    // candle body
    const bh = l.len*0.4;
    bgx.fillStyle=`rgba(${l.color},${l.alpha*0.6})`;
    bgx.fillRect(l.x-3, l.y+l.len*0.3*l.dir, 6, bh*l.dir);
  });
  requestAnimationFrame(drawBg);
}
drawBg();

/* ── Price chart ── */
const pc = document.getElementById('price-chart');
const px = pc.getContext('2d');
pc.width = pc.offsetWidth * window.devicePixelRatio;
pc.height = 160 * window.devicePixelRatio;
px.scale(window.devicePixelRatio, window.devicePixelRatio);
const W = pc.offsetWidth, H = 160;

// Generate fake price data
let priceData = [];
let p = 103000;
for(let i=0;i<80;i++){
  p += (Math.random()-0.48)*400;
  priceData.push(p);
}

function drawChart(){
  px.clearRect(0,0,W,H);
  const min = Math.min(...priceData)-500;
  const max = Math.max(...priceData)+500;
  const range = max-min;
  const pts = priceData.map((v,i)=>({ x: (i/(priceData.length-1))*W, y: H-(((v-min)/range)*(H-20)+10) }));

  // Gradient fill
  const grad = px.createLinearGradient(0,0,0,H);
  grad.addColorStop(0,'rgba(0,200,150,0.25)');
  grad.addColorStop(1,'rgba(0,200,150,0)');
  px.beginPath();
  pts.forEach((pt,i)=> i===0 ? px.moveTo(pt.x,pt.y) : px.lineTo(pt.x,pt.y));
  px.lineTo(W,H); px.lineTo(0,H); px.closePath();
  px.fillStyle=grad; px.fill();

  // Line
  px.beginPath();
  pts.forEach((pt,i)=> i===0 ? px.moveTo(pt.x,pt.y) : px.lineTo(pt.x,pt.y));
  px.strokeStyle='rgba(0,200,150,0.9)'; px.lineWidth=2; px.stroke();

  // Current price dot
  const last = pts[pts.length-1];
  px.beginPath();
  px.arc(last.x,last.y,4,0,Math.PI*2);
  px.fillStyle='#00C896'; px.fill();

  // Grid lines
  for(let i=1;i<4;i++){
    const y = (H/4)*i;
    px.beginPath(); px.moveTo(0,y); px.lineTo(W,y);
    px.strokeStyle='rgba(201,168,76,0.06)'; px.lineWidth=1; px.stroke();
  }
}
drawChart();

// Animate price
setInterval(()=>{
  p += (Math.random()-0.48)*300;
  priceData.push(p); priceData.shift();
  document.getElementById('live-price').textContent = '$'+Math.round(p).toLocaleString();
  drawChart();
}, 1500);

/* ── Scroll reveal ── */
const observer = new IntersectionObserver((entries)=>{
  entries.forEach(e=>{
    if(e.isIntersecting){ e.target.style.opacity='1'; e.target.style.transform='translateY(0)'; }
  });
},{threshold:0.1});
document.querySelectorAll('.strat-card,.about-card,.mkt-card,.link-card').forEach(el=>{
  el.style.opacity='0'; el.style.transform='translateY(20px)';
  el.style.transition='opacity 0.6s ease, transform 0.6s ease, border-color 0.3s';
  observer.observe(el);
});
</script>
</body>
</html>
