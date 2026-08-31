<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Convite de Aniversário - Maria 🎂</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif, system-ui;
        }

        body {
            /* Fundo com estampa de flores elegante em tons escuros de vermelho */
            background-color: #2b0408;
            background-image: radial-gradient(#801323 1px, transparent 1px), radial-gradient(#801323 1px, #2b0408 1px);
            background-size: 40px 40px;
            background-position: 0 0, 20px 20px;
            color: #fff;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .container {
            background: linear-gradient(145deg, #5c0a15, #8a1023);
            border: 2px solid #ff4d6d;
            padding: 35px 25px;
            border-radius: 28px;
            max-width: 440px;
            width: 100%;
            box-shadow: 0 25px 35px rgba(0, 0, 0, 0.8), 0 0 20px rgba(239, 68, 68, 0.3);
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        /* Detalhes florais nos cantos em SVG */
        .flor-canto {
            position: absolute;
            width: 80px;
            opacity: 0.15;
            pointer-events: none;
        }

        .flor-top-left {
            top: -10px;
            left: -10px;
        }

        .flor-bottom-right {
            bottom: -10px;
            right: -10px;
            transform: rotate(180deg);
        }

        .badge {
            background: #ff4d6d;
            color: #ffffff;
            font-weight: 700;
            font-size: 0.85rem;
            padding: 6px 16px;
            border-radius: 20px;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            box-shadow: 0 4px 10px rgba(255, 77, 109, 0.4);
            display: inline-block;
        }

        h1 {
            margin-top: 15px;
            font-size: 2rem;
            color: #fff;
            text-shadow: 0 2px 4px rgba(0,0,0,0.5);
        }

        p.desc {
            color: #ffe5ec;
            font-size: 0.95rem;
            margin-top: 8px;
            margin-bottom: 25px;
            line-height: 1.5;
        }

        /* Cartão de Detalhes com Borda Ondulada (Wavy Border) */
        .detalhes {
            background: #3d050d;
            border-radius: 20px;
            padding: 20px;
            margin-bottom: 25px;
            display: flex;
            flex-direction: column;
            gap: 12px;
            text-align: left;
            position: relative;
            /* Efeito de borda recortada/ondulada nos topos */
            border: 2px dashed #ff758f;
        }

        .detalhe-item {
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 0.95rem;
            color: #ffb3c1;
        }

        .detalhe-item strong {
            color: #fff;
        }

        .campo {
            text-align: left;
            margin-bottom: 15px;
        }

        .campo label {
            display: block;
            font-size: 0.85rem;
            color: #ffe5ec;
            margin-bottom: 6px;
        }

        .campo input {
            width: 100%;
            padding: 14px 16px;
            border-radius: 14px;
            border: 1px solid #ff4d6d;
            background: #2b0408;
            color: #fff;
            font-size: 1rem;
            outline: none;
            transition: 0.3s;
        }

        .campo input:focus {
            border-color: #ff758f;
            box-shadow: 0 0 10px rgba(255, 117, 143, 0.5);
        }

        button {
            width: 100%;
            padding: 15px;
            border: none;
            border-radius: 14px;
            background: linear-gradient(135deg, #ff4d6d, #c9184a);
            color: white;
            font-size: 1.05rem;
            font-weight: 700;
            cursor: pointer;
            transition: 0.3s;
            box-shadow: 0 6px 15px rgba(201, 24, 74, 0.4);
        }

        button:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 20px rgba(251, 111, 146, 0.6);
        }

        .lista-presenca {
            margin-top: 25px;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.15);
            text-align: left;
        }

        .lista-presenca h3 {
            font-size: 1rem;
            color: #ffb3c1;
            margin-bottom: 12px;
        }

        .lista-presenca ul {
            list-style: none;
            max-height: 140px;
            overflow-y: auto;
        }

        .lista-presenca li {
            background: rgba(43, 4, 8, 0.6);
            padding: 10px 14px;
            border-radius: 10px;
            margin-bottom: 8px;
            font-size: 0.9rem;
            color: #ffe5ec;
            border: 1px solid rgba(255, 77, 109, 0.3);
        }
    </style>
</head>
<body>

    <div class="container">
        <!-- Elementos decorativos florais -->
        <svg class="flor-canto flor-top-left" viewBox="0 0 100 100" fill="#ffffff">
            <path d="M50,0 C60,30 70,40 100,50 C70,60 60,70 50,100 C40,70 30,60 0,50 C30,40 40,30 50,0 Z" />
        </svg>
        <svg class="flor-canto flor-bottom-right" viewBox="0 0 100 100" fill="#ffffff">
            <path d="M50,0 C60,30 70,40 100,50 C70,60 60,70 50,100 C40,70 30,60 0,50 C30,40 40,30 50,0 Z" />
        </svg>

        <span class="badge">Convite Especial</span>
        <h1>Aniversário da Maria 🌸</h1>
        <p class="desc">Você foi convidado(a) para celebrar esse dia tão especial! Sua presença vai deixar a festa ainda mais completa.</p>

        <div class="detalhes">
            <div class="detalhe-item">📅 <span><strong>Data:</strong> 24 de Outubro</span></div>
            <div class="detalhe-item">⏰ <span><strong>Horário:</strong> 19:30h</span></div>
            <div class="detalhe-item">📍 <span><strong>Local:</strong> Salão de Festas Encantado</span></div>
        </div>

        <form id="form-presenca" action="https://formspree.io/f/SEU_ID_AQUI" method="POST" onsubmit="confirmar(event)">
            <div class="campo">
                <label for="nome">Digite seu nome para confirmar:</label>
                <input type="text" id="nome" name="nome" placeholder="Ex: Lucas Silva" required>
            </div>

            <button type="submit">Confirmar Minha Presença</button>
        </form>

        <div class="lista-presenca">
            <h3>Presenças Confirmadas ✨</h3>
            <ul id="lista-nomes">
                <!-- Nomes confirmados aparecerão aqui -->
            </ul>
        </div>
    </div>

    <script>
        document.addEventListener("DOMContentLoaded", carregarNomes);

        function confirmar(event) {
            const inputNome = document.getElementById("nome");
            const nome = inputNome.value.trim();

            if (nome === "") {
                event.preventDefault();
                alert("Por favor, digite seu nome!");
                return;
            }

            let convidados = JSON.parse(localStorage.getItem("convidados_maria")) || [];
            convidados.push(nome);
            localStorage.setItem("convidados_maria", JSON.stringify(convidados));

            adicionarNaLista(nome);
            alert("Presença confirmada com sucesso!");
        }

        function carregarNomes() {
            let convidados = JSON.parse(localStorage.getItem("convidados_maria")) || [];
            convidados.forEach(nome => adicionarNaLista(nome));
        }

        function adicionarNaLista(nome) {
            const ul = document.getElementById("lista-nomes");
            const li = document.createElement("li");
            li.textContent = "🌸 " + nome;
            ul.appendChild(li);
        }
    </script>

</body>
</html>