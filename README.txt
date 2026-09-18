SIUJIAN TKA PRO — Google Sheets + Apps Script

ISI PAKET
1. database_siujian_tka_PRO.xlsx  : template database profesional.
2. Code.gs                         : backend, autentikasi, CRUD, token, dashboard, ranking, statistik, ekspor.
3. Admin.html                      : dashboard Admin/Guru.
4. Index.html                      : aplikasi ujian siswa dari versi sebelumnya.
5. appsscript.json                 : konfigurasi Apps Script.

STRUKTUR DATA
Pengaturan, Pengguna, Kelas, Siswa, AnggotaKelas, Ujian, Soal, Jadwal, Token,
Hasil, Jawaban, Koreksi, AuditLog.

INSTALASI
1. Upload database_siujian_tka_PRO.xlsx ke Google Drive lalu buka sebagai Google Sheets.
2. Extensions > Apps Script.
3. Buat/isi Code.gs dengan file Code.gs dari paket.
4. Buat file HTML bernama Admin lalu tempel Admin.html.
5. Buat file HTML bernama Index lalu tempel Index.html versi paket.
6. Pastikan appsscript.json sesuai.
7. Jalankan setupDatabasePro() sekali dan izinkan permission.
8. Deploy > New deployment > Web app.
9. Execute as: Me. Akses: pilih sesuai kebijakan sekolah (untuk produksi lebih aman dibatasi domain/sekolah).
10. Portal admin: URL web app + ?page=admin.
11. Portal siswa: URL web app biasa.

AKUN AWAL
admin / admin123
guru / guru123
Segera ganti password admin setelah instalasi.

FITUR PRO
- Login Admin/Guru berbasis sesi.
- Role admin dan guru.
- Database siswa dan kelas.
- Jadwal ujian per kelas.
- Token otomatis per jadwal, dengan masa berlaku.
- Dashboard jumlah siswa/kelas/ujian/hasil dan ringkasan nilai.
- Ranking nilai dan statistik distribusi.
- Export CSV, XLSX, PDF.
- Audit log.
- Tetap menyediakan API dbList/dbGet/dbSet/dbDel agar aplikasi ujian lama dapat menggunakan spreadsheet.

CATATAN KEAMANAN
Ini adalah autentikasi aplikasi, bukan IAM tingkat enterprise. Jangan gunakan password seed di produksi. Untuk ujian resmi, batasi akses Web App ke akun/domain sekolah bila memungkinkan. Tambahkan HTTPS (Google Apps Script sudah menggunakan HTTPS) dan prosedur reset password.

CATATAN INTEGRASI
Versi Admin.html adalah console pengelolaan profesional. Index.html adalah aplikasi ujian siswa versi sebelumnya yang sudah terhubung ke Google Sheets. Jadwal/token dapat dikelola dari console; integrasi validasi token pada halaman siswa dapat dilanjutkan dengan memanggil getActiveScheduleForStudent() sebelum ujian dimulai.
