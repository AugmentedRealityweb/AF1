<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modele AR Simplificate</title>
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
            height: 300px;
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

<div class="model-container" id="models"></div>

<script>
    const models = [
        { file: "adidas.glb", iosFile: "adidas.usdz" },
        { file: "noodle.glb", iosFile: "noodle.usdz" },
        { file: "jordan.glb", iosFile: "jordan.usdz" },
        { file: "nike.glb", iosFile: "nike.usdz" },
        { file: "scaun.glb", iosFile: "scaun.usdz" }
    ];

    models.forEach(model => {
        const modelSection = document.createElement('div');
        modelSection.classList.add('model-section');
        modelSection.innerHTML = `
            <model-viewer 
                src="${model.file}" 
                ios-src="${model.iosFile}" 
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
        `;
        document.getElementById('models').appendChild(modelSection);
    });
</script>

</body>
</html>
