# DonghuaFilm Scraper - Node.js Donghua Anime Scraper

> **GitHub Repository Title**
>
> ```text
> DonghuaFilm Scraper - Node.js Donghua Anime Scraper
> ```
>
> **Repository Name**
>
> ```text
> donghuafilm-scraper
> ```
>
> **GitHub Repository Description**
>
> ```text
> Node.js scraper for DonghuaFilm. Get anime lists, search results, anime details, episodes, mirrors, download links, schedules, and A-Z lists in JSON format.
> ```

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-16%2B-339933?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js">
  <img src="https://img.shields.io/badge/Axios-HTTP%20Client-5A29E4?style=for-the-badge&logo=axios&logoColor=white" alt="Axios">
  <img src="https://img.shields.io/badge/Cheerio-HTML%20Parser-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="Cheerio">
  <img src="https://img.shields.io/badge/Creator-SCRIPETEREN-black?style=for-the-badge&logo=github" alt="Creator">
</p>

<p align="center">
  <b>Node.js scraper untuk DonghuaFilm.</b><br>
  Mengambil data homepage, anime terbaru, popular, ongoing, completed, movie, pencarian, detail anime, episode, server, download, jadwal, dan daftar A-Z dalam format JSON.
</p>

---

## ✨ Fitur

- Mengambil data homepage DonghuaFilm
- Mengambil slider atau featured donghua
- Mengambil daftar anime terbaru
- Mengambil daftar anime populer
- Mengambil daftar anime ongoing
- Mengambil daftar anime completed
- Mengambil daftar movie
- Mendukung pagination list anime
- Mencari anime atau donghua berdasarkan keyword
- Mengambil detail series/anime
- Mengambil poster, sinopsis, rating, status, genre, dan informasi tambahan
- Mengambil daftar episode dalam sebuah series
- Mengambil data halaman episode
- Mengambil server atau mirror video
- Decode Base64 pada value server apabila tersedia
- Mengambil iframe video
- Mengambil link download
- Mengambil URL episode sebelumnya dan berikutnya
- Auto detect URL menggunakan command `resolve`
- Mengambil jadwal atau halaman segera tayang
- Mengambil daftar donghua dari A sampai Z
- Menghasilkan output JSON untuk bot, API, website, atau aplikasi

---

## 🛠️ Teknologi

Project ini menggunakan:

