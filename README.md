<!DOCTYPE html>
<html lang="en" class="dark">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>GONION // Precision Craniometric Aesthetics &amp; Softmaxxing Engine</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500;600;700&family=Space+Grotesk:wght@500;600;700&display=swap" rel="stylesheet" />
  <script>
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          fontFamily: {
            display: ['Space Grotesk', 'system-ui', 'sans-serif'],
            sans: ['Inter', 'system-ui', 'sans-serif'],
            mono: ['JetBrains Mono', 'monospace'],
          },
          colors: {
            obsidian: '#07090D',
            panel: '#0D1118',
            panelElevated: '#121824',
            champagne: '#E2C275',
            champagneLight: '#F2DA9B',
            iceCyan: '#38BDF8',
            titanium: '#E2E8F0',
          },
        },
      },
    };
  </script>
  <style>
    /* Luxury Obsidian & Titanium Base */
    :root {
      --bg-obsidian: #07090D;
      --bg-panel: rgba(13, 17, 24, 0.84);
      --border-gold: rgba(226, 194, 117, 0.16);
      --border-gold-hover: rgba(226, 194, 117, 0.42);
      --accent-gold: #E2C275;
      --accent-cyan: #38BDF8;
    }

    body {
      background-color: var(--bg-obsidian);
      color: #F1F5F9;
      font-family: 'Inter', sans-serif;
      overflow-x: hidden;
      background-image:
        radial-gradient(circle at 12% 8%, rgba(226, 194, 117, 0.075), transparent 36%),
        radial-gradient(circle at 88% 85%, rgba(56, 189, 248, 0.065), transparent 42%),
        linear-gradient(to right, rgba(226, 194, 117, 0.022) 1px, transparent 1px),
        linear-gradient(to bottom, rgba(226, 194, 117, 0.022) 1px, transparent 1px);
      background-size: 100% 100%, 100% 100%, 40px 40px, 40px 40px;
    }

    /* Elevated Obsidian Glass Panels with Hairline Champagne Borders */
    .luxury-panel {
      background: var(--bg-panel);
      backdrop-filter: blur(18px);
      -webkit-backdrop-filter: blur(18px);
      border: 1px solid var(--border-gold);
      box-shadow: 0 18px 48px -14px rgba(0, 0, 0, 0.82), inset 0 1px 0 0 rgba(255, 255, 255, 0.04);
    }

    .luxury-subcard {
      background: rgba(18, 24, 36, 0.72);
      border: 1px solid rgba(226, 194, 117, 0.12);
      transition: border-color 0.25s ease, transform 0.2s ease, background-color 0.25s ease;
    }

    .luxury-subcard:hover {
      border-color: var(--border-gold-hover);
      background: rgba(22, 29, 43, 0.85);
    }

    /* Champagne Gold Primary Action CTA */
    .btn-champagne {
      background: linear-gradient(135deg, #E2C275 0%, #C9A34E 55%, #E8CE8B 100%);
      color: #07090D;
      box-shadow: 0 0 26px rgba(226, 194, 117, 0.28), inset 0 1px 0 rgba(255, 255, 255, 0.45);
      transition: all 0.25s cubic-bezier(0.22, 1, 0.36, 1);
    }

    .btn-champagne:hover:not(:disabled) {
      box-shadow: 0 0 38px rgba(226, 194, 117, 0.48), inset 0 1px 0 rgba(255, 255, 255, 0.65);
      transform: translateY(-1px);
    }

    .btn-champagne:disabled {
      opacity: 0.55;
      cursor: not-allowed;
    }

    /* Animated Biometric Laser Sweep */
    @keyframes craniometricSweep {
      0% {
        top: 3%;
        opacity: 0;
      }
      12% {
        opacity: 1;
      }
      50% {
        top: 95%;
        opacity: 1;
      }
      88% {
        opacity: 1;
      }
      100% {
        top: 3%;
        opacity: 0;
      }
    }

    .laser-beam {
      position: absolute;
      left: 0;
      right: 0;
      height: 2.5px;
      background: linear-gradient(90deg, transparent, #E2C275, #38BDF8, #E2C275, transparent);
      box-shadow: 0 0 16px 3px rgba(226, 194, 117, 0.75), 0 0 32px 6px rgba(56, 189, 248, 0.45);
      animation: craniometricSweep 2.3s cubic-bezier(0.45, 0.05, 0.55, 0.95) infinite;
      pointer-events: none;
      z-index: 20;
    }

    .scan-tint {
      background: linear-gradient(180deg, rgba(226, 194, 117, 0.1) 0%, rgba(56, 189, 248, 0.05) 100%);
    }

    /* Custom Scrollbar */
    ::-webkit-scrollbar {
      width: 6px;
      height: 6px;
    }
    ::-webkit-scrollbar-track {
      background: #07090D;
    }
    ::-webkit-scrollbar-thumb {
      background: #1E2533;
      border-radius: 9999px;
    }
    ::-webkit-scrollbar-thumb:hover {
      background: #E2C275;
    }

    /* Prevent touch scrolling while adjusting craniometric points */
    #craniometricCanvas {
      touch-action: none;
      user-select: none;
      -webkit-user-select: none;
    }
  </style>
</head>
<body class="min-h-screen flex flex-col selection:bg-[#E2C275]/30 selection:text-[#F2DA9B]">

  <!-- Non-Blocking Toast Notification Stack -->
  <div id="toastContainer" class="fixed top-4 right-4 z-50 flex flex-col gap-2 max-w-sm w-full pointer-events-none px-4 sm:px-0"></div>

  <!-- Luxury Biometric Brand Header -->
  <header class="sticky top-0 z-40 luxury-panel border-b border-[#E2C275]/20">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-3.5 flex items-center justify-between gap-4">
      <!-- Custom SVG Emblem + Brand Identity -->
      <div class="flex items-center gap-3.5 sm:gap-4">
        <!-- Bespoke Craniometric Gonial Angle (Go) + Golden-Ratio Caliper Arc SVG Emblem -->
        <div class="relative w-11 h-11 sm:w-12 sm:h-12 rounded-xl bg-gradient-to-b from-[#141A26] to-[#080B10] border border-[#E2C275]/40 flex items-center justify-center shadow-lg shadow-black/60 shrink-0">
          <svg class="w-8 h-8 sm:w-9 sm:h-9" viewBox="0 0 48 48" fill="none" xmlns="http://www.w3.org/2000/svg" aria-label="Gonion Craniometric Emblem">
            <defs>
              <linearGradient id="goldGrad" x1="6" y1="6" x2="42" y2="42" gradientUnits="userSpaceOnUse">
                <stop offset="0%" stop-color="#F5E1A4" />
                <stop offset="55%" stop-color="#E2C275" />
                <stop offset="100%" stop-color="#9E7B2F" />
              </linearGradient>
              <linearGradient id="titaniumGrad" x1="10" y1="8" x2="38" y2="40" gradientUnits="userSpaceOnUse">
                <stop offset="0%" stop-color="#FFFFFF" />
                <stop offset="100%" stop-color="#94A3B8" />
              </linearGradient>
            </defs>
            <!-- Outer Optical Caliper Ring -->
            <circle cx="24" cy="24" r="20" stroke="rgba(226, 194, 117, 0.22)" stroke-width="1" stroke-dasharray="2 3" />
            <!-- Golden-Ratio Caliper Arc -->
            <path d="M 35 10 A 18 18 0 0 1 13 38" stroke="url(#goldGrad)" stroke-width="1.75" stroke-linecap="round" />
            <!-- Secondary Fibonacci Arc -->
            <path d="M 28 14 A 11 11 0 0 1 16 31" stroke="#38BDF8" stroke-width="1.15" stroke-opacity="0.75" stroke-linecap="round" />
            <!-- Stylized Mandibular Ramus & Gonial Angle (Go) Vector -->
            <path d="M 15 11 L 18.5 29.5 L 36 35.5" stroke="url(#titaniumGrad)" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round" />
            <!-- Gonial Angle Arc Indicator -->
            <path d="M 17.6 24.5 A 5.5 5.5 0 0 0 23.4 31.2" stroke="#E2C275" stroke-width="1.3" />
            <!-- Precision Reticle Node at Gonial Vertex (Go) -->
            <circle cx="18.5" cy="29.5" r="4.2" fill="#07090D" stroke="#E2C275" stroke-width="1.6" />
            <circle cx="18.5" cy="29.5" r="1.4" fill="#38BDF8" />
            <!-- Micro Caliper Tick Marks -->
            <line x1="24" y1="2.5" x2="24" y2="5.5" stroke="#E2C275" stroke-width="1.2" />
            <line x1="42.5" y1="24" x2="45.5" y2="24" stroke="#E2C275" stroke-width="1.2" />
          </svg>
        </div>

        <!-- Brand Wordmark, Pill Badge & Tagline -->
        <div>
          <div class="flex flex-wrap items-center gap-2 sm:gap-2.5">
            <span class="font-display font-bold tracking-[0.26em] text-lg sm:text-xl text-white">GONION</span>
            <span class="text-[10px] font-mono uppercase tracking-[0.14em] px-2.5 py-0.5 rounded-full bg-[#E2C275]/12 text-[#E2C275] border border-[#E2C275]/35">
              CRANIOMETRIC ENGINE // OPTICS v2.4
            </span>
          </div>
          <p class="text-[11px] sm:text-xs text-slate-400 mt-0.5 tracking-wide">
            Architectural Facial Geometry &amp; Evidence-Based Softmaxxing Diagnostics
          </p>
        </div>
      </div>

      <!-- Ephemeral Privacy Indicator -->
      <div class="hidden md:flex items-center gap-2.5 px-3.5 py-1.5 rounded-full bg-[#0D1118] border border-[#E2C275]/25 text-xs text-slate-300 shrink-0">
        <span class="w-2 h-2 rounded-full bg-[#38BDF8] animate-pulse"></span>
        <span class="font-mono text-[11px] text-[#E2C275]">ZERO-RETENTION</span>
        <span class="text-slate-500">|</span>
        <span class="text-[11px] text-slate-400">Local Optical Processing</span>
      </div>
    </div>
  </header>

  <!-- Main Craniometric Studio Workspace -->
  <main class="flex-1 max-w-7xl w-full mx-auto px-4 sm:px-6 lg:px-8 py-6 sm:py-8 space-y-7">

    <!-- Top Quick-Launch Calibration Strip -->
    <section class="luxury-panel rounded-2xl p-4 sm:p-5 flex flex-col lg:flex-row lg:items-center justify-between gap-4">
      <div class="space-y-1 max-w-2xl">
        <div class="flex items-center gap-2 text-[11px] font-mono uppercase tracking-[0.16em] text-[#E2C275]">
          <span>12-Point Anatomical Mapping</span>
          <span class="text-slate-600">•</span>
          <span class="text-[#38BDF8]">Frankfurt Plane &amp; Golden Ratio Φ</span>
        </div>
        <h1 class="font-display text-lg sm:text-xl lg:text-2xl font-bold text-white tracking-tight">
          Precision Craniofacial Telemetry &amp; Personalized Softmaxxing Protocol
        </h1>
      </div>

      <div class="flex flex-wrap items-center gap-2.5 shrink-0">
        <button id="loadSubjectBtn" type="button" class="px-4 py-2.5 rounded-xl bg-[#131926] hover:bg-[#192234] text-[#F2DA9B] border border-[#E2C275]/35 text-xs sm:text-sm font-semibold flex items-center gap-2 transition active:scale-[0.99]">
          <svg class="w-4 h-4 text-[#E2C275]" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.9">
            <path stroke-linecap="round" stroke-linejoin="round" d="M9 3v2m6-2v2M9 19v2m6-2v2M5 9H3m2 6H3m18-6h-2m2 6h-2M7 19h10a2 2 0 002-2V7a2 2 0 00-2-2H7a2 2 0 00-2 2v10a2 2 0 002 2zM9 9h6v6H9V9z" />
          </svg>
          Load Calibration Subject
        </button>

        <button id="openWebcamBtn" type="button" class="px-4 py-2.5 rounded-xl bg-[#131926] hover:bg-[#192234] text-[#38BDF8] border border-[#38BDF8]/35 text-xs sm:text-sm font-semibold flex items-center gap-2 transition active:scale-[0.99]">
          <svg class="w-4 h-4 text-[#38BDF8]" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.9">
            <path stroke-linecap="round" stroke-linejoin="round" d="M15 10l4.553-2.276A1 1 0 0121 8.618v6.764a1 1 0 01-1.447.894L15 14M5 18h8a2 2 0 002-2V8a2 2 0 00-2-2H5a2 2 0 00-2 2v8a2 2 0 002 2z" />
          </svg>
          Live Optical Capture
        </button>
      </div>
    </section>

    <!-- Primary Two-Column Layout: Left = 12-Point Craniometric Canvas & Telemetry | Right = Controls, Report & Consultant -->
    <div class="grid grid-cols-1 lg:grid-cols-12 gap-6 lg:gap-8 items-start">

      <!-- LEFT COLUMN (5 cols): Interactive Landmark Canvas, Overlays & Live Telemetry HUD -->
      <div class="lg:col-span-5 space-y-5">

        <!-- Interactive 12-Point Landmark Viewport Card -->
        <div class="luxury-panel rounded-2xl p-4 sm:p-5 space-y-4">
          <div class="flex items-center justify-between gap-2">
            <div class="flex items-center gap-2">
              <span class="w-2 h-2 rounded-full bg-[#E2C275]"></span>
              <h2 class="text-xs font-mono font-semibold uppercase tracking-[0.14em] text-slate-200">
                12-Point Landmark Matrix
              </h2>
            </div>
            <div class="flex items-center gap-2">
              <button id="resetLandmarksBtn" type="button" class="text-[11px] font-mono px-2.5 py-1.5 rounded-lg bg-white/5 hover:bg-white/10 text-slate-300 border border-white/10 transition">
                Recenter Nodes
              </button>
              <label for="photoInput" class="cursor-pointer text-[11px] font-mono px-2.5 py-1.5 rounded-lg bg-[#E2C275]/15 hover:bg-[#E2C275]/25 text-[#F2DA9B] border border-[#E2C275]/35 font-medium transition">
                Upload Portrait
              </label>
              <input id="photoInput" type="file" accept="image/jpeg,image/png,image/webp" class="hidden" />
            </div>
          </div>

          <!-- Canvas Container -->
          <div id="canvasDropZone" class="relative w-full aspect-[4/5] max-h-[530px] rounded-xl overflow-hidden bg-[#050609] border border-[#E2C275]/20 flex items-center justify-center group">

            <!-- Empty Drag & Drop Prompt -->
            <div id="emptyUploadState" class="absolute inset-0 flex flex-col items-center justify-center p-6 text-center z-10 transition">
              <div class="w-16 h-16 rounded-2xl bg-[#E2C275]/10 border border-[#E2C275]/30 flex items-center justify-center mb-4 text-[#E2C275] group-hover:scale-105 transition">
                <svg class="w-8 h-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.6">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M3 9a2 2 0 012-2h.93a2 2 0 001.664-.89l.812-1.22A2 2 0 0110.07 4h3.86a2 2 0 011.664.89l.812 1.22A2 2 0 0018.07 7H19a2 2 0 012 2v9a2 2 0 01-2 2H5a2 2 0 01-2-2V9z" />
                  <path stroke-linecap="round" stroke-linejoin="round" d="M15 13a3 3 0 11-6 0 3 3 0 016 0z" />
                </svg>
              </div>
              <p class="font-display text-base font-semibold text-white mb-1">Drop Front-Facing Portrait</p>
              <p class="text-xs text-slate-400 mb-5 max-w-xs leading-relaxed">
                Supports JPG, PNG, or WebP. Neutral expression, level head posture, and balanced front lighting yield peak craniometric accuracy.
              </p>
              <div class="flex flex-wrap items-center justify-center gap-2.5">
                <button type="button" onclick="document.getElementById('photoInput').click()" class="px-4 py-2.5 rounded-xl btn-champagne font-bold text-xs">
                  Select File
                </button>
                <button type="button" onclick="loadCalibrationSubject()" class="px-4 py-2.5 rounded-xl bg-white/5 hover:bg-white/10 text-slate-200 font-medium text-xs border border-white/15 transition">
                  Load Calibration Subject
                </button>
              </div>
            </div>

            <!-- Live Webcam Overlay with Frankfurt Horizontal Plane Crosshair Guide -->
            <div id="webcamContainer" class="hidden absolute inset-0 bg-black z-30 flex flex-col">
              <video id="webcamVideo" autoplay playsinline muted class="w-full h-full object-cover scale-x-[-1]"></video>
              <div class="absolute inset-0 pointer-events-none flex items-center justify-center">
                <svg class="w-full h-full" viewBox="0 0 400 500" preserveAspectRatio="none">
                  <defs>
                    <mask id="craniometricOvalMask">
                      <rect width="400" height="500" fill="white" />
                      <ellipse cx="200" cy="242" rx="116" ry="158" fill="black" />
                    </mask>
                  </defs>
                  <rect width="400" height="500" fill="rgba(7, 9, 13, 0.68)" mask="url(#craniometricOvalMask)" />
                  <!-- Craniometric Alignment Oval -->
                  <ellipse cx="200" cy="242" rx="116" ry="158" fill="none" stroke="#E2C275" stroke-width="2" stroke-dasharray="7 5" />
                  <!-- Midsagittal Vertical Axis -->
                  <line x1="200" y1="62" x2="200" y2="422" stroke="rgba(56, 189, 248, 0.55)" stroke-width="1" stroke-dasharray="4 4" />
                  <!-- Frankfurt Horizontal Plane Crosshair Guide -->
                  <line x1="55" y1="218" x2="345" y2="218" stroke="#38BDF8" stroke-width="1.2" stroke-dasharray="5 3" />
                  <text x="62" y="212" fill="#38BDF8" font-family="JetBrains Mono, monospace" font-size="8.5" letter-spacing="1">FRANKFURT PLANE 0°</text>
                  <!-- Subnasale & Menton Reference Ticks -->
                  <line x1="175" y1="295" x2="225" y2="295" stroke="rgba(226, 194, 117, 0.5)" stroke-width="1" />
                  <line x1="182" y1="398" x2="218" y2="398" stroke="rgba(226, 194, 117, 0.5)" stroke-width="1" />
                </svg>
                <span class="absolute top-3.5 px-3 py-1 rounded-full bg-[#07090D]/85 border border-[#E2C275]/40 text-[10px] font-mono tracking-wider text-[#F2DA9B]">
                  ALIGN PUPILS WITH FRANKFURT PLANE
                </span>
              </div>
              <div class="absolute bottom-4 inset-x-4 flex items-center justify-center gap-3 z-40">
                <button id="captureWebcamBtn" type="button" class="px-5 py-2.5 rounded-xl btn-champagne font-bold text-xs sm:text-sm flex items-center gap-2">
                  <span class="w-2.5 h-2.5 rounded-full bg-[#07090D]"></span>
                  Capture Frame
                </button>
                <button id="cancelWebcamBtn" type="button" class="px-4 py-2.5 rounded-xl bg-[#0D1118]/90 hover:bg-[#161D2B] text-slate-200 border border-white/15 text-xs sm:text-sm font-medium">
                  Cancel
                </button>
              </div>
            </div>

            <!-- Interactive HTML5 Craniometric Canvas -->
            <canvas id="craniometricCanvas" class="w-full h-full block cursor-crosshair"></canvas>

            <!-- Active Laser Diagnostic Sweep -->
            <div id="laserScanOverlay" class="hidden absolute inset-0 scan-tint z-20 pointer-events-none">
              <div class="laser-beam"></div>
              <div class="absolute bottom-3 inset-x-3 bg-[#07090D]/92 backdrop-blur-md border border-[#E2C275]/45 rounded-xl px-3.5 py-2.5 flex items-center justify-between gap-2">
                <div class="flex items-center gap-2.5">
                  <span class="w-2 h-2 rounded-full bg-[#38BDF8] animate-ping"></span>
                  <span id="scanStatusText" class="text-xs font-mono text-[#F2DA9B]">Triangulating gonial vertices...</span>
                </div>
                <span class="text-[10px] font-mono text-[#38BDF8] tracking-wider">GONION OPTICS</span>
              </div>
            </div>
          </div>

          <!-- Active Landmark Readout Bar -->
          <div class="flex items-center justify-between gap-2 text-[11px] text-slate-400">
            <span>Hover or drag any node for loupe precision.</span>
            <span id="activeNodeBadge" class="font-mono text-[#E2C275] truncate">12 Nodes Calibrated</span>
          </div>

          <!-- 4 Toggleable Biometric Vector Overlays -->
          <div class="space-y-2 pt-2 border-t border-[#E2C275]/15">
            <span class="text-[10px] font-mono uppercase tracking-[0.16em] text-slate-400 block">
              Biometric Vector Layers
            </span>
            <div class="grid grid-cols-2 gap-2">
              <button type="button" data-overlay="thirds" class="overlay-toggle active flex items-center justify-between px-3 py-2 rounded-xl text-xs font-medium border transition bg-[#E2C275]/15 border-[#E2C275]/45 text-[#F2DA9B]">
                <span>Facial Thirds</span>
                <span class="w-2 h-2 rounded-full bg-[#E2C275]"></span>
              </button>
              <button type="button" data-overlay="canthal" class="overlay-toggle active flex items-center justify-between px-3 py-2 rounded-xl text-xs font-medium border transition bg-[#38BDF8]/15 border-[#38BDF8]/45 text-sky-200">
                <span>Canthal Tilt &amp; IPD</span>
                <span class="w-2 h-2 rounded-full bg-[#38BDF8]"></span>
              </button>
              <button type="button" data-overlay="jaw" class="overlay-toggle active flex items-center justify-between px-3 py-2 rounded-xl text-xs font-medium border transition bg-[#E2C275]/15 border-[#E2C275]/45 text-[#F2DA9B]">
                <span>Zygomatic-to-Gonial</span>
                <span class="w-2 h-2 rounded-full bg-[#E2C275]"></span>
              </button>
              <button type="button" data-overlay="symmetry" class="overlay-toggle active flex items-center justify-between px-3 py-2 rounded-xl text-xs font-medium border transition bg-[#38BDF8]/15 border-[#38BDF8]/45 text-sky-200">
                <span>Midsagittal Symmetry</span>
                <span class="w-2 h-2 rounded-full bg-[#38BDF8]"></span>
              </button>
            </div>
          </div>
        </div>

        <!-- Live Craniometric Telemetry HUD -->
        <div class="luxury-panel rounded-2xl p-4 sm:p-5 space-y-3">
          <div class="flex items-center justify-between">
            <h3 class="text-[11px] font-mono uppercase tracking-[0.16em] text-[#E2C275]">
              Live Craniometric Telemetry HUD
            </h3>
            <span class="text-[10px] font-mono text-[#38BDF8]">REAL-TIME SYNC</span>
          </div>

          <div class="grid grid-cols-2 gap-2.5">
            <div class="luxury-subcard rounded-xl p-3">
              <div class="text-[10px] font-mono uppercase text-slate-400">Thirds Balance (Tr-G-Sn-Me)</div>
              <div id="metricThirds" class="text-xs sm:text-sm font-mono font-bold text-white mt-0.5">33 / 34 / 33%</div>
              <div id="metricThirdsStatus" class="text-[10px] text-[#E2C275] mt-0.5">96.8% Proportional</div>
            </div>

            <div class="luxury-subcard rounded-xl p-3">
              <div class="text-[10px] font-mono uppercase text-slate-400">Mean Canthal Tilt</div>
              <div id="metricCanthal" class="text-xs sm:text-sm font-mono font-bold text-[#38BDF8] mt-0.5">+4.8°</div>
              <div id="metricCanthalStatus" class="text-[10px] text-slate-400 mt-0.5">Positive Orbital Axis</div>
            </div>

            <div class="luxury-subcard rounded-xl p-3">
              <div class="text-[10px] font-mono uppercase text-slate-400">Bigonial / Bizygomatic</div>
              <div id="metricJawRatio" class="text-xs sm:text-sm font-mono font-bold text-white mt-0.5">0.79</div>
              <div id="metricJawStatus" class="text-[10px] text-[#E2C275] mt-0.5">Gonial Angle ~122°</div>
            </div>

            <div class="luxury-subcard rounded-xl p-3">
              <div class="text-[10px] font-mono uppercase text-slate-400">Bilateral Symmetry Index</div>
              <div id="metricSymmetry" class="text-xs sm:text-sm font-mono font-bold text-[#38BDF8] mt-0.5">95.4%</div>
              <div id="metricShape" class="text-[10px] text-slate-400 mt-0.5">Arch: Sculpted Oval</div>
            </div>
          </div>
        </div>
      </div>

      <!-- RIGHT COLUMN (7 cols): Diagnostic Parameters, AI Report & Gonion Consultant -->
      <div class="lg:col-span-7 space-y-6">

        <!-- Diagnostic Configuration & Primary CTA Panel -->
        <div class="luxury-panel rounded-2xl p-5 sm:p-6 space-y-5">
          <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-2">
            <div>
              <h2 class="font-display text-base sm:text-lg font-bold text-white tracking-tight">
                Diagnostic Calibration Parameters
              </h2>
              <p class="text-xs text-slate-400">
                Select structural reference baseline and primary optimization vector before scanning.
              </p>
            </div>
            <span class="text-[10px] font-mono px-2.5 py-1 rounded-md bg-[#E2C275]/10 text-[#E2C275] border border-[#E2C275]/25 self-start">
              OPTICAL INPUT READY
            </span>
          </div>

          <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
            <!-- Architectural Baseline -->
            <div class="space-y-2">
              <label class="text-[10px] font-mono uppercase tracking-[0.15em] text-slate-400 block">
                Architectural Baseline
              </label>
              <div id="baselineSelector" class="grid grid-cols-1 gap-1.5">
                <button type="button" data-value="Masculine Structure" class="pref-baseline active py-2 px-3 rounded-xl text-xs font-semibold border border-[#E2C275]/50 bg-[#E2C275]/15 text-[#F2DA9B] text-left flex items-center justify-between transition">
                  <span>Masculine Structure</span>
                  <span class="w-1.5 h-1.5 rounded-full bg-[#E2C275]"></span>
                </button>
                <button type="button" data-value="Feminine Structure" class="pref-baseline py-2 px-3 rounded-xl text-xs font-semibold border border-white/10 bg-white/5 text-slate-300 hover:bg-white/10 text-left flex items-center justify-between transition">
                  <span>Feminine Structure</span>
                  <span class="w-1.5 h-1.5 rounded-full bg-transparent"></span>
                </button>
                <button type="button" data-value="Balanced / Androgynous" class="pref-baseline py-2 px-3 rounded-xl text-xs font-semibold border border-white/10 bg-white/5 text-slate-300 hover:bg-white/10 text-left flex items-center justify-between transition">
                  <span>Balanced / Androgynous</span>
                  <span class="w-1.5 h-1.5 rounded-full bg-transparent"></span>
                </button>
              </div>
            </div>

            <!-- Primary Optimization Vector -->
            <div class="space-y-2 flex flex-col justify-between">
              <div class="space-y-2">
                <label for="vectorSelect" class="text-[10px] font-mono uppercase tracking-[0.15em] text-slate-400 block">
                  Primary Optimization Vector
                </label>
                <select id="vectorSelect" class="w-full py-2.5 px-3.5 rounded-xl bg-[#111622] border border-[#E2C275]/25 text-xs sm:text-sm text-white focus:outline-none focus:border-[#E2C275] transition">
                  <option value="Holistic Harmony">Holistic Harmony (Full Craniofacial Balance)</option>
                  <option value="Mandibular & Gonial Definition">Mandibular &amp; Gonial Definition</option>
                  <option value="Periorbital & Canthal Axis">Periorbital &amp; Canthal Axis</option>
                  <option value="Dermal Clarity & Contrast">Dermal Clarity &amp; Contrast</option>
                </select>
              </div>

              <div class="p-3 rounded-xl bg-[#0A0E15] border border-white/5 text-[11px] text-slate-400 leading-relaxed">
                <span class="text-[#38BDF8] font-mono font-semibold">NOTE:</span> Drag any of the 12 anatomical handles on the portrait to refine coordinates prior to executing diagnostic.
              </div>
            </div>
          </div>

          <!-- Primary CTA Button -->
          <button id="runDiagnosticBtn" type="button" class="w-full py-3.5 px-6 rounded-xl btn-champagne font-display font-bold text-sm sm:text-base tracking-[0.14em] uppercase flex items-center justify-center gap-2.5">
            <svg class="w-5 h-5" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2.2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" />
            </svg>
            <span id="runDiagnosticBtnText">RUN GONION DIAGNOSTIC</span>
          </button>
        </div>

        <!-- Pre-Scan Placeholder -->
        <div id="reportPlaceholder" class="luxury-panel rounded-2xl p-8 sm:p-10 text-center space-y-4 border-dashed border-[#E2C275]/25">
          <div class="w-14 h-14 rounded-2xl bg-[#E2C275]/10 border border-[#E2C275]/30 mx-auto flex items-center justify-center text-[#E2C275]">
            <svg class="w-7 h-7" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.6">
              <path stroke-linecap="round" stroke-linejoin="round" d="M11 3.055A9.001 9.001 0 1020.945 13H11V3.055z" />
              <path stroke-linecap="round" stroke-linejoin="round" d="M20.488 9H15V3.512A9.025 9.025 0 0120.488 9z" />
            </svg>
          </div>
          <div class="space-y-1.5 max-w-md mx-auto">
            <h3 class="font-display text-base sm:text-lg font-bold text-white">Awaiting Craniometric Scan</h3>
            <p class="text-xs text-slate-400 leading-relaxed">
              Click <span class="text-[#F2DA9B] font-semibold">Load Calibration Subject</span> or upload a front-facing portrait, verify the 12 anatomical nodes, and press <span class="text-[#E2C275] font-semibold">RUN GONION DIAGNOSTIC</span>.
            </p>
          </div>
        </div>

        <!-- FULL GONION DIAGNOSTIC REPORT (Revealed after scan) -->
        <div id="reportContainer" class="hidden space-y-6">

          <!-- 1. Gonion Aesthetic Index Card -->
          <div class="luxury-panel rounded-2xl p-5 sm:p-6 relative overflow-hidden">
            <div class="absolute -top-12 -right-12 w-64 h-64 bg-[#E2C275]/10 rounded-full blur-3xl pointer-events-none"></div>
            <div class="relative z-10 space-y-5">
              <div class="flex flex-wrap items-center justify-between gap-2 border-b border-white/10 pb-3">
                <div class="flex items-center gap-2">
                  <span class="w-2 h-2 rounded-full bg-[#E2C275]"></span>
                  <h3 class="font-display text-sm sm:text-base font-bold uppercase tracking-wider text-white">
                    Gonion Aesthetic Index
                  </h3>
                </div>
                <span id="analysisSourceBadge" class="text-[10px] font-mono px-2.5 py-1 rounded-md bg-[#38BDF8]/10 text-[#38BDF8] border border-[#38BDF8]/30">
                  GEMINI VISION + CRANIOMETRICS
                </span>
              </div>

              <div class="flex flex-col md:flex-row md:items-center justify-between gap-6">
                <!-- Dual Radial Gauges: Current Harmony vs Projected Softmaxxing Ceiling -->
                <div class="flex items-center justify-center sm:justify-start gap-4 sm:gap-6 shrink-0">
                  <!-- Current Harmony Score -->
                  <div class="text-center">
                    <div class="relative w-24 h-24 sm:w-28 sm:h-28 flex items-center justify-center">
                      <svg class="w-full h-full -rotate-90" viewBox="0 0 100 100">
                        <circle cx="50" cy="50" r="42" stroke="rgba(255,255,255,0.08)" stroke-width="7.5" fill="none" />
                        <circle id="currentScoreRing" cx="50" cy="50" r="42" stroke="#38BDF8" stroke-width="7.5" stroke-linecap="round" fill="none" stroke-dasharray="263.89" stroke-dashoffset="68" style="transition: stroke-dashoffset 0.9s ease;" />
                      </svg>
                      <div class="absolute inset-0 flex flex-col items-center justify-center">
                        <span id="currentRatingValue" class="text-2xl sm:text-3xl font-extrabold font-mono text-white">7.4</span>
                        <span class="text-[10px] font-mono text-slate-400">/ 10</span>
                      </div>
                    </div>
                    <span class="text-[10px] font-mono uppercase tracking-wider text-[#38BDF8] mt-1.5 block">Current Harmony</span>
                  </div>

                  <!-- Delta Indicator -->
                  <div class="flex flex-col items-center">
                    <span id="potentialDeltaBadge" class="px-2.5 py-1 rounded-full bg-[#E2C275]/15 border border-[#E2C275]/40 text-[#F2DA9B] font-mono text-xs font-bold">
                      +1.2
                    </span>
                    <svg class="w-5 h-5 text-slate-500 my-1" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                      <path stroke-linecap="round" stroke-linejoin="round" d="M14 5l7 7m0 0l-7 7m7-7H3" />
                    </svg>
                    <span class="text-[9px] font-mono tracking-widest text-slate-500">CEILING</span>
                  </div>

                  <!-- Projected Softmaxxing Ceiling -->
                  <div class="text-center">
                    <div class="relative w-24 h-24 sm:w-28 sm:h-28 flex items-center justify-center">
                      <svg class="w-full h-full -rotate-90" viewBox="0 0 100 100">
                        <circle cx="50" cy="50" r="42" stroke="rgba(255,255,255,0.08)" stroke-width="7.5" fill="none" />
                        <circle id="potentialScoreRing" cx="50" cy="50" r="42" stroke="#E2C275" stroke-width="7.5" stroke-linecap="round" fill="none" stroke-dasharray="263.89" stroke-dashoffset="36" style="transition: stroke-dashoffset 0.9s ease;" />
                      </svg>
                      <div class="absolute inset-0 flex flex-col items-center justify-center">
                        <span id="potentialRatingValue" class="text-2xl sm:text-3xl font-extrabold font-mono text-[#F2DA9B]">8.6</span>
                        <span class="text-[10px] font-mono text-slate-400">/ 10</span>
                      </div>
                    </div>
                    <span class="text-[10px] font-mono uppercase tracking-wider text-[#E2C275] mt-1.5 block">Softmaxxing Ceiling</span>
                  </div>
                </div>

                <!-- Structural Classification Pills & Executive Summary -->
                <div class="flex-1 space-y-3">
                  <div class="grid grid-cols-1 sm:grid-cols-3 gap-2">
                    <div class="luxury-subcard rounded-xl px-3 py-2">
                      <span class="text-[9px] font-mono uppercase text-slate-400 block">Face Architecture</span>
                      <span id="detectedFaceShape" class="text-xs font-semibold text-white">Sculpted Oval</span>
                    </div>
                    <div class="luxury-subcard rounded-xl px-3 py-2">
                      <span class="text-[9px] font-mono uppercase text-slate-400 block">Contrast Tier</span>
                      <span id="detectedContrast" class="text-xs font-semibold text-[#F2DA9B]">High Contrast</span>
                    </div>
                    <div class="luxury-subcard rounded-xl px-3 py-2">
                      <span class="text-[9px] font-mono uppercase text-slate-400 block">Key Strength</span>
                      <span id="detectedKeyStrength" class="text-xs font-semibold text-[#38BDF8]">Canthal Vector</span>
                    </div>
                  </div>

                  <!-- Comparative Linear Trajectory Bar -->
                  <div class="space-y-1">
                    <div class="flex justify-between text-[10px] font-mono text-slate-400">
                      <span>BASELINE HARMONY</span>
                      <span>OPTIMIZED POTENTIAL</span>
                    </div>
                    <div class="w-full h-2 rounded-full bg-white/10 overflow-hidden relative">
                      <div id="ceilingLinearBar" class="absolute inset-y-0 left-0 bg-[#E2C275]/45 rounded-full transition-all duration-700" style="width: 86%"></div>
                      <div id="currentLinearBar" class="absolute inset-y-0 left-0 bg-gradient-to-r from-[#38BDF8] to-[#E2C275] rounded-full transition-all duration-700" style="width: 74%"></div>
                    </div>
                  </div>

                  <p id="executiveSummaryText" class="text-xs sm:text-sm text-slate-300 leading-relaxed">
                    Balanced craniometric thirds and a positive lateral canthal axis establish a strong architectural baseline.
                  </p>
                </div>
              </div>
            </div>
          </div>

          <!-- 2. 5 Craniometric & Feature Breakdown Cards -->
          <div class="luxury-panel rounded-2xl p-5 sm:p-6 space-y-4">
            <div class="flex items-center justify-between">
              <h3 class="font-display text-sm sm:text-base font-bold text-white flex items-center gap-2">
                <span class="w-2 h-2 rounded-full bg-[#38BDF8]"></span>
                Craniometric &amp; Feature Breakdown
              </h3>
              <span class="text-[10px] font-mono text-slate-400 tracking-wider">5 ANATOMICAL ZONES</span>
            </div>
            <div id="featureBreakdownList" class="grid grid-cols-1 gap-3.5">
              <!-- Populated dynamically -->
            </div>
          </div>

          <!-- 3. 4-Tab Actionable Softmaxxing Protocol -->
          <div class="luxury-panel rounded-2xl p-5 sm:p-6 space-y-4">
            <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-3">
              <div>
                <h3 class="font-display text-sm sm:text-base font-bold text-white flex items-center gap-2">
                  <span class="w-2 h-2 rounded-full bg-[#E2C275]"></span>
                  Personalized Softmaxxing Protocol
                </h3>
                <p class="text-xs text-slate-400">
                  Evidence-based, non-invasive grooming, myofunctional, dermal, and framing specs.
                </p>
              </div>
              <button id="copyProtocolBtn" type="button" class="self-start sm:self-auto px-3.5 py-2 rounded-xl bg-[#E2C275]/12 hover:bg-[#E2C275]/22 border border-[#E2C275]/35 text-xs font-mono font-semibold text-[#F2DA9B] flex items-center gap-1.5 transition">
                <svg class="w-3.5 h-3.5" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M8 16H6a2 2 0 01-2-2V6a2 2 0 012-2h8a2 2 0 012 2v2m-6 12h8a2 2 0 002-2v-8a2 2 0 00-2-2h-8a2 2 0 00-2 2v8a2 2 0 002 2z" />
                </svg>
                Copy Full Protocol
              </button>
            </div>

            <!-- 4 Protocol Category Tabs -->
            <div class="flex flex-wrap gap-2 border-b border-white/10 pb-3" role="tablist">
              <button type="button" data-tab="gonial" class="plan-tab active px-3.5 py-2 rounded-xl text-xs font-semibold bg-[#E2C275]/20 text-[#F2DA9B] border border-[#E2C275]/45 transition">
                Gonial &amp; Jawline
              </button>
              <button type="button" data-tab="periorbital" class="plan-tab px-3.5 py-2 rounded-xl text-xs font-semibold bg-white/5 text-slate-300 border border-white/10 hover:bg-white/10 transition">
                Periorbital &amp; Brow
              </button>
              <button type="button" data-tab="dermal" class="plan-tab px-3.5 py-2 rounded-xl text-xs font-semibold bg-white/5 text-slate-300 border border-white/10 hover:bg-white/10 transition">
                Dermal &amp; Contrast
              </button>
              <button type="button" data-tab="framing" class="plan-tab px-3.5 py-2 rounded-xl text-xs font-semibold bg-white/5 text-slate-300 border border-white/10 hover:bg-white/10 transition">
                Hair &amp; Structural Framing
              </button>
            </div>

            <!-- Active Tab Cards -->
            <div id="planTabContent" class="space-y-3">
              <!-- Populated dynamically -->
            </div>
          </div>

          <!-- 4. Context-Aware Gonion AI Consultant Chat -->
          <div class="luxury-panel rounded-2xl p-5 sm:p-6 space-y-4">
            <div class="flex items-center justify-between gap-2">
              <div class="flex items-center gap-3">
                <div class="w-9 h-9 rounded-xl bg-[#E2C275]/15 border border-[#E2C275]/35 flex items-center justify-center text-[#E2C275]">
                  <svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M8 10h.01M12 10h.01M16 10h.01M9 16H5a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v8a2 2 0 01-2 2h-5l-5 5v-5z" />
                  </svg>
                </div>
                <div>
                  <h3 class="font-display text-sm sm:text-base font-bold tracking-wide text-white">
                    GONION CONSULTANT // DIRECT ADVISORY
                  </h3>
                  <p class="text-[11px] text-slate-400">
                    Synced with your 12-point craniometric telemetry &amp; diagnostic report
                  </p>
                </div>
              </div>
              <span class="text-[10px] font-mono px-2.5 py-1 rounded-md bg-[#38BDF8]/10 text-[#38BDF8] border border-[#38BDF8]/30">
                ACTIVE
              </span>
            </div>

            <!-- Quick-Ask Prompt Chips -->
            <div class="flex flex-wrap gap-2">
              <button type="button" class="quick-prompt text-[11px] px-3 py-1.5 rounded-full bg-white/5 hover:bg-[#E2C275]/15 text-slate-300 hover:text-[#F2DA9B] border border-white/10 hover:border-[#E2C275]/40 transition">
                Best haircut for my bigonial ratio?
              </button>
              <button type="button" class="quick-prompt text-[11px] px-3 py-1.5 rounded-full bg-white/5 hover:bg-[#E2C275]/15 text-slate-300 hover:text-[#F2DA9B] border border-white/10 hover:border-[#E2C275]/40 transition">
                How to sharpen gonial definition naturally?
              </button>
              <button type="button" class="quick-prompt text-[11px] px-3 py-1.5 rounded-full bg-white/5 hover:bg-[#E2C275]/15 text-slate-300 hover:text-[#F2DA9B] border border-white/10 hover:border-[#E2C275]/40 transition">
                Optimize my facial contrast
              </button>
            </div>

            <!-- Conversation Feed -->
            <div id="coachChatLog" class="max-h-72 overflow-y-auto space-y-3 pr-1">
              <div class="bg-[#121824] border border-[#E2C275]/20 rounded-2xl rounded-tl-sm p-3.5 text-xs sm:text-sm text-slate-200 leading-relaxed">
                Telemetry locked. Ask for exact barber guard tapers, myofunctional posture cues, skincare actives, or eyewear geometry calibrated to your <span id="coachFaceShapeMention" class="text-[#F2DA9B] font-semibold">craniometric profile</span>.
              </div>
            </div>

            <!-- Consultant Input Form -->
            <form id="coachChatForm" class="flex items-center gap-2 pt-1">
              <input id="coachChatInput" type="text" placeholder="Consult Gonion Advisory..." class="flex-1 bg-[#0B0F17] border border-[#E2C275]/25 focus:border-[#E2C275] rounded-xl px-4 py-3 text-xs sm:text-sm text-white placeholder-slate-500 focus:outline-none transition" />
              <button id="coachSendBtn" type="submit" class="px-4 py-3 rounded-xl btn-champagne font-bold text-xs sm:text-sm flex items-center gap-1.5 shrink-0">
                <span>Send</span>
                <svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2.2">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M13 5l7 7-7 7M5 5l7 7-7 7" />
                </svg>
              </button>
            </form>
          </div>

        </div>
      </div>
    </div>
  </main>

  <!-- Discreet Grounded Ethical Footer -->
  <footer class="border-t border-[#E2C275]/15 py-5 px-4 sm:px-6 text-center space-y-1">
    <p class="text-xs font-mono tracking-wider text-slate-400">
      GONION // PRECISION CRANIOMETRIC AESTHETICS &amp; SOFTMAXXING ENGINE
    </p>
    <p class="text-[11px] text-slate-500 max-w-2xl mx-auto">
      Advisory Note: Designed exclusively for healthy, sustainable, non-invasive grooming, skincare, posture, and styling optimization. All optical imagery remains ephemeral within your browser session.
    </p>
  </footer>

  <!-- Self-Contained Craniometric Engine & Gemini AI Integration -->
  <script>
    /**
     * ============================================================================
     * GONION // Precision Craniometric Aesthetics & Softmaxxing Engine
     * ============================================================================
     */

    const apiKey = "";
    const GEMINI_MODEL = "gemini-3-flash-preview";

    // Central Application State
    const appState = {
      imageLoaded: false,
      sourceImage: null,
      baseline: "Masculine Structure",
      vector: "Holistic Harmony",
      overlays: {
        thirds: true,
        canthal: true,
        jaw: true,
        symmetry: true,
      },
      landmarks: {},
      hoveredNode: null,
      draggingNode: null,
      pointerCanvasPos: null,
      metrics: {
        thirds: [33, 34, 33],
        thirdsScore: 96.8,
        canthalTiltDeg: 4.8,
        ipdRatio: 0.46,
        jawToCheekRatio: 0.79,
        gonialAngleDeg: 122,
        goldenRatioScore: 92.1,
        symmetryScore: 95.4,
        estimatedShape: "Sculpted Oval",
      },
      currentReport: null,
      activePlanTab: "gonial",
      chatHistory: [],
      webcamStream: null,
      imageDrawRect: { x: 0, y: 0, w: 0, h: 0 },
    };

    // 12 Anatomical Craniometric Landmarks (Normalized [0..1])
    const DEFAULT_LANDMARKS = {
      trichion:            { x: 0.50, y: 0.165, code: "Tr", name: "Trichion (Hairline)", color: "#E2C275" },
      glabella:            { x: 0.50, y: 0.365, code: "G",  name: "Glabella (Brow)", color: "#E2C275" },
      subnasale:           { x: 0.50, y: 0.575, code: "Sn", name: "Subnasale (Nose Base)", color: "#E2C275" },
      menton:              { x: 0.50, y: 0.815, code: "Me", name: "Menton (Chin Tip)", color: "#E2C275" },
      leftZygion:          { x: 0.265, y: 0.515, code: "Zy-L", name: "Left Zygion (Cheekbone)", color: "#F2DA9B" },
      rightZygion:         { x: 0.735, y: 0.515, code: "Zy-R", name: "Right Zygion (Cheekbone)", color: "#F2DA9B" },
      leftGonion:          { x: 0.315, y: 0.695, code: "Go-L", name: "Left Gonion (Jaw Angle)", color: "#E2C275" },
      rightGonion:         { x: 0.685, y: 0.695, code: "Go-R", name: "Right Gonion (Jaw Angle)", color: "#E2C275" },
      leftLateralCanthus:  { x: 0.325, y: 0.410, code: "Ex-L", name: "Left Lateral Canthus", color: "#38BDF8" },
      leftMedialCanthus:   { x: 0.430, y: 0.422, code: "En-L", name: "Left Medial Canthus", color: "#38BDF8" },
      rightMedialCanthus:  { x: 0.570, y: 0.422, code: "En-R", name: "Right Medial Canthus", color: "#38BDF8" },
      rightLateralCanthus: { x: 0.675, y: 0.410, code: "Ex-R", name: "Right Lateral Canthus", color: "#38BDF8" },
    };

    // DOM Element References
    const canvas = document.getElementById("craniometricCanvas");
    const ctx = canvas.getContext("2d");
    const emptyUploadState = document.getElementById("emptyUploadState");
    const webcamContainer = document.getElementById("webcamContainer");
    const webcamVideo = document.getElementById("webcamVideo");
    const laserScanOverlay = document.getElementById("laserScanOverlay");
    const scanStatusText = document.getElementById("scanStatusText");

    /**
     * Non-Blocking Toast Banner
     */
    function showToast(message, type = "gold") {
      const container = document.getElementById("toastContainer");
      const toast = document.createElement("div");
      const palette = {
        gold: "bg-[#0D1118]/95 border-[#E2C275]/45 text-[#F2DA9B]",
        cyan: "bg-[#0D1118]/95 border-[#38BDF8]/45 text-sky-200",
        warn: "bg-[#0D1118]/95 border-amber-500/45 text-amber-200",
        err:  "bg-[#0D1118]/95 border-rose-500/45 text-rose-200",
      };
      toast.className = `pointer-events-auto px-4 py-3 rounded-xl border backdrop-blur-md shadow-2xl text-xs font-medium flex items-center justify-between gap-3 transition-all duration-300 ${palette[type] || palette.gold}`;
      toast.innerHTML = `<span>${message}</span><button type="button" class="text-white/60 hover:text-white text-sm leading-none">&times;</button>`;
      toast.querySelector("button").addEventListener("click", () => toast.remove());
      container.appendChild(toast);
      setTimeout(() => {
        toast.style.opacity = "0";
        setTimeout(() => toast.remove(), 300);
      }, 4200);
    }

    /**
     * Reset 12 Craniometric Landmarks to Default Coordinates
     */
    function resetLandmarks() {
      appState.landmarks = JSON.parse(JSON.stringify(DEFAULT_LANDMARKS));
      computeCraniometricMetrics();
      renderCraniometricCanvas();
    }

    /**
     * Responsive High-DPI Canvas Sizing
     */
    function resizeCanvas() {
      const rect = canvas.parentElement.getBoundingClientRect();
      const dpr = Math.min(window.devicePixelRatio || 1, 2);
      canvas.width = Math.max(300, Math.floor(rect.width * dpr));
      canvas.height = Math.max(375, Math.floor(rect.height * dpr));
      ctx.setTransform(dpr, 0, 0, dpr, 0, 0);
      renderCraniometricCanvas();
    }

    /**
     * Render High-Detail Sculpted Chiaroscuro Calibration Subject Portrait
     */
    function loadCalibrationSubject() {
      stopWebcam();
      const offscreen = document.createElement("canvas");
      offscreen.width = 640;
      offscreen.height = 800;
      const octx = offscreen.getContext("2d");

      // Deep obsidian studio backdrop with champagne & ice-cyan rim glow
      const bgGrad = octx.createRadialGradient(320, 340, 30, 320, 400, 490);
      bgGrad.addColorStop(0, "#1B2230");
      bgGrad.addColorStop(0.58, "#0D1119");
      bgGrad.addColorStop(1, "#05070B");
      octx.fillStyle = bgGrad;
      octx.fillRect(0, 0, 640, 800);

      const goldRim = octx.createRadialGradient(320, 355, 135, 320, 355, 315);
      goldRim.addColorStop(0, "rgba(226, 194, 117, 0.14)");
      goldRim.addColorStop(1, "rgba(226, 194, 117, 0)");
      octx.fillStyle = goldRim;
      octx.fillRect(0, 0, 640, 800);

      // Shoulders & Tailored Dark Mock-Neck Silhouette
      octx.fillStyle = "#0F141E";
      octx.beginPath();
      octx.moveTo(85, 800);
      octx.quadraticCurveTo(125, 670, 244, 650);
      octx.lineTo(396, 650);
      octx.quadraticCurveTo(515, 670, 555, 800);
      octx.closePath();
      octx.fill();

      // Neck with anatomical sternocleidomastoid sculpting
      const neckGrad = octx.createLinearGradient(252, 540, 388, 540);
      neckGrad.addColorStop(0, "#A9785D");
      neckGrad.addColorStop(0.5, "#D6A387");
      neckGrad.addColorStop(1, "#9E6E54");
      octx.fillStyle = neckGrad;
      octx.beginPath();
      octx.moveTo(254, 535);
      octx.lineTo(245, 675);
      octx.quadraticCurveTo(320, 706, 395, 675);
      octx.lineTo(386, 535);
      octx.closePath();
      octx.fill();

      // Submental shadow under mandibular border
      octx.fillStyle = "rgba(45, 25, 18, 0.44)";
      octx.beginPath();
      octx.ellipse(320, 644, 76, 26, 0, 0, Math.PI * 2);
      octx.fill();

      // Ears
      octx.fillStyle = "#C08D70";
      octx.beginPath();
      octx.ellipse(164, 404, 15, 42, -0.07, 0, Math.PI * 2);
      octx.ellipse(476, 404, 15, 42, 0.07, 0, Math.PI * 2);
      octx.fill();

      // Sculpted Craniofacial Contour with Defined Zygomatic & Gonial Angles
      const faceGrad = octx.createRadialGradient(320, 380, 35, 320, 415, 228);
      faceGrad.addColorStop(0, "#EBC1A8");
      faceGrad.addColorStop(0.62, "#D29D80");
      faceGrad.addColorStop(1, "#AE785B");
      octx.fillStyle = faceGrad;
      octx.beginPath();
      octx.moveTo(320, 126);
      octx.bezierCurveTo(426, 126, 474, 218, 470, 368); // Right zygion arch
      octx.bezierCurveTo(466, 442, 454, 508, 438, 556); // Right gonion vertex
      octx.quadraticCurveTo(384, 636, 320, 652); // Menton
      octx.quadraticCurveTo(256, 636, 202, 556); // Left gonion vertex
      octx.bezierCurveTo(186, 508, 174, 442, 170, 368); // Left zygion arch
      octx.bezierCurveTo(166, 218, 214, 126, 320, 126);
      octx.closePath();
      octx.fill();

      // Chiaroscuro Buccal & Sub-Zygomatic Contour Shading
      octx.fillStyle = "rgba(115, 70, 50, 0.19)";
      octx.beginPath();
      octx.ellipse(214, 476, 23, 54, 0.24, 0, Math.PI * 2);
      octx.ellipse(426, 476, 23, 54, -0.24, 0, Math.PI * 2);
      octx.fill();

      // Forehead, Zygomatic & Nasal Bridge Specular Highlights
      octx.fillStyle = "rgba(255, 240, 228, 0.24)";
      octx.beginPath();
      octx.ellipse(320, 232, 66, 38, 0, 0, Math.PI * 2);
      octx.ellipse(234, 412, 22, 14, -0.3, 0, Math.PI * 2);
      octx.ellipse(406, 412, 22, 14, 0.3, 0, Math.PI * 2);
      octx.fill();

      // Architectural Textured Hair Framing
      octx.fillStyle = "#14161B";
      octx.beginPath();
      octx.moveTo(166, 344);
      octx.bezierCurveTo(152, 208, 198, 92, 320, 88);
      octx.bezierCurveTo(442, 92, 488, 208, 474, 344);
      octx.bezierCurveTo(464, 246, 444, 172, 404, 146);
      octx.quadraticCurveTo(320, 130, 236, 146);
      octx.bezierCurveTo(196, 172, 176, 246, 166, 344);
      octx.closePath();
      octx.fill();

      // Low-Set Horizontal Eyebrows
      octx.fillStyle = "#1B1A1E";
      octx.beginPath();
      octx.moveTo(202, 300);
      octx.quadraticCurveTo(244, 287, 286, 299);
      octx.lineTo(283, 312);
      octx.quadraticCurveTo(244, 301, 202, 309);
      octx.closePath();
      octx.fill();

      octx.beginPath();
      octx.moveTo(438, 300);
      octx.quadraticCurveTo(396, 287, 354, 299);
      octx.lineTo(357, 312);
      octx.quadraticCurveTo(396, 301, 438, 309);
      octx.closePath();
      octx.fill();

      // Helper for Almond Eyes with Positive Canthal Vector
      function drawCalibrationEye(outerX, outerY, innerX, innerY) {
        const midX = (outerX + innerX) / 2;
        const midY = (outerY + innerY) / 2;
        octx.fillStyle = "#F8FAFC";
        octx.beginPath();
        octx.moveTo(outerX, outerY);
        octx.quadraticCurveTo(midX, midY - 13, innerX, innerY);
        octx.quadraticCurveTo(midX, midY + 12, outerX, outerY);
        octx.closePath();
        octx.fill();

        octx.fillStyle = "#2E3A48";
        octx.beginPath();
        octx.arc(midX, midY, 10, 0, Math.PI * 2);
        octx.fill();

        octx.fillStyle = "#07090D";
        octx.beginPath();
        octx.arc(midX, midY, 4.8, 0, Math.PI * 2);
        octx.fill();

        octx.fillStyle = "#FFFFFF";
        octx.beginPath();
        octx.arc(midX - 3, midY - 2.8, 2.1, 0, Math.PI * 2);
        octx.fill();

        octx.strokeStyle = "#14161B";
        octx.lineWidth = 2.6;
        octx.beginPath();
        octx.moveTo(outerX, outerY);
        octx.quadraticCurveTo(midX, midY - 13.5, innerX, innerY);
        octx.stroke();
      }

      drawCalibrationEye(208, 328, 275, 338);
      drawCalibrationEye(432, 328, 365, 338);

      // Nasal Dorsum & Alar Base
      octx.strokeStyle = "rgba(128, 78, 56, 0.36)";
      octx.lineWidth = 2.2;
      octx.beginPath();
      octx.moveTo(308, 342);
      octx.lineTo(304, 444);
      octx.moveTo(332, 342);
      octx.lineTo(336, 444);
      octx.stroke();

      octx.fillStyle = "rgba(120, 72, 52, 0.36)";
      octx.beginPath();
      octx.ellipse(320, 462, 25, 8.5, 0, 0, Math.PI * 2);
      octx.fill();
      octx.fillStyle = "rgba(255, 238, 224, 0.34)";
      octx.beginPath();
      octx.arc(320, 450, 8.5, 0, Math.PI * 2);
      octx.fill();

      // Lips
      octx.fillStyle = "#AE6860";
      octx.beginPath();
      octx.moveTo(275, 520);
      octx.quadraticCurveTo(304, 507, 320, 512);
      octx.quadraticCurveTo(336, 507, 365, 520);
      octx.quadraticCurveTo(320, 524, 275, 520);
      octx.closePath();
      octx.fill();

      octx.fillStyle = "#BF786F";
      octx.beginPath();
      octx.moveTo(277, 520);
      octx.quadraticCurveTo(320, 545, 363, 520);
      octx.quadraticCurveTo(320, 525, 277, 520);
      octx.closePath();
      octx.fill();

      appState.sourceImage = offscreen;
      appState.imageLoaded = true;
      emptyUploadState.classList.add("hidden");
      resetLandmarks();
      showToast("Calibration Subject loaded. Fine-tune any of the 12 landmarks or run diagnostic.", "gold");
    }

    /**
     * Handle File Picker / Drag-and-Drop Image Upload
     */
    function handleImageFile(file) {
      if (!file || !file.type.startsWith("image/")) {
        showToast("Please upload a valid JPG, PNG, or WebP portrait.", "warn");
        return;
      }
      stopWebcam();
      const reader = new FileReader();
      reader.onload = (event) => {
        const img = new Image();
        img.onload = () => {
          appState.sourceImage = img;
          appState.imageLoaded = true;
          emptyUploadState.classList.add("hidden");
          resetLandmarks();
          showToast("Portrait loaded. Align craniometric nodes and run diagnostic.", "gold");
        };
        img.onerror = () => showToast("Unable to decode image file.", "err");
        img.src = event.target.result;
      };
      reader.readAsDataURL(file);
    }

    /**
     * Live Optical Webcam Capture
     */
    async function startWebcam() {
      try {
        const stream = await navigator.mediaDevices.getUserMedia({
          video: { facingMode: "user", width: { ideal: 720 }, height: { ideal: 900 } },
          audio: false,
        });
        appState.webcamStream = stream;
        webcamVideo.srcObject = stream;
        webcamContainer.classList.remove("hidden");
      } catch (err) {
        showToast("Optical camera unavailable. Upload a file or load Calibration Subject.", "warn");
      }
    }

    function stopWebcam() {
      if (appState.webcamStream) {
        appState.webcamStream.getTracks().forEach((t) => t.stop());
        appState.webcamStream = null;
      }
      webcamContainer.classList.add("hidden");
    }

    function captureWebcamFrame() {
      if (!webcamVideo.videoWidth) return;
      const cap = document.createElement("canvas");
      cap.width = webcamVideo.videoWidth;
      cap.height = webcamVideo.videoHeight;
      const cctx = cap.getContext("2d");
      cctx.translate(cap.width, 0);
      cctx.scale(-1, 1);
      cctx.drawImage(webcamVideo, 0, 0);

      stopWebcam();
      appState.sourceImage = cap;
      appState.imageLoaded = true;
      emptyUploadState.classList.add("hidden");
      resetLandmarks();
      showToast("Optical frame captured. Verify 12 landmarks before running diagnostic.", "gold");
    }

    /**
     * Compute Exact Craniometric Ratios from the 12 Landmark Nodes
     */
    function computeCraniometricMetrics() {
      const lm = appState.landmarks;
      if (!lm.trichion) return;

      // 1. Facial Thirds (Upper: Tr->G, Middle: G->Sn, Lower: Sn->Me)
      const upper = Math.max(0.01, lm.glabella.y - lm.trichion.y);
      const middle = Math.max(0.01, lm.subnasale.y - lm.glabella.y);
      const lower = Math.max(0.01, lm.menton.y - lm.subnasale.y);
      const totalH = upper + middle + lower;

      const pUpper = Math.round((upper / totalH) * 100);
      const pMiddle = Math.round((middle / totalH) * 100);
      const pLower = Math.max(1, 100 - pUpper - pMiddle);

      const thirdsDeviation = (Math.abs(pUpper - 33.3) + Math.abs(pMiddle - 33.3) + Math.abs(pLower - 33.3)) / 3;
      const thirdsScore = Number(Math.max(62, Math.min(99.5, 100 - thirdsDeviation * 2.1)).toFixed(1));

      // 2. Mean Canthal Tilt (degrees) & Interpupillary / Bizygomatic Spacing
      const lDx = Math.max(0.005, lm.leftMedialCanthus.x - lm.leftLateralCanthus.x);
      const lDy = lm.leftMedialCanthus.y - lm.leftLateralCanthus.y;
      const lTilt = (Math.atan2(lDy, lDx) * 180) / Math.PI;

      const rDx = Math.max(0.005, lm.rightLateralCanthus.x - lm.rightMedialCanthus.x);
      const rDy = lm.rightMedialCanthus.y - lm.rightLateralCanthus.y;
      const rTilt = (Math.atan2(rDy, rDx) * 180) / Math.PI;

      const meanTilt = Number(((lTilt + rTilt) / 2).toFixed(1));

      const leftPupilX = (lm.leftLateralCanthus.x + lm.leftMedialCanthus.x) / 2;
      const rightPupilX = (lm.rightMedialCanthus.x + lm.rightLateralCanthus.x) / 2;
      const ipdSpan = Math.abs(rightPupilX - leftPupilX);

      // 3. Bigonial (Go-Go) to Bizygomatic (Zy-Zy) Ratio & Projected Gonial Angle
      const bizygomaticW = Math.max(0.05, Math.abs(lm.rightZygion.x - lm.leftZygion.x));
      const bigonialW = Math.max(0.03, Math.abs(lm.rightGonion.x - lm.leftGonion.x));
      const jawRatio = Number((bigonialW / bizygomaticW).toFixed(2));
      const ipdRatio = Number((ipdSpan / bizygomaticW).toFixed(2));

      // Estimate 2D projected gonial angle (ramus vector Zy->Go vs mandibular body Go->Me)
      const v1x = lm.leftZygion.x - lm.leftGonion.x;
      const v1y = lm.leftZygion.y - lm.leftGonion.y;
      const v2x = lm.menton.x - lm.leftGonion.x;
      const v2y = lm.menton.y - lm.leftGonion.y;
      const dot = v1x * v2x + v1y * v2y;
      const mag = Math.max(0.0001, Math.hypot(v1x, v1y) * Math.hypot(v2x, v2y));
      const gonialAngleDeg = Math.round((Math.acos(Math.max(-1, Math.min(1, dot / mag))) * 180) / Math.PI);

      // 4. Golden Ratio Phi (1.618) Index
      const actualLW = totalH / bizygomaticW;
      const phiDiff = Math.abs(actualLW - 1.618) / 1.618;
      const goldenRatioScore = Number(Math.max(66, Math.min(99.3, (1 - phiDiff * 0.85) * 100)).toFixed(1));

      // 5. Midsagittal Bilateral Symmetry Index
      const midX = (lm.trichion.x + lm.glabella.x + lm.subnasale.x + lm.menton.x) / 4;
      const zyAsym = Math.abs((midX - lm.leftZygion.x) - (lm.rightZygion.x - midX));
      const goAsym = Math.abs((midX - lm.leftGonion.x) - (lm.rightGonion.x - midX));
      const exAsym = Math.abs((midX - lm.leftLateralCanthus.x) - (lm.rightLateralCanthus.x - midX));
      const asymPenalty = (zyAsym + goAsym + exAsym) * 100;
      const symmetryScore = Number(Math.max(70, Math.min(99.5, 100 - asymPenalty * 1.35)).toFixed(1));

      // 6. Face Architecture Classification
      let shape = "Sculpted Oval";
      if (jawRatio >= 0.87 && actualLW < 1.48) shape = "Angular Square";
      else if (jawRatio <= 0.72 && pUpper >= 34) shape = "Tapered Heart";
      else if (jawRatio <= 0.75 && bizygomaticW > 0.44) shape = "Chiseled Diamond";
      else if (actualLW >= 1.68) shape = "Elongated Oblong";
      else if (actualLW <= 1.36 && jawRatio < 0.84) shape = "Soft Round";

      appState.metrics = {
        thirds: [pUpper, pMiddle, pLower],
        thirdsScore,
        canthalTiltDeg: meanTilt,
        ipdRatio,
        jawToCheekRatio: jawRatio,
        gonialAngleDeg,
        goldenRatioScore,
        symmetryScore,
        estimatedShape: shape,
      };

      // Update Live Craniometric Telemetry HUD
      document.getElementById("metricThirds").textContent = `${pUpper} / ${pMiddle} / ${pLower}%`;
      document.getElementById("metricThirdsStatus").textContent = `${thirdsScore}% Proportional`;

      const sign = meanTilt > 0 ? "+" : "";
      document.getElementById("metricCanthal").textContent = `${sign}${meanTilt}°`;
      document.getElementById("metricCanthalStatus").textContent =
        meanTilt >= 2 ? `Positive • IPD ${ipdRatio}` : meanTilt >= -1 ? `Neutral • IPD ${ipdRatio}` : `Negative • IPD ${ipdRatio}`;

      document.getElementById("metricJawRatio").textContent = jawRatio.toFixed(2);
      document.getElementById("metricJawStatus").textContent = `Gonial Angle ~${gonialAngleDeg}°`;

      document.getElementById("metricSymmetry").textContent = `${symmetryScore}%`;
      document.getElementById("metricShape").textContent = `Arch: ${shape}`;
    }

    /**
     * Render Interactive 12-Point Craniometric Canvas + Overlays + Magnifier Loupe
     */
    function renderCraniometricCanvas() {
      const rect = canvas.parentElement.getBoundingClientRect();
      const cw = rect.width;
      const ch = rect.height;

      ctx.clearRect(0, 0, cw, ch);
      if (!appState.imageLoaded || !appState.sourceImage) return;

      const img = appState.sourceImage;
      const iw = img.width || img.naturalWidth;
      const ih = img.height || img.naturalHeight;

      const scale = Math.min(cw / iw, ch / ih);
      const drawW = iw * scale;
      const drawH = ih * scale;
      const drawX = (cw - drawW) / 2;
      const drawY = (ch - drawH) / 2;
      appState.imageDrawRect = { x: drawX, y: drawY, w: drawW, h: drawH };

      // Draw Portrait
      ctx.drawImage(img, drawX, drawY, drawW, drawH);

      // Luxury Optical Vignette
      const vig = ctx.createRadialGradient(cw / 2, ch / 2, drawW * 0.32, cw / 2, ch / 2, Math.max(cw, ch) * 0.72);
      vig.addColorStop(0, "rgba(7, 9, 13, 0)");
      vig.addColorStop(1, "rgba(7, 9, 13, 0.42)");
      ctx.fillStyle = vig;
      ctx.fillRect(0, 0, cw, ch);

      const toPx = (pt) => ({
        x: drawX + pt.x * drawW,
        y: drawY + pt.y * drawH,
      });

      const lm = appState.landmarks;
      const pTr = toPx(lm.trichion);
      const pGl = toPx(lm.glabella);
      const pSn = toPx(lm.subnasale);
      const pMe = toPx(lm.menton);
      const pZyL = toPx(lm.leftZygion);
      const pZyR = toPx(lm.rightZygion);
      const pGoL = toPx(lm.leftGonion);
      const pGoR = toPx(lm.rightGonion);
      const pExL = toPx(lm.leftLateralCanthus);
      const pEnL = toPx(lm.leftMedialCanthus);
      const pEnR = toPx(lm.rightMedialCanthus);
      const pExR = toPx(lm.rightLateralCanthus);

      ctx.save();

      // Overlay 1: Midsagittal Symmetry Axis
      if (appState.overlays.symmetry) {
        const midX = (pTr.x + pGl.x + pSn.x + pMe.x) / 4;
        ctx.strokeStyle = "rgba(56, 189, 248, 0.72)";
        ctx.lineWidth = 1.4;
        ctx.setLineDash([6, 4]);
        ctx.beginPath();
        ctx.moveTo(midX, Math.max(10, pTr.y - 26));
        ctx.lineTo(midX, Math.min(ch - 10, pMe.y + 26));
        ctx.stroke();
        ctx.setLineDash([]);
      }

      // Overlay 2: Facial Thirds Horizontal Caliper Planes
      if (appState.overlays.thirds) {
        const span = drawW * 0.35;
        const midX = (pGl.x + pSn.x) / 2;
        const planes = [
          { y: pTr.y, pct: `${appState.metrics.thirds[0]}%` },
          { y: pGl.y, pct: `${appState.metrics.thirds[1]}%` },
          { y: pSn.y, pct: `${appState.metrics.thirds[2]}%` },
          { y: pMe.y, pct: "" },
        ];
        ctx.strokeStyle = "rgba(226, 194, 117, 0.72)";
        ctx.lineWidth = 1.25;
        ctx.font = "600 10px 'JetBrains Mono', monospace";
        ctx.fillStyle = "#F2DA9B";

        planes.forEach((pl, i) => {
          ctx.setLineDash([4, 4]);
          ctx.beginPath();
          ctx.moveTo(midX - span, pl.y);
          ctx.lineTo(midX + span, pl.y);
          ctx.stroke();
          ctx.setLineDash([]);
          if (i < 3) {
            const nextY = planes[i + 1].y;
            ctx.fillText(pl.pct, midX + span + 6, (pl.y + nextY) / 2 + 3);
          }
        });
      }

      // Overlay 3: Canthal Tilt & Interpupillary Spacing (IPD)
      if (appState.overlays.canthal) {
        ctx.strokeStyle = "#38BDF8";
        ctx.lineWidth = 1.9;
        ctx.beginPath();
        ctx.moveTo(pExL.x - 14, pExL.y - (pEnL.y - pExL.y) * 0.45);
        ctx.lineTo(pEnL.x, pEnL.y);
        ctx.moveTo(pEnR.x, pEnR.y);
        ctx.lineTo(pExR.x + 14, pExR.y - (pEnR.y - pExR.y) * 0.45);
        ctx.stroke();

        // Intercanthal & Pupil Spacing Span
        const pPupilL = { x: (pExL.x + pEnL.x) / 2, y: (pExL.y + pEnL.y) / 2 };
        const pPupilR = { x: (pEnR.x + pExR.x) / 2, y: (pEnR.y + pExR.y) / 2 };
        ctx.strokeStyle = "rgba(56, 189, 248, 0.45)";
        ctx.setLineDash([3, 3]);
        ctx.beginPath();
        ctx.moveTo(pPupilL.x, pPupilL.y);
        ctx.lineTo(pPupilR.x, pPupilR.y);
        ctx.stroke();
        ctx.setLineDash([]);
      }

      // Overlay 4: Zygomatic-to-Gonial Ratio & Mandibular Projection
      if (appState.overlays.jaw) {
        // Bizygomatic Width Line (Zy-L to Zy-R)
        ctx.strokeStyle = "rgba(242, 218, 155, 0.85)";
        ctx.lineWidth = 1.6;
        ctx.beginPath();
        ctx.moveTo(pZyL.x, pZyL.y);
        ctx.lineTo(pZyR.x, pZyR.y);
        ctx.stroke();

        // Bigonial Width Line (Go-L to Go-R)
        ctx.strokeStyle = "rgba(226, 194, 117, 0.9)";
        ctx.lineWidth = 1.8;
        ctx.beginPath();
        ctx.moveTo(pGoL.x, pGoL.y);
        ctx.lineTo(pGoR.x, pGoR.y);
        ctx.stroke();

        // Mandibular Ramus & Lower-Third Perimeter (Zy -> Go -> Me)
        ctx.strokeStyle = "rgba(226, 194, 117, 0.55)";
        ctx.lineWidth = 1.5;
        ctx.beginPath();
        ctx.moveTo(pZyL.x, pZyL.y);
        ctx.lineTo(pGoL.x, pGoL.y);
        ctx.lineTo(pMe.x, pMe.y);
        ctx.lineTo(pGoR.x, pGoR.y);
        ctx.lineTo(pZyR.x, pZyR.y);
        ctx.stroke();
      }

      // Render 12 Draggable Craniometric Handles
      const activeKey = appState.draggingNode || appState.hoveredNode;
      Object.entries(lm).forEach(([key, pt]) => {
        const px = toPx(pt);
        const isFocused = activeKey === key;

        // Outer precision ring
        ctx.beginPath();
        ctx.arc(px.x, px.y, isFocused ? 11 : 7, 0, Math.PI * 2);
        ctx.fillStyle = isFocused ? "rgba(226, 194, 117, 0.28)" : "rgba(7, 9, 13, 0.72)";
        ctx.fill();

        ctx.lineWidth = isFocused ? 2.2 : 1.7;
        ctx.strokeStyle = pt.color;
        ctx.stroke();

        // Core crosshair point
        ctx.beginPath();
        ctx.arc(px.x, px.y, 2.3, 0, Math.PI * 2);
        ctx.fillStyle = "#FFFFFF";
        ctx.fill();

        // Anatomical Label Tag on Hover or Drag
        if (isFocused) {
          const labelText = `${pt.code} • ${pt.name}`;
          ctx.font = "600 10px 'JetBrains Mono', monospace";
          const tw = ctx.measureText(labelText).width + 14;
          const boxX = Math.max(8, Math.min(cw - tw - 8, px.x - tw / 2));
          const boxY = px.y > 46 ? px.y - 30 : px.y + 16;

          ctx.fillStyle = "rgba(7, 9, 13, 0.92)";
          ctx.strokeStyle = "#E2C275";
          ctx.lineWidth = 1;
          ctx.beginPath();
          ctx.roundRect(boxX, boxY, tw, 20, 6);
          ctx.fill();
          ctx.stroke();

          ctx.fillStyle = "#F2DA9B";
          ctx.fillText(labelText, boxX + 7, boxY + 13.5);
        }
      });

      // Precision Optical Magnifier Loupe when Hovering or Dragging a Node
      if (activeKey && lm[activeKey]) {
        const targetPx = toPx(lm[activeKey]);
        const loupeRadius = 38;
        const loupeX = targetPx.x < cw / 2 ? cw - loupeRadius - 14 : loupeRadius + 14;
        const loupeY = loupeRadius + 14;

        ctx.save();
        ctx.beginPath();
        ctx.arc(loupeX, loupeY, loupeRadius, 0, Math.PI * 2);
        ctx.clip();

        ctx.fillStyle = "#05070B";
        ctx.fillRect(loupeX - loupeRadius, loupeY - loupeRadius, loupeRadius * 2, loupeRadius * 2);

        // Draw 2.2x magnified region of source image around landmark
        const zoom = 2.2;
        const srcX = lm[activeKey].x * iw;
        const srcY = lm[activeKey].y * ih;
        const sampleHalf = (loupeRadius / scale) / zoom;
        ctx.drawImage(
          img,
          srcX - sampleHalf,
          srcY - sampleHalf,
          sampleHalf * 2,
          sampleHalf * 2,
          loupeX - loupeRadius,
          loupeY - loupeRadius,
          loupeRadius * 2,
          loupeRadius * 2
        );

        // Reticle crosshairs inside loupe
        ctx.strokeStyle = "rgba(226, 194, 117, 0.85)";
        ctx.lineWidth = 1;
        ctx.beginPath();
        ctx.moveTo(loupeX - loupeRadius, loupeY);
        ctx.lineTo(loupeX + loupeRadius, loupeY);
        ctx.moveTo(loupeX, loupeY - loupeRadius);
        ctx.lineTo(loupeX, loupeY + loupeRadius);
        ctx.stroke();
        ctx.restore();

        // Loupe outer bezel
        ctx.beginPath();
        ctx.arc(loupeX, loupeY, loupeRadius, 0, Math.PI * 2);
        ctx.strokeStyle = "#E2C275";
        ctx.lineWidth = 2;
        ctx.stroke();
      }

      ctx.restore();
    }

    /**
     * Mouse & Touch Event Handlers for 12-Point Landmark Calibration
     */
    function getPointerPos(e) {
      const rect = canvas.getBoundingClientRect();
      const clientX = e.touches ? e.touches[0].clientX : e.clientX;
      const clientY = e.touches ? e.touches[0].clientY : e.clientY;
      return {
        x: clientX - rect.left,
        y: clientY - rect.top,
      };
    }

    function findNearestLandmark(pos) {
      const { x: drawX, y: drawY, w: drawW, h: drawH } = appState.imageDrawRect;
      if (!drawW || !drawH) return null;

      let closestKey = null;
      let minDist = 24;

      Object.entries(appState.landmarks).forEach(([key, pt]) => {
        const lx = drawX + pt.x * drawW;
        const ly = drawY + pt.y * drawH;
        const dist = Math.hypot(pos.x - lx, pos.y - ly);
        if (dist < minDist) {
          minDist = dist;
          closestKey = key;
        }
      });

      return closestKey;
    }

    function onPointerDown(e) {
      if (!appState.imageLoaded) return;
      const pos = getPointerPos(e);
      const hit = findNearestLandmark(pos);
      if (hit) {
        if (e.cancelable) e.preventDefault();
        appState.draggingNode = hit;
        document.getElementById("activeNodeBadge").textContent = `Calibrating: ${appState.landmarks[hit].name}`;
        renderCraniometricCanvas();
      }
    }

    function onPointerMove(e) {
      if (!appState.imageLoaded) return;
      const pos = getPointerPos(e);
      appState.pointerCanvasPos = pos;

      if (appState.draggingNode) {
        if (e.cancelable) e.preventDefault();
        const { x: drawX, y: drawY, w: drawW, h: drawH } = appState.imageDrawRect;
        const normX = Math.max(0.05, Math.min(0.95, (pos.x - drawX) / drawW));
        const normY = Math.max(0.05, Math.min(0.95, (pos.y - drawY) / drawH));

        appState.landmarks[appState.draggingNode].x = normX;
        appState.landmarks[appState.draggingNode].y = normY;

        computeCraniometricMetrics();
        renderCraniometricCanvas();
      } else if (!e.touches) {
        const hovered = findNearestLandmark(pos);
        if (hovered !== appState.hoveredNode) {
          appState.hoveredNode = hovered;
          canvas.style.cursor = hovered ? "grab" : "crosshair";
          document.getElementById("activeNodeBadge").textContent = hovered
            ? `${appState.landmarks[hovered].code}: ${appState.landmarks[hovered].name}`
            : "12 Nodes Calibrated";
          renderCraniometricCanvas();
        }
      }
    }

    function onPointerUp() {
      if (appState.draggingNode) {
        appState.draggingNode = null;
        document.getElementById("activeNodeBadge").textContent = "12 Nodes Calibrated";
        renderCraniometricCanvas();
      }
    }

    canvas.addEventListener("mousedown", onPointerDown);
    window.addEventListener("mousemove", onPointerMove);
    window.addEventListener("mouseup", onPointerUp);

    canvas.addEventListener("touchstart", onPointerDown, { passive: false });
    window.addEventListener("touchmove", onPointerMove, { passive: false });
    window.addEventListener("touchend", onPointerUp);

    /**
     * Extract Clean Base64 JPEG for Gemini Vision Analysis
     */
    function getCleanBase64Image() {
      if (!appState.sourceImage) return null;
      const tmp = document.createElement("canvas");
      const maxDim = 768;
      const sw = appState.sourceImage.width || appState.sourceImage.naturalWidth;
      const sh = appState.sourceImage.height || appState.sourceImage.naturalHeight;
      const scale = Math.min(1, maxDim / Math.max(sw, sh));
      tmp.width = Math.round(sw * scale);
      tmp.height = Math.round(sh * scale);
      const tctx = tmp.getContext("2d");
      tctx.drawImage(appState.sourceImage, 0, 0, tmp.width, tmp.height);
      return tmp.toDataURL("image/jpeg", 0.85).split(",")[1];
    }

    /**
     * Exponential Backoff Fetch Helper for Gemini API
     */
    async function fetchGeminiWithRetry(url, payload, maxRetries = 3) {
      let delay = 1000;
      for (let attempt = 0; attempt <= maxRetries; attempt++) {
        try {
          const response = await fetch(url, {
            method: "POST",
            headers: { "Content-Type": "application/json" },
            body: JSON.stringify(payload),
          });
          if (!response.ok) throw new Error(`HTTP ${response.status}`);
          return await response.json();
        } catch (err) {
          if (attempt === maxRetries) throw err;
          await new Promise((r) => setTimeout(r, delay));
          delay *= 2;
        }
      }
    }

    /**
     * Intelligent Local Craniometric Fallback Engine
     * Computes accurate scores & custom protocol from live 12-point telemetry
     */
    function buildLocalCraniometricReport() {
      const m = appState.metrics;
      const isFem = appState.baseline === "Feminine Structure";
      const isMasc = appState.baseline === "Masculine Structure";

      const periorbitalScore = Number(Math.min(9.5, Math.max(6.4, 7.2 + m.canthalTiltDeg * 0.21)).toFixed(1));
      const mandibularScore = Number(
        Math.min(9.3, Math.max(6.2, 6.7 + (m.jawToCheekRatio - 0.71) * 7.8 + (m.thirdsScore - 85) * 0.03)).toFixed(1)
      );
      const zygomaticScore = Number(Math.min(9.4, Math.max(6.5, 7.0 + (m.goldenRatioScore - 82) * 0.11)).toFixed(1));
      const symmetryScore10 = Number(Math.min(9.6, Math.max(6.6, m.symmetryScore / 10.5)).toFixed(1));
      const dermalScore = Number(
        Math.min(9.1, Math.max(6.6, 7.2 + (appState.vector === "Dermal Clarity & Contrast" ? 0.2 : 0.35))).toFixed(1)
      );

      const currentRating = Number(
        ((periorbitalScore + mandibularScore + zygomaticScore + symmetryScore10 + dermalScore) / 5).toFixed(1)
      );
      const potentialRating = Number(Math.min(9.6, currentRating + 1.2).toFixed(1));

      // Determine top structural strength dynamically
      const ranked = [
        { label: "Canthal & Orbital Vector", val: periorbitalScore },
        { label: "Gonial & Mandibular Taper", val: mandibularScore },
        { label: "Zygomatic Projection", val: zygomaticScore },
        { label: "Midsagittal Symmetry", val: symmetryScore10 },
      ].sort((a, b) => b.val - a.val);

      return {
        source: "CRANIOMETRIC GEOMETRIC ENGINE",
        currentRating,
        potentialRating,
        faceShape: m.estimatedShape,
        contrastTier: "High Chiaroscuro Contrast",
        keyStrength: ranked[0].label,
        executiveSummary: `Your ${m.estimatedShape.toLowerCase()} architecture exhibits ${m.symmetryScore}% midsagittal alignment, a ${m.canthalTiltDeg >= 0 ? "+" : ""}${m.canthalTiltDeg}° lateral canthal tilt, and a ${m.jawToCheekRatio} bigonial-to-bizygomatic ratio. Focusing on ${appState.vector.toLowerCase()} via targeted myofunctional posture, contrast-aligned grooming, and ${m.estimatedShape.toLowerCase()} framing yields a projected +${(potentialRating - currentRating).toFixed(1)} harmonic gain.`,
        features: [
          {
            name: "Periorbital & Canthal Architecture",
            score: periorbitalScore,
            metricTag: `Tilt ${m.canthalTiltDeg >= 0 ? "+" : ""}${m.canthalTiltDeg}° • IPD ${m.ipdRatio}`,
            observation: `Exocanthion-to-endocanthion axis registers a ${m.canthalTiltDeg >= 1.5 ? "positive upward" : "level"} vector with ${m.ipdRatio} interpupillary spacing ratio. Cold lymphatic drainage and precision brow tail shaping will amplify orbital depth.`,
          },
          {
            name: "Mandibular & Gonial Projection",
            score: mandibularScore,
            metricTag: `Go/Zy ${m.jawToCheekRatio} • ~${m.gonialAngleDeg}°`,
            observation: `Bigonial width measures ${(m.jawToCheekRatio * 100).toFixed(0)}% of bizygomatic width with an estimated ${m.gonialAngleDeg}° gonial vertex. Submental debloating and proper tongue-palate posture will sharpen the mandibular border.`,
          },
          {
            name: "Zygomatic & Midface Balance",
            score: zygomaticScore,
            metricTag: `Midface ${m.thirds[1]}% • Φ ${m.goldenRatioScore}%`,
            observation: `Middle third accounts for ${m.thirds[1]}% of total vertical height with strong lateral zygion projection. Lean body-fat maintenance enhances sub-malar chiaroscuro shadow.`,
          },
          {
            name: "Facial Thirds & Midsagittal Symmetry",
            score: symmetryScore10,
            metricTag: `${m.thirds.join("/")} • ${m.symmetryScore}% Sym`,
            observation: `Upper, middle, and lower proportions align at ${m.thirds[0]}/${m.thirds[1]}/${m.thirds[2]}% with ${m.symmetryScore}% bilateral correspondence across the vertical axis.`,
          },
          {
            name: "Dermal Texture & Facial Contrast",
            score: dermalScore,
            metricTag: `${m.estimatedShape} • Contrast`,
            observation: `Surface light reflection and brow-to-skin luminance contrast support clear feature separation; retinoid renewal and dark-anchor wardrobe tones will maximize visual crispness.`,
          },
        ],
        actionPlan: {
          gonial: [
            {
              title: "Myofunctional Palate Posture & Cervical Alignment",
              detail: `Rest the full tongue flat against the hard palate behind the upper incisors with molars in light contact, and align ears over shoulders to elevate the hyoid bone and tighten submental contour.`,
            },
            {
              title: "Potassium-Sodium Debloating Protocol",
              detail: `Maintain 3.2L daily hydration paired with potassium-dense whole foods (avocado, spinach, coconut water) while reducing late-evening sodium to unveil crisp gonial angles within 48–72 hours.`,
            },
            {
              title: isMasc ? "Gonial-Defining Stubble & Neckline Spec" : "Lymphatic Jawline Sculpting & Lean Conditioning",
              detail: isMasc
                ? `Either keep a clean-shaven finish to display natural gonial bone edges or trim uniform 3mm stubble with a crisp neckline set two fingers above the thyroid cartilage.`
                : `Perform 2 minutes of upward gua sha / knuckle drainage from menton to gonion each morning alongside sustainable lean conditioning to accentuate jawline definition.`,
            },
          ],
          periorbital: [
            {
              title: "Orbital Brow Architecture",
              detail: isFem
                ? `Comb brow hairs upward with clear peptide gel and groom only stray hairs beneath the lateral arch to reinforce a lifted, positive canthal frame.`
                : `Preserve dense, low-set brow thickness; clean only central glabella strays and brush hairs outward to create a strong supraorbital brow ridge.`,
            },
            {
              title: "Chilled Caffeine & Peptide Periorbital Care",
              detail: `Apply a refrigerated 5% caffeine + acetyl tetrapeptide-5 serum every morning using gentle ring-finger tapping from medial to lateral canthus to eliminate morning orbital fluid retention.`,
            },
            {
              title: "Sleep Architecture & Blue-Light Hygiene",
              detail: `Aim for 7.5–8.5 hours of back-sleeping on a slightly elevated silk/satin pillowcase to prevent unilateral periorbital compression and sclera redness.`,
            },
          ],
          dermal: [
            {
              title: "Clinical AM/PM Epidermal Renewal",
              detail: `Morning: gentle amino-acid cleanser, 5% niacinamide serum, lightweight ceramide barrier lotion, and invisible SPF 50+. Evening: double cleanse followed by adapalene or retinol 3–4 nights weekly.`,
            },
            {
              title: "Chiaroscuro Contrast Optimization",
              detail: `Keep eyebrows, lashes, and hairline edges well-defined and richly pigmented (using tinted brow gel or castor/peptide conditioning) to sharpen dark-on-light facial contrast.`,
            },
            {
              title: "Lip Barrier & Dental Brightness",
              detail: `Apply overnight lanolin or squalane lip therapy and use enamel-safe hydrogen peroxide strips periodically so perioral contrast looks clean and healthy.`,
            },
          ],
          framing: [
            {
              title: `${m.estimatedShape} Cut Geometry & Temple Taper`,
              detail: isFem
                ? `Request soft cheekbone-grazing curtain layers with subtle crown volume to harmonize your ${m.thirds[0]}% upper third and frame the zygomatic arch.`
                : `Ask your barber for a mid-taper fade (guard #1.5–#3) rather than high bald sides, keeping 2.5–3.5 inches of textured volume on top to complement your ${m.jawToCheekRatio} bigonial ratio.`,
            },
            {
              title: "Optical Frame & Sunglasses Geometry",
              detail:
                m.estimatedShape.includes("Square") || m.estimatedShape.includes("Diamond")
                  ? `Select slightly curved panto or keyhole-bridge acetate frames to balance angular mandibular geometry.`
                  : `Choose architectural rectangular or structured browline frames to add crisp horizontal width across the upper midface.`,
            },
            {
              title: "Collar Architecture & Contrast Palette",
              detail: `Pair obsidian, deep charcoal, midnight navy, or crisp off-white tops with structured collars/necklines near the face to reinforce visual symmetry and jaw-to-shoulder proportion.`,
            },
          ],
        },
      };
    }

    /**
     * Run Gonion AI Diagnostic via Gemini Vision (`gemini-3-flash-preview`)
     */
    async function runGonionDiagnostic() {
      if (!appState.imageLoaded) {
        showToast("Upload a portrait, capture via optical webcam, or load Calibration Subject first.", "warn");
        return;
      }

      const btn = document.getElementById("runDiagnosticBtn");
      const btnText = document.getElementById("runDiagnosticBtnText");
      btn.disabled = true;
      btnText.textContent = "RUNNING DIAGNOSTIC...";
      laserScanOverlay.classList.remove("hidden");

      const scanMessages = [
        "Triangulating gonial vertices (Go-L / Go-R)...",
        "Computing canthal tilt & Frankfurt horizontal plane...",
        "Evaluating zygomatic projection & chiaroscuro contrast...",
        "Synthesizing personalized Softmaxxing protocol...",
      ];
      let msgIndex = 0;
      scanStatusText.textContent = scanMessages[0];
      const msgTimer = setInterval(() => {
        msgIndex = (msgIndex + 1) % scanMessages.length;
        scanStatusText.textContent = scanMessages[msgIndex];
      }, 850);

      try {
        const base64Image = getCleanBase64Image();
        const m = appState.metrics;

        const systemInstruction = `You are GONION, an elite, objective, constructive Craniometric Aesthetics & Softmaxxing Diagnostic Engine.
Analyze the provided front-facing portrait alongside the user's calibrated 12-point craniometric telemetry.
Maintain a refined, architectural, encouraging, scientifically grounded tone focused exclusively on non-invasive Softmaxxing (gonial posture/debloating, periorbital grooming, dermal skincare/contrast, and hair/collar framing). Never suggest invasive procedures.
Provide realistic scores on a 10-point scale (e.g., 6.6 to 8.5 current harmony, and +0.8 to +1.4 realistic softmaxxing ceiling).`;

        const userPrompt = `Execute a complete Gonion Craniometric & Aesthetic Diagnostic.
Calibration Settings:
- Architectural Baseline: ${appState.baseline}
- Primary Optimization Vector: ${appState.vector}

12-Point Craniometric Telemetry:
- Facial Thirds (Tr-G / G-Sn / Sn-Me): ${m.thirds[0]}% / ${m.thirds[1]}% / ${m.thirds[2]}% (${m.thirdsScore}% proportional)
- Mean Canthal Tilt: ${m.canthalTiltDeg} degrees
- IPD-to-Bizygomatic Ratio: ${m.ipdRatio}
- Bigonial-to-Bizygomatic Ratio (Go/Zy): ${m.jawToCheekRatio} (Est. Gonial Angle ~${m.gonialAngleDeg}°)
- Golden Ratio (1.618) Alignment: ${m.goldenRatioScore}%
- Midsagittal Bilateral Symmetry Index: ${m.symmetryScore}%
- Geometric Architecture Estimate: ${m.estimatedShape}

Return a structured JSON diagnostic report matching the exact schema.`;

        const payload = {
          contents: [
            {
              role: "user",
              parts: [
                { text: userPrompt },
                {
                  inlineData: {
                    mimeType: "image/jpeg",
                    data: base64Image,
                  },
                },
              ],
            },
          ],
          systemInstruction: {
            parts: [{ text: systemInstruction }],
          },
          generationConfig: {
            responseMimeType: "application/json",
            responseSchema: {
              type: "OBJECT",
              properties: {
                currentRating: { type: "NUMBER" },
                potentialRating: { type: "NUMBER" },
                faceShape: { type: "STRING" },
                contrastTier: { type: "STRING" },
                keyStrength: { type: "STRING" },
                executiveSummary: { type: "STRING" },
                features: {
                  type: "ARRAY",
                  items: {
                    type: "OBJECT",
                    properties: {
                      name: { type: "STRING" },
                      score: { type: "NUMBER" },
                      metricTag: { type: "STRING" },
                      observation: { type: "STRING" },
                    },
                    required: ["name", "score", "metricTag", "observation"],
                  },
                },
                actionPlan: {
                  type: "OBJECT",
                  properties: {
                    gonial: {
                      type: "ARRAY",
                      items: {
                        type: "OBJECT",
                        properties: {
                          title: { type: "STRING" },
                          detail: { type: "STRING" },
                        },
                        required: ["title", "detail"],
                      },
                    },
                    periorbital: {
                      type: "ARRAY",
                      items: {
                        type: "OBJECT",
                        properties: {
                          title: { type: "STRING" },
                          detail: { type: "STRING" },
                        },
                        required: ["title", "detail"],
                      },
                    },
                    dermal: {
                      type: "ARRAY",
                      items: {
                        type: "OBJECT",
                        properties: {
                          title: { type: "STRING" },
                          detail: { type: "STRING" },
                        },
                        required: ["title", "detail"],
                      },
                    },
                    framing: {
                      type: "ARRAY",
                      items: {
                        type: "OBJECT",
                        properties: {
                          title: { type: "STRING" },
                          detail: { type: "STRING" },
                        },
                        required: ["title", "detail"],
                      },
                    },
                  },
                  required: ["gonial", "periorbital", "dermal", "framing"],
                },
              },
              required: [
                "currentRating",
                "potentialRating",
                "faceShape",
                "contrastTier",
                "keyStrength",
                "executiveSummary",
                "features",
                "actionPlan",
              ],
            },
          },
        };

        const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/${GEMINI_MODEL}:generateContent?key=${apiKey}`;
        const result = await fetchGeminiWithRetry(apiUrl, payload, 2);

        const rawJson = result?.candidates?.[0]?.content?.parts?.[0]?.text;
        if (!rawJson) throw new Error("Empty diagnostic response");

        const report = JSON.parse(rawJson);
        report.source = "GEMINI VISION + CRANIOMETRICS";
        appState.currentReport = report;
        renderDiagnosticReport(report);
        showToast("Gonion Diagnostic complete. Telemetry & protocol updated.", "gold");
      } catch (err) {
        const fallback = buildLocalCraniometricReport();
        appState.currentReport = fallback;
        renderDiagnosticReport(fallback);
        showToast("Diagnostic synthesized via Craniometric Geometric Engine.", "cyan");
      } finally {
        clearInterval(msgTimer);
        laserScanOverlay.classList.add("hidden");
        btn.disabled = false;
        btnText.textContent = "RE-RUN GONION DIAGNOSTIC";
      }
    }

    /**
     * Render the Structured Gonion Diagnostic Report into the DOM
     */
    function renderDiagnosticReport(report) {
      document.getElementById("reportPlaceholder").classList.add("hidden");
      const container = document.getElementById("reportContainer");
      container.classList.remove("hidden");

      const cur = Math.max(1, Math.min(10, Number(report.currentRating) || 7.4));
      const pot = Math.max(cur, Math.min(10, Number(report.potentialRating) || 8.6));
      const delta = (pot - cur).toFixed(1);

      document.getElementById("currentRatingValue").textContent = cur.toFixed(1);
      document.getElementById("potentialRatingValue").textContent = pot.toFixed(1);
      document.getElementById("potentialDeltaBadge").textContent = `+${delta}`;

      // Radial Ring Gauges (circumference = 2 * pi * 42 = 263.89)
      const circ = 263.89;
      document.getElementById("currentScoreRing").style.strokeDashoffset = circ * (1 - cur / 10);
      document.getElementById("potentialScoreRing").style.strokeDashoffset = circ * (1 - pot / 10);

      // Linear Trajectory Bar
      document.getElementById("currentLinearBar").style.width = `${Math.round(cur * 10)}%`;
      document.getElementById("ceilingLinearBar").style.width = `${Math.round(pot * 10)}%`;

      document.getElementById("detectedFaceShape").textContent = report.faceShape || appState.metrics.estimatedShape;
      document.getElementById("detectedContrast").textContent = report.contrastTier || "High Contrast";
      document.getElementById("detectedKeyStrength").textContent = report.keyStrength || "Canthal Vector";
      document.getElementById("analysisSourceBadge").textContent = report.source || "GEMINI VISION + CRANIOMETRICS";
      document.getElementById("executiveSummaryText").textContent = report.executiveSummary;
      document.getElementById("coachFaceShapeMention").textContent = `${report.faceShape} architecture`;

      // Render 5 Feature Breakdown Cards
      const listEl = document.getElementById("featureBreakdownList");
      listEl.innerHTML = "";
      (report.features || []).forEach((feat) => {
        const score = Math.max(1, Math.min(10, Number(feat.score) || 7.5));
        const pct = Math.round(score * 10);
        const card = document.createElement("div");
        card.className = "luxury-subcard rounded-xl p-4 space-y-2.5";
        card.innerHTML = `
          <div class="flex items-center justify-between gap-2">
            <div class="flex items-center gap-2 flex-wrap">
              <span class="font-display text-xs sm:text-sm font-bold text-white">${escapeHtml(feat.name)}</span>
              <span class="text-[10px] font-mono px-2 py-0.5 rounded-md bg-[#38BDF8]/10 text-[#38BDF8] border border-[#38BDF8]/25">
                ${escapeHtml(feat.metricTag || "")}
              </span>
            </div>
            <span class="font-mono text-xs sm:text-sm font-extrabold text-[#F2DA9B]">
              ${score.toFixed(1)} <span class="text-slate-500 font-normal">/ 10</span>
            </span>
          </div>
          <div class="w-full h-1.5 rounded-full bg-white/10 overflow-hidden">
            <div class="h-full rounded-full bg-gradient-to-r from-[#38BDF8] to-[#E2C275] transition-all duration-700" style="width: ${pct}%"></div>
          </div>
          <p class="text-xs text-slate-300 leading-relaxed">${escapeHtml(feat.observation)}</p>
        `;
        listEl.appendChild(card);
      });

      renderPlanTab(appState.activePlanTab);

      if (window.innerWidth < 1024) {
        container.scrollIntoView({ behavior: "smooth", block: "start" });
      }
    }

    /**
     * Render Selected Softmaxxing Protocol Tab
     */
    function renderPlanTab(tabKey) {
      appState.activePlanTab = tabKey;

      document.querySelectorAll(".plan-tab").forEach((btn) => {
        const active = btn.dataset.tab === tabKey;
        btn.className = active
          ? "plan-tab active px-3.5 py-2 rounded-xl text-xs font-semibold bg-[#E2C275]/20 text-[#F2DA9B] border border-[#E2C275]/45 transition"
          : "plan-tab px-3.5 py-2 rounded-xl text-xs font-semibold bg-white/5 text-slate-300 border border-white/10 hover:bg-white/10 transition";
      });

      const contentEl = document.getElementById("planTabContent");
      contentEl.innerHTML = "";

      if (!appState.currentReport || !appState.currentReport.actionPlan) return;
      const items = appState.currentReport.actionPlan[tabKey] || [];

      items.forEach((item, idx) => {
        const row = document.createElement("div");
        row.className = "luxury-subcard rounded-xl p-4 flex items-start gap-3.5";
        row.innerHTML = `
          <div class="w-6 h-6 rounded-lg bg-[#E2C275]/15 border border-[#E2C275]/40 text-[#F2DA9B] font-mono text-xs font-bold flex items-center justify-center shrink-0 mt-0.5">
            0${idx + 1}
          </div>
          <div class="space-y-1">
            <h4 class="font-display text-xs sm:text-sm font-bold text-white">${escapeHtml(item.title)}</h4>
            <p class="text-xs text-slate-300 leading-relaxed">${escapeHtml(item.detail)}</p>
          </div>
        `;
        contentEl.appendChild(row);
      });
    }

    /**
     * Copy Full Protocol via document.execCommand('copy') for iFrame Safety
     */
    function copyFullProtocol() {
      if (!appState.currentReport) return;
      const r = appState.currentReport;
      const lines = [
        `GONION // CRANIOMETRIC AESTHETICS & SOFTMAXXING PROTOCOL`,
        `Current Harmony: ${r.currentRating}/10 | Softmaxxing Ceiling: ${r.potentialRating}/10`,
        `Architecture: ${r.faceShape} | Contrast: ${r.contrastTier} | Key Strength: ${r.keyStrength}`,
        `Summary: ${r.executiveSummary}`,
        ``,
        `--- ACTIONABLE PROTOCOL ---`,
      ];

      const tabs = [
        ["Gonial & Jawline", r.actionPlan.gonial],
        ["Periorbital & Brow", r.actionPlan.periorbital],
        ["Dermal & Contrast", r.actionPlan.dermal],
        ["Hair & Structural Framing", r.actionPlan.framing],
      ];

      tabs.forEach(([title, list]) => {
        lines.push(`\n[${title}]`);
        (list || []).forEach((it) => lines.push(`• ${it.title}: ${it.detail}`));
      });

      const ta = document.createElement("textarea");
      ta.value = lines.join("\n");
      ta.style.position = "fixed";
      ta.style.opacity = "0";
      document.body.appendChild(ta);
      ta.select();
      try {
        document.execCommand("copy");
        showToast("Full Gonion Softmaxxing Protocol copied to clipboard.", "gold");
      } catch (e) {
        showToast("Clipboard restricted. Please select text manually.", "warn");
      }
      document.body.removeChild(ta);
    }

    /**
     * Context-Aware Gonion AI Consultant Chat
     */
    async function sendConsultantMessage(question) {
      const trimmed = question.trim();
      if (!trimmed) return;

      const chatLog = document.getElementById("coachChatLog");
      const sendBtn = document.getElementById("coachSendBtn");
      const inputEl = document.getElementById("coachChatInput");

      const userBubble = document.createElement("div");
      userBubble.className =
        "ml-auto max-w-[85%] bg-[#E2C275]/18 border border-[#E2C275]/40 rounded-2xl rounded-tr-sm p-3.5 text-xs sm:text-sm text-[#F2DA9B] leading-relaxed";
      userBubble.textContent = trimmed;
      chatLog.appendChild(userBubble);

      inputEl.value = "";
      sendBtn.disabled = true;

      const typing = document.createElement("div");
      typing.className =
        "mr-auto max-w-[85%] bg-[#121824] border border-white/10 rounded-2xl rounded-tl-sm p-3.5 text-xs text-slate-400 font-mono flex items-center gap-2";
      typing.innerHTML = `<span class="w-2 h-2 rounded-full bg-[#38BDF8] animate-ping"></span><span>Consulting craniometric telemetry...</span>`;
      chatLog.appendChild(typing);
      chatLog.scrollTop = chatLog.scrollHeight;

      const r = appState.currentReport || buildLocalCraniometricReport();
      const m = appState.metrics;

      try {
        const systemInstruction = `You are GONION CONSULTANT, an architectural, encouraging, scientifically grounded aesthetics & grooming advisor.
Tailor every answer directly to the user's calibrated telemetry:
- Baseline: ${appState.baseline} | Vector: ${appState.vector}
- Harmony Score: ${r.currentRating}/10 -> Ceiling ${r.potentialRating}/10
- Face Architecture: ${r.faceShape} | Contrast: ${r.contrastTier} | Key Strength: ${r.keyStrength}
- Craniometrics: Thirds ${m.thirds.join("/")}% | Canthal Tilt ${m.canthalTiltDeg}° | Go/Zy Ratio ${m.jawToCheekRatio} | Gonial Angle ~${m.gonialAngleDeg}° | Symmetry ${m.symmetryScore}%
Keep responses crisp (3–4 short bullet points or 2 concise paragraphs), practical, and strictly non-invasive.`;

        appState.chatHistory.push({ role: "user", parts: [{ text: trimmed }] });

        const payload = {
          contents: appState.chatHistory.slice(-6),
          systemInstruction: {
            parts: [{ text: systemInstruction }],
          },
        };

        const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/${GEMINI_MODEL}:generateContent?key=${apiKey}`;
        const res = await fetchGeminiWithRetry(apiUrl, payload, 2);
        const replyText = res?.candidates?.[0]?.content?.parts?.[0]?.text;
        if (!replyText) throw new Error("Empty consultant response");

        appState.chatHistory.push({ role: "model", parts: [{ text: replyText }] });
        typing.remove();
        appendConsultantReply(replyText);
      } catch (err) {
        typing.remove();
        appendConsultantReply(generateLocalConsultantReply(trimmed, r, m));
      } finally {
        sendBtn.disabled = false;
        chatLog.scrollTop = chatLog.scrollHeight;
      }
    }

    function appendConsultantReply(text) {
      const chatLog = document.getElementById("coachChatLog");
      const bubble = document.createElement("div");
      bubble.className =
        "mr-auto max-w-[90%] bg-[#121824] border border-[#E2C275]/20 rounded-2xl rounded-tl-sm p-3.5 text-xs sm:text-sm text-slate-200 leading-relaxed whitespace-pre-line";
      bubble.innerHTML = escapeHtml(text).replace(
        /\*\*(.*?)\*\*/g,
        '<strong class="text-[#F2DA9B] font-semibold">$1</strong>'
      );
      chatLog.appendChild(bubble);
    }

    function generateLocalConsultantReply(q, report, m) {
      const lower = q.toLowerCase();
      if (lower.includes("hair") || lower.includes("cut") || lower.includes("bigonial")) {
        return `For your **${report.faceShape}** architecture with a **${m.jawToCheekRatio}** bigonial-to-bizygomatic ratio:\n• **Lateral Taper:** Request a low-to-mid taper fade (guard #1.5 to #3) rather than high shaved sides so temple volume supports your zygomatic width.\n• **Top Geometry:** Keep 2.5–3.5 inches of textured layers styled forward or into a relaxed side-part to balance your ${m.thirds[0]}% upper third.\n• **Perimeter:** Ask for a clean natural nape taper to accentuate your ~${m.gonialAngleDeg}° gonial angle.`;
      }
      if (lower.includes("gonial") || lower.includes("jaw") || lower.includes("sharpen")) {
        return `To sharpen your **~${m.gonialAngleDeg}°** gonial projection and **${m.jawToCheekRatio}** Go/Zy ratio naturally:\n• **Tongue-Palate Posture:** Keep the posterior third of the tongue resting against the roof of the mouth with nasal breathing to lift the submental floor.\n• **Electrolyte Balance:** Pair 3.2L water intake with potassium-rich foods while cutting late-night sodium to clear sub-mandibular puffiness.\n• **Neck & Body-Fat Conditioning:** Deep neck flexor chin-tucks and lean body-fat optimization reveal the underlying mandibular border.`;
      }
      if (lower.includes("contrast")) {
        return `To elevate your **${report.contrastTier}** profile:\n• **Periorbital & Brow Framing:** Condition brows with peptide/castor serum and brush them horizontally so eye framing stays dark and crisp against the skin.\n• **Epidermal Luminance:** Daily SPF 50 + niacinamide evens skin tone so natural eye and hair contrast stands out.\n• **Wardrobe Anchors:** Wear obsidian, charcoal, or crisp off-white near the collar to amplify facial chiaroscuro.`;
      }
      return `Aligned with your **${report.faceShape}** telemetry (${m.symmetryScore}% symmetry, ${m.canthalTiltDeg >= 0 ? "+" : ""}${m.canthalTiltDeg}° canthal tilt):\n1. **Mandibular Crispness:** Prioritize evening sodium moderation and tongue-palate posture.\n2. **Orbital Framing:** Chilled 5% caffeine serum + minimal brow tail cleanup.\n3. **Architectural Framing:** Tapered temple styling paired with dark-anchor collar tones.`;
    }

    function escapeHtml(str) {
      return String(str)
        .replace(/&/g, "&amp;")
        .replace(/</g, "&lt;")
        .replace(/>/g, "&gt;")
        .replace(/"/g, "&quot;");
    }

    /**
     * Wire All Event Listeners on Load
     */
    window.addEventListener("DOMContentLoaded", () => {
      resetLandmarks();
      resizeCanvas();

      document.getElementById("loadSubjectBtn").addEventListener("click", loadCalibrationSubject);
      document.getElementById("openWebcamBtn").addEventListener("click", startWebcam);
      document.getElementById("captureWebcamBtn").addEventListener("click", captureWebcamFrame);
      document.getElementById("cancelWebcamBtn").addEventListener("click", stopWebcam);
      document.getElementById("resetLandmarksBtn").addEventListener("click", () => {
        resetLandmarks();
        showToast("12 craniometric nodes recentered.", "gold");
      });

      // File Input & Drag-and-Drop
      document.getElementById("photoInput").addEventListener("change", (e) => {
        if (e.target.files && e.target.files[0]) handleImageFile(e.target.files[0]);
      });

      const dropZone = document.getElementById("canvasDropZone");
      dropZone.addEventListener("dragover", (e) => {
        e.preventDefault();
        dropZone.classList.add("border-[#E2C275]");
      });
      dropZone.addEventListener("dragleave", () => {
        dropZone.classList.remove("border-[#E2C275]");
      });
      dropZone.addEventListener("drop", (e) => {
        e.preventDefault();
        dropZone.classList.remove("border-[#E2C275]");
        if (e.dataTransfer.files && e.dataTransfer.files[0]) handleImageFile(e.dataTransfer.files[0]);
      });

      // Biometric Overlay Toggles
      document.querySelectorAll(".overlay-toggle").forEach((btn) => {
        btn.addEventListener("click", () => {
          const key = btn.dataset.overlay;
          appState.overlays[key] = !appState.overlays[key];
          const isOn = appState.overlays[key];
          const dot = btn.querySelector("span:last-child");
          const isCyanLayer = key === "canthal" || key === "symmetry";

          if (isOn) {
            btn.className = isCyanLayer
              ? "overlay-toggle active flex items-center justify-between px-3 py-2 rounded-xl text-xs font-medium border transition bg-[#38BDF8]/15 border-[#38BDF8]/45 text-sky-200"
              : "overlay-toggle active flex items-center justify-between px-3 py-2 rounded-xl text-xs font-medium border transition bg-[#E2C275]/15 border-[#E2C275]/45 text-[#F2DA9B]";
            dot.className = isCyanLayer ? "w-2 h-2 rounded-full bg-[#38BDF8]" : "w-2 h-2 rounded-full bg-[#E2C275]";
          } else {
            btn.className =
              "overlay-toggle flex items-center justify-between px-3 py-2 rounded-xl text-xs font-medium border transition bg-white/5 border-white/10 text-slate-400";
            dot.className = "w-2 h-2 rounded-full bg-slate-600";
          }
          renderCraniometricCanvas();
        });
      });

      // Architectural Baseline Selector
      document.querySelectorAll(".pref-baseline").forEach((btn) => {
        btn.addEventListener("click", () => {
          appState.baseline = btn.dataset.value;
          document.querySelectorAll(".pref-baseline").forEach((b) => {
            const active = b === btn;
            const dot = b.querySelector("span:last-child");
            b.className = active
              ? "pref-baseline active py-2 px-3 rounded-xl text-xs font-semibold border border-[#E2C275]/50 bg-[#E2C275]/15 text-[#F2DA9B] text-left flex items-center justify-between transition"
              : "pref-baseline py-2 px-3 rounded-xl text-xs font-semibold border border-white/10 bg-white/5 text-slate-300 hover:bg-white/10 text-left flex items-center justify-between transition";
            dot.className = active ? "w-1.5 h-1.5 rounded-full bg-[#E2C275]" : "w-1.5 h-1.5 rounded-full bg-transparent";
          });
        });
      });

      // Primary Optimization Vector Selector
      document.getElementById("vectorSelect").addEventListener("change", (e) => {
        appState.vector = e.target.value;
      });

      // Run Gonion Diagnostic CTA
      document.getElementById("runDiagnosticBtn").addEventListener("click", runGonionDiagnostic);

      // Softmaxxing Protocol Tabs
      document.querySelectorAll(".plan-tab").forEach((tabBtn) => {
        tabBtn.addEventListener("click", () => renderPlanTab(tabBtn.dataset.tab));
      });

      // Copy Protocol
      document.getElementById("copyProtocolBtn").addEventListener("click", copyFullProtocol);

      // Gonion Consultant Chat
      document.getElementById("coachChatForm").addEventListener("submit", (e) => {
        e.preventDefault();
        sendConsultantMessage(document.getElementById("coachChatInput").value);
      });

      document.querySelectorAll(".quick-prompt").forEach((chip) => {
        chip.addEventListener("click", () => sendConsultantMessage(chip.textContent));
      });

      window.addEventListener("resize", resizeCanvas);
    });
  </script>
</body>
</html>
