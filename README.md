<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Для Арины!!!!!</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-image: url('https://i.pinimg.com/736x/76/54/bc/7654bc59ae93ff0292fe5fe6ee1bd09f.jpg');
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            text-align: center;
        }
        img {
            max-width: 50%;
            margin: 20px 0;
        }
        iframe {
            width: 100%;
            height: 100%;
            max-width: 80%;
            max-height: 80%;
            margin: 20px 0;
            border: none;
            display: none; /* Видео изначально скрыто */
        }
        p {
            font-size: 1.2em;
            color: #333;
            background-color: rgba(255, 255, 255, 0.8);
            padding: 10px;
            border-radius: 5px;
        }
        button {
            font-size: 1.2em;
            padding: 10px 20px;
            background-color: #ff6b6b;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: transform 0.2s;
        }
        button:hover {
            transform: scale(1.1); /* Лёгкая анимация при наведении */
        }
    </style>
</head>
<body>
    <img src="https://media1.tenor.com/m/Yp0KOBZZ9RYAAAAd/%D0%BA%D0%BE%D1%82-%D0%BF%D0%BE%D1%86%D0%B5%D0%BB%D1%83%D0%B9.gif" alt="Котик целует экран">
    <p>Я не знаю секрет счастья, но когда ты рядом - я счастлив. Прости за те резкие слова, что я тебе сказал в тот день. Ты для меня действительно особенный и дорогой человек🤍</p>
    <button onclick="showVideo()">Тыкни на меня</button>
    <iframe id="surpriseVideo" src="https://drive.google.com/file/d/1S01KDJRQ-KRlaAsWZ1quUqCjGCUVvPAn/preview" allow="fullscreen"></iframe>
    <script>
        function showVideo() {
            const video = document.getElementById('surpriseVideo');
            video.style.display = 'block'; // Показываем видео
            // Проверяем поддержку полноэкранного режима
            if (video.requestFullscreen) {
                video.requestFullscreen().catch(err => {
                    console.log('Полноэкранный режим не сработал: ' + err.message);
                });
            } else if (video.webkitRequestFullscreen) { /* Safari */
                video.webkitRequestFullscreen().catch(err => {
                    console.log('Полноэкранный режим не сработал: ' + err.message);
                });
            } else if (video.msRequestFullscreen) { /* IE11 */
                video.msRequestFullscreen().catch(err => {
                    console.log('Полноэкранный режим не сработал: ' + err.message);
                });
            }
        }
    </script>
</body>
</html>
