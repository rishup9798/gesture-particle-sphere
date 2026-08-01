# Particle Sphere — Gesture-Driven Point Field

A single-file, framework-free 3D particle sphere (3,000 points) controlled entirely by hand gestures via webcam. Built with [Three.js](https://threejs.org/) and [MediaPipe Hands](https://developers.google.com/mediapipe).

**[Live demo →](https://rishup9798.github.io/particle-sphere/particle-sphere.html)**


## Features

- **3,000 particles** distributed on a Fibonacci sphere, rendered with additive-blended WebGL points
- **One hand** — move your palm to translate and rotate the sphere in real time
- **Pinch and hold** (thumb + index finger) — charges a ring indicator; release to trigger a particle explosion that reforms back into a sphere
- **Two hands** — spread apart to grow the sphere, bring together to shrink it
- **Finger count** (0–5) — shifts the particle color across a six-color palette
- **Webcam background toggle** — overlay the live camera feed behind the particle field

## Tech stack

- [Three.js](https://threejs.org/) r128 — WebGL rendering
- [MediaPipe Hands](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker) — real-time hand landmark tracking
- Vanilla JS, HTML, CSS — no build step, no frameworks

## Running locally

Camera access requires a secure context, so opening the file directly (`file://`) won't work. Serve it locally instead:

```bash
# Python
python3 -m http.server 8000

# or Node
npx serve .
```

Then open `http://localhost:8000/particle-sphere.html` and allow camera access when prompted.

## Browser support

Requires a modern browser with WebGL and `getUserMedia` support (Chrome, Edge, Firefox). Some strict tracking-prevention settings or ad-blockers may block the CDN scripts — allow third-party scripts for this page if the sphere doesn't appear.

## License

MIT
