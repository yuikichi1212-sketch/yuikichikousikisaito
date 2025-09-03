import React from "react";
import { motion } from "framer-motion";
import { Mail, Phone, Youtube } from "lucide-react";
import { Button } from "@/components/ui/button";

// ゆいきち YouTube 公式サイト
// 動画IDを差し替えて使えます。

export default function YuiKichiYouTubeSite() {
  return (
    <div className="min-h-screen bg-gradient-to-b from-white to-slate-50 text-slate-800 antialiased">
      {/* Header */}
      <header className="max-w-6xl mx-auto p-6 flex items-center justify-between">
        <div className="flex items-center gap-3">
          <Youtube className="w-8 h-8 text-red-600" />
          <h1 className="text-xl font-bold">ゆいきち YouTube 公式サイト</h1>
        </div>
        <nav className="hidden md:flex gap-4 items-center">
          <a href="#videos" className="text-sm hover:underline">Videos</a>
          <a href="#about" className="text-sm hover:underline">About</a>
          <a href="#contact" className="text-sm hover:underline">Contact</a>
          <Button size="sm" asChild>
            <a href="https://www.youtube.com/" target="_blank">チャンネル登録</a>
          </Button>
        </nav>
      </header>

      {/* Hero */}
      <section className="max-w-6xl mx-auto px-6 py-12 grid md:grid-cols-2 gap-8 items-center">
        <motion.div
          initial={{ opacity: 0, x: -30 }}
          animate={{ opacity: 1, x: 0 }}
          transition={{ duration: 0.6 }}
        >
          <h2 className="text-3xl md:text-4xl font-extrabold leading-tight">
            ようこそ、ゆいきちチャンネルへ！
          </h2>
          <p className="mt-4 text-slate-600">
            日常のVlog、ゲーム実況、音楽、色々なコンテンツをお届けしています。
            最新動画やおすすめ動画はこちらからチェック！
          </p>
          <div className="mt-6">
            <Button asChild>
              <a href="https://www.youtube.com/" target="_blank">YouTubeで見る</a>
            </Button>
          </div>
        </motion.div>

        <motion.div
          initial={{ opacity: 0, scale: 0.98 }}
          animate={{ opacity: 1, scale: 1 }}
          transition={{ duration: 0.6 }}
          className="flex justify-center md:justify-end"
        >
          <div className="w-full max-w-md aspect-video bg-black rounded-2xl overflow-hidden shadow-lg">
            {/* 最新動画 - YouTube iframe */}
            <iframe
              className="w-full h-full"
              src="https://www.youtube.com/embed/dQw4w9WgXcQ"
              title="YouTube video"
              frameBorder="0"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
              allowFullScreen
            ></iframe>
          </div>
        </motion.div>
      </section>

      {/* Video List */}
      <section id="videos" className="max-w-6xl mx-auto px-6 py-12">
        <h3 className="text-2xl font-bold">おすすめ動画</h3>
        <p className="text-slate-500 mt-2">ピックアップした動画を紹介します。</p>

        <div className="mt-6 grid grid-cols-1 md:grid-cols-3 gap-6">
          {[
            "dQw4w9WgXcQ",
            "M7lc1UVf-VE",
            "ysz5S6PUM-U"
          ].map((id, i) => (
            <div key={i} className="bg-white rounded-2xl overflow-hidden shadow-md">
              <div className="aspect-video">
                <iframe
                  className="w-full h-full"
                  src={`https://www.youtube.com/embed/${id}`}
                  title={`video-${i}`}
                  frameBorder="0"
                  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                  allowFullScreen
                ></iframe>
              </div>
              <p className="p-3 text-sm text-slate-600">動画タイトル {i + 1}</p>
            </div>
          ))}
        </div>
      </section>

      {/* About */}
      <section id="about" className="max-w-6xl mx-auto px-6 py-12">
        <div className="bg-white rounded-2xl p-8 shadow-sm">
          <h3 className="text-2xl font-bold">About</h3>
          <p className="mt-4 text-slate-600 leading-relaxed">
            ゆいきちのYouTubeチャンネルでは、楽しい日常のVlogやゲーム実況、音楽活動など幅広く配信しています。
            ぜひチャンネル登録して、一緒に盛り上がりましょう！
          </p>
        </div>
      </section>

      {/* Contact */}
      <section id="contact" className="max-w-4xl mx-auto px-6 py-12">
        <div className="bg-white rounded-2xl p-8 shadow-sm">
          <h3 className="text-2xl font-bold">Contact</h3>
          <p className="text-slate-500 mt-2">お仕事依頼・コラボ相談はこちらから。</p>

          <form className="mt-6 grid gap-3">
            <div className="grid md:grid-cols-2 gap-3">
              <input className="p-3 rounded-lg border" placeholder="お名前" />
              <input className="p-3 rounded-lg border" placeholder="メールアドレス" />
            </div>
            <input className="p-3 rounded-lg border" placeholder="件名" />
            <textarea className="p-3 rounded-lg border h-32" placeholder="メッセージ" />
            <div className="flex items-center gap-3 mt-2">
              <Mail className="w-5 h-5" />
              <span className="text-sm text-slate-500">返信には数日いただく場合があります。</span>
            </div>
            <div className="mt-4">
              <Button>送信</Button>
            </div>
          </form>

          <div className="mt-6 flex flex-col md:flex-row gap-4 items-start md:items-center">
            <div className="flex items-center gap-3">
              <Phone className="w-5 h-5" />
              <div>
                <div className="text-sm font-medium">公式お問い合わせ</div>
                <div className="text-xs text-slate-500">support@example.com</div>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="mt-12 border-t">
        <div className="max-w-6xl mx-auto px-6 py-8 flex flex-col md:flex-row justify-between items-center gap-4">
          <div className="text-sm text-slate-500">© {new Date().getFullYear()} ゆいきち YouTube Official</div>
          <div className="flex gap-3 text-sm">
            <a href="#" className="hover:underline">利用規約</a>
            <a href="#" className="hover:underline">プライバシー</a>
          </div>
        </div>
      </footer>
    </div>
  );
}
