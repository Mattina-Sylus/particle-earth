## Project Prompt: Particle Earth with Hand Gesture Control

**Goal:** Create a 3D particle-based Earth visualization with real-time hand gesture control using a webcam.

**Technical Requirements:**
- **Framework:** Three.js (r134 or later)
- **Hand Tracking:** MediaPipe Hands (with Camera Utils)
- **Rendering:** Custom GLSL shaders (vertex & fragment shaders)
- **Particle System:** 200,000+ particles
- **Color Palette:** Ocean blue (deep blue), Land (green/brown), Polar (white), Clouds (semi-transparent white), Atmosphere (light blue glow)

**Visual Features Required:**
1. **Earth Surface:** Particles distributed on a sphere with geographic color variation (ocean, land, poles).
2. **Atmosphere:** A layer of larger, semi-transparent blue particles around the edge.
3. **Clouds:** Dynamic white particles moving slightly faster than the surface to simulate flowing clouds.
4. **Starfield:** Background with twinkling stars and a subtle nebula/milky way effect.
5. **Distant Planets:** A few colored spheres in the background.

**Gesture Controls (MediaPipe):**
- **Rotation:** Hand horizontal position (hand[9].x) → Maps to 360° rotation (0 to 2*PI).
- **Scale:** Distance between thumb (hand[4]) and index finger (hand[8]) → Maps to zoom (0.15 to 2.5).
- **Tilt:** Hand vertical position (hand[9].y) → Maps to tilt angle (-0.6 to 1.0 radians).
- **Idle Mode:** When no hand is detected, the Earth should auto-rotate slowly.

**UI Requirements:**
- Title: "EARTH" in the top-left corner with a glass-morphism panel.
- Status text showing "Auto Cruise" or "Manual Control".
- Fullscreen button in the bottom-right.
- GitHub link in the top-right corner.

**Output:** A single, self-contained HTML file with all CSS and JavaScript embedded.
