<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ゆいきち公式サイト</title>
  <style>
    body {
      font-family: "Trebuchet MS", sans-serif;
      text-align: center;
      margin: 0;
      padding: 0;
      transition: background 0.5s, color 0.5s;
    }

    /* 通常モード（灰色） */
    body.normal {
      background: #555;
      color: #fff;
    }

    /* ライトモード（白） */
    body.light {
      background: #fff;
      color: #000;
    }

    /* ダークモード（黒） */
    body.dark {
      background: #111;
      color: #ddd;
    }

    header {
      background: #228B22;
      padding: 20px;
      border-bottom: 4px solid #006400;
      box-shadow: 0 4px 8px rgba(0,0,0,0.3);
      position: relative;
    }
    header h1 {
      margin: 0;
      font-size: 2.5rem;
      color: #FFD700;
      text-shadow: 2px 2px #000;
    }
    #modeToggle {
      position: absolute;
      top: 15px;
      right: 15px;
      padding: 6px 12px;
      background: #444;
      color: white;
      border: none;
      border-radius: 6px;
      cursor: pointer;
    }

    section {
      padding: 30px 10px;
      background: rgba(0,0,0,0.6);
      margin: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.4);
    }
    body.light section {
      background: rgba(0,0,0,0.05);
    }
    body.normal section {
      background: rgba(0,0,0,0.6);
    }
    body.dark section {
      background: rgba(255,255,255,0.05);
    }

    iframe {
      max-width: 90%;
      border-radius: 12px;
      border: 4px solid #333;
      background: #000;
    }
    a.button {
      display: inline-block;
      margin: 10px;
      padding: 12px 24px;
      background: #8B4513;
      color: #fff;
      text-decoration: none;
      border-radius: 6px;
      border: 3px solid #5A2D0C;
      font-weight: bold;
      box-shadow: 2px 2px 0 #000;
      transition: 0.2s;
    }
    a.button:hover {
      background: #A0522D;
      transform: translateY(-2px);
    }

    .gallery img {
      width: 200px;
      margin: 10px;
      border-radius: 8px;
      border: 3px solid #444;
      transition: transform 0.2s;
      cursor: pointer;
    }
    .gallery img:hover {
      transform: scale(1.1);
    }

    /* ライトボックス */
    #lightbox {
      display: none;
      position: fixed;
      z-index: 9999;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: rgba(0,0,0,0.8);
      justify-content: center;
      align-items: center;
    }
    #lightbox img {
      max-width: 90%;
      max-height: 90%;
      border: 4px solid #fff;
      border-radius: 12px;
    }
    footer {
      background: #111;
      color: #aaa;
      padding: 10px;
      margin-top: 20px;
      font-size: 0.9rem;
    }
    body.light footer {
      background: #eee;
      color: #444;
    }
  </style>
</head>
<body class="normal">
  <header>
    <h1> ゆいきち公式サイト </h1>
    <p>ようこそ！マイクラ実況ゆいきちワールドへ！</p>
    <button id="modeToggle">モード切替</button>
  </header>

  <section>
    <h2>おすすめ動画</h2>
    <iframe width="560" height="315"
            src="https://www.youtube.com/embed/hkhgFTBFkr4"
            title="YouTube video player"
            frameborder="0"
            allowfullscreen>
    </iframe>
  </section>

  <section>
    <h2> ギャラリー</h2>
    <div class="gallery">
      <img src="https://i.imgur.com/pL2sRcl.png" alt="チャンネルアイコン">
      <img src="https://i.imgur.com/U8Ffcgd.png" alt="チャンネルバナー">
      <img src="https://i.imgur.com/owsD0LS.jpeg" alt="10分建築ビル">
      <img src="https://i.imgur.com/BdrazJy.png" alt="ゆいきちナビQRコード">
      <img src="https://i.imgur.com/lvbDh4f.png" alt="ゆいきちスタンプ商品">
    </div>
  </section>

  <footer>
    <p>&copy; 2025 ゆいきち公式サイト</p>
  </footer>

  <!-- ライトボックス -->
  <div id="lightbox">
    <img src="" alt="拡大画像">
  </div>

  <script>
    // 3モード切替
    const modes = ["normal", "light", "dark"];
    let currentMode = 0;
    document.getElementById("modeToggle").addEventListener("click", () => {
      document.body.classList.remove(modes[currentMode]);
      currentMode = (currentMode + 1) % modes.length;
      document.body.classList.add(modes[currentMode]);
    });

    // ギャラリー拡大表示
    const lightbox = document.getElementById("lightbox");
    const lightboxImg = lightbox.querySelector("img");
    document.querySelectorAll(".gallery img").forEach(img => {
      img.addEventListener("click", () => {
        lightbox.style.display = "flex";
        lightboxImg.src = img.src;
      });
    });
    lightbox.addEventListener("click", () => {
      lightbox.style.display = "none";
    });
  </script>
</body>
</html>
