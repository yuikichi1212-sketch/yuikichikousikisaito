<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ゆいきち公式サイト</title>
  <style>
    body {
      font-family: "Trebuchet MS", sans-serif;
      background: #555; /* 通常モード 灰色背景 */
      color: #fff;
      text-align: center;
      margin: 0;
      padding: 0;
      transition: background 0.5s, color 0.5s;
    }
    body.light {
      background: #fff; /* ライトモード 白背景 */
      color: #000;
    }
    body.dark {
      background: #111; /* ダークモード 黒背景 */
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
      background: rgba(255,255,255,0.8);
    }
    body.dark section {
      background: rgba(0,0,0,0.8);
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
  </style>
</head>
<body>
  <header>
    <h1> ゆいきち公式サイト </h1>
    <p>ようこそ！マイクラ実況ゆいきちワールドへ！</p>
    <button id="modeToggle">モード切替</button>
  </header>

  <!-- おすすめ動画 -->
  <section>
    <h2> おすすめ動画</h2>
    <iframe width="560" height="315"
            src="https://www.youtube.com/embed/hkhgFTBFkr4"
            title="YouTube video player"
            frameborder="0"
            allowfullscreen>
    </iframe>
  </section>

  <!-- お知らせ -->
  <section>
    <h2> お知らせ</h2>
    <ul style="list-style:none; padding:0;">
      <li>チャンネル登録者数2025年10月1日45人突破！</li>
      <li> ゆいきちLINEスタンプ販売中！ぜひサイトの一番下からチェック！</li>
      <li>ゆいクラ投稿予定！(2025年10月2日記入。)</li>
    </ul>
  </section>

  <!-- シリーズ動画 -->
  <section>
    <h2> シリーズ</h2>
    <iframe width="560" height="315"
            src="https://www.youtube.com/embed/videoseries?list=PLzhtEQbW0_4xaJ8LELjkFi-IcagEpzkT-"
            title="YouTube playlist"
            frameborder="0"
            allowfullscreen>
    </iframe>
    <p>ゆいきち１０分建築</p>
  </section>

  <!-- ギャラリー -->
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

  <!-- プロフィール -->
  <section>
    <h2> プロフィール</h2>
    <p>どうも今日も、ゆいきちです。<br>
       マイクラ実況を中心に動画投稿しています！<br>
       やっていること：サバイバル生活・建築<br>
       好きなこと：栄させるw</p>
  </section>

  <!-- リンク集 -->
  <section>
    <h2>🔗 リンク</h2>
    <p>
      <a class="button" href="https://www.youtube.com/@ゆいきち-j4c" target="_blank">YouTubeチャンネル</a>
      <a class="button" href="https://www.starico.jp/detail/a3169966.html" target="_blank">ゆいきちスタンプ</a>
      <a class="button" href="https://yuikichi1212-sketch.github.io/yuikichinavi/" target="_blank">ゆいきちナビ</a>
    </p>
  </section>

  <footer>
    <p>&copy; 2025 ゆいきち公式サイト</p>
  </footer>

  <!-- ライトボックス -->
  <div id="lightbox">
    <img src="" alt="拡大画像">
  </div>

  <script>
    // モード切替（通常→ライト→ダーク→通常…）
    const modes = ["normal", "light", "dark"];
    let current = 0;
    const body = document.body;
    const button = document.getElementById("modeToggle");

    button.addEventListener("click", () => {
      // 現在のクラスを消す
      body.classList.remove("light", "dark");
      // 次のモードへ
      current = (current + 1) % modes.length;
      if (modes[current] !== "normal") {
        body.classList.add(modes[current]);
      }
      // ボタンの表示を変更
      button.textContent = 
        modes[current] === "normal" ? "モード: 通常" :
        modes[current] === "light" ? "モード: ライト" :
        "モード: ダーク";
    });
    button.textContent = "モード: 通常";

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
