## PD + webasembly + javascript ui

Athmosferic rain and wind sound generator


[Live Demo](https://ledlaux.github.io/pd-rainwind-synth/)


## Technical Overview ##

This project bridges the gap between high-performance audio DSP (Digital Signal Processing) and modern web technologies. By using Heavy (hvcc)—the compiler behind PlugData's web export—the original Pure Data patch is converted into highly optimized C++ and then compiled into WebAssembly.

## Key Features ##

Low-Latency Audio: Running the synth engine in a WebAudio Worklet ensures the audio remains glitch-free even when the UI is performing complex animations.

Procedural Visuals: The background animation is a custom HTML5 Canvas engine that is "hard-wired" to the synth parameters. When you change the rain density or storm level, the visuals react in perfect sync with the sound.

Modern Glassmorphism UI: A clean, minimalist interface using CSS backdrop-filters and vertical faders to mimic high-end studio rack gear.

## The Workflow ##

Sound Design:  Rain and wind synthesizer is an original [patch](https://youtu.be/ZXwk8sDts0Y) by Simple Trax and Taavi Viikman adapted by me for the hvcc compilation.  

Compilation: Exported from Plugdata via the Heavy compiler to generate the .js and .wasm binaries required for browser execution.  

UI Integration: As I am not good at ui desing I asked a help from Gemini AI to make me a javascript web ui. GUI sliders where mapped to specific MIDI (CC) defined in the PD patch, creating a seamless bridge between the HTML front-end and the Wasm back-end.  
