# Split-Eye Mind Machine

A browser-based light-and-sound machine in the style of mind machines and Mindroid.
Each eye gets its own flicker frequency, images can be overlaid on the flashing
fields, and a binaural beat plays through headphones.

Open `index.html` in a browser (no build step). For the full effect, run it on a
phone inside a VR / Cardboard-style headset so each lens sees one half of the screen.

## Features
- **Independent eye frequencies** (0.5–40 Hz) plus a right-eye phase offset (180° = alternating flash).
- **Sigil charge program**: gaze at the sigil in alpha, descend to 6 Hz theta with it hidden, then a 1 s on / 1 s off signal, a steady charge where the flicker switches to the complementary colour at the same frequency, a fade-out release that turns the colour back, and the sigil stays hidden afterwards. All timings adjustable.
- **Programs** that ramp each eye over time (alpha, split alpha/theta, theta, beta focus, sleep) with a live chart.
- **Waveforms**: square (adjustable on-time), sine, triangle; per-eye colour and brightness; fade in/out.
- **Image overlay**: the default is a red sigil shown as black lines on red light. Load your own images, same image in both eyes, a different image per eye, or a side-by-side
  stereo pair. Recolour lines to any colour (optional solid background), flip line and light colours, choose steady / flash-with-light / dark-phase timing, blend mode, opacity, size and a crossfading slideshow.
- **Binaural audio** via Web Audio: carrier ± beat/2 per ear, beat derived from the eyes (average, difference,
  left, right) or set manually, with an optional pink-noise bed.
- **Headset options**: round field per lens, eye-spacing adjust, centre divider, fixation dot.
- Fullscreen and screen wake lock on start; settings are remembered locally.

Controls: tap the screen to show/hide the panel, Space to start/stop, Esc to stop, H to toggle the panel.

## Timing note
A screen can only show flicker up to half its refresh rate (30 Hz on a 60 Hz display, 60 Hz on 120 Hz).
The app measures your display and warns when a frequency exceeds that limit.

## Safety
Flashing light between roughly 3 and 30 Hz can trigger seizures in people with photosensitive epilepsy.
The app shows a warning before every first session. Don't use it if you or close family have a history
of seizures, and stop immediately if you feel unwell.
