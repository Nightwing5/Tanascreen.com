<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tanascreen | Media Collective & Systems</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Header & Navigation -->
    <header>
        <nav class="container">
            <div class="brand-text">TANASCREEN</div>
            <ul class="nav-links">
                <li><a href="#about">Systems</a></li>
                <li><a href="#film">Film Unit</a></li>
                <li><a href="#music">The Risevibe</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Showcase Section -->
    <section class="hero container">
        <!-- Tanascreen Main Logo Asset -->
        <img src="logo.png" alt="Tanascreen Logo" class="main-logo">
        <h1>Tanascreen</h1>
        <p class="subtitle">Production | Music Label | Information Systems</p>
        <p class="tagline">A tech-driven media collective unifying cinema, audio engineering, and digital pipeline automation.</p>
        <a href="#film" class="btn">Explore Portfolio</a>
    </section>

    <!-- Film Portfolio Grid -->
    <section id="film" class="portfolio-section container">
        <h2>🎥 Film Production</h2>
        <div class="grid">
            <div class=" card video-card">
                <div class="media-placeholder">Music Video Placeholder</div>
                <h3>The Risevibe Session #1</h3>
                <p>Shot entirely on manual mobile hardware. Directed by Tanascreen.</p>
            </div>
            <div class=" card video-card">
                <div class="media-placeholder">Commercial Placeholder</div>
                <h3>Brand Visualizer</h3>
                <p>Post-production and color grading handled in DaVinci Resolve.</p>
            </div>
        </div>
    </section>

    <!-- Music Label Component (The Risevibe) -->
    <section id="music" class="music-section container">
        <h2>🎵 The Risevibe Label</h2>
        <p>Independent campus audio distribution and sync licensing infrastructure.</p>
        <div class="grid">
            <div class=" card audio-card">
                <div class="audio-player-mock">🔊 Audio Streaming Engine</div>
                <h3>Artist Track Title</h3>
                <p>Distributed worldwide via RouteNote networks.</p>
            </div>
        </div>
    </section>

    <!-- Footer Systems Tag -->
    <footer>
        <p>&copy; 2026 Tanascreen Collective. Powered by your-username.github.io</p>/* --- 2003 Cyberpunk Style Resets & Palettes --- */
:root {
    --matrix-green: #00ff66;
    --dark-void: #030303;
    --neon-glow: rgba(0, 255, 102, 0.4);
    --vintage-amber: #ffb300;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Courier New', Courier, monospace;
    overflow: hidden;
}

body {
    background-color: var(--dark-void);
    height: 100vh;
    width: 100vw;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
}

.intro-container {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    position: relative;
    z-index: 5;
}

/* --- CRT Screen Glass Distortion Filter Layers --- */
.crt-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: radial-gradient(circle, transparent 50%, rgba(0, 0, 0, 0.75) 100%);
    z-index: 20;
    pointer-events: none;
}

.scanlines {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(rgba(18, 16, 16, 0) 50%, rgba(0, 0, 0, 0.35) 50%), linear-gradient(90deg, rgba(255, 0, 0, 0.04), rgba(0, 255, 0, 0.01), rgba(0, 0, 255, 0.04));
    background-size: 100% 4px, 6px 100%;
    z-index: 21;
    pointer-events: none;
}

/* --- Diagnostic Terminal Text Module --- */
.boot-terminal {
    width: 80%;
    max-width: 600px;
    color: var(--matrix-green);
    font-size: 0.9rem;
    text-shadow: 0 0 6px var(--neon-glow);
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
}

.boot-terminal p {
    white-space: nowrap;
    width: 0;
    overflow: hidden;
    animation: typing 0.6s steps(40, end) forwards;
}

.boot-terminal p:nth-child(2) { animation-delay: 0.8s; }
.boot-terminal p:nth-child(3) { animation-delay: 1.6s; }
.boot-terminal p:nth-child(4) { animation-delay: 2.4s; }

.status-success {
    color: #ffffff;
    background: var(--matrix-green);
    color: #000;
    font-weight: bold;
    padding: 0 0.3rem;
}

/* --- Main Glitch Title Card Configuration --- */
.title-card-wrapper {
    text-align: center;
    opacity: 0;
    transform: scale(1.3);
    transition: all 0.5s cubic-bezier(0.19, 1, 0.22, 1);
}

.glitch-title {
    font-size: 5rem;
    font-weight: 900;
    color: #ffffff;
    letter-spacing: 8px;
    position: relative;
    text-shadow: 0 0 20px rgba(255, 255, 255, 0.3);
    animation: masterGlitch 3s infinite linear alternate-reverse;
}

.sub-title {
    font-size: 0.8rem;
    letter-spacing: 6px;
    color: var(--vintage-amber);
    margin-top: 1rem;
    text-transform: uppercase;
}

/* --- Vintage MP3 Player Interface Panel --- */
.mp3-player-ui {
    position: absolute;
    bottom: 10%;
    width: 320px;
    border: 1px solid #333;
    background: #0d0d0d;
    padding: 0.8rem;
    opacity: 0;
    transition: opacity 1s ease-in-out 0.5s;
    border-radius: 4px;
}

.player-header {
    font-size: 0.65rem;
    color: #888;
    margin-bottom: 0.5rem;
}

.progress-track {
    width: 100%;
    height: 6px;
    background: #1a1a1a;
    border: 1px solid #222;
    margin-bottom: 0.4rem;
}

.progress-fill {
    height: 100%;
    width: 0;
    background: var(--matrix-green);
    animation: trackBuffer 10s linear infinite;
}

.bitrate-tag {
    font-size: 0.55rem;
    color: var(--matrix-green);
    text-align: right;
}

/* --- Falling Stream Line Grid Noise --- */
.network-grid {
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    z-index: 1;
    opacity: 0.15;
}

.grid-stream-line {
    position: absolute;
    color: var(--matrix-green);
    font-size: 0.7rem;
    writing-mode: vertical-rl;
    text-orientation: upright;
    transform: translateY(-100%);
    animation: fallStream linear infinite;
}

/* --- Keyframe Animation Definitions --- */
@keyframes typing {
    from { width: 0 }
    to { width: 100% }
}

@keyframes fallStream {
    0% { transform: translateY(-100%); }
    100% { transform: translateY(100vh); }
}

@keyframes trackBuffer {
    0% { width: 0%; }
    100% { width: 100%; }
}

@keyframes masterGlitch {
    0% {
        text-shadow: 2px -1px 0 #ff00c1, -2px 2px 0 #00fff0;
    }
    15% {
        text-shadow: -3px 2px 0 #ff00c1, 3px -1px 0 #00fff0;
    }
    30% {
        transform: skewX(0deg);
    }
    31% {
        transform: skewX(-10deg);
        text-shadow: 4px -3px 0 #00ff66;
    }
    32% {
        transform: skewX(5deg);
    }
    35% {
        transform: skewX(0deg);
    }
    100% {
        text-shadow: 1px -2px 0 #ff00c1, -1px 1px 0 #00fff0;
    }
}

    </footer>

</body>
</html>
