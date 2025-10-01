<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ゆいきち公式サイト</title>
  <style>
    body {
      font-family: "Trebuchet MS", sans-serif;
      background: url('https://i.imgur.com/O7KXy1K.png') repeat;
      color: #fff;
      text-align: center;
      margin: 0;
      padding: 0;
      transition: background 0.5s, color 0.5s;
    }
    body.dark {
      background: url('https://i.imgur.com/WwBdT8t.png') repeat; /* 夜空背景 */
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
    #darkToggle {
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
  </style>
</head>
<body>
  <header>
    <h1>🎮 ゆいきち公式サイト 🎮</h1>
    <p>ようこそ！マイクラ実況ゆいきちワールドへ！</p>
    <button id="darkToggle">🌙 ダークモード</button>
  </header>

  <!-- 最新動画 -->
  <section>
    <h2>🎥 最新動画</h2>
    <iframe width="560" height="315"
            src="https://www.youtube.com/embed/hkhgFTBFkr4"
            title="YouTube video player"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
            allowfullscreen>
    </iframe>
  </section>

  <!-- お知らせ -->
  <section>
    <h2>🔔 お知らせ</h2>
    <ul style="list-style:none; padding:0;">
      <li>📅 2025-10-01 新作動画を公開しました！</li>
      <li>🔥 スタンプ販売中！ぜひチェックしてね</li>
      <li>⚒️ サイトにマイクラ風デザイン追加！</li>
    </ul>
  </section>

  <!-- シリーズ動画 -->
  <section>
    <h2>📺 人気シリーズ</h2>
    <iframe width="560" height="315"
            src="https://www.youtube.com/embed/videoseries?list=PLxxxxxxx"
            title="YouTube playlist"
            frameborder="0"
            allowfullscreen>
    </iframe>
    <p>（プレイリストIDに差し替えてください）</p>
  </section>

  <!-- ギャラリー -->
  <section>
    <h2>📷 ギャラリー</h2>
    <div class="gallery">
      <img src="https://i.imgur.com/5WqYtC7.png" alt="マイクラ建築1">
      <img src="https://i.imgur.com/sZX2K5U.png" alt="マイクラ建築2">
      <img src="https://i.imgur.com/JkE8zWf.png" alt="マイクラ建築3">
    </div>
  </section>

  <!-- プロフィール -->
  <section>
    <h2>🎮 プロフィール</h2>
    <p>こんにちは！ゆいきちです。<br>
       マイクラ実況を中心に動画投稿しています！<br>
       得意なこと：サバイバル生活・建築<br>
       好きなこと：冒険・仲間と遊ぶこと</p>
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
    <p>&copy; 2025 ゆいきち | マイクラ実況公式サイト</p>
  </footer>

  <script>
    document.getElementById("darkToggle").addEventListener("click", function() {
      document.body.classList.toggle("dark");
    });
  </script>
</body>
</html>
