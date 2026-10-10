# Technical architecture

## Runtime layers
1. **Presentation:** HTML HUD and responsive CSS.
2. **Rendering:** Three.js scene, camera, lighting, aquarium glass, reef geometry, voxel character, fish meshes.
3. **Simulation:** Frame-loop updates fish movement, attraction, bite timing, line tension, catches and timer.
4. **Input:** Pointer, keyboard and touch-friendly primary action.
5. **State:** `idle`, `ready`, `waiting`, `bite`, `reeling`, and `done` states.
6. **Delivery:** Vite creates a static `dist/` bundle; GitHub Actions deploys it to GitHub Pages.

## Extension seams
- Move fish behavior into `src/systems/FishSystem.js`.
- Replace procedural fish with licensed glTF models in `public/models/`.
- Add texture and audio assets beneath `public/`.
- Add Web Audio and accessibility settings.
- Keep any physical aquarium installation isolated from live fish and aquarium structure.

## Data flow
Input -> state machine -> gameplay simulation -> Three.js scene + HTML HUD -> browser renderer.
