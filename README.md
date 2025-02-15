<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kalp Animasyonu</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f3f3f3;
            margin: 0;
            font-family: Arial, sans-serif;
            text-align: center;
            overflow: hidden;
        }
        #message {
            font-size: 30px;
            color: #333;
            opacity: 1;
            transition: opacity 2s ease-in-out;
        }
        .heart {
            position: absolute;
            font-size: 150px;
            color: red;
            animation: heartBeat 1s ease-in-out infinite;
            opacity: 0;
        }
        @keyframes heartBeat {
            0% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.3);
            }
            100% {
                transform: scale(1);
            }
        }
    </style>
</head>
<body>
    <div id="message">Seni seviyorum, iyi geceler</div>
    <div id="heart" class="heart">❤️</div>

    <script>
        window.onload = function() {
            setTimeout(function() {
                document.getElementById('message').style.opacity = '0';
                setTimeout(function() {
                    document.getElementById('heart').style.opacity = '1';
                }, 1000);
            }, 3000);
        }
    </script>
</body>
</html>
