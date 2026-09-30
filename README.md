# Park Master 3D

A cinematic 3D car parking game built with [three.js](https://threejs.org). Everything is in a single `index.html`: no build step, no assets to download.

## Play

- Open `index.html` in a modern browser (Chrome, Edge, Firefox, Safari). Three.js loads from a CDN, so you need an internet connection.
- Or serve it locally: `python3 -m http.server` and open http://localhost:8000
- Or enable **GitHub Pages** on this repo to get a shareable link.

## Controls

| Key | Action |
| --- | --- |
| `W` / `↑` | Accelerate (brakes while reversing) |
| `S` / `↓` | Brake, then reverse |
| `A` `D` / `←` `→` | Steer |
| `Space` | Handbrake (drifts, leaves skid marks) |
| `C` | Cycle camera: chase, drone, top-down, hood |
| `H` | Horn |
| `M` | Mute |
| `R` | Restart level |
| `Esc` / `P` | Pause |

On phones and tablets, on-screen touch controls appear automatically.

## How to park

Get all four corners inside the glowing bay, line up straight (on some levels the nose has to face the arrow), stop, and hold for a moment. You get 3 stars for a clean park under par time. Bumps and a slow time each cost a star. At 100% damage the car is wrecked.

## Levels

1. **First Steps**: nose-in bay parking
2. **Back It In**: reverse into a bay
3. **Parallel Pro**: parallel park on a live street with traffic that honks at you
4. **Pillar Garage**: tight bay between concrete pillars, with a cone slalom
5. **Midnight Angles**: 45° angled bay, with a patrol car in the lane

## Features

- Kinematic bicycle-model car physics with body pitch and roll, steering front wheels, and handbrake drifts
- Oriented-box (SAT) collisions: parked cars set off their alarms, cones get knocked over, sparks, screen shake, damage
- Cinematic fly-in for each level with letterbox bars, an orbit camera when you park, and confetti
- Night city with a sunset sky, lit windows, street lamps with volumetric light cones, real headlights, brake and reverse lights, and bloom
- Parking sensor that beeps faster as you get close, a live minimap, and parking guidance
- Fully synthesized audio (engine, tyre screech, crashes, horn, alarms, chimes), with no audio files
- Progress, stars, car colour and camera choice are saved in `localStorage`
