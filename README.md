# PassiveGuard — Interactive 3D Simulator

Team AWJ · MEDATHON 2026 · Track: Medical Tools & Devices Innovation

A single-file, offline-capable simulator of PassiveGuard, a battery-free mechanical early-warning indicator
(silicone membrane → lever → green / yellow / red). It covers two applications: IV Guardian (IV infiltration /
extravasation) and TraumaGate (vented chest seal).

**Live demo:** https://n1nfa.github.io/IV-passive-guard-/ (GitHub Pages, served from `main` / root).
You can also download `index.html` and open it in any modern browser; no server, install or internet is needed.

## What this is, and what it is not

- A digital prototype built from **calculations and published animal-study figures**. No bench tests have been run yet.
- Every input is tagged in the app by origin (published / calibrated / assumed). The banner
  "Calculated, not measured · no bench tests yet" stays visible on purpose.
- The skin-lift share (default 30 % of leaked volume) is calibrated to a swine study (Doughty 2016, "raised approximately 1 mm").
  There are no human volume-to-dome-height data.
- Outputs are not clinical results and must not be read as device performance.

## Physics used

- Swelling area from leaked volume: power law through two swine points (1 mL and 10 mL).
- Skin lift: spherical cap from a share of the leaked volume.
- Cantilever stiffness: k = 3EI/a³; tip travel amplified by the lever geometry.
- Chest seal: large-deflection membrane (Hencky) response to pressure; thresholds from swine data.

## Contents

- `index.html` — the whole simulator (three.js inlined).
