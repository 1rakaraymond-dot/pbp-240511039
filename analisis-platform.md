
# Analisis Komparatif Platform: Web, Desktop, dan Mobile

## 1. Perbandingan Platform

| Aspek | Web | Desktop | Mobile |
|---|---|---|---|
| Bahasa utama | Sisi klien memakai HTML untuk struktur, CSS untuk tampilan, dan JavaScript untuk interaksi. Sisi server bebas memilih, misalnya C# (ASP.NET), Python (Django), PHP (Laravel), atau JavaScript (Next.js) | C++ (Win32, C++/WinRT) dan C# pada .NET (WPF, Windows Forms, WinUI) | Android memakai Kotlin dan Java. iOS memakai Swift dengan Xcode |
| Arsitektur | 	Client-server. Browser mengirim HTTP request ke web server, lalu server membalas dengan HTTP response. Pada situs dinamis, aplikasi web mengambil data dari database dan memasukkannya ke template HTML | AAplikasi native yang terpasang di komputer dan memanggil API Windows (Win32 atau Windows Runtime). Antarmuka modern dibangun dengan WinUI 3 dan Windows App SDK | Pada Android, aplikasi berjalan di atas kernel Linux. Setiap aplikasi punya proses dan instance Android Runtime (ART) sendiri, dan mengakses fitur perangkat lewat framework API dan HAL |
| Cara distribusi | Di-host pada web server dan dibuka lewat URL di browser tanpa instalasi | Installer, paket MSIX, distribusi internal, atau Microsoft Store | Android lewat Google Play yang dikelola dengan Play Console [6]. iOS lewat App Store setelah melewati App Review, dan di beberapa wilayah Apple mengizinkan distribusi alternatif |
| Keunggulan | Bisa dibuka di perangkat apa pun yang punya browser. Dibangun di atas standar terbuka yang dirancang agar saling kompatibel . Pembaruan cukup dilakukan di server | Akses langsung ke fitur Windows seperti notifikasi, Bluetooth, dan sensor lewat WinRT API. Paket MSIX memberi instalasi dan uninstall yang bersih serta pembaruan otomatis | Portabel dan selalu dibawa pengguna. Framework API dan HAL memberi akses ke kamera, Bluetooth, dan perangkat keras lain|
| Keterbatasan | Perlu koneksi ke server untuk memuat konten. Pengembang tidak tahu perangkat dan browser yang dipakai pengguna, sehingga tampilan harus dirancang fleksibel | Terikat pada sistem operasi tertentu, dalam hal ini Windows. Sebagian fitur modern hanya tersedia jika aplikasi memiliki package identity | Harus mengikuti kebijakan toko aplikasi seperti Play Policies dan App Review [6][7]. Android dan iOS memakai bahasa serta alat yang berbeda, dan ukuran layar sangat beragam |
| Contoh aplikasi | Gmail, Google Docs, Trello | Microsoft Word, Visual Studio Code, VLC Media Player | WhatsApp, Google Maps, Instagram |

## 2. Referensi

1. MDN Web Docs. (n.d.). The web standards model. https://developer.mozilla.org/en-US/docs/Learn_web_development/Getting_started/Web_standards/The_web_standards_model
2. MDN Web Docs. (n.d.). Client-server overview. https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Server-side/First_steps/Client-Server_overview
3. Microsoft Learn. (n.d.). Modern Windows features for desktop apps. https://learn.microsoft.com/en-us/windows/apps/desktop/modernize/
4. Microsoft Learn. (n.d.). Getting started with WinUI. https://learn.microsoft.com/en-us/windows/apps/get-started/
5. Android Developers. (n.d.). Platform architecture. https://developer.android.com/guide/platform
6. Android Developers. (n.d.). Distribute your apps and games on Google Play. https://developer.android.com/distribute
7. Apple Developer. (n.d.). Distribute. https://developer.apple.com/distribute/
8. Android Developers. (n.d.). Android essentials. https://developer.android.com/get-started

## 3. Refleksi

Platform yang paling menarik bagi saya adalah web. Dari tabel perbandingan terlihat bahwa aplikasi web cukup dibuka lewat URL di browser tanpa instalasi, sehingga penggunanya bisa sangat banyak. Saya juga tertarik pada cara browser dan server bertukar data lewat HTTP, karena itu dasar dari hampir semua layanan yang saya pakai setiap hari.

Tantangan terbesar saat setup bukan pada instalasi tools, melainkan pada saat mengirim file ke GitHub. Perintah git push gagal dengan pesan bahwa username atau token tidak valid dan autentikasi password tidak lagi didukung. Dari pesan itu saya memahami bahwa GitHub kini menolak password akun untuk operasi Git. Sebelumnya saya juga sempat bingung mencari installer NPM, padahal NPM sudah ikut terpasang bersama Node.js.

Rencana saya untuk mengatasinya ada tiga. Pertama, membaca pesan error sampai selesai sebelum mencoba solusi apa pun. Kedua, menghapus kredensial lama di Windows Credential Manager lalu masuk kembali melalui browser, atau memakai personal access token jika perlu. Ketiga, selalu memeriksa versi tools dengan perintah di terminal dan membaca dokumentasi resmi agar tidak salah mengunduh. Dengan kebiasaan ini saya berharap persiapan environment pada pertemuan berikutnya berjalan lebih lancar.
