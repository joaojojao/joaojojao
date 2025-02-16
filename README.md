<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chokitos Login</title>
    <script src="https://www.google.com/recaptcha/api.js" async defer></script>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: #000;
            color: #fff;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            position: relative;
            overflow: hidden;
        }

        .container {
            text-align: center;
            background-color: #121212;
            padding: 20px;
            border-radius: 12px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5);
            max-width: 400px;
            width: 100%;
        }

        .container h1 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: #ff5733;
            animation: colorChange 3s infinite alternate;
        }

        @keyframes colorChange {
            0% {
                color: rgb(255, 87, 51); /* Red */
            }
            25% {
                color: rgb(255, 0, 204); /* Pink */
            }
            50% {
                color: rgb(0, 255, 255); /* Cyan */
            }
            75% {
                color: rgb(0, 255, 0); /* Green */
            }
            100% {
                color: rgb(255, 255, 0); /* Yellow */
            }
        }

        .container h1 span {
            color: #ff33a6;
        }

        .container img {
            width: 290px;
            height: auto;
            margin-bottom: 10px;
            border: 5px solid #ff33a6;
            border-radius: 8px;
        }

        .container p {
            font-size: 1.2rem;
            font-weight: bold;
            margin-bottom: 20px;
        }

        .container input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border-radius: 6px;
            border: 1px solid #333;
            background: #1c1c1c;
            color: #fff;
        }

        .container button {
            width: 100%;
            padding: 10px;
            background-color: #ff5733;
            border: none;
            border-radius: 6px;
            color: white;
            cursor: pointer;
            font-size: 1rem;
            margin-top: 10px;
        }

        .container button:hover {
            background-color: #ff7845;
        }

        .captcha {
            margin-top: 20px;
        }

        .links {
            margin-top: 20px;
        }

        .links a {
            color: #ff5733;
            text-decoration: none;
        }

        .links a:hover {
            text-decoration: underline;
        }

        @keyframes moveCat {
            0% {
                left: -100px;
            }
            50% {
                left: 50%;
                transform: translateX(-50%);
            }
            100% {
                left: 100%;
            }
        }

        .cat {
            position: absolute;
            top: 50%;
            width: 100px;
            animation: moveCat 10s linear infinite;
        }
    </style>
</head>
<body>
    <div class="container">
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRlEf88IywpQKi7ejEbNDXXOrbPvAYwtdXq0J6gIpjurnFRCMmF7ckAKSo&s=10" alt="">
        <h1>Dell Vale<span>🧃</span></h1>
        <p><strong>Sala do Bekas e da Dudinha</strong></p>

        <form action="/submit" method="post">
            <input type="text" name="ra" placeholder="Ex: 00011111sp" required>
            <input type="password" name="senha" placeholder="Digite sua senha" required>
            <input type="number" name="min_tempo" placeholder="Tempo Mínimo para cada Tarefa (EM MINUTOS)" min="1" required>
            <input type="number" name="max_tempo" placeholder="Tempo Máximo para cada Tarefa (EM MINUTOS)" min="2" required>

            <div class="g-recaptcha" data-sitekey="YOUR_SITE_KEY"></div>

            <button type="submit">Login</button>
        </form>

        <div class="links">
            <a href="#">Atividades Pendentes</a> |
            <a href="#">Atividades Expiradas</a>
        </div>

        <p>Entre no nosso grupo do whatsapp!</p>
    </div>

</body>
</html>
 
