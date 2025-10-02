<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ゆいきち公式サイト</title>
  <style>
    body {
      font-family: "Trebuchet MS", sans-serif;
      background: #fff; /* 通常(ライト)モード */
      color: #000;
      margin: 0;
      padding: 0;
      transition: background 0.5s, color 0.5s;
      scroll-behavior: smooth;
    }
    body.dark {
      background: #555; /* ダークモード */
      color: #fff;
    }
    header {
      background: #228B22;
      padding: 20px;
      border-bottom: 4px solid #006400;
      box-shadow: 0 4px 8px rgba(0,0,0,0.3);
      position: fixed;
      top: 0;
      width: 100%;
      z-index: 1000;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    header h1 {
      margin: 0;
      font-size: 1.5rem;
      color: #FFD700;
      text-shadow: 2px 2px #000;
    }
    #modeToggle {
      padding: 6px 12px;
      background: #444;
      color: white;
      border: none;
      border-radius: 6px;
      cursor: pointer;
    }
    /* ハンバーガー */
    .hamburger {
      font-size: 24px;
      cursor: pointer;
      background: none;
      border: none;
      color: #fff;
      margin-left: 10px;
    }
    /* サイドメニュー */
    .sideMenu {
      height: 100%;
      width: 0;
      position: fixed;
      top: 0;
      right: 0;
      background: #333;
      overflow-x: hidden;
      transition: 0.4s;
      padding-top: 60px;
      z-index: 2000;
    }
    .sideMenu a {
      padding: 12px 24px;
      text-decoration: none;
      color: #fff;
      display: block;
      transition: 0.3s;
    }
    .sideMenu a:hover {
      background: #575757;
    }
    .closeBtn {
      position: absolute;
      top: 10px;
      right: 20px;
      font-size: 28px;
      cursor: pointer;
      color: #fff;
    }
    main {
      margin-top: 100px;
      padding: 10px;
    }
    section {
      padding: 30px 10px;
      background: rgba(0,0,0,0.05);
      margin: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    }
    body.dark section {
      background: rgba(0,0,0,0.6);
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
    /* 投票円グラフ */
    #pollChart {
      max-width: 400px;
      margin: auto;
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
    <h1>ゆいきち公式サイト</h1>
    <div>
      <button id="modeToggle">モード切替</button>
      <button class="hamburger" onclick="openMenu()">☰</button>
    </div>
  </header>

  <!-- サイドメニュー -->
  <div id="sideMenu" class="sideMenu">
    <span class="closeBtn" onclick="closeMenu()">×</span>
    <a href="#recommend">おすすめ動画</a>
    <a href="#news">お知らせ</a>
    <a href="#series">シリーズ</a>
    <a href="#gallery">ギャラリー</a>
    <a href="#profile">プロフィール</a>
    <a href="#links">リンク</a>
    <a href="#vote">投票</a>
  </div>

  <main>
    <!-- おすすめ動画 -->
    <section id="recommend">
      <h2>おすすめ動画</h2>
      <iframe width="560" height="315"
              src="https://www.youtube.com/embed/hkhgFTBFkr4"
              title="YouTube video player"
              frameborder="0"
              allowfullscreen></iframe>
    </section>

    <!-- お知らせ -->
    <section id="news">
      <h2>お知らせ</h2>
      <ul style="list-style:none; padding:0;">
        <li>チャンネル登録者数2025年10月1日45人突破！</li>
        <li>ゆいきちLINEスタンプ販売中！ぜひチェック！</li>
        <li>ゆいクラ投稿予定！(2025年10月2日記入。)</li>
      </ul>
    </section>

    <!-- シリーズ -->
    <section id="series">
      <h2>シリーズ</h2>
      <iframe width="560" height="315"
              src="https://www.youtube.com/embed/videoseries?list=PLzhtEQbW0_4xaJ8LELjkFi-IcagEpzkT-"
              title="YouTube playlist"
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
        <a class="button" href="https://www.youtube.com/@ゆいきち-stoptuy" target="_blank">YouTubeチャンネル</a>
        <a class="button" href="https://www.starico.jp/detail/a3169966.html" target="_blank">ゆいきちスタンプ</a>
        <a class="button" href="https://yuikichi1212-sketch.github.io/yuikichinavi/" target="_blank">ゆいきちナビ</a>
      </p>
    </section>

    <!-- 投票 -->
    <section id="vote">
      <h2>好きな企画に投票！</h2>
      <form id="pollForm">
        <label><input type="radio" name="vote" value="10分建築">10分建築</label><br>
        <label><input type="radio" name="vote" value="ゆいクラ">ゆいクラ</label><br>
        <label><input type="radio" name="vote" value="ショート">ショート</label><br><br>
        <button type="submit">投票する</button>
      </form>
      <canvas id="pollChart"></canvas>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 ゆいきち公式サイト</p>
  </footer>

  <!-- ライトボックス -->
  <div id="lightbox">
    <img src="" alt="拡大画像">
  </div>

  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <script>
    // モード切替
    const body = document.body;
    const button = document.getElementById("modeToggle");
    button.addEventListener("click", () => {
      body.classList.toggle("dark");
    });

    // サイドメニュー開閉
    function openMenu() {
      document.getElementById("sideMenu").style.width = "250px";
    }
    function closeMenu() {
      document.getElementById("sideMenu").style.width = "0";
    }

    // ライトボックス
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
    const ctx = document.getElementById("pollChart").getContext("2d");
    const votes = { "10分建築": 0, "ゆいクラ": 0, "ショート": 0 };
    const pollChart = new Chart(ctx, {
      type: "pie",
      data: {
        labels: Object.keys(votes),
        datasets: [{
          data: Object.values(votes),
          backgroundColor: ["#FF6384", "#36A2EB", "#FFCE56"]
        }]
      }
    });
    document.getElementById("pollForm").addEventListener("submit", e => {
      e.preventDefault();
      const choice = document.querySelector("input[name='vote']:checked");
      if (choice) {
        votes[choice.value]++;
        pollChart.data.datasets[0].data = Object.values(votes);
        pollChart.update();
      }
    });
  </script>
</body>
</html>
