# nexus-bot
Nexus Generasi Baru
README.md

```markdown
# NEXUS WHATSAPP BOT v1.0.0

<p align="center">
  <img src="https://i.ibb.co.com/0j7kZ0P/hutao.png" width="250" alt="NEXUS BOT"/>
</p>

<p align="center">
  <strong>WhatsApp Bot Multi Device dengan Pairing Code</strong>
</p>

<p align="center">
  <a href="#tentang">Tentang</a> •
  <a href="#fitur-lengkap">Fitur Lengkap</a> •
  <a href="#instalasi">Instalasi</a> •
  <a href="#konfigurasi">Konfigurasi</a> •
  <a href="#daftar-perintah">Daftar Perintah</a> •
  <a href="#struktur-proyek">Struktur Proyek</a> •
  <a href="#cara-berkontribusi">Cara Berkontribusi</a> •
  <a href="#lisensi">Lisensi</a> •
  <a href="#kontak">Kontak</a>
</p>

---

## TENTANG

NEXUS WHATSAPP BOT adalah bot WhatsApp modern yang berjalan di atas Node.js menggunakan library **@whiskeysockets/baileys** untuk koneksi Multi Device. Bot ini dirancang dengan sistem **Pairing Code** sehingga Anda tidak perlu lagi memindai QR Code untuk menghubungkan bot ke akun WhatsApp Anda.

Bot ini dibuat dengan tujuan untuk memudahkan pengelolaan grup WhatsApp, menyediakan hiburan melalui berbagai game interaktif, memungkinkan pembuatan APK secara otomatis, serta memiliki berbagai fitur utilitas seperti downloader media sosial, pelacak nomor telepon, dan lain sebagainya.

**Dibuat oleh:** Tuan Profesor Nanxchenker  
**Nomor Kontak:** +62 857-9605-4964  
**Versi:** 1.0.0  
**Lisensi:** MIT  

---

## FITUR LENGKAP

### Sistem Inti
- **Multi Device**: Mendukung koneksi tanpa perlu HP menyala terus (Linked Device).
- **Pairing Code**: Cukup masukkan kode 8 digit dari terminal ke WhatsApp Anda.
- **Auto Reconnect**: Bot akan otomatis tersambung kembali jika koneksi terputus.
- **Rate Limit**: Anti spam untuk mencegah penyalahgunaan.
- **Cooldown System**: Mencegah spam command pada fitur game.

### Menu Interaktif
- **Button Menu**: Menggunakan template button WhatsApp (jika didukung) atau tombol interaktif.
- **Multi Level Menu**: Menu utama, menu fun, menu owner, menu grup, menu builder, menu downloader, menu tools.
- **Thumbnail Kustom**: Setiap menu dilengkapi gambar thumbnail dari `assets/nexus_banner.jpg`.

### Fitur Owner (Khusus Pemilik Bot)
| Perintah | Deskripsi |
|----------|-----------|
| `.addowner 628xxx` | Menambahkan owner baru |
| `.delowner 628xxx` | Menghapus owner |
| `.listowner` | Menampilkan daftar owner |
| `.bc [teks]` | Broadcast pesan ke semua user |
| `.ban 628xxx` | Memblokir pengguna |
| `.unban 628xxx` | Membuka blokir pengguna |
| `.addprem 628xxx [hari]` | Menambahkan akses premium |
| `.delprem 628xxx` | Menghapus akses premium |
| `.listprem` | Menampilkan daftar premium |
| `.addsewa 628xxx [hari]` | Menambahkan masa sewa |
| `.delsewa 628xxx` | Menghapus masa sewa |
| `.listsewa` | Menampilkan daftar sewa |
| `.eval [kode]` | Mengeksekusi kode JavaScript |
| `.backup` | Backup database |

### Fitur Grup (Khusus Admin Grup)
| Perintah | Deskripsi |
|----------|-----------|
| `.kick @user` | Mengeluarkan member dari grup |
| `.add 628xxx` | Menambahkan member ke grup |
| `.tagall [pesan]` | Menandai semua member |
| `.hidetag [pesan]` | Menandai tanpa notifikasi |
| `.promote @user` | Menjadikan admin |
| `.demote @user` | Menurunkan admin |
| `.groupinfo` | Informasi lengkap grup |
| `.setname [nama]` | Mengubah nama grup |
| `.setdesc [deskripsi]` | Mengubah deskripsi grup |
| `.setpp` | Mengubah foto profil grup |
| `.antilink on/off` | Mengaktifkan/menonaktifkan anti link |
| `.welcome on/off` | Mengaktifkan/menonaktifkan pesan welcome |

### Fitur Builder (Pembuat APK)
| Perintah | Deskripsi |
|----------|-----------|
| `.build [url] [nama]` | Membuat APK WebView dari URL |
| `.buildhtml [file] [nama]` | Membuat APK dari file HTML |
| `.buildphoto [file] [nama]` | Membuat APK penampil foto |
| `.buildpdf [file] [nama]` | Membuat APK pembaca PDF |
| `.buildgame [nama]` | Membuat APK game sederhana |
| `.listapk` | Melihat daftar APK yang sudah dibuat |

### Fitur Fun & Game
| Perintah | Deskripsi |
|----------|-----------|
| `.tebakgambar` | Game tebak gambar |
| `.caklontong` | Game Cak Lontong (tebak teka-teki) |
| `.mathquiz` | Kuis matematika acak |
| `.slot [bet]` | Mesin slot (judi virtual) |
| `.dadu [bet] [tebakan]` | Game dadu |
| `.koin [kepala/ekor]` | Tebak koin |
| `.rps [batu/gunting/kertas]` | Batu Gunting Kertas |
| `.tod` | Truth or Dare |
| `.tebakbendera` | Tebak bendera negara |
| `.tebaklirik` | Tebak lirik lagu |
| `.tebakkata` | Tebak kata acak |
| `.susunkata` | Susun kata acak |
| `.kuisanime` | Kuis seputar anime |
| `.kuiskpop` | Kuis seputar KPOP |
| `.kuisfilm` | Kuis seputar film |
| `.kuismusik` | Kuis seputar musik |
| `.kuisgeografi` | Kuis geografi |
| `.kuissejarah` | Kuis sejarah |
| `.kuissains` | Kuis sains |
| `.kuisolahraga` | Kuis olahraga |
| `.casino [bet] [tebakan]` | Game casino |

### Fitur Downloader
| Perintah | Deskripsi |
|----------|-----------|
| `.ytmp4 [url]` | Download video YouTube |
| `.ytmp3 [url]` | Download audio YouTube |
| `.tt [url]` | Download video TikTok |
| `.ig [url]` | Download video Instagram |
| `.fb [url]` | Download video Facebook |
| `.x [url]` | Download video Twitter/X |

### Fitur Tools
| Perintah | Deskripsi |
|----------|-----------|
| `.nik [nomor]` | Parse NIK KTP |
| `.track [nomor]` | Lacak nomor telepon |
| `.ip [alamat]` | Lacak alamat IP |
| `.translate [kode] [teks]` | Terjemahkan teks |
| `.sticker` | Buat stiker dari gambar |
| `.toimg` | Ubah stiker ke gambar |
| `.qr [teks]` | Generate QR Code |

---

## INSTALASI

### Persyaratan Sistem
- **Node.js** versi 18.x atau lebih tinggi
- **npm** versi 9.x atau lebih tinggi
- Koneksi internet stabil
- **Termux** (untuk Android) atau **VPS/PC** (Linux/Windows)

### Langkah Instalasi di Termux (Android)

```bash
# Update Termux
pkg update -y && pkg upgrade -y

