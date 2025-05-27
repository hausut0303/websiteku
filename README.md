<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Basket Elite Trainer - Akademi Basket Profesional</title>
  <style>
    /* CSS tetap sama seperti sebelumnya */
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Arial', sans-serif;
      color: #fff;
      background: linear-gradient(270deg, #4f46e5, #9333ea);
      background-size: 400% 400%;
      animation: gradientBG 15s ease infinite;
      overflow-x: hidden;
      position: relative;
      min-height: 100vh;
    }

    @keyframes gradientBG {
      0% {background-position: 0% 50%;}
      50% {background-position: 100% 50%;}
      100% {background-position: 0% 50%;}
    }

    @keyframes slideText {
      0% { transform: translateX(100%); }
      100% { transform: translateX(-100%); }
    }

    .text-3d-rgb {
      font-size: 1.8rem;
      font-weight: bold;
      text-align: center;
      margin: 20px 0;
      text-transform: uppercase;
      letter-spacing: 2px;
      text-shadow: 2px 2px 4px #000;
      animation: slideText 20s linear infinite;
      white-space: nowrap;
      position: relative;
      z-index: 2;
    }

    nav {
      background: rgba(0,0,0,0.7);
      text-align: center;
      padding: 10px;
      position: relative;
      z-index: 2;
    }

    nav a {
      color: #facc15;
      margin: 0 15px;
      text-decoration: none;
      font-weight: bold;
    }

    .hero {
      position: relative;
      text-align: center;
      padding: 60px 20px 120px;
      position: relative;
      z-index: 2;
    }

    .hero h1 {
      font-size: 3rem;
      font-weight: bold;
      text-shadow: 2px 2px 4px #000;
      margin-bottom: 10px;
    }

    .hero p {
      font-size: 1.2rem;
      max-width: 700px;
      margin: 0 auto;
    }

    .cta {
      background: #facc15;
      color: #000;
      padding: 10px 20px;
      border-radius: 8px;
      text-decoration: none;
      font-weight: bold;
      display: inline-block;
      margin-top: 20px;
      z-index: 2;
      position: relative;
    }

    section {
      padding: 50px 20px;
      text-align: center;
      position: relative;
      z-index: 2;
    }

    .contact-box, .galeri {
      background: rgba(0,0,0,0.5);
      border-radius: 10px;
      padding: 30px;
      margin: 20px auto;
      max-width: 800px;
      position: relative;
      z-index: 2;
    }

    .galeri img {
      width: 200px;
      height: 120px;
      object-fit: cover;
      border-radius: 8px;
      margin: 10px;
    }

    .social-icons a {
      text-decoration: none;
      color: #facc15;
      margin: 0 10px;
      font-size: 1.5rem;
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      gap: 6px;
      font-weight: bold;
    }

    footer {
      text-align: center;
      padding: 20px;
      background: rgba(0,0,0,0.8);
      position: relative;
      z-index: 2;
    }

    /* Canvas Basket Rain di belakang semua */
    #basket-rain {
      position: fixed;
      top: 0;
      left: 0;
      pointer-events: none;
      z-index: 1;
      width: 100vw;
      height: 100vh;
    }
  </style>
</head>
<body>

  <div class="text-3d-rgb">
    Akademi Basket Elite Trainer - Program Latihan Basket Profesional | Jadwal: Setiap Sabtu & Minggu | Lokasi: GOR Pradipa Medan | Benefit: Coaching Eksklusif, Sertifikat, Jersey Latihan, dan Komunitas Basket Keren!
  </div>

  <nav>
    <a href="#tentang">Tentang Kami</a>
    <a href="#program">Program</a>
    <a href="#galeri">Galeri</a>
    <a href="#jadwal">Jadwal</a>
    <a href="#kontak">Kontak</a>
  </nav>

  <header class="hero">
    <h1>Basket Elite Trainer</h1>
    <p>Akademi Basket untuk Pemula hingga Pro • Latihan Intensif & Fun • Mulai dari Usia 7–18 Tahun</p>
    <h2>Form Pendaftaran</h2>
    <a href="#form" class="cta">Daftar Sekarang</a>
