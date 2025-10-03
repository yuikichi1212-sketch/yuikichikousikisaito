<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ゆいきち公式サイト</title>
  <style>
    body {
      font-family: "Trebuchet MS", sans-serif;
      background: #fff; /* ライト */
      color: #000;
      margin: 0;
      padding: 0;
      transition: background 0.5s, color 0.5s;
    }
    body.dark {
      background: #111; /* ダーク */
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
      font-size: 2rem;
      color: #FFD700;
      text-shadow: 2px 2px #000;
    }
    header p {
      margin: 5px 0 0;
    }

    /* ハンバーガーアイコン */
    #menuToggle {
      position: absolute;
      top: 20px;
      right: 60px;
      font-size: 1.8rem;
      color: white;
      background: none;
      border: none;
      cursor: pointer;
      z-index: 2000;
    }

    /* モード切替ボタン */
    #modeToggle {
      position: absolute;
      top: 20px;
      right: 20px;
      font-size: 1.4rem;
      color: white;
      background: none;
      border: none;
      cursor: pointer;
      z-index: 2000;
    }

    /* サイドメニュー */
    #sideMenu {
      position: fixed;
      top: 0;
      right: -250px;
      width: 250px;
      height: 100%;
      background: #333;
      color: white;
      box-shadow: -3px 0 5px rgba(0,0,0,0.5);
      transition: right 0.3s ease;
      z-index: 1500;
      padding-top: 60px;
    }
    #sideMenu.active {
      right: 0;
    }
    #sideMenu a {
      display: block;
      padding: 15px;
      color: white;
      text-decoration: none;
      border-bottom: 1px solid #444;
    }
    #sideMenu a:hover {
      background: #444;
    }

    section {
      padding: 30px 10px;
      background: rgba(0,0,0,0.05);
      margin: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    }
    body.dark section {
      background: rgba(0,0,0,0.8);
    }

    iframe {
      max-width: 90%;
      border-radius: 12px;
      border: 4px solid #333;
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

    footer {
      background: #111;
      color: #aaa;
      padding: 10px;
      margin-top: 20px;
      font-size: 0.9rem;
    }

    /* 投票エリア */
    #pollResult {
      max-width: 400px;
      margin: 0 auto;
    }
    canvas {
      margin-top: 15px;
    }

    /* レスポンシブ */
    @media (max-width: 600px) {
      header h1 {
        font-size: 1.5rem;
      }
      .gallery img {
        width: 120px;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>ゆいきち公式サイト</h1>
    <p>みんな久しぶりーーw</p>
    <button id="menuToggle">☰</button>
    <button id="modeToggle"></button>
  </header>

  <!-- サイドメニュー -->
  <nav id="sideMenu">
    <a href="#video">おすすめ動画</a>
    <a href="#news">お知らせ</a>
    <a href="#series">シリーズ</a>
    <a href="#gallery">ギャラリー</a>
    <a href="#profile">プロフィール</a>
    <a href="#links">リンク</a>
    <a href="#poll">投票</a>
  </nav>

  <!-- おすすめ動画 -->
  <section id="video">
    <h2>おすすめ動画</h2>
    <iframe width="560" height="315"
            src="https://www.youtube.com/embed/hkhgFTBFkr4"
            frameborder="0"
            allowfullscreen></iframe>
  </section>

  <!-- お知らせ -->
  <section id="news">
    <h2>お知らせ</h2>
    <ul style="list-style:none; padding:0;">
      <li>チャンネル登録者数2025年10月1日45人突破！</li>
      <li>ゆいきちLINEスタンプ販売中！ぜひサイトの一番下からチェック！</li>
      <li>ゆいクラ投稿予定！(2025年10月2日記入。)</li>
    </ul>
  </section>

  <!-- シリーズ -->
  <section id="series">
    <h2>シリーズ</h2>
    <iframe width="560" height="315"
            src="https://www.youtube.com/embed/videoseries?list=PLzhtEQbW0_4xaJ8LELjkFi-IcagEpzkT-"
            frameborder="0"
            allowfullscreen></iframe>
    <p>ゆいきち１０分建築</p>
  </section>

  <!-- ギャラリー -->
  <section id="gallery">
    <h2>ギャラリー</h2>
    <div class="gallery">
      <img src="https://i.imgur.com/pL2sRcl.png" alt="チャンネルアイコン">
      <img src="https://i.imgur.com/U8Ffcgd.png" alt="チャンネルバナー">
      <img src="https://i.imgur.com/owsD0LS.jpeg" alt="10分建築ビル">
      <img src="https://i.imgur.com/BdrazJy.png" alt="ゆいきちナビQRコード">
      <img src="https://i.imgur.com/lvbDh4f.png" alt="ゆいきちスタンプ商品">
    </div>
  </section>

  <!-- プロフィール -->
  <section id="profile">
    <h2>プロフィール</h2>
    <p>どうも今日も、ゆいきちです。<br>
       マイクラ実況を中心に動画投稿しています！<br>
       やっていること：サバイバル生活・建築<br>
       好きなこと：栄させるw</p>
  </section>

  <!-- リンク -->
  <section id="links">
    <h2>リンク</h2>
    <p>
      <a href="https://www.youtube.com/@ゆいきち-stoptuy" target="_blank">YouTubeチャンネル</a><br>
      <a href="https://www.starico.jp/detail/a3169966.html" target="_blank">ゆいきちスタンプ</a><br>
      <a href="https://yuikichi1212-sketch.github.io/yuikichinavi/" target="_blank">ゆいきちナビ</a>
    </p>
  </section>

  <!-- 投票 -->
  <section id="poll">
    <h2>好きな企画に投票！</h2>
    <form id="pollForm">
      <label><input type="radio" name="vote" value="10分建築"> 10分建築</label><br>
      <label><input type="radio" name="vote" value="ゆいクラ"> ゆいクラ</label><br>
      <label><input type="radio" name="vote" value="ショート"> ショート</label><br>
      <button type="submit">投票</button>
    </form>
    <div id="pollResult">
      <canvas id="pollChart"></canvas>
    </div>
  </section>

  <footer>
    <p>&copy; 2025 ゆいきち公式サイト</p>
  </footer>

  <!-- Chart.js -->
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <script>
    // メニュー開閉
    const menuToggle = document.getElementById("menuToggle");
    const sideMenu = document.getElementById("sideMenu");
    menuToggle.addEventListener("click", () => {
      sideMenu.classList.toggle("active");
    });

    // モード切替
    const modeToggle = document.getElementById("modeToggle");
    modeToggle.addEventListener("click", () => {
      document.body.classList.toggle("dark");
      if (document.body.classList.contains("dark")) {
        modeToggle.textContent = "☀️";
      } else {
        modeToggle.textContent = "🌙";
      }
    });

    // 投票
    const ctx = document.getElementById('pollChart').getContext('2d');
    let pollData = { "10分建築": 0, "ゆいクラ": 0, "ショート": 0 };
    const pollChart = new Chart(ctx, {
      type: 'pie',
      data: {
        labels: Object.keys(pollData),
        datasets: [{
          data: Object.values(pollData),
          backgroundColor: ["#4CAF50", "#FFD700", "#FF6347"]
        }]
      }
    });
    document.getElementById("pollForm").addEventListener("submit", e => {
      e.preventDefault();
      const choice = document.querySelector("input[name='vote']:checked");
      if (!choice) return alert("投票してください！");
      pollData[choice.value]++;
      pollChart.data.datasets[0].data = Object.values(pollData);
      pollChart.update();
    });
  </script>
</body>
</html>
