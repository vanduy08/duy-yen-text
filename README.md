
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Chữ rơi tình yêu</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      background: black;
      overflow: hidden;
      height: 100vh;
      width: 100vw;
      font-family: sans-serif;
    }
    .container {
      position: relative;
      width: 100%;
      height: 100%;
    }
    .text, .heart {
      position: absolute;
      white-space: nowrap;
      pointer-events: none;
      opacity: 0.85;
      animation: fall linear infinite;
    }
    .text {
      color: white;
      font-size: 1.5rem;
      font-weight: bold;
      text-shadow: 0 0 10px #fff, 0 0 20px #0ff, 0 0 30px #00f;
    }
    .heart {
      color: red;
      font-size: 2rem;
    }
    @keyframes fall {
      0% {
        transform: translateY(-10vh);
        opacity: 1;
      }
      100% {
        transform: translateY(110vh);
        opacity: 0.7;
      }
    }
  </style>
</head>
<body>
  <iframe width="100%" height="166" scrolling="no" frameborder="no" allow="autoplay"
  src="https://w.soundcloud.com/player/?url=https%3A//soundcloud.com/user-899327446/lo-nhu-anh-yeu-em-chi-dan&color=%23ff5500&auto_play=true&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true">
</iframe>
  <!-- Nhạc nền tự động phát -->
  <audio autoplay loop>
    <source src="music.mp3" type="audio/mpeg" />
    Trình duyệt của bạn không hỗ trợ phát nhạc.
  </audio>

  <div class="container" id="container"></div>

  <script>
    const container = document.getElementById('container');
    const texts = [
      'Chúc em luôn Hạnh Phúc',
      'Chúc em luôn Thành Công',
      'Chúc em luôn May Mắn',
      'Anh Yêu Em',
      'Yêu bé Dâu',
      '14/4/2025'
    ];

    for (let i = 0; i < 50; i++) {
      const el = document.createElement('div');
      el.className = 'text';
      el.innerText = texts[Math.floor(Math.random() * texts.length)];
      el.style.left = Math.random() * 100 + 'vw';
      el.style.fontSize = (1 + Math.random() * 1.2) + 'rem';
      el.style.animationDuration = (8 + Math.random() * 6) + 's';
      el.style.animationDelay = (Math.random() * 5) + 's';
      container.appendChild(el);
    }

    for (let i = 0; i < 30; i++) {
      const heart = document.createElement('div');
      heart.className = 'heart';
      heart.innerHTML = '❤️';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.fontSize = (1 + Math.random() * 1.5) + 'rem';
      heart.style.animationDuration = (8 + Math.random() * 6) + 's';
      heart.style.animationDelay = (Math.random() * 5) + 's';
      container.appendChild(heart);
    }
  </script>
</body>
</html>

>
