# Web CV Mikarya Engineering — Produksi

Satu berkas: `index.html` (tampilan & teks sama persis mockup final
`kode-chatgpt/ADAPTASI-KAROSEL-ATAS/index.html`; catatan perancang
sudah dikeluarkan dari halaman).

## Backend (Supabase)

- Proyek: `https://wqljyfhiykwvbffkonyr.supabase.co`
- Tabel `public.foto_galeri` (id, kategori, produk_id, storage_path,
  tautan, urutan, dibuat_pada) + bucket publik `foto-galeri`.
- Galeri Portofolio & galeri tiap produk dimuat dari tabel itu;
  kosong = "Foto menyusul". Foto ber-tautan membuka tab baru.
- Admin: login Google di laci menu; hanya 3 Gmail terdaftar
  (muliaedutama@gmail.com, Iskandar.ik313@gmail.com,
  ajrikamal789@gmail.com) yang mendapat mode admin (tambah/hapus
  foto, ubah link per foto). Unggah dikompres di klien
  (maks 500 KB, sisi terpanjang maks 1600px).

## Sebelum tayang

1. Isi `SUPABASE_ANON_KEY` di `index.html` (satu-satunya tempat,
   cari `__SUPABASE_ANON_KEY__`) dengan publishable/anon key asli
   proyek di atas. Selama placeholder, galeri tampil "Foto
   menyusul" dan login admin nonaktif.
2. Pastikan RLS `foto_galeri` + bucket mengizinkan baca publik dan
   tulis/hapus hanya untuk 3 email admin di atas.
3. Tambahkan domain tayang ke daftar Redirect URLs Supabase Auth.
