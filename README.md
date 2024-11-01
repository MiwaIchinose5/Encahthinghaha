<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> <title>Para Juan 💗</title>
    <style>
        /* Estilos básicos para centralizar o conteúdo */
        body, html {
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            font-family: Arial, sans-serif;
            background-color: #f0f8ff;
        }

        /* Pergunta no centro da tela */
        #question {
            font-size: 1.5em;
            text-align: center;
            cursor: pointer;
        }

        /* Contêiner escondido para a imagem e o botão */
        #response {
            display: none;
            text-align: center;
            margin-top: 20px;
        }

        /* Estilo para o botão */
        #yesButton {
            padding: 10px 20px;
            font-size: 1.2em;
            color: #fff;
            background-color: #ff69b4;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s ease;
            position: relative;
        }

        /* Imagem da garota */
        .chica {
            width: 150px;
            margin-top: 10px;
            display: block;
        }
    </style>
</head>
<body>

    <!-- Pergunta inicial -->
    <div id="question">Juan, ¿tú quieres estar conmigo en cada aventura para siempre?</div>

    <!-- Resposta que aparece após clicar na pergunta -->
    <div id="response">
        <img src="https://example.com/chica.png" alt="Chica" class="chica">
        <button id="yesButton">Sí💗</button>
    </div>

    <script>
        // Quando o usuário clica na pergunta, exibe a resposta
        document.getElementById('question').addEventListener('click', () => {
            document.getElementById('question').style.display = 'none';
            document.getElementById('response').style.display = 'block';
        });

        // Lógica para o botão "sí" se mover
        const yesButton = document.getElementById('yesButton');
        yesButton.addEventListener('mouseover', () => {
            // Calcula posições aleatórias dentro da tela
            const x = Math.random() * (window.innerWidth - yesButton.clientWidth);
            const y = Math.random() * (window.innerHeight - yesButton.clientHeight);
            yesButton.style.position = 'absolute';
            yesButton.style.left = `${x}px`;
            yesButton.style.top = `${y}px`;
        });
    </script>

</body>
</html>
