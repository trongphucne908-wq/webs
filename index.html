<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Góc Karaoke - Cô Oanh</title>
    <style>
        :root {
            --bg-color: #0d0d0d;
            --text-color: #f1f1f1;
            --border-color: #333333;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Times New Roman', Times, serif, sans-serif;
            -webkit-user-select: none;
            -moz-user-select: none;
            -ms-user-select: none;
            user-select: none;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            position: relative;
        }

        /* 1. Màn hình Welcome */
        #welcome-screen {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            background-color: var(--bg-color);
            z-index: 100;
        }

        /* Animation xuất hiện chữ ban đầu */
        .welcome-text {
            font-size: 2.8rem;
            font-weight: 400;
            letter-spacing: 2px;
            text-decoration: underline;
            text-underline-offset: 12px;
            text-decoration-thickness: 1px;
            color: #ffffff;
            animation: welcomeSmooth 1.8s cubic-bezier(0.16, 1, 0.3, 1) forwards;
            opacity: 0;
            transform: translateY(15px);
        }

        .welcome-watermark {
            font-size: 1rem;
            color: #888888;
            letter-spacing: 1.5px;
            text-decoration: underline;
            text-underline-offset: 6px;
            text-decoration-thickness: 1px;
            margin-top: 25px;
            opacity: 0;
            animation: watermarkFadeIn 2s cubic-bezier(0.16, 1, 0.3, 1) 0.4s forwards;
        }

        /* Keyframes xuất hiện chữ */
        @keyframes welcomeSmooth {
            0% {
                opacity: 0;
                transform: translateY(15px);
                letter-spacing: 6px;
            }
            50% {
                opacity: 1;
                transform: translateY(0);
            }
            100% {
                opacity: 1;
                transform: translateY(0);
                letter-spacing: 2px;
            }
        }

        @keyframes watermarkFadeIn {
            0% {
                opacity: 0;
                transform: translateY(10px);
            }
            100% {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* HIỆU ỨNG BIẾN MẤT: Phóng to chậm + Mờ dần */
        #welcome-screen.zoom-fade-out .welcome-text,
        #welcome-screen.zoom-fade-out .welcome-watermark {
            animation: zoomAndFade 1.2s cubic-bezier(0.25, 1, 0.5, 1) forwards !important;
        }

        @keyframes zoomAndFade {
            0% {
                opacity: 1;
                transform: scale(1);
            }
            100% {
                opacity: 0;
                transform: scale(1.35);
                filter: blur(4px);
            }
        }

        /* 2. Menu chính tối giản */
        #main-menu {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 16px;
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.8s cubic-bezier(0.4, 0, 0.2, 1), transform 0.8s cubic-bezier(0.4, 0, 0.2, 1);
            pointer-events: none;
            width: 100%;
            max-width: 400px;
            padding: 0 20px;
        }

        #main-menu.show {
            opacity: 1;
            transform: translateY(0);
            pointer-events: auto;
        }

        .menu-title {
            font-size: 1.4rem;
            font-weight: 400;
            letter-spacing: 1px;
            margin-bottom: 10px;
            text-decoration: underline;
            text-underline-offset: 8px;
            text-decoration-thickness: 1px;
            color: #888;
        }

        /* NÚT BẤM VÀ HIỆU ỨNG GLOW GRADIENT VIỀN KHI CLICK */
        .btn-song {
            position: relative;
            width: 100%;
            padding: 16px 24px;
            font-size: 1.1rem;
            font-weight: 400;
            background: var(--bg-color);
            color: var(--text-color);
            border: 1px solid var(--border-color);
            border-radius: 4px;
            cursor: pointer;
            letter-spacing: 0.5px;
            transition: border-color 0.3s ease, background-color 0.3s ease, transform 0.2s ease;
            text-align: center;
            text-decoration: underline;
            text-underline-offset: 6px;
            text-decoration-color: rgba(255, 255, 255, 0.3);
            outline: none;
            z-index: 1;
            -webkit-user-select: none;
            user-select: none;
        }

        .btn-song:hover {
            border-color: #ffffff;
            background-color: rgba(255, 255, 255, 0.05);
            text-decoration-color: #ffffff;
        }

        .btn-song::after {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(90deg, #ff007f, #00f2fe, #4facfe, #ff007f);
            background-size: 300% 300%;
            border-radius: 6px;
            z-index: -1;
            opacity: 0;
            transition: opacity 0.2s ease;
            filter: blur(6px);
        }

        .btn-song:active {
            transform: scale(0.98);
            border-color: transparent;
        }

        .btn-song:active::after {
            opacity: 1;
            animation: borderGlow 1.5s linear infinite;
        }

        @keyframes borderGlow {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* 3. Màn hình Karaoke */
        #player-container {
            display: none;
            flex-direction: column;
            align-items: center;
            width: 90%;
            max-width: 750px;
            opacity: 0;
            transform: scale(0.98);
            transition: all 0.5s cubic-bezier(0.16, 1, 0.3, 1);
        }

        #player-container.show {
            display: flex;
            opacity: 1;
            transform: scale(1);
        }

        #song-title {
            font-size: 1.2rem;
            font-weight: 400;
            margin-bottom: 20px;
            letter-spacing: 1px;
            text-decoration: underline;
            text-underline-offset: 8px;
            text-decoration-thickness: 1px;
            color: var(--text-color);
        }

        .video-wrapper {
            position: relative;
            width: 100%;
            padding-bottom: 56.25%; /* 16:9 */
            height: 0;
            border: 1px solid var(--border-color);
            border-radius: 6px;
            overflow: hidden;
            background-color: #000;
        }

        .video-wrapper iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
        }

        .btn-back {
            position: relative;
            margin-top: 24px;
            padding: 10px 24px;
            font-size: 0.95rem;
            background: var(--bg-color);
            color: #aaa;
            border: 1px solid var(--border-color);
            border-radius: 4px;
            cursor: pointer;
            letter-spacing: 0.5px;
            text-decoration: underline;
            text-underline-offset: 4px;
            transition: all 0.3s ease;
            outline: none;
            z-index: 1;
            /* Đã khóa hoàn toàn lỗi tô xanh/bôi đen */
            -webkit-user-select: none;
            -moz-user-select: none;
            -ms-user-select: none;
            user-select: none;
        }

        .btn-back:hover {
            color: var(--text-color);
            border-color: var(--text-color);
        }

        .btn-back::after {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(90deg, #ff007f, #00f2fe, #4facfe, #ff007f);
            background-size: 300% 300%;
            border-radius: 6px;
            z-index: -1;
            opacity: 0;
            transition: opacity 0.2s ease;
            filter: blur(6px);
        }

        .btn-back:active {
            transform: scale(0.98);
            border-color: transparent;
        }

        .btn-back:active::after {
            opacity: 1;
            animation: borderGlow 1.5s linear infinite;
        }
    </style>
</head>
<body>

    <!-- Màn hình Welcome -->
    <div id="welcome-screen">
        <div class="welcome-text">Welcome "Cô Oanh"</div>
        <div class="welcome-watermark">made by TrongPhuc</div>
    </div>

    <!-- Menu chính -->
    <div id="main-menu">
        <div class="menu-title">Danh sách bài hát</div>
        <button class="btn-song" onclick="playSong('thannlan')">Con thằn lằn con</button>
        <button class="btn-song" onclick="playSong('vit')">Một con vịt</button>
        <button class="btn-song" onclick="playSong('canhathuongnhau')">Cả nhà thương nhau</button>
        <button class="btn-song" onclick="playSong('bonphuongtroi')">Bốn phương trời</button>
    </div>

    <!-- Màn hình Karaoke -->
    <div id="player-container">
        <div id="song-title"></div>
        <div class="video-wrapper">
            <iframe id="youtube-player" src="" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
        <button class="btn-back" onclick="backToMenu()">Quay lại</button>
    </div>

    <script>
        // Điều khiển chuyển cảnh
        window.addEventListener('DOMContentLoaded', () => {
            setTimeout(() => {
                const welcomeScreen = document.getElementById('welcome-screen');
                const mainMenu = document.getElementById('main-menu');
                
                welcomeScreen.classList.add('zoom-fade-out');
                
                setTimeout(() => {
                    welcomeScreen.style.display = 'none';
                    mainMenu.classList.add('show');
                }, 1200);
            }, 2500);
        });

        // Danh sách bài hát chuẩn link
        const songs = {
            'thannlan': {
                title: 'Con thằn lằn con - Karaoke',
                url: 'https://www.youtube.com/embed/T00p7qKWTWw?autoplay=1'
            },
            'vit': {
                title: 'Một con vịt - Karaoke',
                url: 'https://www.youtube.com/embed/YWsNJV-X68s?autoplay=1'
            },
            'canhathuongnhau': {
                title: 'Cả nhà thương nhau - Karaoke',
                url: 'https://www.youtube.com/embed/Va-uXsyRpsg?autoplay=1'
            },
            'bonphuongtroi': {
                title: 'Bốn phương trời - Karaoke',
                url: 'https://www.youtube.com/embed/0Qv7KOoIOqg?autoplay=1'
            }
        };

        function playSong(songKey) {
            const mainMenu = document.getElementById('main-menu');
            const playerContainer = document.getElementById('player-container');
            const youtubePlayer = document.getElementById('youtube-player');
            const songTitle = document.getElementById('song-title');

            const selectedSong = songs[songKey];
            if (selectedSong) {
                songTitle.innerText = selectedSong.title;
                youtubePlayer.src = selectedSong.url;

                mainMenu.classList.remove('show');
                setTimeout(() => {
                    mainMenu.style.display = 'none';
                    playerContainer.style.display = 'flex';
                    setTimeout(() => playerContainer.classList.add('show'), 50);
                }, 400);
            }
        }

        function backToMenu() {
            const mainMenu = document.getElementById('main-menu');
            const playerContainer = document.getElementById('player-container');
            const youtubePlayer = document.getElementById('youtube-player');

            playerContainer.classList.remove('show');
            setTimeout(() => {
                playerContainer.style.display = 'none';
                youtubePlayer.src = '';
                mainMenu.style.display = 'flex';
                setTimeout(() => mainMenu.classList.add('show'), 50);
            }, 400);
        }
    </script>
</body>
</html>
