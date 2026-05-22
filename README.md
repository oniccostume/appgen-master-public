# 🎮 AppGen Master

<p align="center">
  <img src="https://raw.githubusercontent.com/oniccostume/appgen-master-public/main/favicon.svg" alt="AppGen Master Logo" width="96" height="96">
</p>

<p align="center">
  <strong>7 AI Divisions → 1 Master Prompt. Zero Backend. Free Forever.</strong>
</p>

<p align="center">
  <a href="https://oniccostume.github.io/appgen-master/">🔗 Live Demo</a>
  &nbsp;|&nbsp;
  <a href="#-fitur">✨ Features</a>
  &nbsp;|&nbsp;
  <a href="#-tech-stack">🧰 Tech Stack</a>
  &nbsp;|&nbsp;
  <a href="#-memulai">🚀 Getting Started</a>
</p>

---

## 📖 Tentang

AppGen Master adalah aplikasi web **zero-backend** yang menyimulasikan **7 divisi pengembang AI** — Product Manager, UI/UX Designer, Software Architect, Frontend Developer, Backend Developer, QA Engineer, dan DevOps Engineer. Setiap divisi menganalisis ide aplikasi Anda secara berurutan dan menghasilkan spesifikasi lengkap, yang kemudian digabung menjadi **Master Prompt** siap pakai untuk AI code generator seperti Cursor, Claude Code, OpenCode, dan 15+ alat lainnya. AppGen Master berjalan sepenuhnya di browser, tanpa server, tanpa login, dan sepenuhnya gratis. Semua data disimpan secara lokal di perangkat Anda.

> **Visi:** *"Alat AI harus bisa diakses siapa saja — gratis, tanpa backend, tanpa login."* — OC (Onic Costume)

## ✨ Fitur

AppGen Master hadir dengan berbagai fitur unggulan. **Tujuh divisi AI** (Product Manager, UI/UX Designer, Software Architect, Frontend Developer, Backend Developer, QA Engineer, DevOps Engineer) bekerja secara berurutan untuk menganalisis ide Anda. Jika ada divisi yang gagal, Anda bisa **mengulangnya (retry)** tanpa harus memulai dari awal. Setiap output divisi juga bisa **diedit** sebelum digabungkan. Hasil akhirnya adalah sebuah **Master Prompt** yang bisa diunduh sebagai file `.md` atau diekspor ke **18 alat AI** populer seperti Cursor, Windsurf, Claude Code, dan lainnya.

Untuk pengelolaan, Anda bisa **menyimpan, menghapus, mengganti nama, mengekspor, dan mengimpor proyek** — semuanya tersimpan di `localStorage` browser Anda. Ada juga **Prompt Library** untuk menyimpan template favorit. Tampilannya menggunakan **tema pixel retro** dengan NES.css, font `Press Start 2P`, dan ikon Pixelarticons. Aplikasi ini mendukung **dua bahasa** (Indonesia dan Inggris) dan bisa diinstal sebagai **PWA** di desktop, Android, dan iOS. Dari sisi keamanan, ada **Content Security Policy (CSP)**, **enkripsi API key AES-256-GCM**, sanitasi output dengan **DOMPurify**, dan rate limiting. Semua ini **gratis, tanpa server, tanpa login, tanpa biaya**.

## 🧰 Tech Stack

Aplikasi ini dibangun dengan **React 18** dan **Vite** sebagai build tool. Untuk styling, kami menggunakan **NES.css** (tema retro 8-bit) bersama **Tailwind CSS**. Font yang digunakan adalah **Press Start 2P** dari Google Fonts, dan ikon berasal dari **Pixelarticons** (486 ikon pixel pada grid 24x24). Dukungan multi-bahasa diimplementasikan dengan **react-i18next**, sementara animasi menggunakan CSS Keyframes murni. Fitur PWA didukung oleh **vite-plugin-pwa**. Untuk keamanan, kami mengandalkan **DOMPurify** dan **Web Crypto API (AES-GCM)**. Semua data disimpan secara client-side di `localStorage`.

## 🚀 Memulai

Untuk menjalankan proyek ini secara lokal, Anda memerlukan **Node.js v18+** dan **npm v9+**. Setelah meng-clone repositori (`git clone https://github.com/oniccostume/appgen-master.git`), masuk ke folder proyek (`cd appgen-master`) dan instal dependensi dengan perintah `npm install --legacy-peer-deps`. Jalankan server development dengan `npm run dev` dan buka `http://localhost:5173` di browser. Untuk membuat build production, jalankan `npm run build` — hasilnya akan ada di folder `dist/`, siap di-deploy ke Netlify, Vercel, atau GitHub Pages.

## 🔧 Konfigurasi Provider AI

AppGen Master mendukung 5 provider AI yang sepenuhnya gratis. **Groq** menyediakan model seperti Llama 3.3 70B dan GPT-OSS (cloud gratis). **Google AI Studio** menyediakan Gemini 2.5 Flash dan Gemma 4 (cloud gratis). **Mistral AI** menyediakan Mistral Small 3.2 dan Codestral (cloud gratis). **Ollama** dan **LM Studio** memungkinkan Anda menjalankan model secara lokal dan akan terdeteksi otomatis. Untuk development, Vite Proxy sudah dikonfigurasi untuk semua provider di `vite.config.js`, jadi tidak perlu pengaturan tambahan.

## 📤 Ekspor ke Alat AI

Master Prompt yang dihasilkan bisa diekspor langsung ke 18 alat AI dalam format file yang sesuai: **Cursor** (`.cursorrules`), **Windsurf** (`.windsurfrules`), **VS Code + Copilot** (`.github/copilot-instructions.md`), **Claude Code** (`CLAUDE.md`), **OpenCode** (`AGENTS.md`), **Codex CLI** (`.codex.md`), **Aider** (`aider.conf.md`), **Cline** (`.clinerules`), **Cody** (`.codyrules`), **Continue** (`.continue/rules.md`), **Lovable** (`lovable-context.md`), **Bolt.new** (`bolt-context.md`), **v0 (Vercel)** (`v0-context.md`), **Replit** (`.replit.md`), **Base44** (`base44-context.md`), **Devin** (`devin-context.md`), **Google Antigravity** (`gemini-context.md`), dan **GitHub Copilot** (`copilot-context.md`).

## 🔒 Keamanan

Keamanan adalah prioritas. Aplikasi ini menerapkan **Content Security Policy (CSP)** melalui meta tag. Setiap API key pengguna dienkripsi dengan **AES-256-GCM** menggunakan Web Crypto API sebelum disimpan. Output dari LLM disanitasi dengan **DOMPurify** untuk mencegah XSS. Ada juga **rate limiting** sederhana (cooldown 3 detik) untuk mencegah spam. Header keamanan tambahan seperti `X-Content-Type-Options` dan `Referrer-Policy` dikonfigurasi melalui file `_headers` dan `vercel.json`.

## 📄 Lisensi

MIT © 2026 OC (Onic Costume)

## 🙏 Kredit

Dibuat sepenuhnya oleh **OC (Onic Costume)** — seorang developer yang percaya bahwa alat AI harus bisa diakses siapa saja, gratis, tanpa backend, tanpa login.

---

<p align="center">
  <strong>🎮 AppGen Master — Dari Ide Liar Jadi Aplikasi Nyata dalam 7 Langkah!</strong>
</p>
