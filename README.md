<!DOCTYPE html>
<html lang="eng">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Produse de calitate superioară</title>
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
            justify-content: space-around; /* Modificat pentru a centra modelele pe pagina */
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
        .content {
            max-width: 1200px;
            margin: auto;
            padding: 20px;
        }
        h2, h3 {
            margin: 10px 0; /* Redus pentru a economisi spațiu */
            font-size: 0.9rem; /* Text mai mic pentru titlu și subtitlu */
            text-align: center;
        }
        .ar-button {
            display: block;
            margin: 10px auto;
            padding: 5px 10px;
            font-size: 0.8rem; /* Text mai mic pentru buton */
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

<div class="content">
    <div class="model-container" id="models"></div>
</div>

<script>
    const models = [
        { id: 'model1', file: "adidas.glb", iosFile: "adidas.usdz", title: "Cumpără acum Adidas Samba OG", url: "https://unfazed.ro/products/adidas-samba-og-cloud-white?_pos=1&_sid=6d480c095&_ss=r", subtitle: "Adidas Samba OG \"Cloud White\"" },
        { id: 'model2', file: "noodle.glb", iosFile: "noodle.usdz", title: "Descoperă Noodle-ul nostru de top", url: "#", subtitle: "Noodle - Gust și Aromă Inegalabilă" },
        { id: 'model3', file: "jordan.glb", iosFile: "jordan.usdz", title: "Cumpără acum Air Jordan 4 Retro", url: "https://unfazed.ro/products/air-jordan-4-retro-se-craft-medium-olive", subtitle: "Air Jordan 4 Retro SE Craft \"Medium Olive\"" },
        { id: 'model4', file: "nike.glb", iosFile: "nike.usdz", title: "Cumpără acum Nike Air Force 1", url: "https://unfazed.ro/products/nike-air-force-1-low-triple-white", subtitle: "Nike Air Force 1 Low \"Triple White\"" },
        { id: 'model5', file: "scaun.glb", iosFile: "scaun.usdz", title: "Descoperă noul nostru Scaun Confortabil", url: "#", subtitle: "Scaun Confortabil - Design Modern" }
    ];

    models.forEach(model => {
        const modelSection = document.createElement('div');
        modelSection.classList.add('model-section');
        modelSection.innerHTML = `
            <h2><a href="${model.url}" target="_blank">${model.title}</a></h2>
            <h3>${model.subtitle}</h3>
            <model-viewer 
                src="${model.file}" 
                ios-src="${model.iosFile}" 
                ar 
                ar-modes="webxr scene-viewer quick-look" 
                camera-controls 
                auto-rotate 
                environment-image="neutral" 
                shadow-intensity="1" 
                alt="${model.subtitle}"
                min-camera-orbit="auto 0deg 0deg" 
                max-camera-orbit="auto 80deg auto">
                <button slot="ar-button" class="ar-button">👋 Activează modul AR</button>
            </model-viewer>
        `;
        document.getElementById('models').appendChild(modelSection);
    });
</script>

</body>
</html>
