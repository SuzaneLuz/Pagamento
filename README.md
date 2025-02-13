# Pagamento
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Página de Pagamento</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        .container {
            max-width: 400px;
            margin: auto;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 10px;
        }
        .form-group {
            margin-bottom: 15px;
        }
        .form-group label {
            display: block;
            margin-bottom: 5px;
        }
        .form-group input {
            width: 100%;
            padding: 8px;
            box-sizing: border-box;
        }
        .result {
            margin-top: 20px;
            font-weight: bold;
        }
        .link {
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Página de Pagamento</h2>
        <div class="form-group">
            <label for="nome">Nome:</label>
            <input type="text" id="nome">
        </div>
        <div class="form-group">
            <label for="valor">Valor por hora:</label>
            <input type="number" id="valor" step="0.01">
        </div>
        <div class="form-group">
            <label for="horas">Horas trabalhadas:</label>
            <input type="number" id="horas">
        </div>
        <button onclick="calcularPagamento()">Calcular Pagamento</button>
        </div>
    </div>
        

    <script>
        function calcularPagamento() {
            const nome = document.getElementById('nome').value;
            const valor = parseFloat(document.getElementById('valor').value);
            const horas = parseInt(document.getElementById('horas').value);
            const pagamento = valor * horas;
            document.getElementById('resultado').innerText = `O pagamento para ${nome} deve ser: R$ ${pagamento.toFixed(2)}`;
        }
    </script>
</body>
</html>
