# Praktikum-4

## TUGAS PRAKTIKUM 4 (TABEL PEGAWAI)
1.	Tampilkan pegawai yang gajinya bukan 2.000.000 dan 1.250.000 !
2.	Tampilkan pegawai yang tunjangannya NULL!
3.	Tampilkan pegawai yang tunjangannya tidak NULL!
4.	Tampilkan/hitung jumlah baris/record tabel pegawai!
5.	Tampilkan/hitung jumlah total gaji di tabel pegawai!
6.	Tampilkan/hitung rata-rata gaji pegawai!
7.	Tampilkan gaji terkecil!
8.	Tampilkan gaji terbesar!

PENJELASAN


### 1.	Tampilkan pegawai yang gajinya bukan 2.000.000 dan 1.250.000 !

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

`SELECT * FROM pegawai WHERE gajih NOT IN (2000000, 1250000);`

Dan hasilnya akan seperti ini :

![image](https://github.com/Heryantokurnia/Praktikum-4/assets/141998024/4e580583-3bb5-4b86-84bd-dce0ff01e338)

### 2.	Tampilkan pegawai yang tunjangannya NULL!

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

`SELECT * FROM pegawai WHERE tunjangan IS NULL; `

Dan hasilnya akan seperti ini :

![image](https://github.com/Heryantokurnia/Praktikum-4/assets/141998024/16950ed6-2d1c-4333-bd8b-3960bf6aa8cf)

### 3.	Tampilkan pegawai yang tunjangannya tidak NULL!

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :
	
`SELECT * FROM pegawai WHERE tunjangan IS NOT NULL;`

Dan hasilnya akan seperti ini :

![image](https://github.com/Heryantokurnia/Praktikum-4/assets/141998024/0ffebe47-b6ec-468d-8228-1b373a62372a)

## HASIL DARI 1 - 3

![image](https://github.com/Heryantokurnia/Praktikum-4/assets/141998024/06839f76-6c14-485a-b482-7daad459ad16)

### 4.	Tampilkan/hitung jumlah baris/record tabel pegawai!

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

`SELECT COUNT(*) AS jumlah_baris FROM pegawai;`

Dan hasilnya akan seperti ini :

![image](https://github.com/Heryantokurnia/Praktikum-4/assets/141998024/c5c0da82-9f04-44af-88af-2f9572bd8b4d)

### 5.	Tampilkan/hitung jumlah total gaji di tabel pegawai!

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :


`SELECT SUM(gaji) AS total_gaji FROM pegawai; `

Dan hasilnya akan seperti ini :

![image](https://github.com/Heryantokurnia/Praktikum-4/assets/141998024/3d86721b-8c25-4dcb-bae3-341e658f30f6)

### 6.	Tampilkan/hitung rata-rata gaji pegawai!

Jawab 

Untuk perintahnya bisa menggunkan perintah seperti ini :

`SELECT AVG(gaji) AS rata_gaji FROM pegawai`

Dan hasilnya akan seperti ini :

![image](https://github.com/Heryantokurnia/Praktikum-4/assets/141998024/5b9375f1-df3d-4fab-b0b1-f33300d77fc1)

### 7.	Tampilkan gaji terkecil!

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

`SELECT MIN(gaji) AS gaji_terkecil FROM pegawai;`

Dan hasilnya akan seperti ini :

![image](https://github.com/Heryantokurnia/Praktikum-4/assets/141998024/d3b917e8-7005-49e3-8ce9-a2015ec1a941)

### 8.	Tampilkan gaji terbesar!

Jawab 

Untuk perintahnya bisa menggunkan perintah seperti ini :

`SELECT MAX(gaji) AS gaji_terbesar FROM pegawai;`

Dan hasilnya akan seperti ini :

![image](https://github.com/Heryantokurnia/Praktikum-4/assets/141998024/884ddeb8-5530-496d-ad03-43c5b2b60cae)

## TUGAS PRAKTIKUM 4 (TABEL HEWAN)
1.	Tampilkan jumlah hewan yang dimiliki setiap owner
2.	Tampilkan jumlah hewan berdasarkan spesies
3.	Tampilkan jumlah hewan berdasarkan jenis kelamin
4.	Tampilkan jumlah hewan berdasarkan spesies dan jenis kelamin
5.	Tampilkan jumlah hewan berdasarkan spesis (cat dan dog saja) dan jenis kelamin
6.	Tampilkan jumlah hewan berdasarkan jenis kelamin yang diketahui saja

PENJELASAN

### 1. Tampilkan jumlah hewan yang dimiliki setiap owner

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

`SELECT owner, COUNT(*) AS Jumlah_hewan_setiap_owner FROM hewan GROUP BY owner; `

Dan hasilnya akan seperti ini :

![image](https://github.com/Heryantokurnia/Praktikum-4/assets/141998024/c2f79225-7d45-4015-b21c-53789b8a403e)

### 2.	Tampilkan jumlah hewan berdasarkan spesies

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

`SELECT Species, COUNT(*) AS Jumlah_hewan_berdasarkan_Species FROM hewan GROUP BY Species; `

Dan hasilnya akan seperti ini :

![image](https://github.com/Heryantokurnia/Praktikum-4/assets/141998024/c7577f83-33aa-4bd2-85fc-f1353e0c1f63)

### 3.	Tampilkan jumlah hewan berdasarkan jenis kelamin

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

`SELECT sex, COUNT(*) AS Jumlah_hewan_berdasarkan_jenis_kelamin FROM hewan GROUP BY sex; `

Dan hasilnya akan seperti ini :

![image](https://github.com/Heryantokurnia/Praktikum-4/assets/141998024/2dba9be5-ee55-4bf0-b742-b4231492f3d0)

### 4.	Tampilkan jumlah hewan berdasarkan spesies dan jenis kelamin

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

` SELECT species, sex, COUNT(*) AS jumlah FROM hewan GROUP BY species, sex;  `

Dan hasilnya akan seperti ini :

![sex and species](https://github.com/Heryantokurnia/Praktikum-4/assets/141998024/10627e1b-3f61-418f-8c6d-251791f97b28)

### 5.	Tampilkan jumlah hewan berdasarkan spesis (cat dan dog saja) dan jenis kelamin

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

` SELECT species, sex, COUNT(*) AS jumlah FROM hewan WHERE species IN ('cat', 'dog') GROUP BY species, sex;  `

Dan hasilnya akan seperti ini :

![image](https://github.com/Heryantokurnia/Praktikum-4/assets/141998024/2c3dc657-a23a-4053-befe-1e91a888b8cc)

### 6.	Tampilkan jumlah hewan berdasarkan jenis kelamin yang diketahui saja

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

` SELECT sex, COUNT(*) AS jumlah FROM hewan GROUP BY sex;   `

Dan hasilnya akan seperti ini :

![image](https://github.com/Heryantokurnia/Praktikum-4/assets/141998024/e1ccaba2-de53-4839-8ee6-be25e869a72d)
