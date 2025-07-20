<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Ucapan Ulang Tahun Najwa Alya Shafarina</title>
  <script src="https://cdn.tailwindcss.com"></script>

  <style>
    @import url('https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@400;600&display=swap');

    body {
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #f7e7db, #fce4e1);
      color: #50332f;
      min-height: 100vh;
      overflow-x: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 1.5rem;
    }

    main {
      max-width: 600px;
      background: rgba(255 248 244 / 0.9);
      border-radius: 24px;
      padding: 2rem 2.5rem;
      box-shadow:
        0 15px 30px rgb(255 209 155 / 0.3),
        0 4px 8px rgb(255 209 155 / 0.15);
      position: relative;
      text-align: center;
    }

    h1 {
      font-weight: 700;
      font-size: 2.5rem;
      letter-spacing: 0.03em;
      margin-bottom: 1rem;
      color: #b25c49;
    }

    .birthday-msg {
      font-size: 1.2rem;
      line-height: 1.6;
      padding-bottom: 1.5rem;
      color: #6d4736;
      font-weight: 500;
    }

    .signature {
      font-family: 'Great Vibes', cursive;
      font-size: 2.4rem;
      color: #bb7e69;
      margin-top: 2rem;
      user-select: none;
    }

    .photo-container {
      margin: 1.5rem auto 2rem;
      width: 220px;
      height: 220px;
      border-radius: 50%;
      overflow: hidden;
      border: 5px solid #f6d0bb;
      box-shadow: 0 6px 14px rgb(183 132 104 / 0.3);
      background: #fef4f1;
    }

    .photo-container img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: center;
      display: block;
    }

    /* Light confetti animation */
    .confetti-piece {
      position: fixed;
      width: 12px;
      height: 12px;
      background-color: #f4bbad;
      opacity: 0.8;
      top: -15px;
      animation-timing-function: cubic-bezier(0.3, 0.7, 0.4, 1);
      pointer-events: none;
      z-index: 1000;
      border-radius: 3px;
      filter: drop-shadow(0 0 1px rgb(160 60 38));
    }

    .confetti-piece:nth-child(2n) {
      background-color: #f5d0bc;
      width: 9px;
      height: 9px;
      border-radius: 50%;
    }

    .toggle-audio {
      margin-top: 1rem;
      font-size: 0.9rem;
      color: #a8705a;
      user-select: none;
      cursor: pointer;
      border: 1.5px solid #c39986;
      border-radius: 20px;
      padding: 0.4rem 1.2rem;
      transition: background-color 0.3s, color 0.3s;
      display: inline-block;
    }

    .toggle-audio:hover {
      background-color: #c39986;
      color: #fff;
    }

    /* Time lock container style */
    #locked-message {
      max-width: 400px;
      padding: 2rem;
      background: #fceeeb;
      border: 2px solid #e0a897;
      border-radius: 20px;
      text-align: center;
      font-weight: 600;
      color: #aa6d62;
      box-shadow:
        0 8px 10px rgb(208 119 96 / 0.25);
      user-select: none;
    }
  </style>
</head>

