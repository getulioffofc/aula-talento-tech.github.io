<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulário de Cadastro</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f9f9f9;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #3498db;
            color: white;
            text-align: center;
            padding: 20px;
        }

        section {
            display: flex;
            justify-content: center;
            padding: 20px;
        }

        .form-container {
            background-color: #ffffff;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            width: 300px;
        }

        .form-container input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        .form-container button {
            width: 100%;
            padding: 10px;
            background-color: #2ecc71;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .form-container button:hover {
            background-color: #27ae60;
        }
    </style>
</head>
<body>

<header>
    <h1>Cadastro de Usuário</h1>
</header>

<section>
    <div class="form-container">
        <form action="site2.html" method="GET" onsubmit="saveData(event)">
            <label for="nome">Nome:</label>
            <input type="text" id="nome" name="nome" required>

            <label for="idade">Idade:</label>
            <input type="number" id="idade" name="idade" required>

            <label for="estado">Estado:</label>
            <input type="text" id="estado" name="estado" required>

            <button type="submit">Entrar</button>
        </form>
    </div>
</section>

<script>
    function saveData(event) {
        event.preventDefault(); // Evita o envio do formulário

        // Armazena os dados no localStorage para acessar na próxima página
        const nome = document.getElementById("nome").value;
        const idade = document.getElementById("idade").value;
        const estado = document.getElementById("estado").value;

        localStorage.setItem("nome", nome);
        localStorage.setItem("idade", idade);
        localStorage.setItem("estado", estado);

        // Redireciona para o segundo site
        window.location.href = "site2.html";
    }
</script>

</body>
</html>

