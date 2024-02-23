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
            justify-content: space-between;
            margin: 20px auto;
            max-width: 1200px; /* Lărgimea totală a containerului */
        }
        .model-section {
            width: calc(33.333% - 10px); /* Trei pe rând, cu ajustare pentru spațiere */
            margin-bottom: 40px;
        }
        model-viewer {
            width: 100%;
            height: 200px;
        }
        .nav-button {
            cursor: pointer;
            background-color: #007BFF;
            border: none;
            border-radius: 20px;
            padding: 10px 20px;
            font-size: 16px;
            color: white;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
            transition: background-color 0.3s, box-shadow 0.3s;
        }
        .nav-button:hover {
            background-color: #0056b3;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
        }
        @keyframes levitate {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-10px);
            }
        }
        .levitate {
            display: inline-block;
            animation: levitate 1s ease-in-out infinite;
        }
    </style>
</head>
<body>

<div class="model-container">
    <!-- Model 1 -->
    <div class="model-section">
        <h2 style="text-align: center;"><a href="#" target="_blank">Cumpără acum Adidas Samba OG</a></h2>
        <h3>Adidas Samba OG "Cloud White"</h3>
        <model-viewer 
            src="adidas.glb" 
            ios-src="adidas.usdz" 
            ar 
            ar-modes="webxr scene-viewer quick-look" 
            camera-controls 
            auto-rotate 
            environment-image="neutral" 
            shadow-intensity="1" 
            alt="Adidas Samba OG"
            min-camera-orbit="auto 0deg 0deg" 
            max-camera-orbit="auto 80deg auto">
            <button slot="ar-button" class="ar-button">
                <span class="levitate">👋</span> Activează modul AR
            </button>
        </model-viewer>
    </div>
    <!-- Model 2 -->
    <div class="model-section">
        <h2 style="text-align: center;"><a href="#" target="_blank">Descoperă Noodle-ul nostru de top</a></h2>
        <h3>Noodle - Gust și Aromă Inegalabilă</h3>
        <model-viewer 
            src="noodle.glb" 
            ios-src="noodle.usdz" 
            ar 
            ar-modes="webxr scene-viewer quick-look" 
            camera-controls 
            auto-rotate 
            environment-image="neutral" 
            shadow-intensity="1" 
            alt="Noodle"
            min-camera-orbit="auto 0deg 0deg" 
            max-camera-orbit="auto 80deg auto">
            <button slot="ar-button" class="ar-button">
                <span class="levitate">👋</span> Activează modul AR
            </button>
        </model-viewer>
    </div>
    <!-- Model 3 -->
    <div class="model-section">
        <h2 style="text-align: center;"><a href="https://unfazed.ro/products/air-jordan-4-retro-se-craft-medium-olive" target="_blank">Cumpără acum Air Jordan 4 Retro</a></h2>
        <h3>Air Jordan 4 Retro SE Craft "Medium Olive"</h3>
        <model-viewer 
            src="jordan.glb" 
            ios-src="jordan.usdz" 
            ar 
            ar-modes="webxr scene-viewer quick-look" 
            camera-controls 
            auto-rotate 
            environment-image="neutral" 
            shadow-intensity="1" 
            alt="Air Jordan 4 Retro"
            min-camera-orbit="auto 0deg 0deg" 
            max-camera-orbit="auto 80deg auto">
            <button slot="ar-button" class="ar-button">
                <span class="levitate">👋</span> Activează modul AR
            </button>
        </title>
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
            justify-content: space-between;
            margin: 20px auto;
            max-width: 1200px; /* Mărit pentru a încăpea trei modele pe rând */
        }
        .model-section {
            width: 30%;
            margin-bottom: 40px;
            box-sizing: border-box; /* Asigură că paddingul și borderul sunt incluse în lățime */
            padding: 0 10px; /* Spațiu între modele */
        }
        model-viewer {
            width: 100%;
            height: 300px; /* Mărit pentru o vizualizare mai bună */
        }
        .content {
            max-width: 1200px;
            margin: auto;
            padding: 20px;
        }
        @keyframes levitate {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-10px);
            }
        }
        .levitate {
            display: inline-block;
            animation: levitate 1s ease-in-out infinite;
        }
    </style>
</head>
<body>

<div class="content">
    <div class="model-container">
        <!-- Modele pe primul rând -->
        <div class="model-section" id="model1"></div>
        <div class="model-section" id="model2"></div>
        <div class="model-section" id="model3"></div>
        <!-- Modele pe al doilea rând -->
        <div class="model-section" id="model4"></div>
        <div class="model-section" id="model5"></div>
    </div>
</div>

<script>
    const models = [
        { containerId: 'model1', file: "adidas.glb", iosFile: "adidas.usdz", title: "Cumpără acum Adidas Samba OG", url: "https://unfazed.ro/products/adidas-samba-og-cloud-white?_pos=1&_sid=6d480c095&_ss=r", subtitle: "Adidas Samba OG \"Cloud White\"" },
        { containerId: 'model2', file: "noodle.glb", iosFile: "noodle.usdz", title: "Descoperă Noodle-ul nostru de top", url: "#", subtitle: "Noodle - Gust și Aromă Inegalabilă" },
        { containerId: 'model3', file: "jordan.glb", iosFile: "jordan.usdz", title: "Cumpără acum Air Jordan 4 Retro", url: "https://unfazed.ro/products/air-jordan-4-retro-se-craft-medium-olive", subtitle: "Air Jordan 4 Retro SE Craft \"Medium Olive\"" },
        { containerId: 'model4', file: "nike.glb", iosFile: "nike.usdz", title: "Cumpără acum Nike Air Force 1", url: "https://unfazed.ro/products/nike-air-force-1-low-triple-white", subtitle: "Nike Air Force 1 Low \"Triple White\"" },
        { containerId: 'model5', file: "scaun.glb", iosFile: "scaun.usdz", title: "Descoperă noul nostru Scaun Confortabil", url: "#", subtitle: "Scaun Confortabil - Design Modern" }
    ];

    function createModelSection(model) {
        const section = document.createElement('div');
        section.innerHTML = `
            <h2 style="text-align: center;"><a href="${model.url}" target="_blank">${model.title}</a></h2>
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
                <button slot="ar-button" class="levitate">👋 Activează modul AR</button>
            </model-viewer>
        `;
        document.getElementById(model.containerId).appendChild(section);
    }

    models.forEach(createModelSection);
</script>

</body>
</html>
