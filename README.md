<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jornada do Meu Aniversário Especial</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f4f4f9;
            margin: 0;
            padding: 20px;
        }
        h1, h2 {
            color: #4CAF50;
        }
        p {
            font-size: 18px;
            color: #333;
            margin: 20px 0;
        }
        iframe {
            width: 100%;
            max-width: 720px;
            height: 405px;
            border: none;
            border-radius: 15px;
            margin: 20px 0;
        }
        button {
            padding: 15px 30px;
            font-size: 16px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
        #senha-container, #conteudo, #localizacao {
            display: none;
        }
        input[type="text"] {
            padding: 10px;
            font-size: 16px;
            border: 1px solid #ccc;
            border-radius: 5px;
            margin-right: 10px;
        }
    </style>
    <script>
        function iniciarJornada() {
            document.querySelector('#senha-container').style.display = 'block';
        }

        function verificarSenha() {
            const senha = document.querySelector('#senha').value;
            if (senha === "2017") {
                document.querySelector('#senha-container').style.display = 'none';
                document.querySelector('#conteudo').style.display = 'block';
            } else {
                alert("Senha incorreta. Tente novamente.");
            }
        }

        function verificarResposta() {
            const resposta = document.querySelector('#resposta').value.toLowerCase();
            if (resposta === "pequerrucha") {
                document.querySelector('#misterio').style.display = 'none';
                document.querySelector('#localizacao').style.display = 'block';
            } else {
                alert("Resposta incorreta. Tente novamente.");
            }
        }
    </script>
</head>
<body>
    <h1>Jornada do Meu Aniversário Especial</h1>
    <button onclick="iniciarJornada()">Iniciar Jornada</button>

    <div id="senha-container">
        <h2>Digite a senha para começar:</h2>
        <input type="text" id="senha" placeholder="Digite a senha">
        <button onclick="verificarSenha()">Enviar</button>
    </div>

    <div id="conteudo">
        <h2>Feliz Aniversário Kamilly</h2>
        <p>
            “Parabéns, Kamilly! Você passou pela primeira etapa da jornada e está cada vez mais perto da grande surpresa!
Eu fico muito feliz de ver você se divertindo com tudo isso. Cada detalhe foi pensado com amor, porque você merece todo o carinho do mundo.
        </p>

        <iframe 
            src="https://youtu.be/dvZMCnuNZOQ" 
            allowfullscreen>
        </iframe>

        <div id="misterio">
            <h2>Hora do Mistério</h2>
            <p>
                Entre tantos nomes que posso ganhar,  
                esse é único e faz meu coração vibrar.  
                Um apelido doce, cheio de ternura,  
                quem me chama assim só traz doçura.  
            </p>
            <input type="text" id="resposta" placeholder="Digite sua resposta">
            <button onclick="verificarResposta()">Enviar</button>
        </div>

        <div id="localizacao">
            <h2>Parabéns! 🎉</h2>
            <p>
                Envie uma mensagem para Any dizendo a seguinte frase 
                "<b>Pudim Amassado</b>" e poderá seguir sua jornada.
            </p>
        </div>
    </div>
</body>
</html>
