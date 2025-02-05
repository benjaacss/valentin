# valentin
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¿Mi Conicita, quieres ser mi San Valentín?</title>
    <style>
        /* Estilos generales */
        body {
            margin: 0;
            font-family: 'Arial', sans-serif;
            text-align: center;
            color: white;
            overflow: hidden;
            background: linear-gradient(45deg, #ff758c, #ff7eb3, #ff95d9, #ffb6ff);
            background-size: 400% 400%;
            animation: fondoAnimado 10s infinite alternate;
        }

        /* Animación del fondo */
        @keyframes fondoAnimado {
            0% { background-position: 0% 50%; }
            100% { background-position: 100% 50%; }
        }

        .container {
            position: relative;
            margin-top: 15vh;
        }

        /* Imagen GIF */
        .gif-container img {
            width: 60%;
            max-width: 400px;
            border-radius: 20px;
            box-shadow: 0px 0px 15px rgba(255, 51, 102, 0.6);
            animation: aparecer 1.5s ease-in-out;
        }

        h1 {
            font-size: 2.8em;
            animation: aparecer 1.5s ease-in-out;
        }

        @keyframes aparecer {
            from { opacity: 0; transform: scale(0.8); }
            to { opacity: 1; transform: scale(1); }
        }

        p {
            font-size: 1.2em;
            margin-bottom: 30px;
        }

        /* Estilos de los botones */
        .button {
            background: linear-gradient(90deg, #ff3366, #ff6699);
            color: white;
            padding: 15px 40px;
            text-decoration: none;
            font-size: 1.5em;
            border-radius: 50px;
            margin: 10px;
            display: inline-block;
            position: relative;
            box-shadow: 0 0 15px rgba(255, 51, 102, 0.6);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .button:hover {
            transform: scale(1.1);
            box-shadow: 0 0 25px rgba(255, 51, 102, 0.9);
        }

        /* Corazones flotantes */
        .heart {
            position: absolute;
            font-size: 30px;
            color: #ff3366;
            opacity: 0.7;
            animation: flotar 5s linear infinite;
        }

        @keyframes flotar {
            from { transform: translateY(100vh) scale(1); opacity: 1; }
            to { transform: translateY(-10vh) scale(1.5); opacity: 0; }
        }

        /* Mensaje sorpresa cuando dice "Sí" */
        #mensaje-sorpresa {
            display: none;
            font-size: 2em;
            margin-top: 30px;
            animation: aparecer 1s ease-in-out;
        }
    </style>
</head>
<body>

    <div class="container">
        <div class="gif-container">
            <img src="https://elcomercio.pe/resizer/-blHzZbjC6G3mJwO6p7c-534_hs=/1200x0/smart/filters:format(jpeg):quality(75)/cloudfront-us-east-1.images.arcpublishing.com/elcomercio/PWE3D5RQRZE77IPMCUNZROVR7Q.gif" alt="San Valentín">
        </div>
        <h1>¿Mi Conicita, quieres ser mi San Valentín? 💖</h1>
        <p>Eres la persona más especial para mí, y este día no sería igual sin ti. ❤️</p>
        <a href="#" class="button" onclick="mostrarMensaje()">Sí 💕</a>
        <a href="#" class="button">No 💔</a>
        <div id="mensaje-sorpresa">¡Sabía que dirías que sí! 😍💖</div>
    </div>

    <!-- Corazones flotantes generados dinámicamente -->
    <script>
        function generarCorazones() {
            for (let i = 0; i < 15; i++) {
                let heart = document.createElement("div");
                heart.innerHTML = "❤️";
                heart.classList.add("heart");
                heart.style.left = Math.random() * 100 + "vw";
                heart.style.animationDuration = Math.random() * 3 + 4 + "s";
                document.body.appendChild(heart);
                setTimeout(() => { heart.remove(); }, 5000);
            }
        }
        setInterval(generarCorazones, 800);

        function mostrarMensaje() {
            document.getElementById("mensaje-sorpresa").style.display = "block";
        }
    </script>

</body>
</html>
