# 📺 Retro Cartoon TV — Web Audio & CRT Render Engine

A zero-dependency, mobile-optimized Web Application built using single-file architectural principles, custom Web Audio synthesis, and GPU-accelerated CRT visual effects.

---

## 📌 Executive Summary

This project demonstrates an interactive, event-driven web application packaged in a single standalone HTML file. Engineered specifically to run natively in mobile web runtimes, it eliminates external asset dependencies, heavy bundlers, and external audio libraries. 

The application delivers retro visual aesthetics (Pop-Art / CRT TV) paired with programmatic 8-bit sound generation via the browser’s native Web Audio API.

---

## 🛠️ Architecture & Technical Highlights

### 1. Zero-Dependency Web Audio Synthesis
* **No MP3/WAV assets**: All sound effects (button clicks, TV static, dynamic action chimes) are synthesized programmatically at runtime using `AudioContext`.
* **Oscillator Pipeline**: Implemented custom envelope control (`gainNode.gain.exponentialRampToValueAtTime`) and frequency modulation using `triangle` and `sawtooth` waveforms to mimic vintage hardware sounds without network overhead.

### 2. Hardware-Accelerated CRT Rendering
* **CSS Layering Engine**: CRT scanlines, screen flicker, and curvature are achieved using lightweight CSS overlays (`repeating-linear-gradient`, `radial-gradient`, `mix-blend-mode`).
* **Performance**: Utilizes `will-change` properties and GPU-backed CSS transitions (`transform`, `opacity`) to guarantee steady 60 FPS transitions on mobile hardware without causing layout reflows or repaints.

### 3. State Management & Lifecycle
* **Reactive Channel Filtering**: Implements a clean state array with in-memory array manipulation for category filtering (`Jokes`, `Motivation`, `Prompts`).
* **Custom Dynamic Injection**: Real-time DOM mutation allowing users to push custom quotes directly into state while retaining category filter integrity.

### 4. Mobile-First Touch Target Engineering
* Designed entirely using relative units (`rem`, `vh/vw`, `flexbox`/`grid`) with generous tap targets exceeding standard accessibility guidelines (minimum 48px target bounds for touch interaction).

---

## 🚀 Quick Start / Local Setup

Because the application is entirely self-contained:

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/retro-cartoon-tv.git](https://github.com/your-username/retro-cartoon-tv.git)
   cd retro-cartoon-tv

 * Run locally:
   Open index.html directly in any modern desktop or mobile browser (Chrome, Safari, Firefox, Edge). No HTTP server or build step required.
🕹️ Features
 * Interactive CRT TV Interface: Dynamic channels, animated screen static, and analog channel knobs.
 *  Arcade Push Button: Tactile visual compression feedback coupled with instant Web Audio responses.
 * Category Channels: Switch seamlessly between global entries, humor, motivational quotes, and creative prompts.
 * Custom Quote Injector: Add personalized entries directly to the broadcast stream on the fly.
 * Comic Book Aesthetic: Halftone dots, dynamic action overlays (BAM!, KAPOW!), and custom pop-art speech bubbles.
🔮 Future Engineering Roadmap
 * [ ] Web Storage Persistence: Implement localStorage / IndexedDB sync to persist custom user-added quotes across sessions.
 * [ ] PWA Support: Add Service Workers and a Web App Manifest for full offline installation capability on mobile devices.
 * [ ] Canvas-Based CRT Effects: Transition static overlays to an HTML5 Canvas WebGL shader for advanced screen distortion and glow.