- [Node.js](https://nodejs.org/)
- [Axios](https://axios-http.com/)
- [Cheerio](https://cheerio.js.org/)
- Built-in module `https`

---

## 📂 Struktur Project

```text
donghuafilm-scraper/
├── donghuafilm.js
├── package.json
├── package-lock.json
├── .gitignore
├── README.md
└── LICENSE
```

---

## ⚙️ Instalasi

Clone repository:

```bash
git clone [https://github.com/SCRIPETEREN/donghuafilm-scraper.git](https://github.com/SCRIPETEREN/donghuafilm-scraper.git)
```

Masuk ke folder project:

```bash
cd donghuafilm-scraper
```

Install semua dependency:

```bash
npm install
```

Jika belum memiliki file `package.json`, install dependency manual:

```bash
npm install axios cheerio
```

Jalankan scraper:

```bash
node donghuafilm.js
```

Command tanpa argument akan menjalankan command `home`.

---

## 📦 package.json

Gunakan file `package.json` berikut:

```json
{
  "name": "donghuafilm-scraper",
  "version": "1.0.0",
  "description": "Node.js scraper untuk mengambil data anime dan donghua dari DonghuaFilm.",
  "main": "donghuafilm.js",
  "scripts": {
    "start": "node donghuafilm.js",
    "home": "node donghuafilm.js home",
    "anime": "node donghuafilm.js anime",
    "latest": "node donghuafilm.js latest",
    "popular": "node donghuafilm.js popular",
    "ongoing": "node donghuafilm.js ongoing",
    "complete": "node donghuafilm.js complete",
    "movie": "node donghuafilm.js movie"
  },
  "keywords": [
    "donghua",
    "donghuafilm",
    "scraper",
    "anime",
    "nodejs",
    "axios",
    "cheerio",
    "indonesia"
  ],
  "author": "SCRIPETEREN",
  "license": "MIT",
  "dependencies": {
    "axios": "^1.7.9",
    "cheerio": "^1.0.0"
  }
}
```

Install dependency:

```bash
npm install
```

Jalankan melalui NPM:

```bash
npm start
```

Contoh command NPM lain:

```bash
npm run latest
```

```bash
npm run popular
```

```bash
npm run ongoing
```

---

## 🚀 Cara Penggunaan

Format dasar:

```bash
node donghuafilm.js <command> <input>
```

Contoh:

```bash
node donghuafilm.js search "swallowed star"
```

---

## 📋 Daftar Command

| Command | Keterangan | Contoh |
|---|---|---|
| `home` | Mengambil data halaman utama | `node donghuafilm.js home` |
| `anime` | Mengambil anime terbaru | `node donghuafilm.js anime` |
| `latest` | Alias dari anime terbaru | `node donghuafilm.js latest` |
| `popular` | Mengambil anime populer | `node donghuafilm.js popular` |
| `ongoing` | Mengambil anime ongoing | `node donghuafilm.js ongoing` |
| `complete` | Mengambil anime completed | `node donghuafilm.js complete` |
| `movie` | Mengambil daftar movie | `node donghuafilm.js movie` |
| `page <path>` | Mengambil halaman pagination | `node donghuafilm.js page /anime/page/2/` |
| `search <query>` | Mencari anime atau donghua | `node donghuafilm.js search "soul land"` |
| `detail <slug/url>` | Mengambil detail anime | `node donghuafilm.js detail /anime/swallowed-star/` |
| `episode <url>` | Mengambil data episode | `node donghuafilm.js episode /swallowed-star-episode-242-subtitle-indonesia/` |
| `resolve <url>` | Deteksi otomatis tipe URL | `node donghuafilm.js resolve https://donghuafilm.com/anime/swallowed-star/` |
| `jadwal` | Mengambil jadwal tayang | `node donghuafilm.js jadwal` |
| `schedule` | Alias dari command jadwal | `node donghuafilm.js schedule` |
| `az [huruf]` | Mengambil daftar A-Z | `node donghuafilm.js az A` |

---

## 🏠 Homepage

Untuk mengambil data homepage:

```bash
node donghuafilm.js home
```

Data yang dapat diperoleh:

- Slider atau donghua unggulan
- Judul donghua
- URL detail
- Slug
- Backdrop image
- Sinopsis singkat
- Section anime dari homepage
- Anime populer jika section tersebut tersedia

Contoh output:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": {
    "slider": [
      {
        "title": "Contoh Donghua",
        "url": "[https://donghuafilm.com/anime/contoh-donghua/](https://donghuafilm.com/anime/contoh-donghua/)",
        "slug": "anime/contoh-donghua",
        "backdrop": "[https://example.com/backdrop.jpg](https://example.com/backdrop.jpg)",
        "synopsis": "Sinopsis singkat donghua."
      }
    ],
    "popular": [],
    "sections": {}
  }
}
```

---

## 🆕 Anime Terbaru

Untuk mengambil daftar anime terbaru:

```bash
node donghuafilm.js anime
```

Atau:

```bash
node donghuafilm.js latest
```

Endpoint yang digunakan:

```text
/anime/?status=&type=&order=update
```

Contoh output:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": {
    "items": [
      {
        "title": "Swallowed Star Episode 242 Subtitle Indonesia",
        "series": "Swallowed Star",
        "episode": "Episode 242",
        "type": "ONA",
        "sub": "SUB",
        "url": "[https://donghuafilm.com/swallowed-star-episode-242-subtitle-indonesia/](https://donghuafilm.com/swallowed-star-episode-242-subtitle-indonesia/)",
        "slug": "swallowed-star-episode-242-subtitle-indonesia",
        "poster": "[https://example.com/poster.jpg](https://example.com/poster.jpg)",
        "content_id": "123"
      }
    ],
    "next": "[https://donghuafilm.com/anime/page/2/](https://donghuafilm.com/anime/page/2/)",
    "current_page": 1,
    "total_page": "100"
  }
}
```

---

## 🔥 Anime Populer

Untuk mengambil daftar anime populer:

```bash
node donghuafilm.js popular
```

Endpoint:

```text
/anime/?status=&type=&order=popular
```

---

## 🔄 Anime Ongoing

Untuk mengambil donghua yang masih tayang:

```bash
node donghuafilm.js ongoing
```

Endpoint:

```text
/anime/?status=ongoing&type=&order=update
```

---

## ✅ Anime Completed

Untuk mengambil donghua yang sudah selesai atau tamat:

```bash
node donghuafilm.js complete
```

Endpoint:

```text
/anime/?status=completed&type=&order=update
```

---

## 🎬 Movie

Untuk mengambil daftar movie:

```bash
node donghuafilm.js movie
```

Endpoint:

```text
/anime/?status=&type=movie&order=update
```

---

## 📄 Pagination

Untuk mengambil halaman tertentu dari daftar anime:

```bash
node donghuafilm.js page /anime/page/2/
```

Bisa juga menggunakan URL penuh:

```bash
node donghuafilm.js page [https://donghuafilm.com/anime/page/2/](https://donghuafilm.com/anime/page/2/)
```

Contoh output:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": {
    "items": [],
    "next": "[https://donghuafilm.com/anime/page/3/](https://donghuafilm.com/anime/page/3/)",
    "current_page": 2,
    "total_page": "100"
  }
}
```

---

## 🔎 Search

Format pencarian:

```bash
node donghuafilm.js search "<keyword>"
```

Contoh:

```bash
node donghuafilm.js search "swallowed star"
```

```bash
node donghuafilm.js search "battle through the heavens"
```

```bash
node donghuafilm.js search "soul land"
```

```bash
node donghuafilm.js search "renegade immortal"
```

Contoh output:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": {
    "query": "swallowed star",
    "heading": "Search Results for: swallowed star",
    "total": 10,
    "items": []
  }
}
```

