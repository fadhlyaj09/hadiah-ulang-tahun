<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Selamat Ulang Tahun ke-20, Najwa Alya Shafarina!</title>
    <!-- Memuat font dari Google Fonts untuk tampilan modern dan elegan -->
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&family=Playfair+Display:ital,wght@0,400;0,700;1,400&display=swap" rel="stylesheet">
    <style>
        /* Styling dasar untuk body */
        body {
            margin: 0;
            font-family: 'Montserrat', sans-serif;
            background-color: #F8F4E3; /* Warna pastel cream */
            color: #5C4B51; /* Warna teks yang lebih gelap */
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            overflow-x: hidden; /* Mencegah scroll horizontal */
            position: relative;
        }

        /* Kelas untuk menyembunyikan elemen */
        .hidden {
            display: none !important;
        }

        /* Styling untuk pesan akses terbatas */
        #access-message {
            text-align: center;
            font-size: 1.5em;
            color: #A0522D; /* Warna sienna */
            padding: 20px;
            border: 2px dashed #A0522D;
            border-radius: 10px;
            background-color: #FFF9ED;
            max-width: 600px;
            margin: 20px;
        }

        /* Styling untuk konten utama situs */
        #main-content {
            background-color: #FFFFFF;
            box-shadow: 0 0 30px rgba(0, 0, 0, 0.1);
            border-radius: 15px;
            padding: 40px;
            max-width: 900px;
            width: 90%; /* Responsif */
            text-align: center;
            position: relative;
            z-index: 1; /* Memastikan konten di atas confetti */
            overflow: hidden;
            box-sizing: border-box; /* Memastikan padding termasuk dalam lebar */
        }

        /* Styling untuk header */
        header h1 {
            font-family: 'Playfair Display', serif;
            font-size: 3.5em; /* Ukuran font besar */
            color: #DAA520; /* Warna goldenrod (emas) */
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1); /* Efek bayangan teks */
        }

        header h2 {
            font-family: 'Montserrat', sans-serif;
            font-size: 2em;
            color: #E6B98F; /* Warna gold/pink yang lebih terang */
            margin-top: 0;
        }

        /* Styling untuk bagian pesan */
        .message-section {
            margin: 40px 0;
            line-height: 1.8;
            font-size: 1.1em;
            text-align: justify; /* Teks rata kiri-kanan */
            color: #5C4B51;
        }

        /* Styling untuk tanda tangan */
        .signature {
            font-family: 'Playfair Display', serif;
            font-style: italic;
            font-size: 1.3em;
            margin-top: 30px;
            text-align: right;
            color: #DAA520;
        }

        /* Styling untuk bagian galeri/slideshow */
        .gallery-section {
            margin-top: 50px;
        }

        .gallery-section h3 {
            font-family: 'Playfair Display', serif;
            font-size: 2em;
            color: #DAA520;
            margin-bottom: 30px;
        }

        .slideshow-container {
            max-width: 700px;
            position: relative;
            margin: auto;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        /* Gambar slideshow */
        .mySlides {
            display: none;
        }

        .mySlides img {
            width: 100%;
            height: auto;
            display: block;
        }

        /* Tombol navigasi slideshow */
        .prev, .next {
            cursor: pointer;
            position: absolute;
            top: 50%;
            width: auto;
            padding: 16px;
            margin-top: -22px;
            color: white;
            font-weight: bold;
            font-size: 18px;
            transition: 0.6s ease;
            border-radius: 0 3px 3px 0;
            user-select: none;
            background-color: rgba(0,0,0,0.5);
        }

        .next {
            right: 0;
            border-radius: 3px 0 0 3px;
        }

        .prev:hover, .next:hover {
            background-color: rgba(0,0,0,0.8);
        }

        /* Indikator dot slideshow */
        .dot {
            cursor: pointer;
            height: 15px;
            width: 15px;
            margin: 0 2px;
            background-color: #bbb;
            border-radius: 50%;
            display: inline-block;
            transition: background-color 0.6s ease;
        }

        .active, .dot:hover {
            background-color: #717171;
        }

        /* Animasi fade untuk slideshow */
        .fade {
            animation-name: fade;
            animation-duration: 1.5s;
        }

        @keyframes fade {
            from {opacity: .4}
            to {opacity: 1}
        }

        /* Styling footer */
        footer {
            margin-top: 50px;
            padding-top: 20px;
            border-top: 1px solid #eee;
            color: #A0A0A0;
            font-size: 0.9em;
        }

        /* Kontrol audio */
        .audio-control {
            position: absolute;
            top: 20px;
            right: 20px;
            z-index: 10;
        }

        .audio-control button {
            background-color: #DAA520;
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 5px;
            cursor: pointer;
            font-family: 'Montserrat', sans-serif;
            font-size: 0.9em;
            transition: background-color 0.3s ease;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }

        .audio-control button:hover {
            background-color: #C19100;
        }

        /* Kontainer untuk animasi confetti */
        .confetti-container {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            overflow: hidden;
            pointer-events: none; /* Memungkinkan klik melewati confetti */
            z-index: 0; /* Di belakang konten utama */
        }

        /* Styling dasar untuk setiap confetti */
        .confetti {
            position: absolute;
            width: 10px;
            height: 10px;
            background-color: #FFD700; /* Warna emas */
            opacity: 0;
            animation: fall 3s ease-out forwards; /* Animasi jatuh */
            border-radius: 50%; /* Bentuk bulat */
            box-shadow: 0 0 5px rgba(255, 215, 0, 0.5);
        }

        /* Variasi warna confetti */
        .confetti.pink { background-color: #FFC0CB; } /* Pink */
        .confetti.light-blue { background-color: #ADD8E6; } /* Biru muda */
        .confetti.purple { background-color: #B19CD9; } /* Ungu muda */
        .confetti.orange { background-color: #FFB347; } /* Oranye */

        /* Keyframes untuk animasi jatuh confetti */
        @keyframes fall {
            0% {
                transform: translateY(-100px) rotateZ(0deg);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            100% {
                transform: translateY(calc(100vh + 100px)) rotateZ(720deg);
                opacity: 0;
            }
        }

        /* Media queries untuk responsivitas */
        @media (max-width: 768px) {
            header h1 {
                font-size: 2.5em;
            }
            header h2 {
                font-size: 1.5em;
            }
            .message-section {
                font-size: 1em;
            }
            .signature {
                font-size: 1.1em;
            }
            .audio-control {
                top: 10px;
                right: 10px;
            }
            #main-content {
                padding: 20px;
            }
        }

        @media (max-width: 480px) {
            header h1 {
                font-size: 2em;
            }
            header h2 {
                font-size: 1.2em;
            }
            #access-message {
                font-size: 1.2em;
            }
            .audio-control button {
                padding: 8px 12px;
                font-size: 0.8em;
            }
        }
    </style>
</head>
<body>
    <!-- Pesan yang ditampilkan jika waktu akses belum tiba atau sudah lewat -->
    <div id="access-message" class="hidden">
        <p>Ups! Santai...buru-buru amat si lo, tuggu lah!</p>
    </div>

    <!-- Konten utama situs, awalnya tersembunyi -->
    <div id="main-content" class="hidden">
        <!-- Elemen audio untuk musik latar -->
        <!-- Pastikan Anda memiliki file 'happy-birthday.mp3' di folder yang sama -->
        <audio id="birthday-song" src="happy-birthday.mp3" loop autoplay></audio>
        <div class="audio-control">
            <button id="play-pause-btn">Pause Musik</button>
        </div>

        <!-- Kontainer untuk animasi confetti -->
        <div class="confetti-container"></div>

        <header>
            <h1>Selamat Ulang Tahun ke-20</h1>
            <h2>Untuk Najwa Alya Shafarina!</h2>
        </header>

        <section class="message-section">
            <p>Najwa Alya Shafarina,</p>
            <p>Di hari istimewamu yang ke-20 ini, aku ingin mengucapkan selamat ulang tahun yang paling tulus dari lubuk hati. Semoga setiap langkahmu dipenuhi kebahagiaan, kesehatan, dan keberkahan. Semoga semua impian dan cita-citamu tercapai, dan jalanmu selalu diterangi cahaya kebaikan.</p>
            <p>Dua puluh tahun adalah awal dari babak baru yang menakjubkan. Semoga kamu terus tumbuh menjadi pribadi yang luar biasa, menginspirasi banyak orang, dan selalu menemukan kebahagiaan dalam setiap momen. Terima kasih telah menjadi pribadi yang hangat, ceria, dan penuh semangat.</p>
            <p>Dengan cinta dan doa,</p>
            <p class="signature">Seseorang yang Menyayangimu</p>
        </section>

        <section class="gallery-section">
            <h3>Momen Indah Kita</h3>
            <div class="slideshow-container">
                <!-- Pastikan Anda memiliki file 'image1.jpg', 'image2.jpg', 'image3.jpg' -->
                <div class="mySlides fade">
                    <img src="image1.jpg" alt="Momen Indah 1" style="width:100%">
                </div>
                <div class="mySlides fade">
                    <img src="image2.jpg" alt="Momen Indah 2" style="width:100%">
                </div>
                <div class="mySlides fade">
                    <img src="image3.jpg" alt="Momen Indah 3" style="width:100%">
                </div>
                <!-- Tombol navigasi slideshow -->
                <a class="prev" onclick="plusSlides(-1)">&#10094;</a>
                <a class="next" onclick="plusSlides(1)">&#10095;</a>
            </div>
            <br>
            <!-- Indikator dot slideshow -->
            <div style="text-align:center">
                <span class="dot" onclick="currentSlide(1)"></span>
                <span class="dot" onclick="currentSlide(2)"></span>
                <span class="dot" onclick="currentSlide(3)"></span>
            </div>
        </section>

        <footer>
            <p>&copy; 2025 Halaman Spesial untuk Najwa.</p>
        </footer>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const accessMessage = document.getElementById('access-message');
            const mainContent = document.getElementById('main-content');
            const birthdaySong = document.getElementById('birthday-song');
            const playPauseBtn = document.getElementById('play-pause-btn');
            const confettiContainer = document.querySelector('.confetti-container');

            // Tanggal dan waktu target akses (20 Juli 2025, 15:25 WIB)
            // Penting: Sesuaikan zona waktu jika server atau browser tidak berada di WIB.
            // Di sini menggunakan offset +07:00 untuk WIB.
            const targetDate = new Date('2025-07-20T15:25:00+07:00'); 

            /**
             * Fungsi untuk memeriksa apakah waktu saat ini berada dalam jendela akses.
             * Situs hanya bisa diakses tepat pada menit 15:25 WIB tanggal 20 Juli 2025.
             */
            function checkAccess() {
                const now = new Date();
                
                // Memeriksa apakah tanggal, jam, dan menit saat ini sesuai dengan target
                const isTargetDay = now.getDate() === targetDate.getDate() &&
                                    now.getMonth() === targetDate.getMonth() &&
                                    now.getFullYear() === targetDate.getFullYear();
                
                const isTargetTime = now.getHours() === targetDate.getHours() &&
                                     now.getMinutes() === targetDate.getMinutes();

                if (isTargetDay && isTargetTime) {
                    mainContent.classList.remove('hidden'); // Tampilkan konten utama
                    accessMessage.classList.add('hidden'); // Sembunyikan pesan akses
                    birthdaySong.play(); // Putar musik
                    startConfetti(); // Mulai animasi confetti
                } else {
                    accessMessage.classList.remove('hidden'); // Tampilkan pesan akses
                    mainContent.classList.add('hidden'); // Sembunyikan konten utama
                    birthdaySong.pause(); // Hentikan musik jika tidak pada waktu akses
                }
            }

            // Periksa akses segera saat halaman dimuat
            checkAccess();

            // Atur interval untuk memeriksa akses setiap detik jika konten utama tersembunyi
            // Ini penting agar situs otomatis terbuka saat waktu yang ditentukan tiba
            if (mainContent.classList.contains('hidden')) {
                setInterval(checkAccess, 1000); // Periksa setiap 1 detik
            }

            // Kontrol Audio (Play/Pause)
            let isPlaying = true; // Status awal musik
            playPauseBtn.addEventListener('click', function() {
                if (isPlaying) {
                    birthdaySong.pause();
                    playPauseBtn.textContent = 'Putar Musik'; // Ubah teks tombol
                } else {
                    birthdaySong.play();
                    playPauseBtn.textContent = 'Pause Musik'; // Ubah teks tombol
                }
                isPlaying = !isPlaying; // Balik status musik
            });

            // Fungsionalitas Slideshow
            let slideIndex = 1; // Indeks slide saat ini
            showSlides(slideIndex); // Tampilkan slide pertama saat dimuat

            // Fungsi untuk mengubah slide (maju/mundur)
            function plusSlides(n) {
                showSlides(slideIndex += n);
            }

            // Fungsi untuk menampilkan slide tertentu berdasarkan dot
            function currentSlide(n) {
                showSlides(slideIndex = n);
            }

            // Fungsi utama untuk menampilkan slide
            function showSlides(n) {
                let i;
                let slides = document.getElementsByClassName("mySlides");
                let dots = document.getElementsByClassName("dot");
                if (n > slides.length) {slideIndex = 1} // Kembali ke slide pertama jika melebihi jumlah slide
                if (n < 1) {slideIndex = slides.length} // Kembali ke slide terakhir jika kurang dari 1
                for (i = 0; i < slides.length; i++) {
                    slides[i].style.display = "none"; // Sembunyikan semua slide
                }
                for (i = 0; i < dots.length; i++) {
                    dots[i].className = dots[i].className.replace(" active", ""); // Hapus kelas 'active' dari semua dot
                }
                slides[slideIndex-1].style.display = "block"; // Tampilkan slide saat ini
                dots[slideIndex-1].className += " active"; // Tambahkan kelas 'active' ke dot yang sesuai
            }

            // Animasi Confetti
            const confettiColors = ['#FFD700', '#FFC0CB', '#ADD8E6', '#B19CD9', '#FFB347']; // Warna confetti

            /**
             * Fungsi untuk membuat dan menjatuhkan satu confetti.
             */
            function createConfetti() {
                const confetti = document.createElement('div');
                confetti.classList.add('confetti');
                // Pilih warna acak
                confetti.style.backgroundColor = confettiColors[Math.floor(Math.random() * confettiColors.length)];
                // Posisi awal acak di bagian atas layar
                confetti.style.left = Math.random() * 100 + 'vw';
                // Ukuran acak
                const size = Math.random() * 10 + 5; // Ukuran antara 5px dan 15px
                confetti.style.width = size + 'px';
                confetti.style.height = size + 'px';
                // Durasi animasi acak
                confetti.style.animationDuration = (Math.random() * 2 + 3) + 's'; // Antara 3s dan 5s
                // Delay animasi acak
                confetti.style.animationDelay = (Math.random() * 0.5) + 's'; // Hingga 0.5s delay

                confettiContainer.appendChild(confetti);

                // Hapus confetti setelah animasinya selesai untuk menghemat memori
                confetti.addEventListener('animationend', () => {
                    confetti.remove();
                });
            }

            let confettiInterval; // Variabel untuk menyimpan interval confetti

            /**
             * Fungsi untuk memulai animasi confetti secara terus-menerus.
             */
            function startConfetti() {
                // Hentikan interval sebelumnya jika ada untuk menghindari duplikasi
                if (confettiInterval) {
                    clearInterval(confettiInterval);
                }
                // Buat confetti baru setiap 100ms
                confettiInterval = setInterval(createConfetti, 100); 
            }

            /**
             * Fungsi untuk menghentikan animasi confetti.
             */
            function stopConfetti() {
                clearInterval(confettiInterval);
                // Hapus semua confetti yang ada
                confettiContainer.innerHTML = '';
            }
        });
    </script>
</body>
</html>
