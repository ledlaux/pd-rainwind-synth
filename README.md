# 🌧️ PD + WebAssembly + Web UI  
## Atmospheric Rain & Wind Sound Generator  

🔊 **Live Demo:**  
https://ledlaux.github.io/pd-rainwind-synth/

---

## Overview

This project explores the integration of **Pure Data (PD)**, **WebAssembly (Wasm)**, and **Web UI technologies** to create an interactive atmospheric rain and wind sound generator.

The synthesizer runs entirely in the browser using a high-performance DSP engine compiled from a PD patch into WebAssembly via Heavy (hvcc). The result is a responsive, low-latency procedural soundscape generator with reactive visuals.

---

## Technical Architecture

### 🎛 Sound Engine

The core synthesizer is based on an original [patch](https://youtu.be/ZXwk8sDts0Y) by Simple Trax and Taavi Viikman, adapted for WebAssembly compilation.

- Built in **Pure Data**
- Compiled using **Plugdata Compile Mode**
- Exported via **Heavy (hvcc)** to optimized C++
- Compiled into `.wasm` and `.js` binaries
- Executed inside a **WebAudio Worklet** for real-time performance

This ensures:

- Low-latency audio processing  
- Glitch-free playback  
- Stable performance even during UI animation updates  

---

### 🌩 Visual Engine

The background animation is a custom **HTML5 Canvas** rendering engine directly mapped to synthesizer parameters.

- Rain density affects particle intensity  
- Storm level influences animation dynamics  
- Visuals react in real-time to sound changes  

This creates a tightly coupled audio-visual experience.

---

### 🎚 User Interface (Gemini AI)

The UI follows a clean, minimalist approach:

- Custom CSS styling 
- Responsive layout  
- Intuitive parameter controls  

Sliders in the HTML interface are mapped to specific **MIDI CC values** defined in the PD patch.








