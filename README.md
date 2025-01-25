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
        <h2>Digite a senha para continuar</h2>
        <input type="text" id="senha" placeholder="Senha">
        <button onclick="verificarSenha()">Entrar</button>
    </div>

    <div id="conteudo">
        <h2>Feliz Aniversário, Kamilly!</h2>
        <p>Seja bem-vinda à jornada para comemorar mais um ano de vida. Você é muito especial, e para que saiba o quanto é importante, você irá dar início a um caminho onde encontrará todos aqueles que te desejam o melhor. Mas antes da revelação, terá que desvendar as charadas. Espero que se divirta muito! Tudo isso foi feito com muito carinho somente para você. Obrigado por ser luz na minha vida. Feliz 23 aninhos de vida!!! — Wallyson Nascimento.</p>
        
        <iframe src="https://www.youtube.com/embed/dvZMCnuNZOQ" allowfullscreen></iframe>
        
        <h2>Hora do Mistério</h2>
        <p>Entre tantos nomes que posso ganhar,  
           esse é único e faz meu coração vibrar.  
           Um apelido doce, cheio de ternura,  
           quem me chama assim só traz doçura.</p>
        <input type="text" id="resposta" placeholder="Resposta">
        <button onclick="verificarResposta()">Responder</button>
    </div>

    <div id="localizacao">
        <h2>Parabéns! Você acertou!</h2>
        <p>Envie uma mensagem para Lucas dizendo a seguinte frase: "Pôneis Malditos" e poderá seguir sua jornada.</p>
    </div>
</body>
</html>