<form action="https://formspree.io/f/xblovwog" method="POST">
    <!-- Form Pendaftaran -->
    <section id="form" style="max-width: 500px; margin: 40px auto; background: rgba(0,0,0,0.5); padding: 25px; border-radius: 10px; color: #fff; position: relative; z-index: 2;">
      <h2 style="margin-bottom: 15px;">Form Pendaftaran</h2>
      <form id="registrationForm">
        <label for="nama" style="display:block; margin-bottom:6px;">Nama Lengkap:</label>
        <input type="text" id="nama" name="nama" required style="width:100%; padding:8px; margin-bottom:15px; border-radius:6px; border:none;">

        <label for="umur" style="display:block; margin-bottom:6px;">Umur:</label>
        <input type="number" id="umur" name="umur" min="7" max="18" required style="width:100%; padding:8px; margin-bottom:15px; border-radius:6px; border:none;">

        <label for="email" style="display:block; margin-bottom:6px;">Email:</label>
        <input type="email" id="email" name="email" required style="width:100%; padding:8px; margin-bottom:15px; border-radius:6px; border:none;">

        <label for="hp" style="display:block; margin-bottom:6px;">Nomor HP:</label>
        <input type="tel" id="hp" name="hp" required style="width:100%; padding:8px; margin-bottom:15px; border-radius:6px; border:none;">

        <button type="submit" style="width:100%; background:#facc15; border:none; padding:12px; font-weight:bold; border-radius:8px; cursor:pointer;">Kirim Pendaftaran</button>
      </form>
      <p id="msg" style="margin-top:15px;"></p>
    </section>

    <!-- Tambahkan Canvas untuk Efek Basket Rain -->
    <canvas id="basket-rain"></canvas>

  </header>

  <!-- Konten lainnya tetap sama -->
  <section id="tentang">
    <h2>Tentang Kami</h2>
    <p>Kami adalah akademi basket profesional yang fokus membantu anak-anak dan remaja mengembangkan skill basket mereka dengan metode latihan yang terstruktur, pelatih berpengalaman, dan fasilitas lengkap.</p>
  </section>

  <section id="program">
    <h2>Program Kami</h2>
    <ul style="list-style: none; padding: 0;">
      <li>🏀 Camp Liburan</li>
      <li>🏀 Latihan Privat</li>
      <li>🏀 Kelas Kelompok</li>
    </ul>
  </section>

  <section id="jadwal">
    <h2>Jadwal Latihan</h2>
    <p>📅 Sabtu & Minggu: 08.00 - 10.00 WIB | 📍 GOR Pradipa Medan</p>
  </section>

  <section id="galeri">
    <h2>Galeri Kegiatan</h2>
    <div class="galeri">
    <div class="gallery-item">
   <img src="https://s14.gifyu.com/images/bxbfJ.png">
  <p style="text-align: center; font-weight: bold; margin-top: 8px;">2ND RED BULL 22/MEI 2023</p>
  <img src="https://s14.gifyu.com/images/bxb5N.md.png">
  <p style="text-align: center; font-weight: bold; margin-top: 8px;">XYZ BASKET TEAM GO TO MIKIE FUNLAND 27/JUNI 2023</p>
  <img src="https://s14.gifyu.com/images/bxb5Y.md.png">
  <p style="text-align: center; font-weight: bold; margin-top: 8px;">BANJIR PIALA KAPOLRES MEDAN BELAWAN 1/JUNI 2023</p>
  <img src="https://s14.gifyu.com/images/bxbr8.md.png">
  <p style="text-align: center; font-weight: bold; margin-top: 8px;">3RD PLACE MBA VOL-2 8/AGUSTUS 2023</p>
  <img src="https://s14.gifyu.com/images/bxbr0.md.png">
  <p style="text-align: center; font-weight: bold; margin-top: 8px;">2ND PORKOT MEDAN 25/AGUSTUS 2023</p>
  <img src="https://s14.gifyu.com/images/bxbDd.md.png">
  <p style="text-align: center; font-weight: bold; margin-top: 8px;">2ND CKS CUP 26/AGUSTUS 2023</p>
  <img src="https://s14.gifyu.com/images/bxboL.md.png">
  <p style="text-align: center; font-weight: bold; margin-top: 8px;">2ND BRAHRANG CUP 17/SEPTEMBER 2023</p>
  <img src="https://s14.gifyu.com/images/bxboV.md.png">
  <p style="text-align: center; font-weight: bold; margin-top: 8px;">RAJAWALI BASKETBALL TEAM COME TO SMA.WAHIDIN MEDAN</p>
  <img src="https://s14.gifyu.com/images/bxbo5.md.png">
  <p style="text-align: center; font-weight: bold; margin-top: 8px;">2ND WAHIDIN CUP 9/MARET 2024</p>
  <img src="https://s14.gifyu.com/images/bxbYW.md.png">
  <p style="text-align: center; font-weight: bold; margin-top: 8px;">2ND YAMAHA FAZZIO CUP 30/NOVEMBER 2024</p>
  <img src="https://s14.gifyu.com/images/bxbAL.png">
  <p style="text-align: center; font-weight: bold; margin-top: 8px;">FANTASTIC FOUR DBL SERIES NORTH SUMATERA 2024/2025</p>
    </div>
  </section>

  <section id="kontak">
    <h2>Hubungi Kami</h2>
    <div class="contact-box">
      <p>📍 Lokasi: GOR Pradipa Medan</p>
      <p>📞 WhatsApp: <a href="https://wa.me/6285836776346" target="_blank" style="color: #facc15;">+62 858-3677-6346</a></p>
      <p>📧 Email: hausut981@gmail.com</p>
      <div class="social-icons">
        <a href="https://instagram.com/krik_7kik" target="_blank">📸 Instagram</a>
        <a href="https://facebook.com/jangkrik" target="_blank">📘 Facebook</a>
        <a href="https://tiktok.com/@j4ngkr1k.c4st1l0" target="_blank">🎵 TikTok</a>
        <a href="https://youtube.com/@jangkrik" target="_blank">▶️ YouTube</a>
      </div>
    </div>
  </section>

  <footer>
    &copy; 2025 Basket Elite Trainer. crate by Xruzz.
  </footer>

  <script>
    const canvas = document.getElementById("basket-rain");
    const ctx = canvas.getContext("2d");

    function resizeCanvas() {
      canvas.width = window.innerWidth;
      canvas.height = window.innerHeight;
    }
    resizeCanvas();
    window.addEventListener("resize", resizeCanvas);

    const balls = [];
    const basketImg = new Image();
    basketImg.src = 'https://upload.wikimedia.org/wikipedia/commons/thumb/7/7a/Basketball.png/240px-Basketball.png';

    for (let i = 0; i < 30; i++) {
      balls.push({
        x: Math.random() * canvas.width,
        y: Math.random() * canvas.height,
        speed: 0.3 + Math.random() * 0.7,
        size: 10 + Math.random() * 5
      });
    }

    function animate() {
      ctx.clearRect(0, 0, canvas.width, canvas.height);
      balls.forEach(ball => {
        ctx.drawImage(basketImg, ball.x, ball.y, ball.size, ball.size);
        ball.y += ball.speed;
        if (ball.y > canvas.height) {
          ball.y = -ball.size;
          ball.x = Math.random() * canvas.width;
        }
      });
      requestAnimationFrame(animate);
    }

    basketImg.onload = animate;

    // Script Form Validasi
    const form = document.getElementById('registrationForm');
    const msg = document.getElementById('msg');

    form.addEventListener('submit', function(e) {
      e.preventDefault();
      const nama = form.nama.value.trim();
      const umur = form.umur.value;
      const email = form.email.value.trim();
      const hp = form.hp.value.trim();

      if (umur < 7 || umur > 18) {
        msg.style.color = 'red';
        msg.textContent = 'Umur harus antara 7 hingga 18 tahun.';
        return;
      }

      msg.style.color = '#0f0';
      msg.textContent = 'Terima kasih sudah mendaftar, kami akan menghubungi Anda segera.';
      form.reset();
    });
  </script>
</body>
</html>
