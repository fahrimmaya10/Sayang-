<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jangan Marah Ya</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            text-align: center;
            background-color: #ffe6e6;
            margin: 0;
            padding: 0;
        }

        h1 {
            color: #ff6666;
        }

        .container {
            display: none;
            margin-top: 50px;
        }

        button {
            background-color: #ff4d4d;
            border: none;
            color: white;
            padding: 15px 30px;
            font-size: 20px;
            border-radius: 50px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        button:hover {
            background-color: #ff1a1a;
        }

        .heart {
            margin-top: 50px;
        }

        #audio {
            display: none;
        }

        .slide {
            display: none;
            margin-top: 50px;
        }

        .active {
            display: block;
        }
    </style>
</head>
<body>

    <h1>Coba Pencet</h1>
    <div class="heart">
        <button id="loveButton">💖 Love 💖</button>
    </div>

    <div class="container">
        <div class="slide active">
            <h1>Sayang, jangan marah ya!</h1>
            <button id="nextButton1">Pencet tombolnya</button>
        </div>
        <div class="slide">
            <h1>I love you, Sayang Cahaya!</h1>
            <button id="nextButton2">💖 Love you 💖</button>
        </div>
    </div>

    <!-- Masukkan link lagu di sini -->
    <audio id="audio" controls autoplay>
        <source src="YOUR_SONG_LINK_HERE" type="audio/mpeg">
        Browser-mu tidak mendukung pemutaran audio.
    </audio>

    <script>
        const loveButton = document.getElementById('loveButton');
        const container = document.querySelector('.container');
        const audio = document.getElementById('audio');
        const slides = document.querySelectorAll('.slide');
        let currentSlide = 0;

        loveButton.addEventListener('click', function() {
            audio.play();
            container.style.display = 'block';
            loveButton.style.display = 'none';
        });

        document.getElementById('nextButton1').addEventListener('click', function() {
            slides[currentSlide].classList.remove('active');
            currentSlide++;
            slides[currentSlide].classList.add('active');
        });

        document.getElementById('nextButton2').addEventListener('click', function() {
            alert('I love you! Jangan marah ya, Sayang Cahaya 😘');
        });
    </script>

</body>
</html>