# Install Node.js dan npm
pkg install nodejs -y

# Clone repository
git clone https://github.com/nanxchenker/nexus-bot.git

# Masuk ke folder
cd nexus_bot

# Install dependensi
npm install

# Jalankan bot
npm start
```

Langkah Instalasi di VPS/PC (Linux)

```bash
# Update sistem
sudo apt update && sudo apt upgrade -y

# Install Node.js 18
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt install -y nodejs

# Clone repository
git clone https://github.com/nanxchenker/nexus-bot.git

# Masuk ke folder
cd nexus_bot

# Install dependensi
npm install

# Jalankan bot
npm start
```

Langkah Instalasi di Windows

```bash
# Download dan install Node.js dari https://nodejs.org

# Download project sebagai ZIP atau clone dengan Git
git clone https://github.com/nanxchenker/nexus-bot.git

# Masuk ke folder
cd nexus_bot

# Install dependensi
npm install

# Jalankan bot
npm start
```

Menghubungkan ke WhatsApp

1. Setelah bot dijalankan, akan muncul Pairing Code 8 digit di terminal.
2. Buka aplikasi WhatsApp di ponsel Anda.
3. Masuk ke Setelan (Settings) > Perangkat Tertaut (Linked Devices).
4. Ketuk Tautkan Perangkat (Link a Device).
5. Masukkan kode yang muncul di terminal.
6. Tunggu hingga muncul status "WhatsApp Connected!" di terminal.
7. Bot siap digunakan.

---

KONFIGURASI

File config.js adalah pusat pengaturan bot. Berikut penjelasan setiap bagian:

```javascript
const CONFIG = {
    bot: {
        name: 'NEXUS BOT',              // Nama bot yang ditampilkan
        version: '1.0.0',               // Versi bot
        ownerNumber: ['+6285796054964'], // Nomor owner (array, bisa lebih dari 1)
        ownerName: 'Tuan Profesor Nanxchenker', // Nama pemilik
        prefix: '.',                     // Awalan perintah (bisa diganti)
        pairingCode: true                // Aktifkan pairing code (true) atau QR (false)
    },
    limits: {
        free: 10,                        // Jumlah build gratis per hari
        premium: 100,                    // Jumlah build premium per hari
        owner: 9999                      // Jumlah build owner per hari
    },
    game: {
        rewards: {
            tebakGambar: 500,            // Hadiah poin tebak gambar
            cakLontong: 300,             // Hadiah poin cak lontong
            mathQuiz: 200,               // Hadiah poin math quiz
            // ... dan seterusnya
        }
    }
};
```

Penting: Jangan pernah membagikan file sessions/ kepada siapapun. Folder tersebut berisi kredensial WhatsApp Anda.

---

DAFTAR PERINTAH LENGKAP

Menu Utama

Perintah Deskripsi
.menu Menampilkan menu utama dengan tombol interaktif
.infobot Menampilkan informasi bot (versi, uptime, RAM)
.ping Mengecek kecepatan respon bot

Owner Commands

Perintah Deskripsi
.owner Menampilkan nama owner
.addowner 628xxx Menambah owner baru
.delowner 628xxx Menghapus owner
.listowner Daftar owner
.bc [teks] Broadcast pesan
.ban 628xxx Ban pengguna
.unban 628xxx Unban pengguna
.addprem 628xxx [hari] Tambah premium
.delprem 628xxx Hapus premium
.listprem Daftar premium
.addsewa 628xxx [hari] Tambah sewa
.delsewa 628xxx Hapus sewa
.listsewa Daftar sewa
.eval [kode] Eksekusi kode
.backup Backup database

Group Commands

Perintah Deskripsi
.kick @user Kick member
.add 628xxx Tambah member
.tagall [pesan] Tag semua
.hidetag [pesan] Tag tersembunyi
.promote @user Jadikan admin
.demote @user Turunkan admin
.groupinfo Info grup
.setname [nama] Ganti nama grup
.setdesc [desk] Ganti deskripsi
.antilink on/off Anti link
.welcome on/off Welcome message

Builder Commands

Perintah Deskripsi
.build [url] [nama] Build APK WebView
.buildhtml [file] [nama] Build APK HTML
.buildphoto [file] [nama] Build APK foto
.buildpdf [file] [nama] Build APK PDF
.buildgame [nama] Build APK game
.listapk Lihat APK

Fun Commands

Perintah Deskripsi
.tebakgambar Game tebak gambar
.caklontong Game cak lontong
.mathquiz Kuis matematika
.slot [bet] Mesin slot
.dadu [bet] [tebak] Game dadu
.koin [kepala/ekor] Tebak koin
.rps [batu/gunting/kertas] Batu Gunting Kertas
.tod Truth or Dare
.tebakbendera Tebak bendera
.tebaklirik Tebak lirik
.tebakkata Tebak kata
.susunkata Susun kata
.kuisanime Kuis anime
.kuiskpop Kuis KPOP
.kuisfilm Kuis film
.kuismusik Kuis musik
.kuisgeografi Kuis geografi
.kuissejarah Kuis sejarah
.kuissains Kuis sains
.kuisolahraga Kuis olahraga
.casino [bet] [tebak] Casino

Downloader Commands

Perintah Deskripsi
.ytmp4 [url] Download YT video
.ytmp3 [url] Download YT audio
.tt [url] Download TikTok
.ig [url] Download Instagram
.fb [url] Download Facebook
.x [url] Download Twitter/X

Tools Commands

Perintah Deskripsi
.nik [nomor] Parse NIK
.track [nomor] Lacak nomor
.ip [alamat] Lacak IP
.translate [kode] [teks] Terjemahkan
.sticker Buat stiker
.toimg Stiker ke gambar
.qr [teks] Generate QR

---

STRUKTUR PROYEK

```
nexus_bot/
├── README.md              # Dokumentasi lengkap proyek (file ini)
├── LICENSE                # Lisensi MIT
├── package.json           # Konfigurasi npm dan dependensi
├── config.js              # File konfigurasi utama
├── index.js               # Entry point bot
├── nexus.js               # File utama bot (semua fitur di sini)
├── assets/
│   └── nexus_banner.jpg   # Gambar banner untuk menu
├── database/
│   └── db.js              # Modul database (JSON file based)
├── lib/
│   ├── functions.js       # Fungsi utilitas
│   └── baileys.js         # Koneksi WhatsApp Baileys
└── commands/
    ├── menu.js            # Handler menu dan info bot
    ├── owner.js           # Handler perintah owner
    ├── group.js           # Handler perintah grup
    ├── fun.js             # Handler game dan hiburan
    └── builder.js         # Handler APK Builder
