# GGS separator digital twin

A 3D digital twin of the GGS inlet separator (V-101) and crude-oil transfer pump (P-201), built for our group research project on petroleum anomaly detection.

**Open it:** https://oshan-paul.github.io/ggs-digital-twin/

## What it shows

- The separator, pump, piping and both gas detectors in 3D. Drag to orbit, scroll to zoom, click any equipment for its readings and properties.
- Five live sensor tags: separator pressure (PT-101), fluid temperature (TT-101), pump vibration (VT-201), H₂S (AT-301) and methane (AT-302).
- 15 simulated runs: normal operation, and gas leak, pressure drop, overpressure and pump fault at subtle, moderate and severe levels.
- The scores from both models (Isolation Forest v1 and LSTM autoencoder v1) and the resulting alert level, with a timeline you can scrub.

## Where the numbers come from

The sensor values are the team's synthetic telemetry (generator v2, 10-second readings). The model scores on this page were recorded by streaming each run through the team's FastAPI service. The equipment geometry and tag numbers are illustrative, not to scale.

## Live scoring on your own machine

With the main project installed, run `run_twin.bat` from the project folder. It starts the anomaly API and opens the twin at `http://localhost:8600`, where every reading is scored live by the models instead of replayed.

Proof of concept on simulated data. Not a safety system.
