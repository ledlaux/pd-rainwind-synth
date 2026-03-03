## PD + webasembly + web ui

Athmosferic rain and wind sound generator


[Live Demo](https://ledlaux.github.io/pd-rainwind-synth/)


## Technical Overview ##

This project is a result of my exploration of Plugdata compile mode. It connects high-performance audio DSP with web technologies. By using Heavy (hvcc) - the PD patch is converted into highly optimized C++ and then compiled into WebAssembly.


## Key Features ##

Low-Latency Audio: Running the synth engine in a WebAudio Worklet ensures the audio remains glitch-free even when the UI is performing complex animations.

Visuals: The background animation is a custom HTML5 Canvas engine that is wired to the synth parameters. When you change the rain density or storm level, the visuals react.

UI: A clean, minimalist interface using CSS designed by Gemini AI.

## The Workflow ##

Sound Design:  Rain and wind synthesizer is an original [patch](https://youtu.be/ZXwk8sDts0Y) by Simple Trax and Taavi Viikman adapted by me for the hvcc compilation.  

Compilation: Exported from Plugdata via the Heavy compiler to generate the .js and .wasm binaries required for browser execution.  

UI Integration: GUI sliders where mapped to specific MIDI (CC) defined in the PD patch, creating a seamless bridge between the HTML front-end and the Wasm back-end.  
