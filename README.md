<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ゆいきち公式サイト</title>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <style>
    body {
      font-family: "Trebuchet MS", sans-serif;
      background: #fff; /* 通常モード 白背景 */
      color: #000;
      text-align: center;
      margin: 0;
      padding: 0;
      transition: background 0.5s, color 0.5s;
    }
    body.dark {
      background: #555; /* ダークモード 灰色背景 */
      color: #fff;
    }
    body.black {
      background: #111; /* ブラックモード 黒背景 */
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
      background: rgba(255,255,255,0.9);
      margin: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.4);
    }
    body.dark section {
      background: rgba(0,0,0,0.6);
    }
    body.black section {
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
    .vote-options button {
      margin: 8px;
      padding: 10px 20px;
      font-size: 1rem;
      border-radius: 8px;
      border: none;
      cursor: pointer;
      background: #228B22;
      color: white;
      transition: 0.3s;
    }
    .vote-options button:hover {
      background: #2ecc71;
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
      <li>チャンネル登録者数2025年10月1日 45人突破！</li>
      <li>ゆいきちLINEスタンプ販売中！ぜひチェック！</li>
      <li>ゆいクラ投稿予定！（2025年10月2日記入）</li>
    </ul>
  </section>

  <!-- シリーズ動画 -->
  <section>
    <h2> シリーズ動画</h2>
    <iframe width="560" height="315"
            src="https://www.youtube.com/embed/videoseries?list=PLzhtEQbW0_4xaJ8LELjkFi-IcagEpzkT-"
            title="YouTube playlist"
            frameborder="0"
            allowfullscreen>
    </iframe>
    <p>ゆいきち 10分建築シリーズ</p>
  </section>

  <!-- 投票機能 -->
  <section>
    <h2> 好きな企画に投票！</h2>
    <div class="vote-options">
      <button onclick="vote('10分建築')">10分建築</button>
      <button onclick="vote('ゆいクラ')">ゆいクラ</button>
      <button onclick="vote('ショート')">ショート</button>
    </div>
    <canvas id="voteChart" width="400" height="400"></canvas>
    <p id="voteMessage"></p>
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
    <p>どうも今日も、ゆいきちです！<br>
       マイクラ実況を中心に動画投稿しています。<br>
       やっていること：サバイバル生活・建築<br>
       好きなこと：栄させるw</p>
  </section>

  <!-- リンク集 -->
  <section>
    <h2> リンク</h2>
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
    // モード切替（通常=白 → ダーク=灰色 → ブラック=黒）
    const modes = ["normal", "dark", "black"];
    let current = 0;
    const body = document.body;
    const button = document.getElementById("modeToggle");

    button.addEventListener("click", () => {
      body.classList.remove("dark", "black");
      current = (current + 1) % modes.length;
      if (modes[current] !== "normal") {
        body.classList.add(modes[current]);
      }
      button.textContent =
        modes[current] === "normal" ? "モード: 通常" :
        modes[current] === "dark" ? "モード: ダーク" :
        "モード: ブラック";
    });
    button.textContent = "モード: 通常";

    // ギャラリー拡大
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

    // 投票機能
    const ctx = document.getElementById('voteChart').getContext('2d');
    let votes = JSON.parse(localStorage.getItem("votes")) || {
      "10分建築": 0,
      "ゆいクラ": 0,
      "ショート": 0
    };
    let hasVoted = localStorage.getItem("hasVoted") === "true";

    const chart = new Chart(ctx, {
      type: 'pie',
      data: {
        labels: Object.keys(votes),
        datasets: [{
          data: Object.values(votes),
          backgroundColor: ["#FF6384", "#36A2EB", "#FFCE56"]
        }]
      }
    });

    function updateChart() {
      chart.data.datasets[0].data = Object.values(votes);
      chart.update();
    }

    function vote(option) {
      if (hasVoted) {
        document.getElementById("voteMessage").textContent = "すでに投票済みです！";
        return;
      }
      votes[option]++;
      hasVoted = true;
      localStorage.setItem("votes", JSON.stringify(votes));
      localStorage.setItem("hasVoted", "true");
      updateChart();
      document.getElementById("voteMessage").textContent = option + " に投票しました！";
    }

    updateChart();
  </script>
</body>
</html>
</!DOCTYPE html>
