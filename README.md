# Ikhwan-nur-ismail
Cara Install Git di Windows
Instalasi Git di Windows memang tidak seperti di Linux yang ketik perintah langsung terinstal.
Kita harus men-download dulu, kemudian melakukan ritual next>next>finish.
Tapi dalam ritual tersebut, ada pilihan yang harus diperhatikan agar perintah git dapat dikenali di CMD.
Selanjutnya menentukan lokasi instalasi. Biarkan saja apa adanya, kemudian klik Next >.
Selanjutnya menentukan lokasi instalasi. Biarkan saja apa adanya, kemudian klik Next >.
Selanjutnya pengaturan PATH Environment. Pilih yang tengah agar perintah git dapat di kenali di Command Prompt (CMD). Setelah i
Menentukan Path Environment
Selanjutnya konversi line ending. Biarkan saja seperti ini, kemudian klik Next >.
Konversi line ending yang akan digunakan
Selanjutnya pemilihan emulator terminal. Pilih saja yang bawah, kemudian klik Next >.
Pemilihan Terminal Emulator
Selanjutnya pemilihan opsi ekstra. Klik saja Next >.
Pemilihan Opsi Ekstra
Selanjutnya pemilihan opsi ekspreimental, langsung saja klik Install untuk memaulai instalasi.
Opsi Eksperimental
Tunggu beberapa saat, instalasi sedang dilakukan.
Sedang Menginstall Git
Setelah selesai, kita bisa langsung klik Finish.
Instalasi Git Selesai
Selamat, Git sudah terinstal di Windows. Untuk mencobanya, silahkan buka CMD atau PowerShell, kemudian ketik perintah git --version.
Perbobaan Perintah Git
3. Konfigurasi Awal yang Harus Dilakukan
Ada beberapa konfigurasi yang harus dupersiapakan sebelum mulai menggunakan Git, seperti name dan email.
Silahkan lakukan konfigurasi dengan perintah berikut ini.
git config --global user.name "Petani Kode"
git config --global user.email contoh@petanikode.com
Kemudian periksa konfigurasinya dengan perintah:
git config --list
Apabila berhasil tampil seperti gambar berikut ini, berarti konfigurasi berhasil.
konfigurasi git
Konfigurasi core.editor bersifat opsional. Sedangkan name dan email wajib.
Jika kamu memiliki akun Github, Gitlab, Bitbucket atau yang lainnya…maka username dan email harus mengikuti akun tersebut agar mudah diintegrasikan.
Repositori merupakan istilah yang digunakan untuk direktori proyek yang menggunakan Git.
Jika kita memiliki sebuah direktori dengan nama proyek-01 dan di dalamnya sudah menggunakan git, maka kita sudah punya repositori bernama proyek-01.
Membuat Repositori
Pembuatan repositori dapat dilakukan dengan perintah git init nama-dir. Contoh:
git init proyek-01
Perintah tersebut akan membuat direktori bernama proyek-01. Kalau direktorinya sudah ada, maka Git akan melakukan inisialisasi di dalam direktori tersebut.
Perintah git init akan membuat sebuah direktori bernama .git di dalam proyek kita. Direktori ini digunakan Git sebagai database untuk menyimpan perubahan yang kita lakukan.
Hati-hati!
Kalau kita menghapus direktori ini, maka semua rekaman atau catatan yang dilakukan oleh Git akan hilang.
Contoh-contoh lain
Perintah berikut ini akan membuat repositori pada direktori saat ini (working directory).
git init .
Tanda titik (.) artinya kita akan membuat repository pada direktori tempat kita berada saat ini.
Membuat repository Git
Perintah berikut ini akan membuat repositori pada direktori /var/www/html/proyekweb/.
git init /var/www/html/proyekweb
.gitignore
.gitignore merupakan sebuah file yang berisi daftar nama-nama file dan direktori yang akan diabaikan oleh Git.
Perubahan apapun yang kita lakukan terhadap file dan direktori yang sudah masuk ke dalam daftar .gitignore tidak akan dicatat oleh Git.
Cara mengunakan .gitignore, buat saja sebuah file bernama .gitignore dalam root direktori proyek/repositori.
File: .gitignore
/vendor/
/upload/
/cache
test.php
Pada contoh file .gitignore di atas, saya memasukan direktori vendor, upload, cache dan file test.php. File dan direktori tersebut akan diabaikan oleh Git.
Pembuatan file .gitignore sebaiknya dilakukan di awal pembuatan repositori.
