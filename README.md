<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Player de Vídeo Personalizado</title>
    <style>
        body {
            background-color: black;
            color: white;
            font-family: Arial, sans-serif;
            text-align: center;
        }
        .video-container {
            position: relative;
            padding-bottom: 56.25%;
            height: 0;
            overflow: hidden;
            max-width: 100%;
            background-color: #333;
            border: 2px solid #ff0000;
            border-radius: 10px;
            margin: 20px auto;
        }
        .video-container iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }
        .list-view {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            margin: 20px 0;
        }
        .list-view button {
            background-color: transparent;
            border: 2px solid #ff0000;
            border-radius: 50%;
            color: #ff0000;
            padding: 10px 20px;
            margin: 10px;
            cursor: pointer;
            transition: background-color 0.3s, color 0.3s;
        }
        .list-view button:hover {
            background-color: #ff0000;
            color: white;
        }
    </style>
</head>
<body>
    <div class="video-container">
        <iframe id="videoPlayer" src="https://example.com/your-video.m3u8" frameborder="0" allowfullscreen></iframe>
    </div>
    <h1>Jogos de Hoje</h1>
    <div class="list-view">
        <button onclick="playVideo('http://7go.xyz:8080/live/5511949680652/551194dd/315115.m3u8')">Grêmio x Palmeiras</button>
        <button onclick="playVideo('http://7go.xyz:8080/live/5511949680652/551194dd/42914.m3u8')">Grêmio x Palmeiras</button>
        <button onclick="playVideo('http://7go.xyz:8080/live/5511949680652/551194dd/31456.m3u8')">Bahia x Juventude</button>
        <button onclick="playVideo('http://7go.xyz:8080/live/5511949680652/551194dd/18951.m3u8')">Fluminense x Internacional</button>
        <button onclick="playVideo('http://7go.xyz:8080/live/5511949680652/551194dd/315114.m3u8')">Corinthians x Vitória</button>
        <button onclick="playVideo('http://7go.xyz:8080/live/5511949680652/551194dd/315115.m3u8')">Argentina x Equador</button>
        <button onclick="playVideo('http://7go.xyz:8080/live/5511949680652/551194dd/18529.m3u8')">Argentina x Equador</button>
    </div>
    <h1>Jogos de Amanhã</h1>
    <div class="list-view">
        <button onclick="playVideo('http://7go.xyz:8080/live/5511949680652/551194dd/18529.m3u8')">Espanha x Alemanha</button>
        <button onclick="playVideo('http://uniplay.link:80/live/262144514/mega96502/21275.m3u8')">Espanha x Alemanha</button>
        <button onclick="playVideo('https://www.youtube.com/embed/p45AMK_udmg?si=ZdfWFqThtfsKaeFn')">Portugal x França</button>
        <button onclick="playVideo('http://uniplay.link:80/live/262144514/mega96502/21275.m3u8')">Ceará x Santos</button>
        <button onclick="playVideo('http://7go.xyz:8080/live/5511949680652/551194dd/315114.m3u8')">Ceará x Santos</button>
        <button onclick="playVideo('http://uniplay.link:80/live/262144514/mega96502/364679.m3u8')">Brusque x Ponte Preta</button>
        <button onclick="playVideo('http://uniplay.link:80/live/262144514/mega96502/21269.m3u8')">Brusque x Ponte Preta</button>
        <button onclick="playVideo('https://www.youtube.com/embed/sm6W-7pOWk0?si=L4DNdEX1Ii9gHPO-')">Brusque x Ponte Preta</button>
        <button onclick="playVideo('http://uniplay.link:80/live/262144514/mega96502/21275.m3u8')">Venezuela x Canadá</button>
    </div>
    <script>
        function playVideo(url) {
            const videoPlayer = document.getElementById('videoPlayer');
            videoPlayer.src = url;
        }

        const videoPlayer = document.getElementById('videoPlayer');
        videoPlayer.addEventListener('error', function() {
            setTimeout(() => {
                videoPlayer.src = videoPlayer.src; // Tenta recarregar o vídeo
            }, 5000); // Tenta recarregar após 5 segundos
        });

        // Direitos autorais
        console.log("Direitos autorais: EmbedMen");
    </script>
</body>
</html>
