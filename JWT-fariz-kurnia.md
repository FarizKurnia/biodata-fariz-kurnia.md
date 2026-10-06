# Product Knowledge: Datadigi JWT (JSON Web Token) Service

## Deskripsi Produk
**Datadigi JWT** adalah layanan autentikasi dan otorisasi berbasis standar industri (RFC 7519) yang digunakan untuk mengamankan pertukaran informasi dan sesi pengguna di seluruh ekosistem aplikasi Datadigi. Layanan ini memastikan bahwa setiap permintaan (*request*) data dari pengguna atau aplikasi klien terverifikasi secara sah, cepat, dan aman tanpa membebani memori server (*stateless*).

## Fitur Utama
- **Autentikasi Stateless:** Mengamankan sesi pengguna tanpa perlu menyimpan *session ID* di server, sehingga mempercepat pemrosesan data.
- **Enkripsi Kriptografi:** Dilengkapi tanda tangan digital (*digital signature*) menggunakan algoritma aman (seperti HS256 atau RS256) untuk mencegah manipulasi data.
- **Otorisasi Berbasis Peran (Role-Based Access):** Mengirimkan klaim (*claims*) data pengguna dan hak akses langsung di dalam token untuk membatasi fitur sesuai kewenangan (misal: Admin, Kasir, Manajer).
- **Manajemen Masa Berlaku (Expiration & Refresh Token):** Mendukung pengaturan *expired time* token secara fleksibel beserta mekanisme *refresh token* untuk memperbarui akses tanpa perlu *login* ulang.

## Keunggulan & Manfaat
- **Keamanan Tingkat Tinggi:** Mencegah peretasan dan perubahan data yang tidak sah (*tampering*) saat dikirimkan antar sistem.
- **Kinerja Cepat & Ringan:** Mempercepat respon aplikasi karena server tidak perlu melakukan *query* database berulang kali hanya untuk memverifikasi identitas pengguna.
- **Mendukung Arsitektur Microservices:** Memudahkan integrasi dan berbagi autentikasi antar berbagai layanan aplikasi Datadigi (seperti DiviPOS, DiviPRO, dan Open API).

## Cara Penggunaan Singkat
1. **Proses Login & Penerbitan Token:**
   - Aplikasi klien mengirimkan kredensial (*username* dan *password*) ke *endpoint* autentikasi (`POST /api/v1/auth/login`).
   - Setelah validasi berhasil, server Datadigi menerbitkan *Access
