---

## 🧬 Interactive 3D Explorer

Launch the web visualizer to inspect model structures and data points in dynamic 3D scenes.

<div align="center">
  <a href="https://tejas-c-0.github.io/AI-Research-Lab/3d-explorer/">
    <img src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=6,11,20&height=150&section=header&text=%E2%96%B6%20%20Launch%20the%203D%20Explorer&fontSize=36&fontColor=ffffff&animation=twinkling" alt="Launch the 3D explorer" width="100%">
  </a>
</div>

<br>

<details>
<summary><b>🛠️ Full Production Source Code: 3D Explorer (Copy to 3d-explorer/index.html)</b></summary>

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AI Research Lab - Interactive 3D Visualizer</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      user-select: none;
    }
    body {
      width: 100vw;
      height: 100vh;
      overflow: hidden;
      background-color: #060913;
      font-family: 'Fira Code', monospace, sans-serif;
      color: #e2e8f0;
    }
    #canvas-container {
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0;
      left: 0;
      z-index: 1;
    }
    #ui-layer {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 10;
      pointer-events: none;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      padding: 24px;
    }
    .interactive {
      pointer-events: auto;
    }
    header {
      background: rgba(10, 15, 29, 0.85);
      backdrop-filter: blur(12px);
      border: 1px solid rgba(109, 40, 217, 0.4);
      padding: 16px 24px;
      border-radius: 12px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      max-width: 1200px;
      margin: 0 auto;
      width: 100%;
      box-shadow: 0 8px 32px rgba(0, 0, 0, 0.5);
    }
    .title-group h1 {
      font-size: 1.25rem;
      color: #a78bfa;
      letter-spacing: 0.5px;
    }
    .title-group p {
      font-size: 0.8rem;
      color: #94a3b8;
      margin-top: 4px;
    }
    nav {
      display: flex;
      gap: 12px;
    }
    .scene-btn {
      background: rgba(26, 35, 126, 0.3);
      border: 1px solid rgba(167, 139, 250, 0.3);
      color: #cbd5e1;
      padding: 8px 16px;
      border-radius: 6px;
      cursor: pointer;
      font-size: 0.85rem;
      transition: all 0.25s ease;
    }
    .scene-btn:hover {
      background: rgba(109, 40, 217, 0.5);
      border-color: #a78bfa;
      color: #ffffff;
    }
    .scene-btn.active {
      background: #6d28d9;
      border-color: #a78bfa;
      color: #ffffff;
      box-shadow: 0 0 12px rgba(167, 139, 250, 0.5);
    }
    #info-card {
      position: absolute;
      bottom: 24px;
      left: 24px;
      width: 360px;
      background: rgba(10, 15, 29, 0.9);
      backdrop-filter: blur(12px);
      border: 1px solid rgba(32, 182, 139, 0.4);
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 8px 32px rgba(0, 0, 0, 0.6);
    }
    #info-card h2 {
      font-size: 1rem;
      color: #20b68b;
      margin-bottom: 8px;
    }
    #info-card p {
      font-size: 0.82rem;
      color: #cbd5e1;
      line-height: 1.5;
      white-space: pre-line;
    }
    #controls-hint {
      position: absolute;
      bottom: 24px;
      right: 24px;
      background: rgba(10, 15, 29, 0.7);
      border: 1px solid rgba(255, 255, 255, 0.1);
      padding: 12px 18px;
      border-radius: 8px;
      font-size: 0.75rem;
      color: #64748b;
      text-align: right;
    }
  </style>
  <script src="[https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js](https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js)"></script>
  <script src="[https://cdn.jsdelivr.net/npm/three@0.128.0/examples/js/controls/OrbitControls.js](https://cdn.jsdelivr.net/npm/three@0.128.0/examples/js/controls/OrbitControls.js)"></script>
</head>
<body>
  <div id="canvas-container"></div>
  <div id="ui-layer">
    <header class="interactive">
      <div class="title-group">
        <h1>🧬 AI Research Lab 3D Explorer</h1>
        <p>Interactive Spatial Representation of Models & Data</p>
      </div>
      <nav>
        <button class="scene-btn active" onclick="switchScene('network')">🧠 Neural Network</button>
        <button class="scene-btn" onclick="switchScene('pipeline')">🔬 Pipeline</button>
        <button class="scene-btn" onclick="switchScene('dataset')">🗂️ Vector Space</button>
      </nav>
    </header>

    <div id="info-card" class="interactive">
      <h2 id="card-title">🧠 Deep Neural Architecture</h2>
      <p id="card-desc">Click any node or object in the 3D space to inspect properties, activation values, and spatial gradients.</p>
    </div>

    <div id="controls-hint">
      Left Click + Drag: Rotate scene<br>
      Right Click + Drag: Pan view<br>
      Scroll Wheel: Zoom in/out
    </div>
  </div>

  <script>
    let scene, camera, renderer, controls, raycaster, mouse;
    let currentSceneType = 'network';
    let interactiveObjects = [];
    let pulseParticles = [];

    function init() {
      const container = document.getElementById('canvas-container');
      scene = new THREE.Scene();
      scene.fog = new THREE.FogExp2(0x060913, 0.008);

      camera = new THREE.PerspectiveCamera(60, window.innerWidth / window.innerHeight, 0.1, 1000);
      camera.position.set(0, 12, 32);

      renderer = new THREE.WebGLRenderer({ antialias: true, alpha: false });
      renderer.setPixelRatio(window.devicePixelRatio);
      renderer.setSize(window.innerWidth, window.innerHeight);
      renderer.toneMapping = THREE.ACESFilmicToneMapping;
      container.appendChild(renderer.domElement);

      controls = new THREE.OrbitControls(camera, renderer.domElement);
      controls.enableDamping = true;
      controls.dampingFactor = 0.05;
      controls.maxPolarAngle = Math.PI / 2 + 0.1;

      raycaster = new THREE.Raycaster();
      mouse = new THREE.Vector2();

      setupLighting();
      setupGrid();
      buildNetworkScene();

      window.addEventListener('resize', onWindowResize);
      window.addEventListener('click', onPointerClick);
      
      animate();
    }

    function setupLighting() {
      const ambientLight = new THREE.AmbientLight(0xffffff, 0.6);
      scene.add(ambientLight);

      const light1 = new THREE.PointLight(0x9876f5, 2, 80);
      light1.position.set(20, 30, 20);
      scene.add(light1);

      const light2 = new THREE.PointLight(0x20b68b, 2, 80);
      light2.position
