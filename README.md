<html lang="ro">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modele 3D și Iframe</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            margin: 0;
            background-image: url('fundal9.jpg');
            background-size: cover;
            background-position: center;
        }
        .model-container, .iframe-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            margin: 20px;
        }
        iframe {
            width: 90%; /* Se ajustează în funcție de preferințe */
            height: 480px;
            border: none;
            border-radius: 20px; /* Ajustează după preferințe */
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
        .ar-button {
            margin-top: 20px;
            padding: 10px 20px;
            font-size: 1rem;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 20px;
            cursor: pointer;
            transition: background-color 0.3s, box-shadow 0.3s;
        }
        .ar-button:hover {
            background-color: #0056b3;
        }
    </style>
    <script type="module" src="https://unpkg.com/@google/model-viewer"></script>
</head>
<body>

<div class="iframe-container">
    <iframe src="https://app.vectary.com/p/22JteF47kVh5ydhQz33Qwv"></iframe>
</div>

<div class="model-container">
    <model-viewer
        src="AF1.glb" ios-src="AF1.usdz"
        ar ar-modes="webxr scene-viewer quick-look"
        camera-controls auto-rotate
        environment-image="neutral" shadow-intensity="1"
        style="width: 90%; height: 480px; border-radius: 20px; box-shadow: 0 4px 8px rgba(0,0,0,0.2);"
        alt="Un model 3D">
    </model-viewer>
    <button class="ar-button">Activează modul AR</button>
</div>

</body>
</html>
