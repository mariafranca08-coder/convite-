<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Convite de Aniversário!</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .card {
            background: white;
            padding: 40px 30px;
            border-radius: 20px;
            box-shadow: 0 15px 30px rgba(0,0,0,0.2);
            text-align: center;
            max-width: 400px;
            width: 100%;
            animation: fadeIn 1s ease-in-out;
        }

        h1 {
            color: #764ba2;
            margin-bottom: 10px;
            font-size: 2rem;
        }

        p.subtitle {
            color: #666;
            margin-bottom: 25px;
            font-size: 1.1rem;
        }

        .info-box {
            background: #f7f7f7;
            padding: 15px;
            border-radius: 12px;
            margin-bottom: 25px;
            text-align: left;
        }

        .info-item {
            margin: 10px 0;
            color: #444;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .btn {
            background: #764ba2;
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 25px;
            font-size: 1rem;
            font-weight: bold;
            cursor: pointer;
            transition: transform 0.2s, background 0.2s;
            width: 100%;
        }

        .btn:hover {
            background: #5a3782;
            transform: scale(1.03);
        }

        .status {
            margin-top: 15px;
            font-weight: bold;
            color: #2e7d32;
            display: none;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>

    <div class="card">
        <h1>🎉 Você foi Convidado! ✨</h1>
        <p class="subtitle">Venha comemorar o meu aniversário!</p>

        <div class="info-box">
            <div class="info-item">📅 <strong>Data:</strong> 25 de Outubro</div>
            <div class="info-item">⏰ <strong>Horário:</strong> 19:00h</div>
            <div class="info-item">📍 <strong>Local:</strong> Minha Casa</div>
        </div>

        <button class="btn" onclick="confirmarPresenca()">Confirmar Presença 👍</button>
        <p id="mensagem" class="status">Presença confirmada! Te vejo lá! 🎈</p>
    </div>

    <script>
        function confirmarPresenca() {
            const mensagem = document.getElementById('mensagem');
            mensagem.style.display = 'block';
        }
    </script>

</body>
</html>