<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Profil Mahasiswa - Miftahul Nurul Aini</title>
  <style>
    /* --- CSS sama seperti versi awalmu, tidak dihapus biar tampilannya tetap cantik --- */
  </style>
</head>
<body>
  <!-- Floating particles -->
  <div class="particles">
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
  </div>

  <!-- Cute decorations -->
  <div class="cute-decoration decoration-1">💖</div>
  <div class="cute-decoration decoration-2">🌸</div>
  <div class="cute-decoration decoration-3">💕</div>

  <div class="container">
    <!-- Profile Card -->
    <div class="profile-card">
      <div class="profile-header">
        <div class="photo-container">
          <img id="profilePhoto" src="foto.JPG" 
               alt="Foto Profil Miftahul Nurul Aini" class="profile-photo">
          <button class="upload-btn" onclick="document.getElementById('photoInput').click()">📷</button>
          <input type="file" id="photoInput" class="file-input" accept="image/*" onchange="changePhoto(event)">
        </div>
        
        <div class="profile-info">
          <h1>Miftahul Nurul Aini</h1>
          
          <div class="info-item">
            <span class="info-icon">🎓</span>
            <strong>NIM:</strong> &nbsp;24416255201025
          </div>

          <div class="info-item">
            <span class="info-icon">🏫</span>
            <strong>Kelas:</strong> &nbsp;IF24B
          </div>
          
          <div class="info-item">
            <span class="info-icon">📧</span>
            <strong>Email:</strong> &nbsp;
            <a href="mailto:if24.miftahulaini@mhs.ubpkarawang.ac.id">if24.miftahulaini@mhs.ubpkarawang.ac.id</a>
          </div>
          
          <div class="info-item">
            <span class="info-icon">🌐</span>
            <strong>Website:</strong> &nbsp;
            <a href="https://www.ubpkarawang.ac.id" target="_blank">www.ubpkarawang.ac.id</a>
          </div>
        </div>
      </div>
    </div>

    <!-- Posts Section -->
    <div class="posts-section">
      <h2>📝 Postingan Saya</h2>
      
      <div class="post-card">
        <h3>Apa itu Attribute</h3>
        <p>Entitas adalah sesuatu yang dapat diidentifikasi secara unik dan perlu disimpan informasinya dalam sebuah sistem. Entitas bisa berupa orang, benda, tempat, peristiwa, ataupun konsep yang ada dalam dunia nyata maupun dunia abstrak, selama itu relevan dengan sistem yang sedang dibuat. Dalam ERD, entitas digambarkan sebagai objek utama yang akan memiliki data tersendiri.</p>
      </div>
      
      <div class="post-card">
        <h3>Apa itu Entitas</h3>
        <p>Atribut adalah karakteristik atau ciri-ciri yang dimiliki oleh entitas maupun relasi. Atribut digunakan untuk menjelaskan detail informasi dari entitas, sehingga setiap entitas bisa dibedakan dan dideskripsikan lebih jelas. Beberapa atribut juga berfungsi sebagai pengenal unik (primary key) agar setiap data dalam entitas tidak bercampur. Dengan kata lain, atribut adalah "sifat" atau "informasi tambahan" yang melekat pada entitas atau relasi.</p>
      </div>
      
      <div class="post-card">
        <h3>Apa itu Relasi dalam ERD.</h3>
        <p>Relasi dalam ERD adalah hubungan yang menggambarkan keterkaitan antara satu entitas dengan entitas lainnya dalam sebuah sistem basis data. Relasi menunjukkan bagaimana data dari entitas yang berbeda saling berhubungan sehingga membentuk struktur informasi yang utuh.</p>
      </div>
    </div>
  </div>

  <script>
    function changePhoto(event) {
      const file = event.target.files[0];
      if (file) {
        const reader = new FileReader();
        reader.onload = function(e) {
          document.getElementById('profilePhoto').src = e.target.result;
        }
        reader.readAsDataURL(file);
      }
    }

    document.getElementById('profilePhoto').addEventListener('click', function() {
      this.style.animation = 'none';
      setTimeout(() => {
        this.style.animation = 'bounce 2s infinite';
      }, 100);
    });

    document.addEventListener('DOMContentLoaded', function() {
      setInterval(() => {
        const decorations = document.querySelectorAll('.cute-decoration');
        const pinkEmojis = ['💖', '💕', '🌸', '🌺', '💗', '💓', '🎀'];
        decorations.forEach(el => {
          el.textContent = pinkEmojis[Math.floor(Math.random() * pinkEmojis.length)];
        });
      }, 3000);
    });
  </script>
</body>
</html>
