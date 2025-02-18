# meu_site_pl

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pergunta do Amor</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
        }
        .heart {
            color: red;
            font-size: 30px;
            position: absolute;
            animation: float 2s ease-in-out infinite;
        }
        @keyframes float {
            0% { transform: translateY(0); opacity: 1; }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0); opacity: 1; }
        }
    </style>
</head>
<body>
    <h1>Você me ama?</h1>
    <button onclick="addHeart()">Sim</button>
    <button onclick="alert('Resposta errada! 😢')">Não</button>
    <script>
        function addHeart() {
            let heart = document.createElement("div");
            heart.classList.add("heart");
            heart.innerHTML = "❤️";
            document.body.appendChild(heart);
            
            let x = Math.random() * window.innerWidth;
            let y = Math.random() * window.innerHeight;
            
            heart.style.left = `${x}px`;
            heart.style.top = `${y}px`;
        }
    </script>
</body>
</html>
