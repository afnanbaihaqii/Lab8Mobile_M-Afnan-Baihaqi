Nama : M Afnan Baihaqi
Nim : H1D022080
Shift : B 

### Screenshot

![Screenshot 2024-11-11 192313](https://github.com/user-attachments/assets/dd40cc79-b155-4557-bfc5-a578af9f0376)

![Screenshot 2024-11-11 192524](https://github.com/user-attachments/assets/fffab219-03f2-4392-b5c4-4875cd07eeab)

![Screenshot 2024-11-11 194622](https://github.com/user-attachments/assets/a92fca8b-ee30-4311-8386-9717b35599de)

![Screenshot 2024-11-11 194631](https://github.com/user-attachments/assets/a8d26bca-5453-44e8-9ecc-7dcf2d2eddf9)

![Screenshot 2024-11-11 203910](https://github.com/user-attachments/assets/609e9f63-5807-431e-bdeb-ec3ee4694069)

### Penjelasan

Halaman MahasiswaPage yang dirancang untuk mengelola data mahasiswa menggunakan API di aplikasi Ionic berbasis Angular. Komponen ini menangani empat fungsi utama: menampilkan daftar mahasiswa, menambah data mahasiswa baru, mengedit data yang sudah ada, dan menghapus data yang tidak lagi dibutuhkan, dengan tampilan berupa modal (popup) yang memudahkan interaksi. Saat halaman pertama kali dimuat, fungsi getMahasiswa() dijalankan untuk mengambil semua data mahasiswa dari server menggunakan API tampil.php. Hasilnya disimpan di dataMahasiswa, sehingga daftar mahasiswa bisa langsung ditampilkan pada halaman. Untuk menambahkan mahasiswa baru, pengguna dapat membuka modal tambah dengan openModalTambah(isOpen: boolean). Modal ini otomatis mengosongkan kolom input nama dan jurusan agar siap diisi data baru. Ketika pengguna memasukkan nama dan jurusan, lalu menekan tombol tambah, fungsi tambahMahasiswa() akan mengirimkan data tersebut ke API tambah.php. Jika data berhasil ditambahkan, modal ditutup, input di-reset, dan daftar mahasiswa diperbarui secara otomatis.

Fungsi hapusMahasiswa(id: any) memudahkan pengguna untuk menghapus data mahasiswa tertentu dengan konfirmasi. Saat pengguna mengklik tombol hapus, muncul pesan konfirmasi yang menanyakan, "Apakah Data ingin dihapus?". Jika pengguna menyetujui, permintaan penghapusan dikirim ke API hapus.php?id=, lalu jika berhasil, daftar mahasiswa di-refresh untuk menghapus data dari tampilan. Jika pengguna membatalkan, proses penghapusan dihentikan tanpa ada perubahan. Untuk mengedit data, pengguna dapat membuka modal edit dengan openModalEdit(isOpen: boolean, idget: any), di mana ID mahasiswa yang ingin diedit akan diambil dan ditampilkan pada input form modal. Data tersebut diambil dari server melalui API lihat.php?id=, lalu diisi dalam form agar pengguna dapat mengubah nama atau jurusan. Setelah selesai, pengguna dapat menyimpan perubahan dengan fungsi editMahasiswa() yang mengirim data terbaru ke API edit.php. Jika perubahan berhasil, modal ditutup, form di-reset, dan tampilan daftar mahasiswa diperbarui. Fungsi tambahan cancel() digunakan untuk menutup modal dan mengosongkan form kapan pun diperlukan. Dengan begitu, pengguna memiliki kontrol penuh dalam mengelola data mahasiswa, dari menambah, melihat, mengedit, hingga menghapus, semuanya dengan konfirmasi dan interaksi yang mudah melalui modal yang tampil dinamis di halaman.
