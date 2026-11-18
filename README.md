# The AI Ad Stack — Sales Website (GitHub Pages)

Landing page penjualan untuk produk **The AI Ad Stack — Turn AI Video Into Product Ads That Sell** ($27 one-time).
Model: theprofitstack.online, tapi copy orisinal dari GUMROAD-LISTING.md Defvy (tanpa janji penghasilan, tanpa testimoni palsu).

## Isi folder ini

- `index.html` — landing page satu file (19 KB, CSS inline, Google Fonts saja). Mobile-first, dark premium + aksen neon green #A6FF00.
- `assets/ai-ad-stack-cover.png` — cover produk (hero image).

Semua tombol beli mengarah ke `https://defvy.gumroad.com/l/ai-ad-stack` (sudah ditandai komentar `TODO` di `index.html`).

## Kenapa folder ini belum live

Pembuatan repo via GitHub MCP **gagal**: `create_repository` mengembalikan `403 Resource not accessible by integration` — integrasi GitHub App yang terhubung tidak punya izin membuat repo. `gh` CLI juga tersedia tapi **belum login**. Jadi repo + Pages harus dibuat manual sekali (5 menit, lihat bawah).

## Langkah manual Defvy (sekali saja)

1. **Buat repo baru** di github.com (login defvychristian):
   - Klik `+` → New repository → Repository name: `ai-ad-stack`
   - Description: `Sales page for The AI Ad Stack — turn AI video into product ads that sell`
   - Public, **jangan** centang "Add a README" (biar tidak bentrok) → Create repository.
2. **Upload file ini** (cara termudah — lewat web):
   - Di halaman repo baru, klik `uploading an existing file` → drag & drop **seluruh isi folder `website/` ini** (`index.html` + folder `assets/`) → Commit changes.
   - Atau via terminal (di folder `website/`):
     ```
     git init
     git add .
     git commit -m "Sales page for The AI Ad Stack"
     git branch -M main
     git remote add origin https://github.com/defvychristian/ai-ad-stack.git
     git push -u origin main
     ```
3. **Aktifkan GitHub Pages**: repo → Settings → Pages → Source: `Deploy from a branch` → Branch: `main`, Folder: `/ (root)` → Save.
4. **Verifikasi**: tunggu 1–2 menit, buka https://defvychristian.github.io/ai-ad-stack/ — harus tampil landing page dengan judul "The AI Ad Stack" dan harga $27.

## Setelah listing Gumroad jadi

1. Buat listing Gumroad dengan slug `ai-ad-stack` (URL jadi `https://defvy.gumroad.com/l/ai-ad-stack` — langsung nyambung, tanpa edit website).
2. Kalau slug-nya beda, ganti URL beli di `index.html` (cari `TODO` / `defvy.gumroad.com/l/ai-ad-stack`, ada di 4 tombol + 1 komentar), commit, push — Pages update otomatis.

## Catatan

- File `index.html` di bawah batas push GitHub MCP (128 KB) — 19 KB — jadi kalau nanti mau push via MCP, bisa.
- Jangan publish file ZIP vault ke repo ini — repo ini HANYA untuk website penjualan. Vault tetap dijual lewat Gumroad.
