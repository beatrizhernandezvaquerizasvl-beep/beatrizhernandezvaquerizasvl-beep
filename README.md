<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0">
  <title>Beatriz Hernández Vaquerizas | Financial Economics & Quantitative Analytics</title>

  <!-- Google Fonts: Editorial Intaglio, Serif Display & Monospace Telemetry -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@600;700;800&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500;700&family=Playfair+Display:ital,wght@0,600;0,700;1,400;1,600&display=swap" rel="stylesheet">

  <style>
    /* ==========================================================================
       VINTAGE WALL STREET & FINANCIAL ANALYTICS HERO BANNER
       ========================================================================== */
    :root {
      --bg-parchment: #EFECE6;
      --bg-parchment-deep: #E5DFD4;
      --bg-card: rgba(247, 244, 238, 0.92);
      --paper-ivory: #F9F7F2;
      
      --ink-charcoal: #262624;
      --ink-muted: #5C5A55;
      --ink-green: #4A5B4E;
      --ink-green-dark: #354338;
      --ink-wine: #8A4843;
      --ink-wine-dark: #67312D;
      --ink-slate: #475560;
      --ink-gold: #BFA878;
      --border-line: #D8D2C4;

      --font-serif-display: 'Cinzel', 'Playfair Display', Georgia, serif;
      --font-serif-text: 'Playfair Display', 'Baskerville', serif;
      --font-sans: 'Inter', -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
      --font-mono: 'JetBrains Mono', 'Courier Prime', monospace;

      --shadow-elevation: 0 18px 45px -12px rgba(45, 40, 30, 0.16);
    }

    *, *::before, *::after {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html, body {
      width: 100%;
      min-height: 100%;
      background-color: var(--bg-parchment);
      color: var(--ink-charcoal);
      font-family: var(--font-sans);
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
      overflow-x: hidden;
    }

    /* Cotton Security Paper Grain Simulation */
    .parchment-grain-overlay {
      position: fixed;
      inset: 0;
      pointer-events: none;
      z-index: 10;
      opacity: 0.045;
      background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noiseFilter'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noiseFilter)'/%3E%3C/svg%3E");
      background-repeat: repeat;
    }

    .parchment-vignette {
      position: fixed;
      inset: 0;
      pointer-events: none;
      z-index: 9;
      background: radial-gradient(circle at 50% 40%, transparent 45%, rgba(45, 38, 28, 0.08) 100%);
    }

    /* Top Market Ticker Tape */
    .top-ticker-bar {
      position: relative;
      z-index: 20;
      background: #20201E;
      color: #DDD8CD;
      font-family: var(--font-mono);
      font-size: 11px;
      letter-spacing: 0.8px;
      overflow: hidden;
      white-space: nowrap;
      border-bottom: 1px solid #333330;
      height: 30px;
      display: flex;
      align-items: center;
    }

    .ticker-track {
      display: inline-flex;
      gap: 32px;
      animation: tickerScroll 48s linear infinite;
      padding-left: 100%;
    }

    .ticker-track:hover { animation-play-state: paused; }

    .ticker-item {
      display: inline-flex;
      align-items: center;
      gap: 8px;
    }

    .ticker-symbol {
      font-weight: 700;
      color: var(--ink-gold);
    }

    .ticker-val-up { color: #7DB88B; }
    .ticker-val-down { color: #D9827B; }

    @keyframes tickerScroll {
      0% { transform: translate3d(0, 0, 0); }
      100% { transform: translate3d(-100%, 0, 0); }
    }

    /* Header Navbar */
    .site-header {
      position: relative;
      z-index: 20;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 18px 48px;
      border-bottom: 1px solid var(--border-line);
      background: rgba(239, 236, 230, 0.85);
      backdrop-filter: blur(10px);
    }

    .header-brand {
      display: flex;
      align-items: center;
      gap: 14px;
    }

    .brand-monogram {
      width: 38px;
      height: 38px;
      border: 1px solid var(--ink-green);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: var(--font-serif-display);
      font-weight: 700;
      font-size: 14px;
      color: var(--ink-green);
      background: var(--paper-ivory);
      box-shadow: 0 2px 6px rgba(0,0,0,0.04);
    }

    .brand-text h1 {
      font-family: var(--font-serif-display);
      font-size: 13.5px;
      letter-spacing: 2px;
      text-transform: uppercase;
      color: var(--ink-charcoal);
      font-weight: 700;
    }

    .brand-text p {
      font-size: 10.5px;
      color: var(--ink-muted);
      letter-spacing: 0.5px;
      text-transform: uppercase;
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 28px;
      list-style: none;
    }

    .nav-links a {
      text-decoration: none;
      font-family: var(--font-mono);
      font-size: 11.5px;
      letter-spacing: 1px;
      text-transform: uppercase;
      color: var(--ink-charcoal);
      transition: color 0.2s ease;
      position: relative;
    }

    .nav-links a::after {
      content: '';
      position: absolute;
      left: 0;
      bottom: -3px;
      width: 0%;
      height: 1px;
      background: var(--ink-wine);
      transition: width 0.25s ease;
    }

    .nav-links a:hover { color: var(--ink-wine); }
    .nav-links a:hover::after { width: 100%; }

    /* Hero Container & Canvas */
    .hero-stage {
      position: relative;
      width: 100%;
      height: calc(100vh - 78px);
      min-height: 640px;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
      background-color: var(--bg-parchment);
    }

    #antiGravityCanvas {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 2;
      cursor: default;
      display: block;
    }

    .hero-content {
      position: relative;
      z-index: 5;
      max-width: 960px;
      padding: 30px 24px;
      text-align: center;
      pointer-events: none;
    }

    .hero-interactive { pointer-events: auto; }

    .hero-pill-badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 6px 16px;
      background: rgba(249, 247, 242, 0.92);
      border: 1px solid var(--border-line);
      border-radius: 999px;
      font-family: var(--font-mono);
      font-size: 11px;
      color: var(--ink-green);
      letter-spacing: 1.5px;
      text-transform: uppercase;
      margin-bottom: 22px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.03);
      backdrop-filter: blur(6px);
    }

    .pill-dot {
      width: 6px;
      height: 6px;
      background-color: var(--ink-wine);
      border-radius: 50%;
      box-shadow: 0 0 8px rgba(138, 72, 67, 0.6);
      animation: pulseDot 2s infinite ease-in-out;
    }

    @keyframes pulseDot {
      0%, 100% { opacity: 1; transform: scale(1); }
      50% { opacity: 0.4; transform: scale(0.85); }
    }

    .hero-headline {
      font-family: var(--font-serif-display);
      font-size: clamp(2.2rem, 5.2vw, 4.2rem);
      font-weight: 700;
      line-height: 1.14;
      color: var(--ink-charcoal);
      letter-spacing: -0.5px;
      margin-bottom: 18px;
      text-wrap: balance;
    }

    .hero-headline em {
      font-family: var(--font-serif-text);
      font-style: italic;
      font-weight: 400;
      color: var(--ink-green);
    }

    .hero-subhead {
      font-size: clamp(1rem, 1.7vw, 1.2rem);
      line-height: 1.6;
      color: var(--ink-muted);
      max-width: 680px;
      margin: 0 auto 30px auto;
      font-weight: 400;
    }

    .hero-tags {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 10px;
      margin-bottom: 34px;
    }

    .tag-badge {
      font-family: var(--font-mono);
      font-size: 11px;
      padding: 5px 12px;
      background: rgba(240, 237, 230, 0.85);
      border: 1px dashed var(--border-line);
      color: var(--ink-slate);
      letter-spacing: 0.5px;
      border-radius: 4px;
    }

    .hero-actions {
      display: inline-flex;
      gap: 16px;
      flex-wrap: wrap;
      justify-content: center;
    }

    .btn-primary {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      padding: 13px 26px;
      background: var(--ink-green);
      color: var(--paper-ivory);
      text-decoration: none;
      font-family: var(--font-serif-display);
      font-size: 12.5px;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      font-weight: 600;
      border: 1px solid var(--ink-green-dark);
      box-shadow: 0 4px 14px rgba(74, 91, 78, 0.28), inset 0 1px 0 rgba(255,255,255,0.2);
      transition: all 0.25s ease;
      cursor: pointer;
    }

    .btn-primary:hover {
      background: var(--ink-green-dark);
      transform: translateY(-2px);
      box-shadow: 0 8px 20px rgba(74, 91, 78, 0.35);
    }

    .btn-secondary {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      padding: 13px 24px;
      background: var(--paper-ivory);
      color: var(--ink-charcoal);
      text-decoration: none;
      font-family: var(--font-serif-display);
      font-size: 12.5px;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      font-weight: 600;
      border: 1px solid var(--border-line);
      box-shadow: 0 4px 12px rgba(0,0,0,0.04);
      transition: all 0.25s ease;
      cursor: pointer;
    }

    .btn-secondary:hover {
      border-color: var(--ink-wine);
      color: var(--ink-wine);
      transform: translateY(-2px);
    }

    .hero-floating-tip {
      margin-top: 28px;
      font-family: var(--font-mono);
      font-size: 11px;
      color: var(--ink-muted);
      display: inline-flex;
      align-items: center;
      gap: 8px;
      letter-spacing: 0.5px;
      background: rgba(245, 242, 235, 0.75);
      padding: 4px 14px;
      border-radius: 999px;
      border: 1px solid var(--border-line);
    }

    /* HUD Controls */
    .physics-hud {
      position: fixed;
      bottom: 24px;
      right: 24px;
      z-index: 30;
      background: var(--bg-card);
      border: 1px solid var(--border-line);
      padding: 16px 20px;
      border-radius: 8px;
      box-shadow: var(--shadow-elevation);
      backdrop-filter: blur(12px);
      width: 290px;
      transition: transform 0.3s cubic-bezier(0.16, 1, 0.3, 1), opacity 0.3s ease;
    }

    .physics-hud.collapsed {
      transform: translateY(calc(100% - 46px));
    }

    .hud-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 14px;
      cursor: pointer;
    }

    .hud-title {
      display: flex;
      align-items: center;
      gap: 8px;
      font-family: var(--font-serif-display);
      font-size: 12px;
      font-weight: 700;
      letter-spacing: 1.2px;
      text-transform: uppercase;
      color: var(--ink-charcoal);
    }

    .hud-indicator {
      width: 8px;
      height: 8px;
      border-radius: 50%;
      background: var(--ink-green);
    }

    .hud-toggle-btn {
      background: none;
      border: none;
      font-size: 16px;
      color: var(--ink-muted);
      cursor: pointer;
      line-height: 1;
    }

    .hud-body {
      display: flex;
      flex-direction: column;
      gap: 12px;
    }

    .hud-control-group {
      display: flex;
      flex-direction: column;
      gap: 4px;
    }

    .hud-label-row {
      display: flex;
      justify-content: space-between;
      font-family: var(--font-mono);
      font-size: 10.5px;
      color: var(--ink-muted);
      text-transform: uppercase;
    }

    .hud-slider {
      appearance: none;
      -webkit-appearance: none;
      width: 100%;
      height: 4px;
      background: #DDD7C9;
      border-radius: 2px;
      outline: none;
    }

    .hud-slider::-webkit-slider-thumb {
      -webkit-appearance: none;
      appearance: none;
      width: 14px;
      height: 14px;
      border-radius: 50%;
      background: var(--ink-green);
      border: 2px solid var(--paper-ivory);
      cursor: pointer;
      box-shadow: 0 1px 3px rgba(0,0,0,0.3);
    }

    .hud-slider::-moz-range-thumb {
      width: 14px;
      height: 14px;
      border-radius: 50%;
      background: var(--ink-green);
      border: 2px solid var(--paper-ivory);
      cursor: pointer;
    }

    .hud-btn-row {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 8px;
      margin-top: 6px;
    }

    .hud-action-btn {
      padding: 8px 10px;
      background: var(--paper-ivory);
      border: 1px solid var(--border-line);
      color: var(--ink-charcoal);
      font-family: var(--font-mono);
      font-size: 10px;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      cursor: pointer;
      border-radius: 4px;
      transition: all 0.2s ease;
    }

    .hud-action-btn:hover {
      background: var(--ink-green);
      color: var(--paper-ivory);
      border-color: var(--ink-green);
    }

    .hud-action-btn.btn-burst {
      grid-column: span 2;
      background: #F4EFE7;
      border-color: var(--ink-wine);
      color: var(--ink-wine-dark);
      font-weight: 700;
    }

    .hud-action-btn.btn-burst:hover {
      background: var(--ink-wine);
      color: var(--paper-ivory);
    }

    @media (max-width: 768px) {
      .site-header { padding: 14px 20px; }
      .nav-links { display: none; }
      .hero-content { padding: 24px 16px; }
      .physics-hud {
        right: 14px;
        bottom: 14px;
        width: calc(100% - 28px);
        max-width: 320px;
      }
    }
  </style>
