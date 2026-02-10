<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Para ti mi amor ❤️</title>

    <meta property="og:title" content="Para Yahaira ❤️">
    <meta property="og:description" content="Tengo una pregunta muy importante para ti 😏💖">
    <meta property="og:type" content="website">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <style>
        body {
            margin: 0;
            font-family: 'Segoe UI', sans-serif;
            background: linear-gradient(135deg, #ff5f6d, #ffc371);
            color: white;
            text-align: center;
            overflow-x: hidden;
        }

        h1 {
            margin-top: 45px;
            font-size: 2.7em;
            animation: latido 1.3s infinite;
        }

        @keyframes latido {
            0% { transform: scale(1); }
            50% { transform: scale(1.08); }
            100% { transform: scale(1); }
        }

        .card {
            background: rgba(255,255,255,0.18);
            border-radius: 25px;
            padding: 30px;
            margin: 30px auto;
            width: 90%;
            max-width: 520px;
            box-shadow: 0 15px 35px rgba(0,0,0,0.25);
        }

        p {
            font-size: 1.1em;
            line-height: 1.6;
        }

        button {
            border: none;
            border-radius: 30px;
            padding: 15px 25px;
            font-size: 1.05em;
            cursor: pointer;
            margin: 10px;
            transition: 0.3s;
        }

        .btn-si {
            background: #ff3366;
            color: white;
        }

        .btn-si:hover {
            background: #ff0033;
            transform: scale(1.1);
        }

        .btn-no {
            background: #ffffff;
            color: #ff3366;
            position: relative;
        }

        .mensaje {
            display: none;
            margin-top: 25px;
            font-size: 1.15em;
            animation: aparecer 1s forwards;
        }

        @keyframes aparecer {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .heart {
            position: fixed;
            top: -10%;
            font-size: 20px;
            animation: caer 5s linear infinite;
            pointer-events: none;
        }

        @keyframes caer {
            0% { transform: translateY(0); opacity: 1; }
            100% { transform: translateY(120vh); opacity: 0; }
        }

        footer {
            margin: 35px 0 20px;
            font-size: 0.9em;
            opacity: 0.85;
        }
    </style>
</head>
<body>

    <h1>Hola mi bebita preciosa 💖</h1>

    <div class="card">
        <p>
            Hola, mi amor 😌  
            <br><br>
            Esta página es solo para ti, Yahaira.  
            Porque eres romántica, divertida  
            y porque contigo todo es mejor y paso los mejores momentos de mi vida 💕
        </p>

        <p><strong>Y ahora la pregunta importante…</strong> 😏</p>

        <h2>¿Quieres ser mi San Valentín? 💘</h2>

        <button class="btn-si" onclick="acepta()">Sí, obvio 💖</button>
        <button class="btn-no" onmouseover="moverNo()">No 🙄</button>

        <div class="mensaje" id="mensajeFinal">
            💕 SABÍA QUE DIRÍAS QUE SÍ 💕  
            <br><br>
            Gracias por elegirme,  
            por hacerme reír  
            y por ser mi persona favorita.
            <br><br>
            Te amo, Yahaira ❤️  
            <br>
            Feliz San Valentín 💘
        </div>
    </div>

    <footer>
        Hecho con amor solo para ti 💌
    </footer>

    <script>
        function acepta() {
            document.getElementById("mensajeFinal").style.display = "block";
        }

        function moverNo() {
            const btn = document.querySelector(".btn-no");
            const x = Math.random() * 200 - 100;
            const y = Math.random() * 200 - 100;
            btn.style.transform = `translate(${x}px, ${y}px)`;
        }

        function crearCorazon() {
            const corazon = document.createElement("div");
            corazon.classList.add("heart");
            corazon.innerHTML = Math.random() > 0.5 ? "❤️" : "💖";
            corazon.style.left = Math.random() * 100 + "vw";
            corazon.style.fontSize = Math.random() * 25 + 15 + "px";
            document.body.appendChild(corazon);

            setTimeout(() => corazon.remove(), 5000);
        }

        setInterval(crearCorazon, 250);
    </script>

</body>
</html>
