<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
      background-image: url('fundal8.jpg');
      background-size: cover;
      background-position: center;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 90vh;
    }
    .model-container {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      margin-top: 50px;
    }
    .model-section {
      text-align: center;
      margin-bottom: 50px; /* Spațiere între model și butonul de navigare */
    }
    model-viewer {
      width: 200px;
      height: 300px;
      margin: 0 auto;
      border-radius: 80px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    }
    .ar-button {
      padding: 5px 10px; /* Ajustat pentru a face butonul mai mic */
      font-size: 0.8rem; /* Ajustat pentru a face textul mai mic */
      margin-top: 235px;
      background-color: #00c8ff;
      border: none;
      border-radius: 20px;
      color: white;
      cursor: pointer;
      transition: background-color 0.3s, box-shadow 0.3s;
    }
    .ar-button:hover {
      background-color: #0056b3;
    }
    .back-link {
      display: block;
      margin-top: 0px; /* Distanța de la model */
      text-decoration: none;
      color: white;
      background-color: #0056b3;
      padding: 10px 15px;
      border-radius: 20px;
      font-size: 0.9rem;
      transition: background-color 0.3s;
    }
    .back-link:hover {
      background-color: #0056b3;
    }
    p {
      color: #FFFFFF;
      font-size: 1.2em;
    }
  </style>
  <script type="module" src="https://unpkg.com/@google/model-viewer"></script>
</head>
<body>
<div class="model-container">
  <!-- Model -->
  <div class="model-section">
    <model-viewer
      src="AF1.glb"
      ios-src="AF1.usdz"
      ar
      ar-modes="webxr scene-viewer quick-look"
      camera-controls
      auto-rotate
      environment-image="neutral"
      shadow-intensity="1"
      loading="lazy"
      alt="Bag"
      min-camera-orbit="auto 0deg 0deg"
      max-camera-orbit="auto 80deg auto">
      <button slot="ar-button" class="ar-button">Activează modul AR</button>
    </model-viewer>
  </div>
  <a href="https://www.titi-valenti.ro/setul-duo-chic-black.html" class="back-link">Înapoi la pagină produs</a>
  <iframe src="https://steli.vercel.app/" title="Chatbot" style="width: 400px; height: 500px; border: none; border-radius: 10px; overflow: auto; position: fixed; bottom: 20px; right: 20px;"></iframe>
</div>
</body>
