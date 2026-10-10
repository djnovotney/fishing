# Fiji Pig Fishing

A playable browser prototype featuring an original voxel pig fisherman above a Fiji-inspired virtual aquarium. Catch five fish in four minutes.

## Folder structure

```
fiji-pig-fishing/
├── .github/workflows/deploy.yml  # GitHub Pages deployment
├── src/main.js                   # Scene, simulation, input, game loop
├── src/style.css                 # HUD and responsive styling
├── ARCHITECTURE.md               # Technical design and extension points
├── index.html                    # Browser entry point
├── package.json                  # Scripts and dependencies
└── vite.config.js                # Relative-path production build
```

## Run locally

1. Install Node.js 20 or newer.
2. In this folder, run `npm install`.
3. Run `npm run dev`.
4. Open the local address Vite prints.

## Put it on GitHub

1. Create an empty GitHub repository.
2. Upload every file and folder in this project, including `.github`.
3. Commit to the `main` branch.
4. In repository **Settings > Pages**, select **GitHub Actions** as the source.
5. The included workflow builds and publishes the game after each push to `main`.

## Controls

- Mouse or A/D: aim
- Click or Space: cast and hook
- Hold Click or Space: reel
- Release: lower line tension

## Production notes

This prototype uses procedural geometry so it runs without paid art assets. Replace it with properly licensed fish, reef, audio and texture assets as visual quality increases. The pig is an original voxel-style character, not a copied game asset.
