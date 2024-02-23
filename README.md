<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modele AR Optimizate</title>
    <script type="module" src="https://unpkg.com/@google/model-viewer"></script>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
        }
        .model-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            margin: 20px auto;
            max-width: 1200px;
        }
        .model-section {
            width: 30%;
            margin-bottom: 40px;
            box-sizing: border-box;
            padding: 0 10px;
        }
        model-viewer {
            width: 100%;
            height: 250px;
        }
        .ar-button {
            display: block;
            margin: 10px auto;
            padding: 5px 10px;
            font-size: 0.8rem;
            cursor: pointer;
            background-color: #007BFF;
            border: none;
            border-radius: 20px;
            color: white;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
            transition: background-color 0.3s, box-shadow 0.3s;
        }
        .ar-button:hover {
            background-color: #0056b3;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
        }
    </style>
</head>
<body>

<div class="model-container">
    <!-- Model 1: Adidas -->
    <div class="model-section">
        <model-viewer src="adidas.glb" ios-src="adidas.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="1" loading="lazy" reveal="auto">
            <button slot="ar-button" class="ar-button">Activează modul AR</button>
        </model-viewer>
    </div>
    <!-- Model 2: Jordan -->
    <div class="model-section">
        <model-viewer src="jordan.glb" ios-src="jordan.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="1" loading="lazy" reveal="auto">
            <button slot="ar-button" class="ar-button">Activează modul AR</button>
        </model-viewer>
    </div>
    <!-- Model 3: Nike -->
    <div class="model-section">
        <model-viewer src="nike.glb" ios-src="nike.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="1" loading="lazy" reveal="auto">
            <button slot="ar-button" class="ar-button">Activează modul AR</button>
        </model-viewer>
    </div>
    <!-- Model 4: Scaun -->
    <div class="model-section">
        <model-viewer src="scaun.glb" ios-src="scaun.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="1" loading="lazy" reveal="auto">
            <button slot="ar-button" class="ar-button">Activează modul AR</button>
        </model-viewer>
    </div>
    <!-- Model 5: Noodle -->
    <div class="model-section">
        <model-viewer src="noodle.glb" ios-src="noodle.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="1" loading="lazy" reveal="auto">
            <button slot="ar-button" class="ar-button">Activează modul AR</button>
        </model-viewer>
    </div>
</div>

</body>
</html>
