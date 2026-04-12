# threejs-fbx-glb-poc

Side-by-side Three.js POC comparing FBX and GLB model loading — metrics, FPS, and export.

## Running locally

```bash
cd path/to/threejs-fbx-glb-poc
python3 -m http.server 8080
# then open http://localhost:8080
```

A local server is required — `fetch()` and the loaders don't work over `file://`.

## Models

| Canvas | Source |
|--------|--------|
| FBX    | `./client-fbx-assets/Imperial Avenue.fbx` (local, gitignored) |
| GLB    | `https://threejs.org/examples/models/gltf/Soldier.glb` (CDN) |

To swap models, edit the constants at the top of the `<script>` in `index.html`:

```js
const FBX_URL = './client-fbx-assets/Imperial Avenue.fbx';
const GLB_URL = 'https://threejs.org/examples/models/gltf/Soldier.glb';
```

## Metrics captured

File Size, Load Time, Parse Time, Time to First Render, Triangles, Draw Calls, Geometry/Texture Memory, Material Type, Animation Count, Bone Detection, Texture Count, Frame Time, FPS.

## Export

- **Export JSON** — downloads a `.json` report with all metrics
- **Copy Summary** — copies a plain-text table to clipboard