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

![1](https://github.com/Berrrnattttt/Ferry_Berrnattt/assets/170847626/a3cc27fb-8745-4799-8d7e-38f6871d8bc1)

### 2.	Tampilkan pegawai yang tunjangannya NULL!

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

`SELECT * FROM pegawai WHERE tunjangan IS NULL; `

Dan hasilnya akan seperti ini :

![2](https://github.com/Berrrnattttt/Ferry_Berrnattt/assets/170847626/22f8b778-e0b6-4f12-80c1-7053b2b05230)

### 3.	Tampilkan pegawai yang tunjangannya tidak NULL!

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :
	
`SELECT * FROM pegawai WHERE tunjangan IS NOT NULL;`

Dan hasilnya akan seperti ini :

![3](https://github.com/Berrrnattttt/Ferry_Berrnattt/assets/170847626/2c54124a-2c0f-4e67-9640-8eaee39c85a9)

## HASIL DARI 1 - 3

![1-3](https://github.com/Berrrnattttt/Ferry_Berrnattt/assets/170847626/0eb953d1-6b3f-4d1a-b052-48fe51b6fd69)

### 4.	Tampilkan/hitung jumlah baris/record tabel pegawai!

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

`SELECT COUNT(*) AS jumlah_baris FROM pegawai;`

Dan hasilnya akan seperti ini :

![4](https://github.com/Berrrnattttt/Ferry_Berrnattt/assets/170847626/20c528b8-25c3-4f6f-8e2d-83fc8eb766c0)

### 5.	Tampilkan/hitung jumlah total gaji di tabel pegawai!

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :


`SELECT SUM(gaji) AS total_gaji FROM pegawai; `

Dan hasilnya akan seperti ini :

![5](https://github.com/Berrrnattttt/Ferry_Berrnattt/assets/170847626/3e6e9b78-5f22-43d4-84d8-ea8aaf67c136)

### 6.	Tampilkan/hitung rata-rata gaji pegawai!

Jawab 

Untuk perintahnya bisa menggunkan perintah seperti ini :

`SELECT AVG(gaji) AS rata_gaji FROM pegawai`

Dan hasilnya akan seperti ini :

![6](https://github.com/Berrrnattttt/Ferry_Berrnattt/assets/170847626/7d1debbd-8cc2-4e80-848a-d0853feaadbd)

### 7.	Tampilkan gaji terkecil!

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

`SELECT MIN(gaji) AS gaji_terkecil FROM pegawai;`

Dan hasilnya akan seperti ini :

![7](https://github.com/Berrrnattttt/Ferry_Berrnattt/assets/170847626/fc689e44-b694-4a7e-a476-1dfee9c849ee)

### 8.	Tampilkan gaji terbesar!

Jawab 

Untuk perintahnya bisa menggunkan perintah seperti ini :

`SELECT MAX(gaji) AS gaji_terbesar FROM pegawai;`

Dan hasilnya akan seperti ini :

![8](https://github.com/Berrrnattttt/Ferry_Berrnattt/assets/170847626/e3790132-d0fa-490c-aade-c26f44ab3758)

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

![hewan 1](https://github.com/Berrrnattttt/Ferry_Berrnattt/assets/170847626/d915f2eb-3907-4237-86c4-7c930709783d)

### 2.	Tampilkan jumlah hewan berdasarkan spesies

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

`SELECT Species, COUNT(*) AS Jumlah_hewan_berdasarkan_Species FROM hewan GROUP BY Species; `

Dan hasilnya akan seperti ini :

![hewan 2](https://github.com/Berrrnattttt/Ferry_Berrnattt/assets/170847626/8de9a260-e30f-4b80-bfd3-3ec1aa38b054)

### 3.	Tampilkan jumlah hewan berdasarkan jenis kelamin

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

`SELECT sex, COUNT(*) AS Jumlah_hewan_berdasarkan_jenis_kelamin FROM hewan GROUP BY sex; `

Dan hasilnya akan seperti ini :

![hewan 3](https://github.com/Berrrnattttt/Ferry_Berrnattt/assets/170847626/5dde4788-49c6-4e4b-861d-127a1c25e329)

### 4.	Tampilkan jumlah hewan berdasarkan spesies dan jenis kelamin

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

` SELECT species, sex, COUNT(*) AS jumlah FROM hewan GROUP BY species, sex;  `

Dan hasilnya akan seperti ini :

![hewan 4](https://github.com/Berrrnattttt/Ferry_Berrnattt/assets/170847626/24b2e8da-cca2-4ba4-b1c6-49bd9aa1ae4a)

### 5.	Tampilkan jumlah hewan berdasarkan spesis (cat dan dog saja) dan jenis kelamin

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

` SELECT species, sex, COUNT(*) AS jumlah FROM hewan WHERE species IN ('cat', 'dog') GROUP BY species, sex;  `

Dan hasilnya akan seperti ini :

![hewan 5](https://github.com/Berrrnattttt/Ferry_Berrnattt/assets/170847626/1921ec83-1f21-40c2-b517-b1ba74c4844b)

### 6.	Tampilkan jumlah hewan berdasarkan jenis kelamin yang diketahui saja

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

` SELECT sex, COUNT(*) AS jumlah FROM hewan GROUP BY sex;   `

Dan hasilnya akan seperti ini :

![hewan 6](https://github.com/Berrrnattttt/Ferry_Berrnattt/assets/170847626/726b3516-167f-411c-98ce-1c5870b7a81c)