---

## 📚 Detail Anime

Untuk mengambil detail sebuah anime atau series:

```bash
node donghuafilm.js detail /anime/swallowed-star/
```

Menggunakan URL penuh:

```bash
node donghuafilm.js detail [https://donghuafilm.com/anime/swallowed-star/](https://donghuafilm.com/anime/swallowed-star/)
```

Menggunakan slug episode:

```bash
node donghuafilm.js detail swallowed-star-episode-242-subtitle-indonesia
```

Data detail yang dapat diperoleh:

- Judul anime
- Slug anime
- URL detail
- Poster
- Sinopsis
- Rating
- Status
- Genre
- Informasi tambahan
- Jumlah episode
- Daftar episode

Contoh output:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": {
    "title": "Swallowed Star",
    "slug": "/anime/swallowed-star/",
    "url": "[https://donghuafilm.com/anime/swallowed-star/](https://donghuafilm.com/anime/swallowed-star/)",
    "poster": "[https://example.com/poster.jpg](https://example.com/poster.jpg)",
    "synopsis": "Sinopsis anime.",
    "rating": 8.5,
    "status": "Ongoing",
    "genres": [
      "Action",
      "Adventure",
      "Fantasy"
    ],
    "info": {
      "japanese": "Tunshi Xingkong",
      "type": "ONA",
      "status": "Ongoing"
    },
    "total_episodes": 242,
    "episodes": []
  }
}
```

---

## ▶️ Detail Episode

Untuk mengambil detail episode:

```bash
node donghuafilm.js episode /swallowed-star-episode-242-subtitle-indonesia/
```

Atau menggunakan URL penuh:

```bash
node donghuafilm.js episode [https://donghuafilm.com/swallowed-star-episode-242-subtitle-indonesia/](https://donghuafilm.com/swallowed-star-episode-242-subtitle-indonesia/)
```

Data yang dapat diperoleh:

- Judul episode
- Nama series
- URL episode
- Server atau mirror video
- Value server
- Hasil decode Base64 jika tersedia
- Iframe video
- Link download
- URL episode sebelumnya
- URL episode berikutnya

Contoh output:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": {
    "title": "Swallowed Star Episode 242 Subtitle Indonesia",
    "series": "Swallowed Star",
    "url": "[https://donghuafilm.com/swallowed-star-episode-242-subtitle-indonesia/](https://donghuafilm.com/swallowed-star-episode-242-subtitle-indonesia/)",
    "servers": [
      {
        "label": "Server 1",
        "value": "PG...",
        "decoded": "<iframe src="[https://example.com/embed](https://example.com/embed)"></iframe>"
      }
    ],
    "iframes": [
      "[https://example.com/embed](https://example.com/embed)"
    ],
    "downloads": [
      {
        "label": "Download 720p",
        "url": "[https://example.com/download](https://example.com/download)"
      }
    ],
    "prev": "[https://donghuafilm.com/episode-sebelumnya/](https://donghuafilm.com/episode-sebelumnya/)",
    "next": "[https://donghuafilm.com/episode-selanjutnya/](https://donghuafilm.com/episode-selanjutnya/)"
  }
}
```

---

## 🧠 Resolve URL Otomatis

Command `resolve` digunakan untuk mendeteksi tipe URL secara otomatis.

Untuk URL anime:

```bash
node donghuafilm.js resolve [https://donghuafilm.com/anime/swallowed-star/](https://donghuafilm.com/anime/swallowed-star/)
```

Untuk URL episode:

```bash
node donghuafilm.js resolve [https://donghuafilm.com/swallowed-star-episode-242-subtitle-indonesia/](https://donghuafilm.com/swallowed-star-episode-242-subtitle-indonesia/)
```

Untuk URL halaman list:

```bash
node donghuafilm.js resolve [https://donghuafilm.com/anime/page/2/](https://donghuafilm.com/anime/page/2/)
```

Tipe URL yang tersedia:

| Type | Keterangan |
|---|---|
| `anime` | Halaman detail series atau anime |
| `episode` | Halaman episode |
| `list` | Halaman daftar anime |

Contoh output:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": {
    "type": "anime",
    "data": {}
  }
}
```

---

## 📅 Jadwal Tayang

Untuk mengambil jadwal atau halaman segera tayang:

```bash
node donghuafilm.js jadwal
```

Atau:

```bash
node donghuafilm.js schedule
```

Halaman sumber:

```text
/segera-tayang/
```

Contoh output:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": [
    {
      "day": "Senin",
      "items": []
    }
  ]
}
```