```

---

CARA BERKONTRIBUSI

Kami sangat terbuka untuk kontribusi dari siapa pun. Berikut langkah-langkah untuk berkontribusi:

1. Fork Repository

Klik tombol Fork di pojok kanan atas halaman GitHub.

2. Clone Repository Anda

```bash
git clone https://github.com/USERNAME_ANDA/nexus-bot.git
cd nexus_bot
```

3. Buat Branch Baru

```bash
git checkout -b fitur-anda
```

4. Lakukan Perubahan

· Tambahkan fitur baru di folder commands/ dengan membuat file baru.
· Update nexus.js untuk menambahkan case perintah baru.
· Update menu.js jika perlu menambahkan menu baru.
· Update config.js jika ada konfigurasi baru.
· Update README.md untuk mendokumentasikan fitur baru.

5. Commit dan Push

```bash
git add .
git commit -m "Menambahkan fitur X"
git push origin fitur-anda
```

6. Buat Pull Request

Buka repository asli dan klik New Pull Request.

Daftar Kontributor

Nama GitHub Kontribusi
Tuan Profesor Nanxchenker @nanxchenker Pembuat utama
[TULIS NAMA ANDA DI SINI] [TULIS GITHUB ANDA] [TULIS KONTRIBUSI ANDA]
[TULIS NAMA ANDA DI SINI] [TULIS GITHUB ANDA] [TULIS KONTRIBUSI ANDA]

---

LISENSI

MIT License

Copyright (c) 2024 Tuan Profesor Nanxchenker

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

KONTAK

· WhatsApp: +62 857-9605-4964
· Email: nexus@mangaverse.com
· GitHub: https://github.com/nanxchenker/nexus-bot

---

<p align="center">
  <strong>Dibuat dengan dedikasi oleh Tuan Profesor Nanxchenker</strong>
</p>

<p align="center">
  NEXUS BOT v1.0.0 — Awal dari segalanya
</p>
```
