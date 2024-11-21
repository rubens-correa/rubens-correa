<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Conta Hackeada</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Arial', sans-serif;
            background: #000;
            color: #fff;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            overflow: hidden;
        }
        .container {
            text-align: center;
            animation: glitch 1.5s infinite;
        }
        .glitch-text {
            font-size: 3rem;
            font-weight: bold;
            color: red;
            text-transform: uppercase;
            position: relative;
        }
        .glitch-text:before, .glitch-text:after {
            content: attr(data-text);
            position: absolute;
            top: 0;
            left: 0;
            color: lime;
            width: 100%;
            overflow: hidden;
            clip-path: inset(0 0 50% 0);
            animation: glitch 1s infinite linear alternate-reverse;
        }
        .glitch-text:after {
            color: blue;
            clip-path: inset(50% 0 0 0);
        }
        @keyframes glitch {
            0%, 100% { transform: translate(0); }
            10% { transform: translate(-2px, -2px); }
            20% { transform: translate(2px, 2px); }
            30% { transform: translate(-2px, 2px); }
            40% { transform: translate(2px, -2px); }
        }
        .message {
            margin-top: 20px;
            font-size: 1.2rem;
            animation: flicker 1s infinite alternate;
        }
        @keyframes flicker {
            0%, 100% { opacity: 0.8; }
            50% { opacity: 1; }
        }
        .skull {
            font-size: 5rem;
            margin-bottom: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="skull">☠️</div>
        <div class="glitch-text" data-text="Conta Hackeada!">Conta Hackeada!</div>
        <div class="message">Todos os seus dados foram comprometidos.<br>Entre em contato para mais informações.</div>
    </div>
</body>
</html>
