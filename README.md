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
            background: #1a0505;
            color: #f8fafc;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .container {
            background: #2d0a0a;
            border: 1px solid #7f1d1d;
            padding: 30px;
            border-radius: 24px;
            max-width: 420px;
            width: 100%;
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.7);
            text-align: center;
        }

        .badge {
            background: #dc2626;
            color: #ffffff;
            font-weight: bold;
            font-size: 0.8rem;
            padding: 6px 14px;
            border-radius: 20px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        h1 {
            margin-top: 15px;
            font-size: 1.8rem;
            color: #fca5a5;
        }

        p.desc {
            color: #fecaca;
            font-size: 0.95rem;
            margin-top: 8px;
            margin-bottom: 25px;
            line-height: 1.4;
        }

        .detalhes {
            background: #1a0505;
            border: 1px solid #450a0a;
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
            color: #fca5a5;
        }

        .campo {
            text-align: left;
            margin-bottom: 15px;
        }

        .campo label {
            display: block;
            font-size: 0.85rem;
            color: #fecaca;
            margin-bottom: 5px;
        }

        .campo input {
            width: 100%;
            padding: 12px 15px;
            border-radius: 12px;
            border: 1px solid #7f1d1d;
            background: #1a0505;
            color: #fff;
            font-size: 1rem;
            outline: none;
        }

        .campo input:focus {
            border-color: #ef4444;
        }

        button {
            width: 100%;
            padding: 14px;
            border: none;
            border-radius: 12px;
            background: #dc2626;
            color: white;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: 0.2s;
        }

        button:hover {
            background: #b91c1c;
        }

        .lista-presenca {
            margin-top: 25px;
            padding-top: 15px;
            border-top: 1px dashed #7f1d1d;
            text-align: left;
        }

        .lista-presenca h3 {
            font-size: 1rem;
            color: #fca5a5;
            margin-bottom: 10px;
        }

        .lista-presenca ul {
            list-style: none;
            max-height: 150px;
            overflow-y: auto;
        }

        .lista-presenca li {
            background: #1a0505;
            padding: 8px 12px;
            border-radius: 8px;
            margin-bottom: 6px;
            font-size: 0.9rem;
            color: #fecaca;
            border: 1px solid #450a0a;
        }
    </style>
</head>
<body>

    <div class="container">
        <span class="badge">Convite Especial</span>
        <h1>Aniversário da Maria 🎉</h1>
        <p class="desc">Você foi convidado(a) para celebrar essa data tão especial no aniversário da Maria! Venha comemorar com a gente!</p>

        <div class="detalhes">
            <div class="detalhe-item">📅 <span><strong>Data:</strong> 24 de Outubro</span></div>
            <div class="detalhe-item">⏰ <span><strong>Horário:</strong> 19:30h</span></div>
            <div class="detalhe-item">📍 <span><strong>Local:</strong> Salão de Festas Encantado</span></div>
        </div>

        <!-- Altere o atributo 'action' com a sua URL do Formspree se quiser receber por e-mail -->
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
                <!-- Os nomes salvos localmente aparecerão aqui -->
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

            // Salva a confirmação no navegador do usuário
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
            li.textContent = "✔️ " + nome;
            ul.appendChild(li);
        }
    </script>

</body>
</html>