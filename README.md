<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ulang Tahun Najwa Alya Shafarina</title>
    <style>
        body {
            margin: 0;
            font-family: poppins, sans-serif;
            color: white;
        }

        .coming-soon {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: black;
            text-align: center;
        }

        .main {
            display: none;
            position: relative;
            height: 100vh;
            background-image: url('https://drive.google.com/uc?export=view&id=1U9DxXlWxDCmL-7R9RqZDYB5QAFF5bRMS');
            background-size: cover;
            background-position: center;
            color: #fff;
            text-align: center;
        }

        h1 {
            margin-top: 20%;
            font-size: 2.5em;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
        }

        button {
            margin-top: 20px;
            padding: 10px 20px;
            font-size: 1.2em;
            background-color: #ff6f61;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        button:hover {
            background-color: #ff4f3d;
        }

        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
        }

        .modal-content {
            background-color: white;
            color: black;
            padding: 20px;
            border-radius: 10px;
            text-align: center;
        }

        .confetti {
            position: absolute;
            width: 100%;
            height: 100%;
            pointer-events: none;
            overflow: hidden;
        }
    </style>
</head>
<body>

    <div class="coming-soon" id="coming-soon">
        <h1>Coming Soon for Najwa’s 20th Birthday 🎉 — Available at 15:40, July 20th 2025</h1>
    </div>

    <div class="main" id="main">
        <audio autoplay loop>
            <source src="https://drive.google.com/uc?export=download&id=1U9DxXlWxDCmL-7R9RqZDYB5QAFF5bRMS" type="audio/mpeg">
        </audio>
        <h1>Selamat Ulang Tahun Najwa Alya Shafarina 💖 20 Tahun Hari Ini!</h1>
        <button id="messageButton">Pesan dari siapa yah</button>
        <div class="confetti" id="confetti"></div>
    </div>

    <div class="modal" id="modal">
        <div class="modal-content">
            <p>Semoga Najwa selalu bahagia, sehat, dan makin bersinar. Selamat 20 tahun! 🥳</p>
            <button onclick="closeModal()">Tutup</button>
        </div>
    </div>

    <script>
        const comingSoon = document.getElementById('coming-soon');
        const main = document.getElementById('main');
        const modal = document.getElementById('modal');
        const messageButton = document.getElementById('messageButton');

        const targetDate = new Date('2025-07-20T15:40:00+07:00');

        function checkAccess() {
            const now = new Date();
            if (now >= targetDate) {
                comingSoon.style.display = 'none';
                main.style.display = 'block';
                startConfetti();
            }
        }

        function startConfetti() {
            // Simple confetti effect
            const confetti = document.getElementById('confetti');
            for (let i = 0; i < 100; i++) {
                const confettiPiece = document.createElement('div');
                confettiPiece.style.position = 'absolute';
                confettiPiece.style.width = '10px';
                confettiPiece.style.height = '10px';
                confettiPiece.style.backgroundColor = 'rgba(255, 255, 255, 0.8)';
                confettiPiece.style.left = Math.random() * 100 + 'vw';
                confettiPiece.style.top = Math.random() * 100 + 'vh';
                confettiPiece.style.transition = 'transform 2s';
                confettiPiece.style.transform = 'translateY(100vh)';
                confetti.appendChild(confettiPiece);
            }
        }

        messageButton.onclick = function() {
            modal.style.display = 'flex';
        }

        function closeModal() {
            modal.style.display = 'none';
        }

        checkAccess();
    </script>

</body>
</html>
