<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8" />
  <title>2025年8月14日 - おでかけ〜♪</title>
  <link rel="stylesheet" href="../style.css" />

  <style>
    #blackout {
      display: none;
      position: fixed;
      inset: 0;
      background: black;
      z-index: 9999;
    }

    .protected-photo {
      width: 100%;
      user-select: none;
      -webkit-user-drag: none;
      pointer-events: auto;
      display: block;
    }

    .watermark-container {
      position: relative;
      display: inline-block;
      width: 100%;
      max-width: 500px;
      margin: 24px auto;
    }

    .watermark {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      color: white;
      font-size: 48px;
      opacity: 0.1;
      background: rgba(0, 0, 0, 0);
      padding: 0;
      border-radius: 0;
      text-shadow: 2px 2px 8px black;
      pointer-events: none;
      white-space: nowrap;
      user-select: none;
    }

    main {
      padding: 20px;
      text-align: center;
    }
  </style>
</head>
<body oncontextmenu="return false;" onselectstart="return false;" ondragstart="return false;">
  <header>
    <h1>HIKARI・HIKARU 日々のブログ</h1>
  </header>

  <main>
    <h2>2025年8月14日 - おでかけ〜♪</h2>
    <p>
      少し前に久しぶりにおでかけしました✨<br>
      その時の写真です...（笑）<br><br>
    </p>

    <!-- image0 -->
    <div class="watermark-container">
      <img src="image0.jpeg" alt="おでかけ写真1" class="protected-photo" />
      <div class="watermark">© HIKARI-HIKARU 2025</div>
    </div>

    <!-- image1 -->
    <div class="watermark-container">
      <img src="image1.jpeg" alt="おでかけ写真2" class="protected-photo" />
      <div class="watermark">© HIKARI-HIKARU 2025</div>
    </div>

    <p>
      以上！<br><br>
      そんな感じです。笑
    </p>
  </main>

  <div id="blackout"></div>

  <script>
    const photos = document.querySelectorAll('.protected-photo');
    const blackout = document.getElementById('blackout');

    photos.forEach((photo) => {
      let timer;
      photo.addEventListener('touchstart', () => {
        timer = setTimeout(() => {
          blackout.style.display = 'block';
        }, 500);
      });
      photo.addEventListener('touchend', () => clearTimeout(timer));
      photo.addEventListener('touchcancel', () => clearTimeout(timer));
    });

    blackout.addEventListener('click', () => {
      blackout.style.display = 'none';
    });
  </script>
</body>
</html>
