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
        model-viewer {
            width: 100%;
            height: 300px;
        }
        .navigation {
            display: flex;
            justify-content: space-between;
            margin-top: 20px;
            padding: 0 20px;
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
        .content {
            max-width: 800px;
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
        .model-section {
            margin-bottom: 40px;
        }
    </style>
</head>
<body>

<div class="content">
    <div class="model-section">
        <h2 style="text-align: center;"><a id="mainTitle1" href="#" target="_blank">Titlu Produs</a></h2>
        <h3 id="subtitle1">Subtitlu Produs</h3>
        <model-viewer 
            id="modelViewer1" 
            src="adidas.glb" 
            ios-src="adidas.usdz" 
            ar 
            ar-modes="webxr scene-viewer quick-look" 
            camera-controls 
            auto-rotate 
            environment-image="neutral" 
            shadow-intensity="1" 
            alt="Produs"
            min-camera-orbit="auto 0deg 0deg" 
            max-camera-orbit="auto 80deg auto">
            <button slot="ar-button" class="ar-button">
                <span class="levitate">👋</span> Activează modul AR
            </button>
        </model-viewer>
    </div>
    <div class="model-section">
        <h2 style="text-align: center;"><a id="mainTitle2" href="#" target="_blank">Titlu Produs</a></h2>
        <h3 id="subtitle2">Subtitlu Produs</h3>
        <model-viewer 
            id="modelViewer2" 
            src="noodle.glb" 
            ios-src="noodle.usdz" 
            ar 
            ar-modes="webxr scene-viewer quick-look" 
            camera-controls 
            auto-rotate 
            environment-image="neutral" 
            shadow-intensity="1" 
            alt="Produs"
            min-camera-orbit="auto 0deg 0deg" 
            max-camera-orbit="auto 80deg auto">
            <button slot="ar-button" class="ar-button">
                <span class="levitate">👋</span> Activează modul AR
            </button>
        </model-viewer>
    </div>
</div>

<script>
    const modelViewer1 = document.getElementById('modelViewer1');
    const modelViewer2 = document.getElementById('modelViewer2');

    const models = [
        { viewer: modelViewer1, titleElementId: 'mainTitle1', subtitleElementId: 'subtitle1', file: "adidas.glb", iosFile: "adidas.usdz", title: "Cumpără acum Adidas Samba OG", url: "https://unfazed.ro/products/adidas-samba-og-cloud-white?_pos=1&_sid=6d480c095&_ss=r", subtitle: "Adidas Samba OG \"Cloud White\"", features: "" },
        { viewer: modelViewer2, titleElementId: 'mainTitle2', subtitleElementId: 'subtitle2', file: "noodle.glb", iosFile: "noodle.usdz", title: "Descoperă Noodle-ul nostru de top", url: "#", subtitle: "Noodle - Gust și Aromă Inegalabilă", features: "" }
    ];

    function updateModels() {
        models.forEach(model => {
            const viewer = model.viewer;
            const titleElement = document.getElementById(model.titleElementId);
            const subtitleElement = document.getElementById(model.subtitleElementId);

            viewer.src = model.file;
            viewer.setAttribute('ios-src', model.iosFile);
            viewer.alt = model.subtitle;
            titleElement.href = model.url;
            titleElement.textContent = model.title;
            subtitleElement.textContent = model.subtitle;
        });
    }

    updateModels();
</script>

</body>
</html>
