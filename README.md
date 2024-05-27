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

![image]

### 2.	Tampilkan pegawai yang tunjangannya NULL!

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

`SELECT * FROM pegawai WHERE tunjangan IS NULL; `

Dan hasilnya akan seperti ini :

![image]

### 3.	Tampilkan pegawai yang tunjangannya tidak NULL!

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :
	
`SELECT * FROM pegawai WHERE tunjangan IS NOT NULL;`

Dan hasilnya akan seperti ini :

![image]

## HASIL DARI 1 - 3

![image]

### 4.	Tampilkan/hitung jumlah baris/record tabel pegawai!

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

`SELECT COUNT(*) AS jumlah_baris FROM pegawai;`

Dan hasilnya akan seperti ini :

![image]

### 5.	Tampilkan/hitung jumlah total gaji di tabel pegawai!

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :


`SELECT SUM(gaji) AS total_gaji FROM pegawai; `

Dan hasilnya akan seperti ini :

![image]

### 6.	Tampilkan/hitung rata-rata gaji pegawai!

Jawab 

Untuk perintahnya bisa menggunkan perintah seperti ini :

`SELECT AVG(gaji) AS rata_gaji FROM pegawai`

Dan hasilnya akan seperti ini :

![image]

### 7.	Tampilkan gaji terkecil!

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

`SELECT MIN(gaji) AS gaji_terkecil FROM pegawai;`

Dan hasilnya akan seperti ini :

![image]

### 8.	Tampilkan gaji terbesar!

Jawab 

Untuk perintahnya bisa menggunkan perintah seperti ini :

`SELECT MAX(gaji) AS gaji_terbesar FROM pegawai;`

Dan hasilnya akan seperti ini :

![image]

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

![image]

### 2.	Tampilkan jumlah hewan berdasarkan spesies

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

`SELECT Species, COUNT(*) AS Jumlah_hewan_berdasarkan_Species FROM hewan GROUP BY Species; `

Dan hasilnya akan seperti ini :

![image]

### 3.	Tampilkan jumlah hewan berdasarkan jenis kelamin

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

`SELECT sex, COUNT(*) AS Jumlah_hewan_berdasarkan_jenis_kelamin FROM hewan GROUP BY sex; `

Dan hasilnya akan seperti ini :

![image]

### 4.	Tampilkan jumlah hewan berdasarkan spesies dan jenis kelamin

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

` SELECT species, sex, COUNT(*) AS jumlah FROM hewan GROUP BY species, sex;  `

Dan hasilnya akan seperti ini :

![sex and species]

### 5.	Tampilkan jumlah hewan berdasarkan spesis (cat dan dog saja) dan jenis kelamin

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

` SELECT species, sex, COUNT(*) AS jumlah FROM hewan WHERE species IN ('cat', 'dog') GROUP BY species, sex;  `

Dan hasilnya akan seperti ini :

![image]

### 6.	Tampilkan jumlah hewan berdasarkan jenis kelamin yang diketahui saja

Jawab :

Untuk perintahnya bisa menggunkan perintah seperti ini :

` SELECT sex, COUNT(*) AS jumlah FROM hewan GROUP BY sex;   `

Dan hasilnya akan seperti ini :

![image]
