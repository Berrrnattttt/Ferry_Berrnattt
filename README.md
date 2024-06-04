# Praktikum-5

## LATIHAN !!!

1. Lakukan join table Mahasiswa dan Dosen

2. Lakukan join tabel Matakuliah dan Dosen
   
3. Lakukan join table JadwalMengajar, Dosen, dan Matakuluan
   
4. Lakukan join tabel KrsMahasiswa, Mahasiswa, Matakuliah, dan Dosen

## JOIN table Mahasiswa dan Dosen

### untuk tabel mahasiswa :
![1](https://github.com/Berrrnattttt/Ferry_Bernat-5/assets/170847626/7ba1deeb-b989-472b-b8ea-9e8d31c9c727)

### untuk tabel dosen :
![2](https://github.com/Berrrnattttt/Ferry_Bernat-5/assets/170847626/fefeb17c-ead7-42ca-b370-45ac7f190e26)

### untuk tabel krs mahasiswa :
![3](https://github.com/Berrrnattttt/Ferry_Bernat-5/assets/170847626/a61687b0-2b2d-496e-ac05-d76cc260393a)

### untuk tabel matakuliah :
![4](https://github.com/Berrrnattttt/Ferry_Bernat-5/assets/170847626/122c15ca-1d4f-4ada-a75d-3853fb30dbc0)

### untuk tabel jadwal mengajar :
![5](https://github.com/Berrrnattttt/Ferry_Bernat-5/assets/170847626/bcd93936-49da-419d-8e3d-bcf543a91f68)

# 1. Lakukan Join Table Mahasiswa Dan Dosen

## Untuk perintah bisa menggunakan (INNER JOIN)

`SELECT tb_mahasiswa.nim, tb_mahasiswa.nama, tb_mahasiswa.jk, tb_dosen.nama AS "Dosen" FROM tb_mahasiswa INNER JOIN tb_dosen ON tb_dosen.kd_ds = tb_mahasiswa.kd_ds;`

Hasilnya akan seperti ini :
![1 1](https://github.com/Berrrnattttt/Ferry_Bernat-5/assets/170847626/28cd5990-e07e-4156-8bf4-d45d40b95c5f)

> Note Digunakan untuk menampilkan baris tabel yang memiliki nilai yang sama pada kolom yang terkait

## Untuk perintah bisa menggunakan (LEFT JOIN)

`SELECT tb_mahasiswa.nim, tb_mahasiswa.nama, tb_mahasiswa.jenis_kelamin, tb_dosen.nama AS "Dosen"
FROM tb_mahasiswa LEFT JOIN tb_dosen ON tb_dosen.kd_ds = tb_mahasiswa.kd_ds;`

Hasilnya akan seperti ini :
![1 2](https://github.com/Berrrnattttt/Ferry_Bernat-5/assets/170847626/41c55ca1-b1dd-49ba-bf0b-b86edfbb9276)

> Note Menampilkan semua data pada table A dan sebagian data pada table B yang bersinggungan dengan table A

## Untuk perintah bisa menggunakan (RIGHT JOIN)

`SELECT tb_mahasiswa.nim, tb_mahasiswa.nama, tb_mahasiswa.jk, tb_dosen.nama AS "Dosen" 
FROM tb_mahasiswa 
RIGHT JOIN tb_dosen ON tb_dosen.kd_ds = tb_mahasiswa.kd_ds;`

Hasilnya akan seperti ini :
![1 3](https://github.com/Berrrnattttt/Ferry_Bernat-5/assets/170847626/d6613b58-4553-4798-bd79-ba8a32763556)

> Note Menampilkan semua data pada table B dan sebagian data pada table A yang bersinggungan dengan table B

# 2 Lakukan join tabel Matakuliah dan Dosen #

## Untuk perintah bisa menggunakan :

`SELECT tb_matakuliah.kd_mk, tb_matakuliah.nama, tb_matakuliah.sks, tb_dosen.nama AS "Dosen Pengampu"
FROM tb_jadwalmengajar
LEFT JOIN tb_matakuliah ON tb_jadwalmengajar.kd_mk = tb_matakuliah.kd_mk
LEFT JOIN tb_dosen ON tb_jadwalmengajar.kd_ds = tb_dosen.kd_ds;`

Hasilnya akan seperti ini :
![1 4](https://github.com/Berrrnattttt/Ferry_Bernat-5/assets/170847626/f292b360-a5a7-4e3f-98cd-5416f4584a3e)

## Untuk perintah bisa menggunakan :

`SELECT tb_jadwalmengajar.hari, tb_jadwalmengajar.jam, tb_jadwalmengajar.ruang, tb_dosen.nama AS "Dosen Pengampu", tb_jadwalmengajar.kd_mk, tb_matakuliah.nama, tb_matakuliah.sks 
FROM tb_jadwalmengajar 
LEFT JOIN tb_matakuliah ON tb_jadwalmengajar.kd_mk = tb_matakuliah.kd_mk 
LEFT JOIN tb_dosen ON tb_jadwalmengajar.kd_ds = tb_dosen.kd_ds;`

Hasilnya akan seperti ini :

![1 5](https://github.com/Berrrnattttt/Ferry_Bernat-5/assets/170847626/c36b1f01-f552-4745-9858-abb88cc13549)

# 3.Lakukan join tabel KrsMahasiswa, Mahasiswa, Matakuliah, dan Dosen #

## Untuk perintah bisa menggunakan :

`SELECT tb_mahasiswa.nim, tb_mahasiswa.nama AS "nama", tb_matakuliah.nama AS "Matakuliah", tb_matakuliah.sks, tb_dosen.nama AS "Dosen Pengampu"
FROM tb_krsmahasiswa
JOIN tb_mahasiswa ON tb_krsmahasiswa.nim = tb_mahasiswa.nim
JOIN tb_matakuliah ON tb_krsMahasiswa.kd_mk = tb_matakuliah.kd_mk
JOIN tb_dosen ON tb_krsmahasiswa.kd_ds = tb_dosen.kd_ds;`

Hasilnya akan seperti ini :

![1 6](https://github.com/Berrrnattttt/Ferry_Bernat-5/assets/170847626/ed28c222-cfb6-4aba-aef0-7c397408a8be)


> ### Join tabel
>  join tabel merujuk pada penggabungan baris-baris data dari dua atau lebih tabel berdasarkan kolom yang memiliki nilai yang sama di setiap tabel. Join tabel memungkinkan kita untuk menggabungkan data dari tabel yang berbeda untuk menghasilkan hasil yang lebih lengkap dan terkait.

> ### Jenis2
> 1. **INNER JOIN** : Menggabungkan baris-baris data dari dua tabel berdasarkan kondisi join yang ditentukan. Hanya baris yang memiliki nilai yang cocok di kedua tabel yang akan dimasukkan ke dalam hasil join.
>
> 2. **LEFT JOIN** : Menggabungkan semua baris dari tabel kiri (left table) dengan baris yang cocok dari tabel kanan (right table) berdasarkan kondisi join. Jika tidak ada nilai yang cocok dalam tabel kanan, kolom-kolom dari tabel kanan akan memiliki nilai NULL dalam hasil join.
>
> 3. **RIGHT JOIN** : Adalah kebalikan dari LEFT JOIN. Ini menggabungkan semua baris dari tabel kanan dengan baris yang cocok dari tabel kiri berdasarkan kondisi join. Jika tidak ada nilai yang cocok dalam tabel kiri, kolom-kolom dari tabel kiri akan memiliki nilai NULL dalam hasil join.
>
> 4. **FULL JOIN** : Menggabungkan semua baris dari kedua tabel, baik dari tabel kiri maupun tabel kanan, berdasarkan kondisi join. Ini akan menghasilkan semua baris dari kedua tabel, dan jika tidak ada nilai yang cocok dalam salah satu tabel, kolom-kolom yang tidak cocok akan memiliki nilai NULL dalam hasil join.
