<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy 20th Birthday Najwa!</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #fff5f7 0%, #fff9f5 100%);
            color: #333;
            overflow-x: hidden;
            text-align: center;
        }
        
        .gold-text {
            background: linear-gradient(to right, #d4af37, #f6e272);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.1);
        }
        
        .birthday-card {
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(233, 150, 150, 0.15);
            padding: 20px;
            margin: 20px;
        }
        
        .confetti {
            position: absolute;
            width: 10px;
            height: 10px;
            background-color: #f00;
            opacity: 0.7;
            animation: fall linear infinite;
        }
        
        @keyframes fall {
            to {
                transform: translateY(100vh);
            }
        }
        
        .balloon {
            position: absolute;
            width: 40px;
            height: 60px;
            border-radius: 50%;
            animation: float 8s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% {
                transform: translateY(0) rotate(5deg);
            }
            50% {
                transform: translateY(-30px) rotate(-5deg);
            }
        }
        
        .signature {
            font-family: 'Dancing Script', cursive;
            font-size: 1.8rem;
            background: linear-gradient(to right, #d4af37, #f6e272);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .music-player {
            margin-top: 20px;
            padding: 10px 20px;
            background-color: #f9ca24;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        
        .music-player:hover {
            background-color: #f6e272;
        }
        
        #slideshow {
            max-width: 600px;
            margin: auto;
            position: relative;
            overflow: hidden;
        }
        
        #slideshow img {
            width: 100%;
            border-radius: 10px;
            display: none;
        }
        
        #slideshow img.active {
            display: block;
        }
    </style>
</head>
<body>
    <div id="confetti"></div>
    <div id="balloons"></div>
    
    <div id="birthday-content" class="birthday-card">
        <h1 class="text-5xl font-bold gold-text">Happy 20th Birthday!</h1>
        <h2 class="text-3xl font-bold">Najwa Alya Shafarina</h2>
        <p class="text-xl">Selamat ulang tahun yang ke-20! Semoga hari ini dipenuhi dengan kebahagiaan dan cinta.</p>
        <p>Semoga semua impianmu menjadi kenyataan dan tahun ini menjadi tahun yang luar biasa untukmu!</p>
        <p class="signature">Dengan cinta,</p>
        
        <div id="slideshow">
            <img src="https://placehold.co/600x400" alt="Memorable photo 1" class="active">
            <img src="https://placehold.co/600x400" alt="Memorable photo 2">
            <img src="https://placehold.co/600x400" alt="Memorable photo 3">
        </div>
        
        <audio id="birthdaySong" loop>
            <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
        </audio>
        <button id="musicToggle" class="music-player">Play Birthday Song</button>
    </div>
    
    <div id="early-access" class="birthday-card hidden">
        <h1 class="text-4xl font-bold">Ups!</h1>
        <p class="text-xl">Halaman spesial ini hanya tersedia pada Pukul 14:30 WIB tanggal 20 Juli 2025. Datang lagi ya nanti!</p>
    </div>

    <script>
        // Validate access time
        const validateAccessTime = () => {
            const targetDate = new Date('July 20, 2025 14:30:00 GMT+0700');
            const now = new Date();
            
            if (now >= targetDate) {
                document.getElementById('birthday-content').classList.remove('hidden');
                document.getElementById('early-access').classList.add('hidden');
                startCelebration();
            } else {
                document.getElementById('birthday-content').classList.add('hidden');
                document.getElementById('early-access').classList.remove('hidden');
            }
        };
        
        // Start celebration effects
        const startCelebration = () => {
            createBalloons();
            createConfetti();
            startSlideshow();
        };
        
        // Create balloons
        const createBalloons = () => {
            const colors = ['#ff6b6b', '#f9ca24', '#7ed6df', '#e056fd', '#686de0'];
            for (let i = 0; i < 15; i++) {
                const balloon = document.createElement('div');
                balloon.className = 'balloon';
                balloon.style.left = `${Math.random() * 100}vw`;
                balloon.style.bottom = '-60px';
                balloon.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                balloon.style.opacity = 0.7;
                balloon.style.animationDuration = `${8 + Math.random() * 10}s`;
                balloon.style.animationDelay = `${Math.random() * 5}s`;
                document.getElementById('balloons').appendChild(balloon);
            }
        };
        
        // Create confetti
        const createConfetti = () => {
            const colors = ['#ff6b6b', '#f9ca24', '#7ed6df', '#e056fd', '#686de0'];
            for (let i = 0; i < 100; i++) {
                const confetti = document.createElement('div');
                confetti.className = 'confetti';
                confetti.style.left = `${Math.random() * 100}vw`;
                confetti.style.top = '-10px';
                confetti.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                confetti.style.animationDuration = `${5 + Math.random() * 10}s`;
                confetti.style.animationDelay = `${Math.random() * 5}s`;
                document.getElementById('confetti').appendChild(confetti);
            }
        };
        
        // Start slideshow
        let currentSlide = 0;
        const slides = document.querySelectorAll('#slideshow img');
        
        const startSlideshow = () => {
            slides[currentSlide].classList.add('active');
            setInterval(() => {
                slides[currentSlide].classList.remove('active');
                currentSlide = (currentSlide + 1) % slides.length;
                slides[currentSlide].classList.add('active');
            }, 3000);
        };
        
        // Music toggle functionality
        const musicToggle = document.getElementById('musicToggle');
        const birthdaySong = document.getElementById('birthdaySong');
        let musicPlaying = false;
        
        musicToggle.addEventListener('click', () => {
            if (musicPlaying) {
                birthdaySong.pause();
                musicPlaying = false;
                musicToggle.textContent = 'Play Birthday Song';
            } else {
                birthdaySong.play();
                musicPlaying = true;
                musicToggle.textContent = 'Pause Song';
            }
        });
        
        // Initialize
        document.addEventListener('DOMContentLoaded', () => {
            validateAccessTime();
            setInterval(validateAccessTime, 60000);
        });
    </script>
</body>
</html>
