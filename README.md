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
            background-image: url('bkgd.jpg'); /* Schimbă imaginea de fundal */
            background-size: cover; /* Asigură-te că imaginea de fundal acoperă întreaga pagină */
            background-position: center; /* Centrează imaginea de fundal */
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .model-container {
            display: flex;
            flex-direction: row; /* Schimbat în row pentru aliniere orizontală */
            align-items: center;
            justify-content: center; /* Centrarea pe orizontală */
            flex-wrap: wrap; /* Permite modelelor să treacă pe rândul următor dacă nu încap */
            width: 100%; /* Asigură că containerul ocupă lățimea ecranului */
            max-width: 1000px; /* O limită maximă pentru a menține design-ul organizat */
        }
        .model-section {
            margin: 20px;
            text-align: center; /* Centrarea textului sub modele */
        }
        model-viewer {
            width: 200px; /* Dimensiunea a fost setată la 200px */
            height: 200px; /* Înălțimea a fost setată la 200px */
            margin: 0 auto; /* Centrarea modelului */
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
            from {
                transform: translateY(0);
            }
            to {
                transform: translateY(-5px);
            }
        }
        p {
            margin-top: 10px; /* Spațiu între buton și text */
            color: #FFFFFF; /* Culoarea textului, alegeți o culoare care se potrivește cu fundalul */
            font-size: 1.2em; /* Mărimea textului */
        }
    </style>
</head>
<body>

<div class="model-container">
    <!-- Model 2: Jordan (Acum pe prima poziție) -->
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
    <!-- Model 1: Adidas (Acum pe a doua poziție) -->
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
    <!-- Model 3: Nike (Rămâne pe a treia poziție) -->
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

</body>
</html>