<body>
  <main id="content" role="main" aria-live="polite">
    <!-- Content dynamically inserted by JavaScript -->
  </main>

  <!-- Audio element for birthday song -->
  <audio id="birthday-audio" loop preload="auto" aria-label="Lagu ulang tahun jambrud" >
    <source src="https://cdn.pixabay.com/download/audio/2021/08/04/audio_a3e4e6f9bd.mp3?filename=happy-birthday-a-song-loop-7053.mp3" type="audio/mpeg" />
    <!-- This audio is an instrumental cheerful birthday loop from Pixabay free sounds -->
    Your browser does not support the audio element.
  </audio>

  <script>
    // Target date and time: 20 July 2025, 16:25 WIB (WIB = UTC+7)
    // We'll compare current time in UTC+7
    function isAccessAllowed() {
      const now = new Date();

      // Convert user's local time to UTC+7 time
      const utc = now.getTime() + (now.getTimezoneOffset() * 60000);
      const utcPlus7 = new Date(utc + (7 * 3600000));

      // Target date exact hour/minute
      // July 20, 2025 16:25 in UTC+7
      const target = new Date(Date.UTC(2025, 6, 20, 16 - 7, 25, 0)); // JS months: 0-based, so 6 = July
      // 16:25 WIB = 16:25 at UTC+7 => in UTC is 09:25

      /* Strict allow exact minute access only:
         show content only if current date and hour/minute matches exactly.
         Allow 1 minute window. */
      if (
        utcPlus7.getFullYear() === 2025 &&
        utcPlus7.getMonth() === 6 &&
        utcPlus7.getDate() === 20 &&
        utcPlus7.getHours() === 16 &&
        utcPlus7.getMinutes() === 25
      ) {
        return true;
      }
      return false;
    }

    // Confetti animation part
    function createConfettiPiece() {
      const confetti = document.createElement('div');
      confetti.classList.add('confetti-piece');
      confetti.style.left = Math.random() * window.innerWidth + 'px';
      confetti.style.backgroundColor = randomPastelColor();
      confetti.style.width = (8 + Math.random() * 6) + 'px';
      confetti.style.height = (8 + Math.random() * 6) + 'px';
      confetti.style.opacity = 0.8 + Math.random() * 0.3;

      confetti.style.animationName = 'confetti-fall';
      confetti.style.animationDuration = 3 + Math.random() * 2 + 's';
      confetti.style.animationTimingFunction = 'ease-out';
      confetti.style.animationIterationCount = '1';

      // Animate falling and drifting
      const startX = Math.random() * window.innerWidth;
      const endX = startX + (Math.random() * 100 - 50);
      confetti.style.left = startX + 'px';

      document.body.appendChild(confetti);

      // Falling animation using JS for better randomization
      let start = null;
      const duration = 3500;
      const initialTop = -20;

      function animate(timestamp) {
        if (!start) start = timestamp;
        const progress = timestamp - start;
        const fraction = Math.min(progress / duration, 1);
        confetti.style.transform = 'translate(' + ((endX - startX) * fraction).toFixed(2) + 'px, ' + ((window.innerHeight + 30) * fraction).toFixed(2) + 'px) rotate(' + (fraction * 360) + 'deg)';

        if (fraction < 1) {
          requestAnimationFrame(animate);
        } else {
          confetti.remove();
        }
      }
      requestAnimationFrame(animate);
    }

    function randomPastelColor() {
      const r = Math.floor((Math.random() * 127) + 128);
      const g = Math.floor((Math.random() * 127) + 128);
      const b = Math.floor((Math.random() * 127) + 128);
      return `rgba(${r}, ${g}, ${b}, 0.8)`;
    }

    function showLockedMessage() {
      const content = document.getElementById('content');
      content.innerHTML = 
        `<div id="locked-message" role="alert" aria-live="assertive">
          <p>
            Ups! bukanya nanti aja, buru-buru amat sih, uda gasabar yaa,<br />
            buka jam <strong>16:25 WIB</strong> tanggal <strong>20 Juli 2025</strong>.<br /><br />
            Datang lagi ya nanti!
          </p>
        </div>`;
    }

    function showBirthdayContent() {
      const content = document.getElementById('content');
      content.innerHTML = `
        <h1 tabindex="0">Selamat Ulang Tahun ke-20, Najwa Alya Shafarina!</h1>
        <div class="photo-container" aria-label="Foto memorable Najwa Alya Shafarina">
          <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/f5f5c616-eb95-4302-b0d8-a1db19127f1d.png" alt="Foto berwarna hitam putih Najwa Alya Shafarina memakai beanie hitam dengan senyuman hangat, latar belakang gelap"/>
        </div>
        <p class="birthday-msg" tabindex="0">
          Dua puluh tahun perjalananmu menginspirasi dan memberi warna pada dunia. Semoga setiap langkahmu selalu dipenuhi kebahagiaan, cinta, dan keberhasilan tanpa batas. Tetaplah bersinar dan menjadi yang terbaik.<br /><br />
          Doaku dan harapanku untukmu adalah kebahagiaan abadi dan segala impianmu menjadi nyata. Teruslah berani bermimpi dan mengejar mimpimu dengan penuh semangat dan keyakinan. Selamat ulang tahun yang ke-20, Najwa!
        </p>
        <p class="signature" aria-label="Tanda tangan pribadi ucapan selamat ulang tahun" tabindex="0">- Dari yang selalu mendukungmu</p>
        <button id="toggle-audio" type="button" class="toggle-audio" aria-pressed="false" aria-label="Toggle musik ulang tahun">🎵 Putar Lagu Ulang Tahun</button>
      `;

      // Attach confetti animation interval
      setInterval(() => {
        createConfettiPiece();
      }, 400);

      // Audio controls
      const audio = document.getElementById('birthday-audio');
      const toggleBtn = document.getElementById('toggle-audio');
      toggleBtn.addEventListener('click', () => {
        if (audio.paused) {
          audio.play();
          toggleBtn.textContent = '🔇 Matikan Lagu Ulang Tahun';
          toggleBtn.setAttribute('aria-pressed', 'true');
        } else {
          audio.pause();
          toggleBtn.textContent = '🎵 Putar Lagu Ulang Tahun';
          toggleBtn.setAttribute('aria-pressed', 'false');
        }
      });
    }

    // Initialization
    document.addEventListener('DOMContentLoaded', () => {
      if (isAccessAllowed()) {
        showBirthdayContent();
      } else {
        showLockedMessage();
      }
    });
  </script>
</body>
</html>

