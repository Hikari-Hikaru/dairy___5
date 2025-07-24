<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8" />
  <title>2025年7月28日 - おでかけ〜♪</title>
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

    .image-row {
      display: flex;
      flex-wrap: nowrap; /* 折り返さない */
      justify-content: center;
      gap: 16px; /* 画像間の余白 */
      margin-top: 20px;
      overflow-x: auto; /* 横スクロール可 */
      padding-bottom: 10px; /* スクロールバーと画像の間に余白 */
    }

    .watermark-container {
      position: relative;
      flex: 0 0 auto; /* 横並び固定 */
      width: 80%; /* 画面幅の80%サイズ */
      max-width: 400px;
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

    /* 横スクロールバーを目立たせない（オプション） */
    .image-row::-webkit-scrollbar {
      height: 8px;
    }
    .image-row::-webkit-scrollbar-thumb {
      background-color: rgba(0,0,0,0.3);
      border-radius: 4px;
    }
  </style>
</head>
<body oncontextmenu="return false;" onselectstart="return false;" ondragstart="return false;">
  <header>
    <h1>HIKARI・HIKARU 日々のブログ</h1>
  </header>

  <main>
    <h2>2025年7月28日 - おでかけ〜♪</h2>
    <p>
      少し前に久しぶりにおでかけしました✨<br>
      その時の写真です...（笑）<br><br>
      以上！<br><br>
      そんな感じです。笑
    </p>

    <!-- 横並び画像 -->
    <div class="image-row">
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
    </div>
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