---

## 🔤 Daftar Anime A-Z

Untuk mengambil semua daftar anime:

```bash
node donghuafilm.js az
```

Untuk mengambil berdasarkan huruf:

```bash
node donghuafilm.js az A
```

Contoh lain:

```bash
node donghuafilm.js az B
```

```bash
node donghuafilm.js az S
```

Untuk daftar angka:

```bash
node donghuafilm.js az 0-9
```

Endpoint:

```text
/az-list/
```

Untuk huruf tertentu:

```text
/az-list/?show=A
```

---

## 🧩 Penggunaan Sebagai Module

Tambahkan kode berikut di bagian paling bawah file `donghuafilm.js`:

```js
if (require.main === module) {
  main()
}

module.exports = {
  getHome,
  getList,
  search,
  getDetail,
  getEpisode,
  getSchedule,
  getAzList,
  resolve
}
```

Kemudian buat file `app.js`:

```js
const {
  search,
  getDetail,
  getEpisode
} = require("./donghuafilm")

async function main() {
  try {
    const searchResult = await search("swallowed star")

    console.log(JSON.stringify(searchResult, null, 2))

    const detail = await getDetail("/anime/swallowed-star/")

    console.log(JSON.stringify(detail, null, 2))
  } catch (error) {
    console.error(error.message)
  }
}

main()
```

Jalankan:

```bash
node app.js
```

---

## 📝 Mengubah Author Response

Pada source code, ubah bagian response sukses berikut:

```js
console.log(JSON.stringify({
  author: "xvlovers",
  status: true,
  data
}, null, 2))
```

Menjadi:

```js
console.log(JSON.stringify({
  author: "SCRIPETEREN",
  status: true,
  data
}, null, 2))
```

Ubah juga bagian response error:

```js
console.log(JSON.stringify({
  author: "SCRIPETEREN",
  status: false,
  message: error.message
}, null, 2))
```

---

## 🛡️ Error Handling

Script memakai `try...catch` untuk menangani error request, URL tidak ditemukan, command tidak tersedia, atau perubahan struktur website.

Contoh response error:

```json
{
  "author": "SCRIPETEREN",
  "status": false,
  "message": "404: /anime/contoh-anime/"
}
```

Contoh command tidak tersedia:

```json
{
  "author": "SCRIPETEREN",
  "status": false,
  "message": "Command tidak dikenal: test"
}
```

---

## 📄 .gitignore

Buat file `.gitignore`:

```gitignore
node_modules/
.env
npm-debug.log*
yarn-debug.log*
yarn-error.log*
.DS_Store
```

---

## ⚠️ Catatan Penting

- Struktur HTML DonghuaFilm dapat berubah kapan saja sehingga selector scraper mungkin perlu diperbarui.
- Jangan melakukan request dalam jumlah besar dalam waktu singkat.
- Gunakan cache, rate limit, delay, atau queue jika scraper digunakan untuk bot atau aplikasi publik.
- Data server, iframe, dan link download dapat berubah sesuai halaman website.
- Opsi `rejectUnauthorized: false` sebaiknya tidak digunakan pada lingkungan production kecuali memang diperlukan.
- Gunakan repository ini untuk pembelajaran web scraping, parsing HTML, riset, dan pengolahan metadata.
- Patuhi ketentuan layanan website sumber serta hukum dan hak cipta yang berlaku.

---

## 📜 License

Project ini menggunakan lisensi MIT.

Buat file `LICENSE`:

```text
MIT License

Copyright (c) 2026 SCRIPETEREN

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files, to deal in the Software
without restriction, including without limitation the rights to use, copy,
modify, merge, publish, distribute, sublicense, and/or sell copies of the
Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 👨‍💻 Creator

```text
SCRIPETEREN
```

```text
[https://github.com/SCRIPETEREN](https://github.com/SCRIPETEREN)
```

<p align="center">
  Made with ❤️ by <a href="https://github.com/SCRIPETEREN">SCRIPETEREN</a>
</p>