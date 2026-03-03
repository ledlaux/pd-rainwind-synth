# Atmospheric Rain & Wind Sound Generator  

  
 **Live Demo:**  
https://ledlaux.github.io/pd-rainwind-synth/
  


##  Overview

This project explores the integration of **Pure Data (PD)**, **WebAssembly (Wasm)**, and **Web UI technologies** to create an interactive rain and wind sound generator.

It runs entirely in the browser using a high-performance DSP engine compiled from a PD patch into WebAssembly via Heavy (hvcc). The result is a responsive, low-latency soundscape generator with reactive visuals.



##  Sound Engine

The core synthesis is based on an original [patch](https://youtu.be/ZXwk8sDts0Y) by Simple Trax and Taavi Viikman, adapted for hvcc.

- Built in **Pure Data**
- Compiled using **Plugdata Compile Mode**
- Exported via **Heavy (hvcc)** to optimized C++
- Compiled into `.wasm` and `.js` binaries
- Executed inside a **WebAudio Worklet** for real-time performance



##  User Interface (Gemini AI)

The UI follows a clean, minimalist approach. The background animation of rain is a custom **HTML5 Canvas**. Visuals react in real-time to some parameters. Sliders in the HTML interface are mapped to specific **MIDI CC values** defined in the PD patch. 






