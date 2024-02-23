<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modele AR cu Navigare</title>
    <script type="module" src="https://unpkg.com/@google/model-viewer"></script>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
        }
        .model-container {
            display: none;
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
        .navigation-buttons {
            text-align: center;
            margin-top: 20px;
        }
        button {
            display: inline-block;
            margin: 0 10px;
            padding: 5px 10px;
            font-size: 1rem;
            cursor: pointer;
            background-color: #007BFF;
            border: none;
            border-radius: 5px;
            color: white;
        }
        button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>

<div id="page1" class="model-container" style="display: flex;">
    <!-- Modele pentru prima pagină -->
    <!-- Model 1: Adidas -->
    <div class="model-section">
        <model-viewer src="adidas.glb" ios-src="adidas.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="1"></model-viewer>
    </div>
    <!-- Model 2: Jordan -->
    <div class="model-section">
        <model-viewer src="jordan.glb" ios-src="jordan.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="1"></model-viewer>
    </div>
    <!-- Model 3: Nike -->
    <div class="model-section">
        <model-viewer src="nike.glb" ios-src="nike.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="1"></model-viewer>
    </div>
</div>

<div id="page2" class="model-container">
    <!-- Modele pentru a doua pagină -->
    <!-- Model 4: Scaun -->
    <div class="model-section">
        <model-viewer src="scaun.glb" ios-src="scaun.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="1"></model-viewer>
    </div>
    <!-- Model 5: Noodle -->
    <div class="model-section">
        <model-viewer src="noodle.glb" ios-src="noodle.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="1"></model-viewer>
    </div>
</div>

<div class="navigation-buttons">
    <button onclick="showPage(1)">Pagina Anterioară</button>
    <button onclick="showPage(2)">Pagina Următoare</button>
</div>

<script>
    function showPage(pageNumber) {
        const page1 = document.getElementById('page1');
        const page2 = document.getElementById('page2');

        if (pageNumber === 1) {
            page1.style.display = 'flex';
            page2.style.display = 'none';
        } else if (pageNumber === 2) {
            page1.style.display = 'none';
            page2.style.display = 'flex';
        }
    }

    // Afișează inițial prima pagină
    showPage(1);
</script>

</body>
</html>
