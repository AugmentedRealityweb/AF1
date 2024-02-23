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
        p {
            margin-top: 10px; 
            color: #FFFFFF; 
            font-size: 1.2em; 
        }
        .navigation-links {
            display: flex;
            justify-content: center; /* Ajustat pentru a centra butonul */
            width: 100%;
            padding: 20px;
        }
        .navigation-link {
            text-decoration: none;
            color: white;
            background-color: #007BFF;
            padding: 10px 20px;
            border-radius: 20px;
            transition: background-color 0.3s;
        }
        .navigation-link:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>

<div class="model-container">
    <!-- Conținutul secțiunilor model rămâne neschimbat -->
</div>

<div class="navigation-links">
    <a href="https://augmentedrealityweb.github.io/toate-produsele/" class="navigation-link">Înapoi la meniul principal</a>
</div>

</body>
</html>
