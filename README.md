<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ulang Tahun Najwa Alya Shafarina</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Montserrat', sans-serif;
            background: linear-gradient(135deg, #fff9f9 0%, #fff1f1 100%);
            color: #5a3e36;
        }
        .special-font {
            font-family: 'Playfair Display', serif;
        }
        .birthday-card {
            background: linear-gradient(to bottom right, #ffffff, #fff9f9);
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.1);
            border-radius: 20px;
            overflow: hidden;
        }
        .hearts {
            position: absolute;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }
        .heart {
            position: absolute;
            opacity: 0;
        }
        .signature {
            font-family: 'Allura', cursive;
            font-size: 2rem;
            color: #d4a373;
        }
        .gold-text {
            color: #d4a373;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
        }
        .confetti {
            position: fixed;
            width: 10px;
            height: 10px;
            background-color: #f9a8d4;
            opacity: 0;
            z-index: -1;
        }
    </style>
</head>
<body class="min-h-screen flex items-center justify-center p-4">
    <div class="hearts" id="hearts-container"></div>
    <div class="confetti" id="confetti-container"></div>
    <audio id="birthdaySong" loop>
        <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
    </audio>

    <div id="birthday-content" style="display: none;">
        <div class="birthday-card w-full max-w-3xl p-8 md:p-12 relative overflow-hidden">
            <div class="absolute -top-40 -right-40 w-80 h-80 rounded-full bg-gradient-to-r from-pink-100 to-pink-50 opacity-70"></div>
            <div class="absolute -bottom-40 -left-40 w-80 h-80 rounded-full bg-gradient-to-r from-amber-50 to-amber-100 opacity-70"></div>
            
            <div class="relative z-10 text-center">
                <div class="flex justify-center mb-8">
                    <img src="https://drive.google.com/file/d/1U9DxXlWxDCmL-7R9RqZDYB5QAFF5bRMS/view?usp=sharing" alt="Najwa Alya Shafarina tersenyum dengan latar belakang dekorasi ulang tahun" class="rounded-lg shadow-md" />
                </div>
                
                <h1 class="text-3xl md:text-5xl font-bold mb-6 special-font gold-text">Selamat Ulang Tahun</h1>
                <h2 class="text-4xl md:text-6xl font-bold mb-8 special-font text-pink-600">Najwa Alya Shafarina</h2>
                
                <div class="text-lg md:text-xl leading-relaxed mb-10 text-left space-y-4">
                    <p class="special-font text-xl">🎉 20 Juli 2005 - 20 Juli 2025 🎉</p>
                    <p>Hai Najwa,</p>
                    <p>Selamat merayakan hari spesialmu yang ke-20! Dua dekade penuh cerita, tawa, dan segala kebaikan yang kamu sebarkan ke sekitar.</p>
                    <p>Semoga tahun ini membawa lebih banyak kebahagiaan, pencapaian, dan petualangan baru. Teruslah bersinar dengan kehangatan dan keceriaanmu yang khas.</p>
                    <p>Kami semua sangat beruntung bisa mengenal seseorang seistimewa dirimu. Selamat bertumbuh dan semoga semua harapanmu terkabul!</p>
                </div>
                
                <div class="flex items-center justify-center space-x-4 mb-10">
                    <button id="playButton" class="px-6 py-2 bg-pink-500 hover:bg-pink-600 text-white rounded-full transition-all shadow-md">
                        Putar Lagu
                    </button>
                    <button id="confettiButton" class="px-6 py-2 bg-amber-500 hover:bg-amber-600 text-white rounded-full transition-all shadow-md">
                        Confetti
                    </button>
                </div>
                
                <div class="border-t border-pink-200 pt-6">
                    <p class="text-gray-600 mb-2">Dengan penuh kasih sayang,</p>
                    <p class="signature">Keluarga & Sahabat</p>
                </div>
            </div>
        </div>
    </div>

    <div id="wrong-date" style="display: none;">
        <div class="text-center max-w-md mx-auto">
            <h1 class="text-3xl font-bold mb-6 text-rose-600">Ups!</h1>
            <p class="text-xl mb-8">Halaman spesial ini hanya tersedia pada tanggal 20 Juli 2025 Pukul 14:30 WIB.</p>
            <p class="text-lg">Datang lagi ya nanti!</p>
            <div class="mt-10">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/39966b41-e198-4f9a-9f3d-8198c2eb4d2f.png" alt="Ilustrasi kalender dengan tanggal 20 Juli 2025 ditandai dengan lingkaran merah" class="mx-auto rounded-lg" />
            </div>
        </div>
    </div>

    <script>
        // Check date
        const targetDate = new Date('2025-07-20T07:30:00Z'); // 15:30 WIB
        const now = new Date();
        
        if (now.toDateString() === targetDate.toDateString()) {
            document.getElementById('birthday-content').style.display = 'block';
            startAnimations();
        } else {
            document.getElementById('wrong-date').style.display = 'block';
        }

        // Music control
        const song = document.getElementById('birthdaySong');
        const playButton = document.getElementById('playButton');
        
        playButton.addEventListener('click', function() {
            if (song.paused) {
                song.play();
                playButton.textContent = 'Pause Lagu';
            } else {
                song.pause();
                playButton.textContent = 'Putar Lagu';
            }
        });

        // Confetti animation
        const confettiButton = document.getElementById('confettiButton');
        const confettiContainer = document.getElementById('confetti-container');
        
        function createConfetti() {
            const confetti = document.createElement('div');
            confetti.className = 'confetti';
            confetti.style.left = Math.random() * 100 + 'vw';
            confetti.style.backgroundColor = `hsl(${Math.random() * 360}, 100%, 75%)`;
            confetti.style.width = Math.random() * 10 + 5 + 'px';
            confetti.style.height = Math.random() * 10 + 5 + 'px';
            
            confettiContainer.appendChild(confetti);
            
            let position = 0;
            let opacity = 1;
            const fallInterval = setInterval(() => {
                position += 2;
                opacity -= 0.01;
                confetti.style.transform = `translateY(${position}px) rotate(${position}deg)`;
                confetti.style.opacity = opacity;
                
                if (position > window.innerHeight || opacity <= 0) {
                    clearInterval(fallInterval);
                    confetti.remove();
                }
            }, 20);
        }
        
        confettiButton.addEventListener('click', function() {
            for (let i = 0; i < 100; i++) {
                setTimeout(createConfetti, i * 50);
            }
        });

        // Heart animation
        function createHeart() {
            const heart = document.createElement('div');
            heart.className = 'heart';
            heart.innerHTML = '❤️';
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.top = '-20px';
            heart.style.fontSize = Math.random() * 20 + 10 + 'px';
            heart.style.color = `hsl(${Math.random() * 60 + 320}, 100%, 70%)`;
            
            document.getElementById('hearts-container').appendChild(heart);
            
            let opacity = 0;
            let rise = 0;
            const riseInterval = setInterval(() => {
                rise += 1;
                opacity += 0.02;
                if (opacity >= 1) opacity = 1;
                heart.style.transform = `translateY(-${rise}px)`;
                heart.style.opacity = opacity;
                
                if (rise > window.innerHeight) {
                    clearInterval(riseInterval);
                    heart.remove();
                }
            }, 50);
        }
        
        function startAnimations() {
            // Background hearts
            setInterval(createHeart, 300);
            
            // Initial confetti burst
            setTimeout(() => {
                for (let i = 0; i < 50; i++) {
                    setTimeout(createConfetti, i * 50);
                }
            }, 1000);
        }
    </script>
</body>
</html>