</head>
<body>

  <!-- Cotton Paper Texture -->
  <div class="parchment-grain-overlay" aria-hidden="true"></div>
  <div class="parchment-vignette" aria-hidden="true"></div>

  <!-- Ticker Superior -->
  <aside class="top-ticker-bar" aria-label="Cotizaciones de mercado">
    <div class="ticker-track">
      <div class="ticker-item"><span class="ticker-symbol">DJIA</span> 43,910.2 <span class="ticker-val-up">▲ +0.78%</span></div>
      <div class="ticker-item"><span class="ticker-symbol">S&amp;P 500</span> 5,864.6 <span class="ticker-val-up">▲ +1.12%</span></div>
      <div class="ticker-item"><span class="ticker-symbol">US10Y</span> 4.318% <span class="ticker-val-down">▼ -0.04%</span></div>
      <div class="ticker-item"><span class="ticker-symbol">BRENT</span> $74.20 <span class="ticker-val-down">▼ -1.2%</span></div>
      <div class="ticker-item"><span class="ticker-symbol">GOLD (OZ)</span> $2,684.50 <span class="ticker-val-up">▲ +0.65%</span></div>
      <div class="ticker-item"><span class="ticker-symbol">FED FUNDS</span> 4.75% <span class="ticker-val-up">▲ 0.00%</span></div>
      <div class="ticker-item"><span class="ticker-symbol">NASDAQ 100</span> 19,281.4 <span class="ticker-val-up">▲ +1.50%</span></div>
      <div class="ticker-item"><span class="ticker-symbol">VIX</span> 14.82 <span class="ticker-val-down">▼ -0.85%</span></div>
      <div class="ticker-item"><span class="ticker-symbol">DJIA</span> 43,910.2 <span class="ticker-val-up">▲ +0.78%</span></div>
      <div class="ticker-item"><span class="ticker-symbol">S&amp;P 500</span> 5,864.6 <span class="ticker-val-up">▲ +1.12%</span></div>
      <div class="ticker-item"><span class="ticker-symbol">US10Y</span> 4.318% <span class="ticker-val-down">▼ -0.04%</span></div>
    </div>
  </aside>

  <!-- Encabezado -->
  <header class="site-header">
    <div class="header-brand">
      <div class="brand-monogram">BH</div>
      <div class="brand-text">
        <h1>Beatriz Hernández</h1>
        <p>Quantitative Economics &amp; Market Intelligence</p>
      </div>
    </div>

    <nav aria-label="Navegación principal">
      <ul class="nav-links">
        <li><a href="#investigacion">Investigación</a></li>
        <li><a href="#modelos">Modelos Cuantitativos</a></li>
        <li><a href="#analitica">Business Analytics</a></li>
        <li><a href="#trayectoria">Archivo</a></li>
        <li><a href="#contacto">Contacto</a></li>
      </ul>
    </nav>
  </header>

  <!-- Hero Banner con Canvas Anti-Gravedad -->
  <main class="hero-stage">
    <canvas id="antiGravityCanvas" aria-label="Simulación física anti-gravedad de billetes de dólar y sellos monetarios interactivos"></canvas>

    <section class="hero-content">
      <div class="hero-interactive">
        <div class="hero-pill-badge">
          <span class="pill-dot"></span>
          <span>Zero-G Financial Dynamics • Browniana Aplicada</span>
        </div>
      </div>

      <h2 class="hero-headline">
        Decodificando la dinámica de mercado con <em>rigor analítico</em>
      </h2>

      <p class="hero-subhead">
        Arquitectura de datos para mercados de capitales, modelos econométricos y análisis avanzado de riesgo macroeconómico.
      </p>

      <div class="hero-interactive hero-tags">
        <span class="tag-badge">Modelos de Volatilidad</span>
        <span class="tag-badge">Stochastic Calculus</span>
        <span class="tag-badge">Análisis Macroeconómico</span>
        <span class="tag-badge">Arbitraje Estadístico</span>
        <span class="tag-badge">Visualización de Datos</span>
      </div>

      <div class="hero-interactive hero-actions">
        <a href="#investigacion" class="btn-primary">
          <span>Explorar Trabajos</span>
          <span aria-hidden="true">→</span>
        </a>
        <a href="#modelos" class="btn-secondary">
          <span>Ver Modelos Interactivos</span>
        </a>
      </div>

      <div class="hero-floating-tip">
        <span>✦ <strong>Interacción:</strong> Pasa el ratón para crear brisa • Arrastra y lanza los billetes</span>
      </div>
    </section>

    <!-- Panel HUD -->
    <aside class="physics-hud" id="physicsHud" aria-label="Controles del simulador físico">
      <div class="hud-header" id="hudToggle" title="Plegar / Desplegar panel">
        <div class="hud-title">
          <span class="hud-indicator"></span>
          <span>Parámetros de Física</span>
        </div>
        <button class="hud-toggle-btn" id="hudChevron" aria-label="Alternar panel">▾</button>
      </div>

      <div class="hud-body">
        <div class="hud-control-group">
          <div class="hud-label-row">
            <span>Fuerza de Brisa</span>
            <span id="breezeVal">0.85</span>
          </div>
          <input type="range" class="hud-slider" id="sliderBreeze" min="0.1" max="2.0" step="0.05" value="0.85">
        </div>

        <div class="hud-control-group">
          <div class="hud-label-row">
            <span>Fricción de Aire</span>
            <span id="frictionVal">0.98</span>
          </div>
          <input type="range" class="hud-slider" id="sliderFriction" min="0.92" max="0.995" step="0.005" value="0.982">
        </div>

        <div class="hud-control-group">
          <div class="hud-label-row">
            <span>Densidad de Activos</span>
            <span id="densityVal">16</span>
          </div>
          <input type="range" class="hud-slider" id="sliderDensity" min="6" max="28" step="1" value="16">
        </div>

        <div class="hud-btn-row">
          <button class="hud-action-btn" id="btnSpawnBill">+ Billete</button>
          <button class="hud-action-btn" id="btnSpawnToken">+ Ficha</button>
          <button class="hud-action-btn btn-burst" id="btnScatter">✦ Dispersar / Impulso</button>
        </div>
      </div>
    </aside>
  </main>

  <!-- Motor Canvas 2D/2.5D Embebido -->
  <script>
  (function () {
    'use strict';

    const CONFIG = {
      itemCountDesktop: 16,
      itemCountMobile: 9,
      mobileBreakpoint: 768,

      airFriction: 0.982,
      angularFriction: 0.965,
      ambientDriftSpeed: 0.42,
      flutterFrequency: 0.022,
      flutterAmplitude: 0.22,
      
      breezeRadius: 220,
      breezeForce: 0.85,
      breezeTorque: 0.0035,
      
      dragSpring: 0.22,
      throwVelocityMultiplier: 1.25,

      palette: {
        bgParchment: '#EFECE6',
        bgParchmentDark: '#E4DFD3',
        inkCharcoal: '#262624',
        inkDollarGreen: '#4A5B4E',
        inkDollarGreenDark: '#354338',
        inkWineRed: '#8A4843',
        inkWineRedDark: '#67312D',
        inkSlateBlue: '#475560',
        inkPaleGold: '#BFA878',
        paperIvory: '#F9F7F2'
      }
    };

    let canvas, ctx;
    let width = 1200;
    let height = 800;
    let dpr = 1;
    let items = [];
    let textures = {};
    let animationFrameId = null;
    let lastTime = performance.now();

    const pointer = {
      x: -9999,
      y: -9999,
      prevX: -9999,
      prevY: -9999,
      vx: 0,
      vy: 0,
      isDown: false,
      dragItem: null,
      lastActive: 0
    };

    function createOffscreen(w, h) {
      const osc = document.createElement('canvas');
      osc.width = Math.round(w * 2);
      osc.height = Math.round(h * 2);
      const octx = osc.getContext('2d');
      octx.scale(2, 2);
      return { canvas: osc, ctx: octx, width: w, height: h };
    }

    function drawGuilloche(ctx, cx, cy, R, r, p, steps, strokeStyle, lineWidth = 0.75) {
      ctx.save();
      ctx.beginPath();
      ctx.strokeStyle = strokeStyle;
      ctx.lineWidth = lineWidth;
      for (let theta = 0; theta <= steps; theta += 0.05) {
        const x = (R - r) * Math.cos(theta) + p * Math.cos((R - r) * theta / r);
        const y = (R - r) * Math.sin(theta) - p * Math.sin((R - r) * theta / r);
        if (theta === 0) ctx.moveTo(cx + x, cy + y);
        else ctx.lineTo(cx + x, cy + y);
      }
      ctx.stroke();
      ctx.restore();
    }

    function drawSecurityBorder(ctx, w, h, color) {
      ctx.save();
      ctx.strokeStyle = color;
      ctx.lineWidth = 0.8;
      const margin = 7;
      const innerMargin = 12;

      ctx.strokeRect(margin, margin, w - margin * 2, h - margin * 2);
      ctx.strokeRect(margin + 2.5, margin + 2.5, w - (margin + 2.5) * 2, h - (margin + 2.5) * 2);

      const cornerSize = 18;
      const corners = [
        [margin, margin],
        [w - margin - cornerSize, margin],
        [margin, h - margin - cornerSize],
        [w - margin - cornerSize, h - margin - cornerSize]
      ];

      corners.forEach(([cx, cy]) => {
        ctx.fillStyle = CONFIG.palette.inkDollarGreenDark;
        ctx.fillRect(cx, cy, cornerSize, cornerSize);
        ctx.strokeStyle = CONFIG.palette.inkPaleGold;
        ctx.strokeRect(cx + 1.5, cy + 1.5, cornerSize - 3, cornerSize - 3);
        drawGuilloche(ctx, cx + cornerSize / 2, cy + cornerSize / 2, 7, 3, 4, Math.PI * 6, CONFIG.palette.paperIvory, 0.6);
      });

      ctx.strokeRect(innerMargin, innerMargin, w - innerMargin * 2, h - innerMargin * 2);

      ctx.strokeStyle = color;
      ctx.beginPath();
      for (let x = margin + cornerSize; x < w - margin - cornerSize; x += 6) {
        ctx.moveTo(x, margin + 2.5);
        ctx.lineTo(x + 3, innerMargin);
        ctx.lineTo(x + 6, margin + 2.5);

        ctx.moveTo(x, h - margin - 2.5);
        ctx.lineTo(x + 3, h - innerMargin);
        ctx.lineTo(x + 6, h - margin - 2.5);
      }
      ctx.stroke();
      ctx.restore();
    }

    function generateBanknoteTexture(variant = 1) {
      const w = 260;
      const h = 100;
      const { canvas: osc, ctx: g } = createOffscreen(w, h);

      g.fillStyle = CONFIG.palette.paperIvory;
      g.fillRect(0, 0, w, h);

      g.strokeStyle = '#ECE5D4';
      g.lineWidth = 0.5;
      g.beginPath();
      for (let x = 0; x < w; x += 8) {
        g.moveTo(x, 0); g.lineTo(x, h);
      }
      for (let y = 0; y < h; y += 8) {
        g.moveTo(0, y); g.lineTo(w, y);
      }
      g.stroke();

      drawSecurityBorder(g, w, h, CONFIG.palette.inkDollarGreen);

      const ovalCx = w / 2;
      const ovalCy = h / 2;
      const ovalRx = 38;
      const ovalRy = 32;

      drawGuilloche(g, ovalCx, ovalCy, 40, 14, 18, Math.PI * 14, CONFIG.palette.inkDollarGreen, 0.7);
      drawGuilloche(g, ovalCx, ovalCy, 32, 8, 12, Math.PI * 10, CONFIG.palette.inkPaleGold, 0.6);

      g.save();
      g.beginPath();
      if (g.ellipse) {
        g.ellipse(ovalCx, ovalCy, ovalRx, ovalRy, 0, 0, Math.PI * 2);
      } else {
        g.arc(ovalCx, ovalCy, (ovalRx + ovalRy) / 2, 0, Math.PI * 2);
      }
      g.clip();

      g.fillStyle = '#E8E3D5';
      g.fillRect(ovalCx - ovalRx, ovalCy - ovalRy, ovalRx * 2, ovalRy * 2);
      g.strokeStyle = CONFIG.palette.inkDollarGreenDark;
      g.lineWidth = 0.5;
      for (let r = 0; r < Math.PI * 2; r += 0.12) {
        g.beginPath();
        g.moveTo(ovalCx, ovalCy);
        g.lineTo(ovalCx + Math.cos(r) * 45, ovalCy + Math.sin(r) * 45);
        g.stroke();
      }

      g.fillStyle = CONFIG.palette.inkCharcoal;
      g.strokeStyle = CONFIG.palette.inkCharcoal;
      g.lineWidth = 1.2;

      if (variant === 1) {
        g.beginPath();
        g.arc(ovalCx, ovalCy - 2, 8, 0, Math.PI * 2);
        g.fill();
        g.beginPath();
        g.arc(ovalCx, ovalCy - 17, 5, 0, Math.PI * 2);
        g.fill();
        g.beginPath();
        g.moveTo(ovalCx - 5, ovalCy - 17);
        g.lineTo(ovalCx - 10, ovalCy - 15);
        g.lineTo(ovalCx - 5, ovalCy - 13);
        g.fill();
        g.beginPath();
        g.moveTo(ovalCx - 8, ovalCy - 6);
        g.quadraticCurveTo(ovalCx - 28, ovalCy - 22, ovalCx - 32, ovalCy);
        g.quadraticCurveTo(ovalCx - 20, ovalCy + 8, ovalCx - 4, ovalCy + 4);
        g.moveTo(ovalCx + 8, ovalCy - 6);
        g.quadraticCurveTo(ovalCx + 28, ovalCy - 22, ovalCx + 32, ovalCy);
        g.quadraticCurveTo(ovalCx + 20, ovalCy + 8, ovalCx + 4, ovalCy + 4);
        g.fill();
        g.lineWidth = 1;
        g.beginPath();
        g.moveTo(ovalCx - 18, ovalCy + 14);
        g.lineTo(ovalCx + 18, ovalCy + 14);
        g.stroke();
      } else {
        g.beginPath();
        g.moveTo(ovalCx - 20, ovalCy + 6);
        g.quadraticCurveTo(ovalCx - 24, ovalCy - 6, ovalCx - 14, ovalCy - 12);
        g.lineTo(ovalCx - 10, ovalCy - 15);
        g.lineTo(ovalCx - 10, ovalCy - 8);
        g.quadraticCurveTo(ovalCx, ovalCy - 14, ovalCx + 12, ovalCy - 8);
        g.quadraticCurveTo(ovalCx + 24, ovalCy - 2, ovalCx + 22, ovalCy + 12);
        g.lineTo(ovalCx + 14, ovalCy + 12);
        g.lineTo(ovalCx + 8, ovalCy + 4);
        g.lineTo(ovalCx - 12, ovalCy + 12);
        g.closePath();
        g.fill();
        g.strokeStyle = CONFIG.palette.paperIvory;
        g.lineWidth = 0.8;
        g.beginPath();
        g.moveTo(ovalCx - 14, ovalCy - 6);
        g.quadraticCurveTo(ovalCx - 2, ovalCy - 10, ovalCx + 14, ovalCy - 4);
        g.stroke();
      }
      g.restore();

      g.strokeStyle = CONFIG.palette.inkDollarGreenDark;
      g.lineWidth = 1.2;
      g.beginPath();
      if (g.ellipse) {
        g.ellipse(ovalCx, ovalCy, ovalRx, ovalRy, 0, 0, Math.PI * 2);
      } else {
        g.arc(ovalCx, ovalCy, (ovalRx + ovalRy) / 2, 0, Math.PI * 2);
      }
      g.stroke();

      const leftSealX = ovalCx - 64;
      const leftSealY = ovalCy + 2;
      g.save();
      g.strokeStyle = CONFIG.palette.inkDollarGreenDark;
      g.fillStyle = '#405244';
      g.lineWidth = 0.8;
      g.beginPath();
      for (let a = 0; a < Math.PI * 2; a += Math.PI / 16) {
        const r1 = 16, r2 = 14;
        g.lineTo(leftSealX + Math.cos(a) * r1, leftSealY + Math.sin(a) * r1);
        g.lineTo(leftSealX + Math.cos(a + 0.1) * r2, leftSealY + Math.sin(a + 0.1) * r2);
      }
      g.closePath();
      g.stroke();
      g.font = 'bold 9px "Playfair Display", Georgia, serif';
      g.textAlign = 'center';
      g.textBaseline = 'middle';
      g.fillText('⚖', leftSealX, leftSealY - 1);
      g.restore();

      const rightSealX = ovalCx + 64;
      const rightSealY = ovalCy + 2;
      g.save();
      g.strokeStyle = CONFIG.palette.inkWineRed;
      g.fillStyle = CONFIG.palette.inkWineRed;
      g.lineWidth = 0.9;
      g.beginPath();
      for (let a = 0; a < Math.PI * 2; a += Math.PI / 18) {
        const r1 = 16.5, r2 = 13.5;
        g.lineTo(rightSealX + Math.cos(a) * r1, rightSealY + Math.sin(a) * r1);
        g.lineTo(rightSealX + Math.cos(a + 0.09) * r2, rightSealY + Math.sin(a + 0.09) * r2);
      }
      g.closePath();
      g.stroke();
      g.font = 'bold 12px "Playfair Display", Georgia, serif';
      g.textAlign = 'center';
      g.textBaseline = 'middle';
      g.fillText(variant === 1 ? 'NY' : 'FED', rightSealX, rightSealY);
      g.restore();

      g.font = 'bold 13px "Cinzel", Georgia, serif';
      g.fillStyle = CONFIG.palette.paperIvory;
      g.textAlign = 'center';
      g.textBaseline = 'middle';
      const denom = variant === 1 ? '100' : '1';
      g.fillText(denom, 16, 16);
      g.fillText(denom, w - 16, 16);
      g.fillText(denom, 16, h - 16);
      g.fillText(denom, w - 16, h - 16);

      g.fillStyle = CONFIG.palette.inkCharcoal;
      g.font = 'bold 7px "Cinzel", serif';
      g.fillText('FEDERAL RESERVE NOTE • SYSTEM OF FINANCE', w / 2, 19);
      g.font = 'italic 6px "Playfair Display", serif';
      g.fillText(variant === 1 ? '— QUANTITATIVE THEORY OF VALUE —' : '— MARKET EQUILIBRIUM & ARBITRAGE —', w / 2, h - 20);
      g.font = 'bold 8px "Cinzel", serif';
      g.fillText(variant === 1 ? 'ONE HUNDRED UNITS' : 'ONE SOVEREIGN UNIT', w / 2, h - 11);

      g.font = '700 7px "JetBrains Mono", monospace';
      g.fillStyle = CONFIG.palette.inkDollarGreenDark;
      g.textAlign = 'left';
      g.fillText('B 84729104 A', 30, h - 23);
      g.textAlign = 'right';
      g.fillStyle = CONFIG.palette.inkWineRedDark;
      g.fillText('SERIES 1944', w - 30, 26);

      return osc;
    }

    function generateTokenTexture(symbol, color) {
      const size = 68;
      const { canvas: osc, ctx: g } = createOffscreen(size, size);
      const cx = size / 2;
      const cy = size / 2;
      const r = 30;

      g.save();
      g.translate(cx, cy);

      g.fillStyle = color;
      g.beginPath();
      const teeth = 36;
      for (let i = 0; i < teeth; i++) {
        const a = (i / teeth) * Math.PI * 2;
        const rad = i % 2 === 0 ? r : r - 2.5;
        g.lineTo(Math.cos(a) * rad, Math.sin(a) * rad);
      }
      g.closePath();
      g.fill();

      g.strokeStyle = CONFIG.palette.paperIvory;
      g.lineWidth = 1.2;
      g.beginPath();
      g.arc(0, 0, r - 5, 0, Math.PI * 2);
      g.stroke();

      g.fillStyle = CONFIG.palette.paperIvory;
      g.textAlign = 'center';
      g.textBaseline = 'middle';
      if (symbol.length <= 2) {
        g.font = 'bold 22px "Cinzel", Georgia, serif';
        g.fillText(symbol, 0, 1);
      } else {
        g.font = 'bold 12px "JetBrains Mono", monospace';
        g.fillText(symbol, 0, 1);
      }
      g.restore();
      return osc;
    }

    function generateTickerTapeTexture(text, width = 230) {
      const height = 44;
      const { canvas: osc, ctx: g } = createOffscreen(width, height);

      g.fillStyle = '#F5F2EB';
      g.fillRect(0, 0, width, height);

      g.strokeStyle = '#D8D1C2';
      g.lineWidth = 0.8;
      g.strokeRect(0, 0, width, height);

      g.fillStyle = CONFIG.palette.bgParchment;
      for (let x = 8; x < width; x += 14) {
        g.beginPath();
        g.arc(x, height - 6, 2, 0, Math.PI * 2);
        g.fill();
        g.strokeStyle = '#D0C9B8';
        g.stroke();
      }

      g.font = '700 10.5px "JetBrains Mono", monospace';
      g.fillStyle = CONFIG.palette.inkCharcoal;
      g.textBaseline = 'middle';
      g.textAlign = 'left';
      g.fillText(text, 10, 18);

      return osc;
    }

    function generateChartPlaqueTexture() {
      const w = 150;
      const h = 90;
      const { canvas: osc, ctx: g } = createOffscreen(w, h);

      g.fillStyle = '#FAF7F0';
      g.fillRect(0, 0, w, h);
      g.strokeStyle = CONFIG.palette.inkDollarGreen;
      g.lineWidth = 1;
      g.strokeRect(3, 3, w - 6, h - 6);
      g.strokeRect(5.5, 5.5, w - 11, h - 11);

      g.font = 'bold 6.5px "Cinzel", Georgia, serif';
      g.fillStyle = CONFIG.palette.inkCharcoal;
      g.textAlign = 'center';
      g.fillText('VOLATILITY INDEX & STOCHASTICS', w / 2, 14);

      g.strokeStyle = '#E2DDCF';
      g.lineWidth = 0.5;
      for (let y = 22; y <= h - 14; y += 10) {
        g.beginPath();
        g.moveTo(12, y); g.lineTo(w - 12, y);
        g.stroke();
      }
      for (let x = 12; x <= w - 12; x += 16) {
        g.beginPath();
        g.moveTo(x, 22); g.lineTo(x, h - 14);
        g.stroke();
      }

      const candles = [
        { x: 24, open: 55, close: 40, high: 32, low: 62, bull: true },
        { x: 42, open: 42, close: 48, high: 36, low: 52, bull: false },
        { x: 60, open: 48, close: 34, high: 28, low: 50, bull: true },
        { x: 78, open: 34, close: 38, high: 30, low: 45, bull: false },
        { x: 96, open: 36, close: 26, high: 22, low: 40, bull: true },
        { x: 114, open: 26, close: 31, high: 24, low: 36, bull: false },
        { x: 132, open: 30, close: 22, high: 18, low: 34, bull: true }
      ];

      candles.forEach(c => {
        g.strokeStyle = CONFIG.palette.inkCharcoal;
        g.lineWidth = 0.9;
        g.beginPath();
        g.moveTo(c.x, c.high);
        g.lineTo(c.x, c.low);
        g.stroke();

        const top = Math.min(c.open, c.close);
        const bHeight = Math.abs(c.open - c.close);
        if (c.bull) {
          g.fillStyle = CONFIG.palette.inkDollarGreen;
          g.fillRect(c.x - 3.5, top, 7, bHeight);
          g.fillStyle = CONFIG.palette.paperIvory;
          g.fillRect(c.x - 2.5, top + 1, 5, Math.max(1, bHeight - 2));
        } else {
          g.fillStyle = CONFIG.palette.inkWineRed;
          g.fillRect(c.x - 3.5, top, 7, bHeight);
        }
        g.strokeStyle = CONFIG.palette.inkCharcoal;
        g.strokeRect(c.x - 3.5, top, 7, bHeight);
      });

      g.strokeStyle = CONFIG.palette.inkSlateBlue;
      g.lineWidth = 1.2;
      g.beginPath();
      g.moveTo(20, 52);
      g.quadraticCurveTo(70, 48, 96, 28);
      g.quadraticCurveTo(116, 20, 134, 22);
      g.stroke();

      return osc;
    }

    function initTextures() {
      textures = {
        bill100: generateBanknoteTexture(1),
        bill1: generateBanknoteTexture(2),
        tokenDollar: generateTokenTexture('$', CONFIG.palette.inkDollarGreen),
        tokenWine: generateTokenTexture('▲', CONFIG.palette.inkWineRed),
        tokenBlue: generateTokenTexture('VOL', CONFIG.palette.inkSlateBlue),
        tokenGold: generateTokenTexture('%', CONFIG.palette.inkWineRedDark),
        tape1: generateTickerTapeTexture('NYSE: SPX 5840.2 ▲ +1.4% • VOL 84.2M • CASH FLOW 8.9B', 250),
        tape2: generateTickerTapeTexture('US10Y 4.31% • GOLD 2,684 • STOXX 50 ▲ +0.8% • LIQUIDITY', 240),
        chartPlaque: generateChartPlaqueTexture()
      };
    }

    class FloatingAsset {
      constructor(type, textureKey, x, y, options = {}) {
        this.type = type;
        this.textureKey = textureKey;
        const tex = textures[textureKey];
        this.w = tex.width / 2;
        this.h = tex.height / 2;

        this.x = x;
        this.y = y;
        this.vx = (Math.random() - 0.5) * CONFIG.ambientDriftSpeed;
        this.vy = (Math.random() - 0.5) * CONFIG.ambientDriftSpeed;
        
        this.z = options.z || (0.7 + Math.random() * 0.6);
        this.baseScale = options.scale || (0.8 + Math.random() * 0.35);

        this.angle = (Math.random() - 0.5) * Math.PI * 0.4;
        this.vAngle = (Math.random() - 0.5) * 0.003;

        this.pitchPhase = Math.random() * Math.PI * 2;
        this.rollPhase = Math.random() * Math.PI * 2;
        this.flutterSpeed = 0.015 + Math.random() * 0.015;

        this.isDragging = false;
        this.dragOffset = { x: 0, y: 0 };
      }

      containsPoint(px, py) {
        const dx = px - this.x;
        const dy = py - this.y;
        const cos = Math.cos(-this.angle);
        const sin = Math.sin(-this.angle);
        const localX = dx * cos - dy * sin;
        const localY = dx * sin + dy * cos;

        const halfW = (this.w * this.baseScale) / 2;
        const halfH = (this.h * this.baseScale) / 2;

        return (
          localX >= -halfW &&
          localX <= halfW &&
          localY >= -halfH &&
          localY <= halfH
        );
      }

      update(time) {
        if (this.isDragging) {
          const targetX = pointer.x + this.dragOffset.x;
          const targetY = pointer.y + this.dragOffset.y;
          
          this.vx = (targetX - this.x) * CONFIG.dragSpring;
          this.vy = (targetY - this.y) * CONFIG.dragSpring;
          this.x += this.vx;
          this.y += this.vy;

          this.vAngle = (this.vx * 0.002) - this.angle * 0.05;
          this.angle += this.vAngle;

          this.z = Math.min(1.5, this.z + 0.04);
          return;
        }

        const ambientCurrentX = Math.sin(time * 0.0008 + this.y * 0.003) * 0.12;
        const ambientCurrentY = Math.cos(time * 0.0006 + this.x * 0.003) * 0.08;
        this.vx += ambientCurrentX * 0.05;
        this.vy += ambientCurrentY * 0.05;

        this.vx *= CONFIG.airFriction;
        this.vy *= CONFIG.airFriction;
        this.vAngle *= CONFIG.angularFriction;

        this.x += this.vx;
        this.y += this.vy;
        this.angle += this.vAngle;

        this.pitchPhase += this.flutterSpeed;
        this.rollPhase += this.flutterSpeed * 0.8;

        this.z += (1.0 - this.z) * 0.02;

        const margin = 40;
        if (this.x < -margin) this.vx += 0.4;
        if (this.x > width + margin) this.vx -= 0.4;
        if (this.y < -margin) this.vy += 0.4;
        if (this.y > height + margin) this.vy -= 0.4;

        const wrapPadding = 120;
        if (this.x < -wrapPadding) this.x = width + wrapPadding * 0.8;
        if (this.x > width + wrapPadding) this.x = -wrapPadding * 0.8;
        if (this.y < -wrapPadding) this.y = height + wrapPadding * 0.8;
        if (this.y > height + wrapPadding) this.y = -wrapPadding * 0.8;
      }

      applyBreeze(mx, my, mvx, mvy) {
        if (this.isDragging) return;

        const dx = this.x - mx;
        const dy = this.y - my;
        const distSq = dx * dx + dy * dy;
        const radius = CONFIG.breezeRadius;

        if (distSq < radius * radius && distSq > 0) {
          const dist = Math.sqrt(distSq);
          const normX = dx / dist;
          const normY = dy / dist;
          const factor = (1 - dist / radius);

          const strength = factor * factor * CONFIG.breezeForce;

          this.vx += normX * strength;
          this.vy += normY * strength;
          this.vx += mvx * factor * 0.15;
          this.vy += mvy * factor * 0.15;

          const cross = normX * mvy - normY * mvx;
          this.vAngle += (cross * CONFIG.breezeTorque * factor) + (Math.sin(dist) * 0.003 * factor);
          this.pitchPhase += factor * 0.1;
        }
      }

      render(ctx) {
        const tex = textures[this.textureKey];
        if (!tex) return;

        const scale = this.baseScale * (0.9 + this.z * 0.1);
        const pitch = Math.sin(this.pitchPhase) * CONFIG.flutterAmplitude;
        const roll = Math.cos(this.rollPhase) * (CONFIG.flutterAmplitude * 0.6);

        const renderW = this.w * scale;
        const renderH = this.h * scale * (1 - Math.abs(pitch) * 0.35);

        ctx.save();
        ctx.translate(this.x, this.y);
        ctx.rotate(this.angle);

        if (this.type === 'bill' || this.type === 'tape') {
          ctx.transform(1, roll * 0.25, 0, 1 - Math.abs(pitch) * 0.15, 0, 0);
        }

        // Sombra suave en elevación Z
        const shadowDist = 14 * this.z;
        const shadowBlur = 18 * this.z;
        ctx.save();
        ctx.shadowColor = 'rgba(40, 35, 25, 0.22)';
        ctx.shadowBlur = shadowBlur;
        ctx.shadowOffsetX = 8 * this.z;
        ctx.shadowOffsetY = shadowDist;
        ctx.fillStyle = 'rgba(0,0,0,0.01)';
        ctx.fillRect(-renderW / 2, -renderH / 2, renderW, renderH);
        ctx.restore();

        // Dibujar textura offscreen
        ctx.drawImage(
          tex,
          0, 0, tex.width, tex.height,
          -renderW / 2, -renderH / 2, renderW, renderH
        );

        // Brillo reflectivo
        if (this.type === 'bill' || this.type
