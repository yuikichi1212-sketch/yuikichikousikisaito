<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ゆいきち公式サイト</title>
  <style>
    body {
      font-family: "Trebuchet MS", sans-serif;
      margin: 0;
      padding: 0;
      background: #fff; /* 通常モード = ライト */
      color: #000;
      transition: background 0.5s, color 0.5s;
      scroll-behavior: smooth;
    }
    body.dark {
      background: #111; /* ダークモード */
      color: #ddd;
    }

    header {
      background: #228B22;
      padding: 20px;
      border-bottom: 4px solid #006400;
      box-shadow: 0 4px 8px rgba(0,0,0,0.3);
      position: sticky;
      top: 0;
      z-index: 1000;
    }
    header h1 {
      margin: 0;
      font-size: 2rem;
      color: #FFD700;
      text-shadow: 2px 2px #000;
    }
    #modeToggle {
      position: absolute;
      top: 15px;
      right: 60px;
      padding: 6px 12px;
      background: #444;
      color: white;
      border: none;
      border-radius: 6px;
      cursor: pointer;
    }

    /* ハンバーガーメニュー */
    #menuToggle {
      position: absolute;
      top: 15px;
      right: 15px;
      font-size: 28px;
      background: none;
      border: none;
      color: white;
      cursor: pointer;
      z-index: 1001;
    }

    /* サイドメニュー */
    #sideMenu {
      position: fixed;
      top: 0;
      right: -250px;
      width: 250px;
      height: 100%;
      background: #333;
      color: #fff;
      padding: 20px;
      box-shadow: -4px 0 8px rgba(0,0,0,0.5);
      transition: right 0.3s;
      z-index: 1000;
    }
    #sideMenu.active {
      right: 0;
    }
    #sideMenu a {
      display: block;
      padding: 10px;
      color: #fff;
      text-decoration: none;
      border-bottom: 1px solid #555;
    }
    #sideMenu a:hover {
      background: #444;
    }

    section {
      padding: 40px 20px;
      margin: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.4);
      background: rgba(255,255,255,0.8);
    }
    body.dark section {
      background: rgba(0,0,0,0.7);
    }

    iframe {
      max-width: 90%;
      border-radius: 12px;
      border: 3px solid #333;
    }

    .gallery img {
      width: 180px;
      margin: 8px;
      border-radius: 8px;
      border: 3px solid #444;
      cursor: pointer;
    }
    .gallery img:hover {
      transform: scale(1.1);
    }

    footer {
      background: #111;
      color: #aaa;
      padding: 15px;
      text-align: center;
      font-size: 0.9rem;
    }

    /* 投票用円グラフ */
    canvas {
      max-width: 300px;
      margin: 20px auto;
      display: block;
    }

    @media(min-width: 768px) {
      #sideMenu {
        position: static;
        width: auto;
        height: auto;
        background: none;
        box-shadow: none;
        display: flex;
        gap: 15px;
      }
      #sideMenu a {
        border: none;
        color: #fff;
      }
      #menuToggle {
        display: none;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>ゆいきち公式サイト</h1>
    <button id="modeToggle">モード切替</button>
    <button id="menuToggle">≡</button>
    <nav id="sideMenu">
      <a href="#video">おすすめ動画</a>
      <a href="#news">お知らせ</a>
      <a href="#series">シリーズ</a>
      <a href="#gallery">ギャラリー</a>
      <a href="#profile">プロフィール</a>
      <a href="#links">リンク</a>
      <a href="#vote">投票</a>
    </nav>
  </header>

  <!-- おすすめ動画 -->
  <section id="video">
    <h2>おすすめ動画</h2>
    <iframe width="560" height="315"
      src="https://www.youtube.com/embed/hkhgFTBFkr4"
      frameborder="0" allowfullscreen></iframe>
  </section>

  <!-- お知らせ -->
  <section id="news">
    <h2>お知らせ</h2>
    <ul style="list-style:none;padding:0;">
      <li>チャンネル登録者数45人突破！</li>
      <li>ゆいきちLINEスタンプ販売中！</li>
      <li>ゆいクラ投稿予定！</li>
    </ul>
  </section>

  <!-- シリーズ -->
  <section id="series">
    <h2>シリーズ</h2>
    <iframe width="560" height="315"
      src="https://www.youtube.com/embed/videoseries?list=PLzhtEQbW0_4xaJ8LELjkFi-IcagEpzkT-"
      frameborder="0" allowfullscreen></iframe>
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
    マイクラ実況を中心に活動！<br>
    サバイバル生活・建築が好き！</p>
  </section>

  <!-- リンク -->
  <section id="links">
    <h2>リンク</h2>
    <p>
      <a href="https://www.youtube.com/@ゆいきち-j4c" target="_blank">YouTubeチャンネル</a> |
      <a href="https://www.starico.jp/detail/a3169966.html" target="_blank">ゆいきちスタンプ</a> |
      <a href="https://yuikichi1212-sketch.github.io/yuikichinavi/" target="_blank">ゆいきちナビ</a>
    </p>
  </section>

  <!-- 投票 -->
  <section id="vote">
    <h2>好きな企画投票</h2>
    <button onclick="vote('建築')">10分建築</button>
    <button onclick="vote('ゆいクラ')">ゆいクラ</button>
    <button onclick="vote('ショート')">ショート</button>
    <canvas id="chart"></canvas>
  </section>

  <footer>
    <p>&copy; 2025 ゆいきち公式サイト</p>
  </footer>

  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <script>
    // ダーク/ライト切替
    const modeBtn = document.getElementById("modeToggle");
    modeBtn.onclick = () => document.body.classList.toggle("dark");

    // ハンバーガーメニュー
    const menuBtn = document.getElementById("menuToggle");
    const sideMenu = document.getElementById("sideMenu");
    menuBtn.onclick = () => sideMenu.classList.toggle("active");

    // 投票機能
    const ctx = document.getElementById("chart").getContext("2d");
    let votes = {建築:0, ゆいクラ:0, ショート:0};
    let chart = new Chart(ctx, {
      type: "pie",
      data: {
        labels: Object.keys(votes),
        datasets: [{data: Object.values(votes), backgroundColor:["#ff6384","#36a2eb","#ffce56"]}]
      }
    });
    function vote(option) {
      votes[option]++;
      chart.data.datasets[0].data = Object.values(votes);
      chart.update();
    }
  </script>
</body>
</html>
