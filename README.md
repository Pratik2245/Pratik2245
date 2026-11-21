<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 950 360" width="100%" height="100%">
  <defs>
    <!-- Background Gradients -->
    <radialGradient id="bgGlow1" cx="20%" cy="30%" r="60%">
      <stop offset="0%" stop-color="#0284c7" stop-opacity="0.35"/>
      <stop offset="100%" stop-color="#030712" stop-opacity="0"/>
    </radialGradient>
    <radialGradient id="bgGlow2" cx="80%" cy="50%" r="55%">
      <stop offset="0%" stop-color="#7c3aed" stop-opacity="0.3"/>
      <stop offset="60%" stop-color="#0f172a" stop-opacity="0"/>
    </radialGradient>
    <radialGradient id="orbGlow3" cx="65%" cy="75%" r="40%">
      <stop offset="0%" stop-color="#10b981" stop-opacity="0.2"/>
      <stop offset="100%" stop-color="#030712" stop-opacity="0"/>
    </radialGradient>

    <!-- Glass Gradients -->
    <linearGradient id="glassBg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#ffffff" stop-opacity="0.08"/>
      <stop offset="100%" stop-color="#ffffff" stop-opacity="0.02"/>
    </linearGradient>
    <linearGradient id="glassBorder" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#38bdf8" stop-opacity="0.6"/>
      <stop offset="50%" stop-color="#818cf8" stop-opacity="0.2"/>
      <stop offset="100%" stop-color="#c084fc" stop-opacity="0.5"/>
    </linearGradient>

    <linearGradient id="chipBorder" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#ffffff" stop-opacity="0.3"/>
      <stop offset="100%" stop-color="#ffffff" stop-opacity="0.05"/>
    </linearGradient>

    <!-- Text Gradients -->
    <linearGradient id="titleGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#f8fafc"/>
      <stop offset="40%" stop-color="#e0f2fe"/>
      <stop offset="80%" stop-color="#7dd3fc"/>
      <stop offset="100%" stop-color="#c084fc"/>
    </linearGradient>

    <!-- 3D Cube Gradients -->
    <linearGradient id="cubeTop" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#38bdf8" stop-opacity="0.85"/>
      <stop offset="100%" stop-color="#0284c7" stop-opacity="0.55"/>
    </linearGradient>
    <linearGradient id="cubeLeft" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%" stop-color="#0369a1" stop-opacity="0.75"/>
      <stop offset="100%" stop-color="#082f49" stop-opacity="0.95"/>
    </linearGradient>
    <linearGradient id="cubeRight" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%" stop-color="#6366f1" stop-opacity="0.75"/>
      <stop offset="100%" stop-color="#312e81" stop-opacity="0.95"/>
    </linearGradient>

    <!-- Filters -->
    <filter id="glassDropShadow" x="-10%" y="-10%" width="130%" height="130%">
      <feDropShadow dx="0" dy="16" stdDeviation="20" flood-color="#000000" flood-opacity="0.65"/>
    </filter>
    <filter id="neonCyanGlow" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="10" result="blur"/>
      <feComposite in="SourceGraphic" in2="blur" operator="over"/>
    </filter>
    <filter id="softGlow">
      <feGaussianBlur stdDeviation="3" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <!-- Cyber Isometric Grid -->
    <pattern id="isometricGrid" width="40" height="40" patternUnits="userSpaceOnUse">
      <path d="M 40 0 L 0 40 M 0 0 L 40 40" fill="none" stroke="#334155" stroke-width="0.75" stroke-opacity="0.22"/>
      <circle cx="20" cy="20" r="1" fill="#38bdf8" fill-opacity="0.3"/>
    </pattern>
  </defs>

  <style>
    @keyframes floatSlow {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-8px); }
    }
    @keyframes floatReverse {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(6px); }
    }
    @keyframes pulsePulse {
      0%, 100% { opacity: 0.6; r: 3.5; }
      50% { opacity: 1; r: 5; }
    }
    .floating-card { animation: floatSlow 6s ease-in-out infinite; }
    .floating-cube { animation: floatReverse 7s ease-in-out infinite; }
    .pulsing-dot { animation: pulsePulse 2.5s ease-in-out infinite; }
  </style>

  <!-- Container -->
  <rect width="950" height="360" rx="20" fill="#030712"/>
  <rect width="950" height="360" rx="20" fill="url(#isometricGrid)"/>

  <!-- Ambient Light -->
  <rect width="950" height="360" rx="20" fill="url(#bgGlow1)"/>
  <rect width="950" height="360" rx="20" fill="url(#bgGlow2)"/>
  <rect width="950" height="360" rx="20" fill="url(#orbGlow3)"/>

  <!-- Outer Glass Border -->
  <rect x="1.5" y="1.5" width="947" height="357" rx="18.5" fill="none" stroke="url(#glassBorder)" stroke-width="1.5"/>

  <!-- Left: Hero Content -->
  <g transform="translate(50, 42)">
    <rect width="215" height="30" rx="15" fill="#0f172a" fill-opacity="0.7" stroke="#38bdf8" stroke-width="1" stroke-opacity="0.4"/>
    <circle cx="16" cy="15" r="4" fill="#38bdf8" class="pulsing-dot" filter="url(#softGlow)"/>
    <text x="30" y="19" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif" font-size="11" font-weight="600" fill="#7dd3fc" letter-spacing="1">SYSTEM ARCHITECT &amp; DEV</text>
  </g>

  <g transform="translate(50, 115)">
    <text font-family="'Orbitron', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif" font-size="44" font-weight="900" letter-spacing="1.5" fill="url(#titleGrad)" filter="url(#glassDropShadow)">
      PRATIK PAITHANKAR
    </text>
  </g>

  <g transform="translate(50, 150)">
    <text font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif" font-size="17" font-weight="500" fill="#94a3b8">
      Building scalable <tspan fill="#38bdf8" font-weight="700">Android</tspan>, modern <tspan fill="#818cf8" font-weight="700">Full-Stack</tspan> &amp; intelligent <tspan fill="#c084fc" font-weight="700">AI Systems</tspan>
    </text>
  </g>

  <g transform="translate(50, 178)">
    <text font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif" font-size="13" font-weight="400" fill="#64748b">
      Turning complex engineering challenges into fluid, aesthetic, real-world solutions.
    </text>
  </g>

  <!-- Glass Tech Chips -->
  <g transform="translate(50, 222)">
    <!-- Mobile Chip -->
    <g transform="translate(0, 0)">
      <rect width="135" height="42" rx="12" fill="url(#glassBg)" stroke="url(#chipBorder)" stroke-width="1" filter="url(#glassDropShadow)"/>
      <rect x="0" y="0" width="135" height="42" rx="12" fill="#0284c7" fill-opacity="0.08"/>
      <circle cx="24" cy="21" r="9" fill="#0369a1" fill-opacity="0.4"/>
      <path d="M21 16 H27 V26 H21 Z" fill="none" stroke="#38bdf8" stroke-width="1.8" stroke-linecap="round"/>
      <circle cx="24" cy="24" r="0.8" fill="#38bdf8"/>
      <text x="42" y="25" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif" font-size="13" font-weight="600" fill="#e0f2fe">Android &amp; Flutter</text>
    </g>

    <!-- MERN Chip -->
    <g transform="translate(148, 0)">
      <rect width="125" height="42" rx="12" fill="url(#glassBg)" stroke="url(#chipBorder)" stroke-width="1" filter="url(#glassDropShadow)"/>
      <rect x="0" y="0" width="125" height="42" rx="12" fill="#10b981" fill-opacity="0.08"/>
      <circle cx="24" cy="21" r="9" fill="#047857" fill-opacity="0.4"/>
      <path d="M20 18 L17 21 L20 24 M28 18 L31 21 L28 24" fill="none" stroke="#34d399" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/>
      <text x="42" y="25" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif" font-size="13" font-weight="600" fill="#d1fae5">MERN Stack</text>
    </g>

    <!-- AI & Systems Chip -->
    <g transform="translate(286, 0)">
      <rect width="150" height="42" rx="12" fill="url(#glassBg)" stroke="url(#chipBorder)" stroke-width="1" filter="url(#glassDropShadow)"/>
      <rect x="0" y="0" width="150" height="42" rx="12" fill="#8b5cf6" fill-opacity="0.08"/>
      <circle cx="24" cy="21" r="9" fill="#6d28d9" fill-opacity="0.4"/>
      <circle cx="21" cy="18" r="1.5" fill="#c084fc"/>
      <circle cx="27" cy="18" r="1.5" fill="#c084fc"/>
      <circle cx="24" cy="24" r="1.5" fill="#c084fc"/>
      <path d="M21 18 L24 24 L27 18" stroke="#c084fc" stroke-width="1.2"/>
      <text x="42" y="25" font-family="-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif" font-size="13" font-weight="600" fill="#ede9fe">AI &amp; Systems</text>
    </g>
  </g>

  <!-- Prompt Line -->
  <g transform="translate(50, 305)">
    <text font-family="'Fira Code', 'Courier New', monospace" font-size="12" fill="#64748b">
      <tspan fill="#38bdf8">pratik@github:~$</tspan> git commit -m "Crafting scalable, user-first experiences" <tspan fill="#34d399">✓</tspan>
    </text>
  </g>

  <!-- Right: 3D Floating Isometric Glass Card -->
  <g class="floating-card" transform="translate(680, 160)">
    <ellipse cx="20" cy="20" rx="140" ry="110" fill="#38bdf8" fill-opacity="0.18" filter="url(#neonCyanGlow)"/>
    <ellipse cx="60" cy="-30" rx="110" ry="90" fill="#a855f7" fill-opacity="0.18" filter="url(#neonCyanGlow)"/>

    <!-- Glass Foundation -->
    <path d="M -90 40 L 90 -40 L 140 10 L -40 90 Z" fill="#0f172a" fill-opacity="0.6" stroke="url(#glassBorder)" stroke-width="1.5"/>

    <!-- 3D Isometric Acrylic Cube -->
    <g class="floating-cube">
      <path d="M 0 -70 L 65 -35 L 0 0 L -65 -35 Z" fill="url(#cubeTop)" stroke="#7dd3fc" stroke-width="1.2" stroke-opacity="0.9"/>
      <path d="M -65 -35 L 0 0 L 0 75 L -65 40 Z" fill="url(#cubeLeft)" stroke="#38bdf8" stroke-width="1.2" stroke-opacity="0.6"/>
      <path d="M 0 0 L 65 -35 L 65 40 L 0 75 Z" fill="url(#cubeRight)" stroke="#818cf8" stroke-width="1.2" stroke-opacity="0.6"/>

      <g transform="translate(0, -35)">
        <polygon points="0,-16 14,-8 14,8 0,16 -14,8 -14,-8" fill="#ffffff" fill-opacity="0.2" stroke="#ffffff" stroke-width="1.2"/>
        <text text-anchor="middle" y="5" font-family="'Orbitron', sans-serif" font-size="14" font-weight="900" fill="#ffffff">&lt;/&gt;</text>
      </g>
    </g>

    <!-- Floating 3D Satellites -->
    <g transform="translate(-100, -50)">
      <rect width="64" height="64" rx="16" fill="url(#glassBg)" stroke="#3ddc84" stroke-width="1.5" stroke-opacity="0.7" filter="url(#glassDropShadow)"/>
      <circle cx="32" cy="32" r="20" fill="#10b981" fill-opacity="0.15"/>
      <path d="M 23 34 A 9 9 0 0 1 41 34 Z" fill="#3ddc84"/>
      <circle cx="27" cy="30" r="1.2" fill="#030712"/>
      <circle cx="37" cy="30" r="1.2" fill="#030712"/>
      <line x1="26" y1="23" x2="24" y2="21" stroke="#3ddc84" stroke-width="1.5" stroke-linecap="round"/>
      <line x1="38" y1="23" x2="40" y2="21" stroke="#3ddc84" stroke-width="1.5" stroke-linecap="round"/>
      <text x="32" y="54" text-anchor="middle" font-family="-apple-system, sans-serif" font-size="9" font-weight="700" fill="#a7f3d0">ANDROID</text>
    </g>

    <g transform="translate(85, -75)">
      <rect width="64" height="64" rx="16" fill="url(#glassBg)" stroke="#38bdf8" stroke-width="1.5" stroke-opacity="0.7" filter="url(#glassDropShadow)"/>
      <circle cx="32" cy="32" r="20" fill="#0284c7" fill-opacity="0.15"/>
      <polygon points="38,20 28,30 38,40 44,40 34,30 44,20" fill="#38bdf8"/>
      <polygon points="34,36 28,42 34,48 40,48 34,42 40,36" fill="#0284c7"/>
      <text x="32" y="56" text-anchor="middle" font-family="-apple-system, sans-serif" font-size="9" font-weight="700" fill="#bae6fd">FLUTTER</text>
    </g>

    <g transform="translate(60, 65)">
      <rect width="64" height="64" rx="16" fill="url(#glassBg)" stroke="#c084fc" stroke-width="1.5" stroke-opacity="0.7" filter="url(#glassDropShadow)"/>
      <circle cx="32" cy="32" r="20" fill="#7c3aed" fill-opacity="0.15"/>
      <circle cx="32" cy="30" r="4" fill="#c084fc"/>
      <circle cx="24" cy="24" r="2.5" fill="#a855f7"/>
      <circle cx="40" cy="24" r="2.5" fill="#a855f7"/>
      <circle cx="32" cy="40" r="2.5" fill="#a855f7"/>
      <line x1="32" y1="30" x2="24" y2="24" stroke="#c084fc" stroke-width="1.2"/>
      <line x1="32" y1="30" x2="40" y2="24" stroke="#c084fc" stroke-width="1.2"/>
      <line x1="32" y1="30" x2="32" y2="40" stroke="#c084fc" stroke-width="1.2"/>
      <text x="32" y="55" text-anchor="middle" font-family="-apple-system, sans-serif" font-size="9" font-weight="700" fill="#f3e8ff">AI CORE</text>
    </g>

    <path d="M -60 -20 Q -20 0 0 -20" fill="none" stroke="#38bdf8" stroke-width="1.5" stroke-dasharray="3 3" stroke-opacity="0.6"/>
    <path d="M 60 -40 Q 30 -10 20 -15" fill="none" stroke="#818cf8" stroke-width="1.5" stroke-dasharray="3 3" stroke-opacity="0.6"/>
    <path d="M 50 50 Q 20 40 10 20" fill="none" stroke="#c084fc" stroke-width="1.5" stroke-dasharray="3 3" stroke-opacity="0.6"/>
  </g>

  <!-- Highlight Rim -->
  <path d="M 30 2 L 920 2" stroke="#ffffff" stroke-width="1" stroke-opacity="0.25" stroke-linecap="round"/>
</svg>
