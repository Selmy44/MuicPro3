# MuicPro3
This a music project 3
<!DOCTYPE html>
<html>
<head>
    <title>Music Platform</title>
    <style>
        /* Inline CSS for styling */
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
        }
        #music-player {
            width: 300px;
            margin: 50px auto;
            padding: 20px;
            background-color: #fff;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
            border-radius: 5px;
        }
        h1 {
            text-align: center;
        }
        audio {
            width: 100%;
        }
        button {
            display: block;
            margin: 10px auto;
            padding: 10px 20px;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <div id="music-player">
        <h1>My Music Player</h1>
        <audio id="audio" controls>
            <source src="your-music.mp3" type="audio/mpeg">
            Your browser does not support the audio element.
        </audio>
        <button id="play-pause">Play</button>
    </div>

    <script>
        // JavaScript for controlling the music player
        const audio = document.getElementById('audio');
        const playPauseButton = document.getElementById('play-pause');

        let isPlaying = false;

        playPauseButton.addEventListener('click', function () {
            if (isPlaying) {
                audio.pause();
                playPauseButton.innerText = 'Play';
            } else {
                audio.play();
                playPauseButton.innerText = 'Pause';
            }
            isPlaying = !isPlaying;
        });
    </script>
</body>
</html>
