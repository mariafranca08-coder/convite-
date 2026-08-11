<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Convite Especial 🎂</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif, system-ui;
        }

        body {
            background: #0f172a;
            color: #f8fafc;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .container {
            background: #1e293b;
            border: 1px solid #334155;
            padding: 30px;
            border-radius: 24px;
            max-width: 420px;
            width: 100%;
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.5);
            text-align: center;
        }

        .badge {
            background: #f59e0b;
            color: #000;
            font-weight: bold;
            font-size: 0.8rem;
            padding: 4px 12px;
            border-radius: 20px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        h1 {
            margin-top: 15px;
            font-size: 1.8rem;
            color: #fff;
        }

        p.desc {
            color: #94a3b8;
            font-size: 0.95rem;
            margin-top: 5px;
            margin-bottom: 25px;
        }

        .detalhes {
            background: #0f172a;
            border-radius: 16px;
            padding: 15px;
            margin-bottom: 20px;
            display: flex;
            flex-direction: column;
            gap: 10px;
            text-align: left;
        }

        .detalhe-item {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 0.95rem;
            color: #cbd5e1;
        }

        .campo {
            text-align: left;
            margin-bottom: 15px;
        }

        .campo label {
            display: block;
            font-size: 0.85rem;
            color: #94a3b8;
            margin-bottom: 5px;
        }

        .campo input {
            width: 100%;
            padding: 12px 15px;
            border-radius: 12px;
            border: 1px solid #334155;
            background: #0f172a;
            color: #fff;
            font-size: 1rem;
            outline: none;
        }

        .campo input:focus {
            border-color: #3b82f6;
        }

        button {
            width: 100%;
            padding: 14px;
            border: none;
            border-radius: 12px;
            background: #3b82f6;
            color: white;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: 0.2s;
        }

        button:hover {
            background: #2563eb;
        }

        /* Cartão de Confirmação */
        .confirmacao-card {
            display: none;
            margin-top: 20px;
            padding: 15px;
            background: #166534;
            border: 1px solid #22c55e;
            border-radius: 12px;
            color: #f0fdf4;
            animation: surgir 0.3s ease;
        }

        @keyframes surgir {
            from { opacity: 0; transform: scale(0.95); }
            to { opacity: 1; transform: scale(1); }
        }
    </style>
</head>
<body>

    <div class="container">
        <span class="badge">Convite de Aniversário</span>
        <h1>Minha Festa! 🎉</h1>
        <p class="desc">Espero você para comemorar comigo!</p>

        <div class="detalhes">
            <div class="detalhe-item">📅 <span><strong>Data:</strong> 15 de Novembro</span></div>
            <div class="detalhe-item">⏰ <span><strong>Horário:</strong> 20:00h</span></div>
            <div class="detalhe-item">📍 <span><strong>Local:</strong> Salão de Festas</span></div>
        </div>

        <div class="campo">
            <label for="nome">Digite seu nome para confirmar:</label>
            <input type="text" id="nome" placeholder="Ex: Lucas Silva">
        </div>

        <button onclick="confirmar()">Confirmar Minha Presença</button>

        <div id="resultado" class="confirmacao-card">
            ✅ Presença de <strong id="nome-confirmado"></strong> confirmada com sucesso!
        </div>
    </div>

    <script>
        // COLOQUE SEU NÚMERO DE WHATSAPP AQUI (DDD + NÚMERO)
        const meuNumero = "5511999998888";

        function confirmar() {
            const inputNome = document.getElementById("nome");
            const nome = inputNome.value.trim();

            if (nome === "") {
                alert("Por favor, digite seu nome!");
                return;
            }

            // Mostra o cartão verde com o nome
            document.getElementById("nome-confirmado").innerText = nome;
            document.getElementById("resultado").style.display = "block";

            // Envia para o WhatsApp após 1 segundo
            const texto = encodeURIComponent(`Opa! Aqui é o(a) ${nome}, confirmando minha presença na sua festa! 🎉`);
            setTimeout(() => {
                window.open(`https://wa.me/${meuNumero}?text=${texto}`, '_blank');
            }, 1000);
        }
    </script>

</body>
</html>