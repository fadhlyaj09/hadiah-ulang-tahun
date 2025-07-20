<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy 20th Birthday Najwa!</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Poppins:wght@300;400;600&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #fff5f7 0%, #fff9f5 100%);
            color: #333;
            overflow-x: hidden;
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
            transition: all 0.3s ease;
        }
        
        .birthday-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(233, 150, 150, 0.2);
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
        
        .heart {
            position: absolute;
            pointer-events: none;
            animation: heartfade 6s linear;
        }
        
        @keyframes heartfade {
            0% {
                opacity: 1;
                transform: translate(0) rotate(0deg) scale(0.5);
            }
            100% {
                opacity: 0;
                transform: translate(0, -100px) rotate(45deg) scale(1);
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
            transition: all 0.3s ease;
        }
        
        .music-player:hover {
            transform: scale(1.05);
        }
    </style>
</head>
<body class="min-h-screen flex items-center justify-center relative overflow-hidden">
    <div id="confetti"></div>
    <div id="balloons"></div>
    
    <div id="birthday-content" class="container mx-auto px-4 py-12">
        <div class="max-w-2xl mx-auto">
            <div class="birthday-card p-8 md:p-12">
                <h1 class="text-5xl md:text-6xl font-bold text-center mb-6 playfair-display gold-text">Happy Birthday!</h1>
                
                <div class="text-center mb-10">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/0921bce4-c790-4d7f-99c8-43e72cfbba4f.png" alt="Najwa Alya Shafarina smiling at her 20th birthday celebration with pink and gold decorations" class="mx-auto rounded-xl shadow-lg mb-6">
                    
                    <h2 class="text-3xl md:text-4xl font-bold mb-4 text-pink-700">Najwa Alya Shafarina</h2>
                    <p class="text-xl text-gray-700 mb-2">Your special day:</p>
                    <p class="text-2xl font-semibold gold-text mb-8">20th July 2025</p>
                </div>
                
                <div class="prose prose-lg mx-auto text-gray-700 mb-10">
                    <p class="text-center mb-4">Dear Najwa,</p>
                    <p class="mb-4">Happy 20th birthday! As you step into this remarkable new chapter of your life, may it be filled with joy, success, and all the wonderful things you deserve.</p>
                    <p class="mb-4">Twenty years of bringing light to the world - may this year be your brightest yet. May your dreams grow bigger, your laughter louder, and your happiness deeper.</p>
                    <p class="mb-4">You're incredibly special to everyone around you. Today we celebrate you - your kindness, your intelligence, and the amazing person you've become.</p>
                    <p class="text-center italic text-pink-600">"The more you praise and celebrate your life, the more there is in life to celebrate."</p>
                    <p class="text-right mt-8 signature">With love</p>
                </div>
                
                <div class="mt-10 text-center">
                    <audio id="birthdaySong" loop class="hidden">
                        <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
                    </audio>
                    <button id="musicToggle" class="music-player bg-pink-100 hover:bg-pink-200 text-pink-700 px-6 py-3 rounded-full shadow-md flex items-center mx-auto transition-all">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" viewBox="0 0 20 20" fill="currentColor">
                            <path d="M18 3a1 1 0 00-1.447-.894L8.763 6H5a3 3 0 000 6h.28l1.771 5.316A1 1 0 008 18h1a1 1 0 001-1v-4.382l6.553 3.276A1 1 0 0018 15V3z" />
                        </svg>
                        <span id="musicText">Play Birthday Song</span>
                    </button>
                </div>
            </div>
        </div>
    </div>
    
    <div id="early-access" class="hidden container mx-auto px-4 py-12">
        <div class="max-w-2xl mx-auto">
            <div class="birthday-card p-8 md:p-12">
                <h1 class="text-4xl font-bold text-center mb-6 text-pink-700">Ups!</h1>
                <p class="text-xl text-center py-10">Halaman spesial ini hanya tersedia pada pukul 14:00 WIB tanggal 21 Juli 2025. Datang lagi ya nanti!</p>
            </div>
        </div>
    </div>

    <script>
        // Validate access time
        const validateAccessTime = () => {
            const targetDate = new Date('July 21, 2025 14:00:00 GMT+0700');
            const now = new Date();
            
            // Check if it's exactly the target date and time
            if (now.getFullYear() === targetDate.getFullYear() &&
                now.getMonth() === targetDate.getMonth() &&
                now.getDate() === targetDate.getDate() &&
                now.getHours() === targetDate.getHours() &&
                Math.abs(now.getMinutes() - targetDate.getMinutes()) <= 5) {
                
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
            
            // Add floating hearts occasionally
            setInterval(() => {
                createHeart();
            }, 800);
        };
        
        // Create balloons
        const createBalloons = () => {
            const colors = ['#ff6b6b', '#f9ca24', '#7ed6df', '#e056fd', '#686de0'];
            const balloonContainer = document.getElementById('balloons');
            
            for (let i = 0; i < 15; i++) {
                const balloon = document.createElement('div');
                balloon.className = 'balloon';
                balloon.style.left = `${Math.random() * 100}vw`;
                balloon.style.bottom = '-60px';
                balloon.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                balloon.style.opacity = 0.7;
                balloon.style.animationDuration = `${8 + Math.random() * 10}s`;
                balloon.style.animationDelay = `${Math.random() * 5}s`;
                
                balloonContainer.appendChild(balloon);
            }
        };
        
        // Create confetti
        const createConfetti = () => {
            const confettiContainer = document.getElementById('confetti');
            const colors = ['#ff6b6b', '#f9ca24', '#7ed6df', '#e056fd', '#686de0'];
            
            for (let i = 0; i < 100; i++) {
                const confetti = document.createElement('div');
                confetti.className = 'confetti';
                confetti.style.left = `${Math.random() * 100}vw`;
                confetti.style.top = '-10px';
                confetti.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                confetti.style.animationDuration = `${5 + Math.random() * 10}s`;
                confetti.style.animationDelay = `${Math.random() * 5}s`;
                confetti.style.width = `${5 + Math.random() * 5}px`;
                confetti.style.height = `${5 + Math.random() * 5}px`;
                confetti.style.borderRadius = '50%';
                
                confettiContainer.appendChild(confetti);
            }
        };
        
        // Create floating hearts
        const createHeart = () => {
            const heart = document.createElement('div');
            heart.className = 'heart';
            
            const xPos = Math.random() * window.innerWidth;
            const size = Math.random() * 10 + 10;
            
            heart.innerHTML = '❤️';
            heart.style.left = `${xPos}px`;
            heart.style.bottom = '0px';
            heart.style.fontSize = `${size}px`;
            heart.style.opacity = 0;
            
            document.body.appendChild(heart);
            
            // Animate the heart
            setTimeout(() => {
                heart.style.opacity = 1;
                heart.style.animation = `heartfade ${6}s linear`;
            }, 10);
            
            // Remove heart after animation
            setTimeout(() => {
                heart.remove();
            }, 6000);
        };
        
        // Music toggle functionality
        const musicToggle = document.getElementById('musicToggle');
        const birthdaySong = document.getElementById('birthdaySong');
        let musicPlaying = false;
        
        musicToggle.addEventListener('click', () => {
            if (musicPlaying) {
                birthdaySong.pause();
                musicPlaying = false;
                document.getElementById('musicText').textContent = 'Play Birthday Song';
                musicToggle.classList.remove('bg-pink-200');
                musicToggle.classList.add('bg-pink-100');
            } else {
                birthdaySong.play();
                musicPlaying = true;
                document.getElementById('musicText').textContent = 'Pause Song';
                musicToggle.classList.remove('bg-pink-100');
                musicToggle.classList.add('bg-pink-200');
            }
        });
        
        // Initialize
        document.addEventListener('DOMContentLoaded', () => {
            validateAccessTime();
            
            // Revalidate every minute in case user keeps the page open
            setInterval(validateAccessTime, 60000);
        });
    </script>
</body>
</html>
