
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
            background-image: url('bkgd.jpg'); 
            background-size: cover; 
            background-position: center; 
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .model-container {
            display: flex;
            flex-direction: row; 
            align-items: center;
            justify-content: center; 
            flex-wrap: wrap; 
            width: 100%; 
            max-width: 400px; 
        }
        .model-section {
            margin: 10px;
            text-align: center; 
        }
        model-viewer {
            width: 200px; 
            height: 200px; 
            margin: 0 auto; 
        }
        .ar-button {
            display: flex;
            align-items: center;
            justify-content: center;
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
        .ar-button:before {
            content: '👉';
            display: inline-block;
            margin-right: 8px;
            animation: levitate 0.5s ease-in-out infinite alternate;
        }
        @keyframes levitate {
            from { transform: translateY(0); }
            to { transform: translateY(-5px); }
        }
        p {
            margin-top: 10px; 
            color: #FFFFFF; 
            font-size: 1.2em; 
        }
        .back-button {
            display: flex;
            justify-content: center;
            width: 100%;
            padding: 20px;
        }
        .back-link {
            text-decoration: none;
            color: white;
            background-color: #007BFF;
            padding: 10px 20px;
            border-radius: 20px;
            transition: background-color 0.3s;
        }
        .back-link:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>

<div class="model-container">
    <div class="model-section">
        <model-viewer 
            src="jordan.glb" 
            ios-src="jordan.usdz" 
            ar 
            ar-modes="webxr scene-viewer quick-look" 
            camera-controls 
            auto-rotate 
            environment-image="neutral" 
            shadow-intensity="1"
            min-camera-orbit="auto 0deg 0deg" 
            max-camera-orbit="auto 80deg auto">
            <button slot="ar-button" class="ar-button">Activează modul AR</button>
        </model-viewer>
        <p>Jordan Air 200E</p>
    </div>
    <div class="model-section">
        <model-viewer 
            src="adidas.glb" 
            ios-src="adidas.usdz" 
            ar 
            ar-modes="webxr scene-viewer quick-look" 
            camera-controls 
            auto-rotate 
            environment-image="neutral" 
            shadow-intensity="1"
            min-camera-orbit="auto 0deg 0deg" 
            max-camera-orbit="auto 80deg auto">
            <button slot="ar-button" class="ar-button">Activează modul AR</button>
        </model-viewer>
        <p>Nike Free Matcon</p>
    </div>
    <div class="model-section">
        <model-viewer 
            src="nike.glb" 
            ios-src="nike.usdz" 
            ar 
            ar-modes="webxr scene-viewer quick-look" 
            camera-controls 
            auto-rotate 
            environment-image="neutral" 
            shadow-intensity="1"
            min-camera-orbit="auto 0deg 0deg" 
            max-camera-orbit="auto 80deg auto">
            <button slot="ar-button" class="ar-button">Activează modul AR</button>
        </model-viewer>
        <p>Nike AirForce 1</p>
    </div>
</div>

<div class="back-button">
    <a href="https://augmentedrealityweb.github.io/toate-produsele/" class="back-link">Înapoi la meniul principal</a>
</div>

</body>
</html>
