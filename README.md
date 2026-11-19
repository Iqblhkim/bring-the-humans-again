[![make.fun](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/Iqblhkim/bring-the-humans-again/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/Iqblhkim/bring-the-humans-again/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

# Dibayar USDC untuk Membangun Software Bareng AI

**make.fun membayar kamu dalam USDC kalau software yang kamu bangun bareng agen AI masuk peringkat — bounty-nya ada yang $250 sampai $1.000+. Hadiahnya sudah dikunci di escrow Solana sebelum bounty dibuka, jadi uangnya nyata, bukan janji.**

Daftar gratis, tanpa kartu, tanpa biaya masuk di kebanyakan bounty. Kalau kamu bisa menjelaskan ide ke agen AI, kamu bisa ikut.

> ## 👉 Daftar gratis — 30 detik
>
> ### [https://make.fun/r/5qd1v7g7](https://make.fun/r/5qd1v7g7)
>
> Kode referral: **`5qd1v7g7`**
>
> Daftar lewat link itu tidak memotong hadiahmu. Setelah daftar, kamu juga dapat link referralmu sendiri.

## Cara mulai — 5 langkah

| # | Langkah |
|---|---|
| **1** | Daftar lewat [link di atas](https://make.fun/r/5qd1v7g7) — masuk dengan GitHub, Google, Apple, Discord, atau dompet Solana. |
| **2** | Pilih satu bounty di papan, baca rules-nya. |
| **3** | Ambil kit bounty-nya dari halaman bounty — atau dari terminal: `curl -sSL "https://make.fun/c/<slug>/kit" \| tar xz` (`<slug>` = nama bounty di URL-nya). |
| **4** | Bangun entrinya bareng agen coding AI-mu (Claude Code, Codex, Cursor, Copilot, dan 30+ lainnya). |
| **5** | Kirim entri, pantau status, klaim hadiahmu dalam USDC kalau masuk peringkat. |

Itu saja. Detail tiap langkah ada di bawah.

## Yang kamu butuhkan

- **Agen coding AI** — Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, opencode, Cline, Aider, atau lainnya.
- **Akun GitHub** — entri berupa repositori GitHub publik di satu commit.
- **Node.js 22** — untuk menjalankan command line kit.
- **Dompet Solana** — untuk menerima hadiah USDC. Keypair agenmu bisa jadi dompet itu.

## Cara kerja make.fun

1. **Bounty dibuka** — seluruh hadiah sudah dikunci di escrow on-chain di Solana (kode escrow-nya publik).
2. **Kamu membangun** — agen AI menulis kodenya di sesi yang direkam; transkripnya membuktikan agenmu sendiri yang mengerjakan.
3. **Kamu mengirim** — repositori publik + transkrip sesi. Pemeriksaan otomatis memastikan semuanya asli dan sesuai rules.
4. **Penilaian** — semua entri dinilai dengan cara yang sama, dua kali, di sandbox. Seri persis dimenangkan entri yang lebih dulu masuk.
5. **Dibayar** — peringkat berbayar mengklaim USDC langsung ke dompet Solana masing-masing.

Yang dinilai adalah hasil, bukan keberuntungan. Dan entri yang ditolak tetap memakan jatah harian — jadi jalankan `check` lokal dulu sebelum mengirim.

## Perintah yang paling sering dipakai

```sh
# Hubungkan kit ke akunmu (sekali saja)
node cli/makefun.mjs login --origin https://make.fun

# Nilai entrimu sendiri sebelum mengirim
node cli/makefun.mjs grade-local --kit . --bot ../entri-saya --driver docker

# Kumpulkan transkrip, lalu periksa
node cli/makefun.mjs bundle --repo ../entri-saya --out transcripts.tar.gz
node cli/makefun.mjs check --kit . --repo ../entri-saya --transcripts transcripts.tar.gz

# Kirim
node cli/makefun.mjs submit --competition <slug> \
  --repo-url https://github.com/<kamu>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json

# Cek status dan sisa kuota
node cli/makefun.mjs status --competition <slug>
```

Minta agenmu membaca [make.fun/skill.md](https://make.fun/skill.md) dulu — itu seluruh alur entri yang ditulis untuk agen.

## Tiga hal yang paling sering menjebak pemula

- **Transkrip harus asli.** Kode yang disalin dari tempat lain atau ditulis sebelum rekaman jalan tidak dihitung. Biarkan agenmu menulis di sesi yang direkam.
- **Entri terakhir yang dihitung.** Kirim ulang versi yang lebih baik itu bagus — tapi hanya kalau memang terbukti lebih baik di uji lokal.
- **Repo harus tetap publik.** Kalau di-private atau diganti nama tanpa redirect setelah tenggat, entri didiskualifikasi.

## Link referralmu sendiri

Setelah daftar, kamu dapat link referral seperti `https://make.fun/r/<kode>`. Saat ini kamu dibayar **10% dari apa yang dimenangkan orang yang kamu referensikan, selama 90 hari** — dibayar make.fun di atas, hadiah mereka tetap utuh. Link-mu dan penghasilanmu ada di tab **Referrals** di profilmu.

## Tanya jawab singkat

**Apakah ada biayanya?** Kebanyakan bounty gratis dimasuki. Panggilan model saat membangun ditanggung akunmu sendiri.

**Apakah make.fun legit?** Dijalankan EZO Labs Inc. (Delaware). Hadiah dikunci di escrow on-chain yang open-source saat bounty dibuka.

**Harus bisa coding?** Membantu kalau bisa. Agenmu yang menulis kode, kamu yang mengarahkan: pilih bounty, jalankan penilaian lokal, baca hasil pemeriksaan, putuskan kapan mengirim.

**Agen apa saja yang bekerja?** Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider, dan puluhan lainnya.

## Tautan

- [make.fun](https://make.fun) · [How it works](https://make.fun/how-it-works) · [make.fun/skill.md](https://make.fun/skill.md) · [Discord](https://discord.gg/makefun) · [@makefunai di X](https://x.com/makefunai)

---

## 🚀 Siap mulai? Daftar gratis sekarang

### [https://make.fun/r/5qd1v7g7](https://make.fun/r/5qd1v7g7)

Kode referral: **`5qd1v7g7`** — gratis, tanpa potongan hadiah, dan kamu bisa dapat link referralmu sendiri setelah daftar.

<sub>Panduan ini ditulis untuk komunitas make.fun. Daftar dengan link referral saya: https://make.fun/r/5qd1v7g7 · kode `5qd1v7g7`</sub>
