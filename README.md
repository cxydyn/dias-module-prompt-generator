# DIAS Module Prompt Generator

Web app sederhana untuk membuat prompt pembuatan modul aplikasi DIAS (standar PTW-style). User cukup mengisi **Judul** dan **Deskripsi** aplikasi, lalu menyalin prompt yang dihasilkan ke Google AI Studio (atau asisten AI lain).

## Fitur

- Form input: Judul & Deskripsi (wajib) + opsi lanjutan (peran, fitur/alur, entitas data, lampiran/export, kebutuhan offline, submodul/halaman DIAS)
- Prompt otomatis mengikuti standar modul DIAS: Next.js (App Router) + React + Tailwind + PWA, Firebase Auth + Firestore (DB), Google Drive via Google Apps Script API (storage lewat proxy `/api/*`), integrasi DIAS (iframe/new_tab, SSO param + fallback), workflow/RBAC/audit trail, testing
- Output prompt siap salin, mencakup konteks, arsitektur standar, kontrak DIAS, kualitas PTW, dan daftar output wajib (kode lengkap, `google-apps-script/`, `.env.example`, README, contoh `AppModule`/mapping route, checklist kepatuhan)

## Cara Pakai

1. Buka `index.html` di browser (double-click / buka file secara lokal).
2. Isi **Judul Aplikasi** dan **Deskripsi Aplikasi**.
3. (Opsional) isi opsi lanjutan bila perlu detail peran/fitur/data/offline/submodul.
4. Klik **Buat Prompt** (atau prompt terbentuk otomatis saat mengetik), lalu klik **Salin Prompt** dan tempel ke Google AI Studio.

## Catatan

- Tidak butuh build/dependency; satu file HTML statis.
- Field opsional yang dikosongkan akan diinstruksikan agar AI menentukan asumsi yang wajar.

## Referensi

Berdasarkan manual/standar pembuatan modul DIAS (PTW-style): arsitektur Firestore + Drive-via-GAS, kontrak `AppModule` & SSO DIAS, RBAC/workflow/audit, PWA & testing.
