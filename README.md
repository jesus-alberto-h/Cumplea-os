<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¡Feliz Cumpleaños! 🎉</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Comic Sans MS', cursive, sans-serif;
            background: radial-gradient(circle, #ff9a9e 0%, #fecfef 100%);
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            color: white;
            text-align: center;
        }

        .container {
            background: rgba(0, 0, 0, 0.5);
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.3);
            position: relative;
            z-index: 1;
        }

        h1 {
            font-size: 4rem;
            color: #ffcc00;
            text-shadow: 0px 0px 10px #ff8800;
            animation: glow 2s infinite alternate;
        }

        p {
            font-size: 1.5rem;
            margin: 10px 0;
        }

        .cake img {
            width: 150px;
            margin: 20px 0;
            animation: bounce 2s infinite;
        }

        .date {
            font-size: 1.5rem;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 10px;
            padding: 10px;
            margin-top: 10px;
        }

        /* Animaciones */
        @keyframes glow {
            from { text-shadow: 0 0 10px #ff8800, 0 0 20px #ff8800; }
            to { text-shadow: 0 0 20px #ffcc00, 0 0 30px #ffcc00; }
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }

        /* Fuegos artificiales */
        .fireworks {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
        }

        .firework {
            position: absolute;
            border-radius: 50%;
            animation: explode 1.5s ease-out forwards, fade 1.5s ease-out forwards;
        }

        @keyframes explode {
            from { transform: scale(0); }
            to { transform: scale(1); }
        }

        @keyframes fade {
            from { opacity: 1; }
            to { opacity: 0; }
        }

        /* Globos */
        .balloon {
            position: absolute;
            bottom: -150px;
            width: 80px;
            height: 100px;
            background-color: #fff;
            border-radius: 50%;
            animation: float 8s ease-in-out infinite;
        }

        @keyframes float {
            0% { transform: translateY(0); }
            50% { transform: translateY(-500px); }
            100% { transform: translateY(0); }
        }

        .balloon:nth-child(1) { left: 10%; background-color: #ff6f61; animation-delay: 0s; }
        .balloon:nth-child(2) { left: 30%; background-color: #ffcc00; animation-delay: 2s; }
        .balloon:nth-child(3) { left: 50%; background-color: #66ff66; animation-delay: 4s; }
        .balloon:nth-child(4) { left: 70%; background-color: #66ccff; animation-delay: 6s; }
        .balloon:nth-child(5) { left: 90%; background-color: #ff66cc; animation-delay: 8s; }
    </style>
</head>
<body>
    <div class="container">
        <h1>¡Feliz Cumpleaños Dani!</h1>
        <p>¡Hoy 16 de septiembre, celebramos a México y tu cumpleaños! 🎉</p>
        <p>🎂 Te deseamos felíz cumpleamos, tu hermos familia. 🎂</p>

        <div class="cake">
            <!-- Aquí se mostrará la imagen aleatoria -->
            <img id="randomImage" alt="Pastel de cumpleaños">
        </div>

        <div class="date">
            <strong>16 de Septiembre</strong>
        </div>
    </div>

    <!-- Animación de fuegos artificiales -->
    <div class="fireworks">
        <div class="firework" style="top: 20%; left: 20%; width: 50px; height: 50px; background-color: #ffcc00;"></div>
        <div class="firework" style="top: 40%; left: 70%; width: 70px; height: 70px; background-color: #ff6f61;"></div>
        <div class="firework" style="top: 60%; left: 40%; width: 60px; height: 60px; background-color: #66ff66;"></div>
        <div class="firework" style="top: 10%; left: 60%; width: 80px; height: 80px; background-color: #66ccff;"></div>
    </div>

    <!-- Globos flotando -->
    <div class="balloon"></div>
    <div class="balloon"></div>
    <div class="balloon"></div>
    <div class="balloon"></div>
    <div class="balloon"></div>

    <!-- Script para cambiar imágenes aleatoriamente -->
    <script>
        // Array de URLs de imágenes
        const images = [
            "cumple.jpeg",
            "cumple2.jpeg",
            "cumple3.jpeg",
            "cumple4.jpeg",
            "cumple5.jpeg"
        ];

        // Función para seleccionar una imagen aleatoria
        function getRandomImage() {
            const randomIndex = Math.floor(Math.random() * images.length);
            return images[randomIndex];
        }

        // Asignar una imagen aleatoria al cargar la página
        const imageElement = document.getElementById("randomImage");
        imageElement.src = getRandomImage();

        // Cambiar la imagen cada 3 segundos
        setInterval(function() {
            imageElement.src = getRandomImage();
        }, 3000); // Cambiar cada 3000 milisegundos (3 segundos)
    </script>

</body>
</html>
