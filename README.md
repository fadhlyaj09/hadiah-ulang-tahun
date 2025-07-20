<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Selamat Ulang Tahun Najwa Alya Shafarina</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            background-color: #f8e1e1;
            color: #333;
            text-align: center;
            overflow: hidden;
        }

        h1 {
            font-size: 3em;
            color: #d4af37; /* Gold color */
        }

        p {
            font-size: 1.5em;
            margin: 20px 0;
        }

        .signature {
            font-style: italic;
            font-size: 1.2em;
            margin-top: 30px;
        }

        .hidden-message {
            display: none;
        }

        .balloons {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://example.com/balloons.png') no-repeat center center;
            background-size: cover;
            animation: float 5s infinite;
        }

        @keyframes float {
            0% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0); }
        }
    </style>
</head>
<body>

    <div class="balloons"></div>

    <h1>Selamat Ulang Tahun Najwa Alya Shafarina!</h1>
    <p>Semoga di usia yang ke-20 ini, Najwa selalu dikelilingi oleh kebahagiaan, cinta, dan kesuksesan. Teruslah bersinar dan menjadi inspirasi bagi banyak orang!</p>
    <p class="signature">- Dengan cinta, teman-temanmu</p>

    <audio controls>
        <source src="https://vocaroo.com/1ecKN8QNPzoi" type="audio/mpeg">
        Your browser does not support the audio element.
    </audio>

    <script>
        const currentDate = new Date();
        const targetDate = new Date('2025-07-20T15:00:00+07:00');

        if (currentDate < targetDate) {
            document.body.innerHTML = "<h1>Ups! Halaman spesial ini hanya tersedia pada pukul 15:00 WIB tanggal 20 Juli 2025. Datang lagi ya nanti!</h1>";
        } else {
            // Show the content if the date is correct
            document.querySelector('.balloons').style.display = 'block';
        }
    </script>

</body>
</html>
