# basis-data-praktikum-5

```
Latihan
1 Lakukan join table Mahasiswa dan Dosen
2 Lakukan join tabel Matakuliah dan Dosen
3 Lakukan join table JadwalMengajar, Dosen, dan Matakuluan
4 Lakukan join tabel KrsMahasiswa, Mahasiswa, Matakuliah, dan Dosen
```
### Tabel Mahasiswa
![WhatsApp Image 2023-06-06 at 12 48 54](https://github.com/Muhamad-Raehan/basis-data-praktikum-5/assets/116246238/82d0d8bd-c80a-48d1-9f43-52de38e30144)

### Tabel Dosen
![WhatsApp Image 2023-06-06 at 12 49 11](https://github.com/Muhamad-Raehan/basis-data-praktikum-5/assets/116246238/88f4593b-4f8f-436a-9979-6df26b6556aa)

### Tabel KrsMahasiswa
![WhatsApp Image 2023-06-06 at 12 49 32](https://github.com/Muhamad-Raehan/basis-data-praktikum-5/assets/116246238/9a0c194a-ca81-4b5d-9b24-9d0afe60d1ef)

### Tabel JadwalMengajar
![WhatsApp Image 2023-06-06 at 12 49 56](https://github.com/Muhamad-Raehan/basis-data-praktikum-5/assets/116246238/3b3b6d8f-718a-4450-91ab-94aeabd7964f)

### Tabel Matakuliah
![WhatsApp Image 2023-06-06 at 12 50 26](https://github.com/Muhamad-Raehan/basis-data-praktikum-5/assets/116246238/0375ad1f-94ce-4306-900e-9fabf1380c7d)

# LATIHAN

1 Lakukan join table Mahasiswa dan Dosen
![WhatsApp Image 2023-06-06 at 12 51 12](https://github.com/Muhamad-Raehan/basis-data-praktikum-5/assets/116246238/20166609-c7c0-4ba3-a863-40a58d424b75)


2 Lakukan join tabel Matakuliah dan Dosen
![WhatsApp Image 2023-06-06 at 12 51 27](https://github.com/Muhamad-Raehan/basis-data-praktikum-5/assets/116246238/c3c2199e-7237-4156-b104-fdaef3d317c2)

```
Pada kode ini hasilnya tabel dosen null karena kedua tabel tidak saling ber relasi
```

3 Lakukan join table JadwalMengajar, Dosen, dan Matakuluan
![WhatsApp Image 2023-06-06 at 12 51 44](https://github.com/Muhamad-Raehan/basis-data-praktikum-5/assets/116246238/1a789bd6-5f7a-497e-8308-749f16db01ee)


4 Lakukan join tabel KrsMahasiswa, Mahasiswa, Matakuliah, dan Dosen
![WhatsApp Image 2023-06-06 at 12 52 01](https://github.com/Muhamad-Raehan/basis-data-praktikum-5/assets/116246238/25dc517e-95ba-43a6-8d0b-cd43b45495bf)

# LATIHAN

1. JOIN table Mahasiswa dan Dosen
```
SELECT Mahasiswa.nim, Mahasiswa.nama, Mahasiswa.jenis_kelamin, Dosen.nama AS 'Dosen' 
FROM Mahasiswa 
JOIN Dosen ON Dosen.kd_ds=Mahasiswa.kd_ds;
```
![WhatsApp Image 2023-06-06 at 12 52 31](https://github.com/Muhamad-Raehan/basis-data-praktikum-5/assets/116246238/b94fb1ce-1dd3-4f2a-bb14-e0bfa77bbd4f)


2. LEFT JOIN table Mahasiswa dan Dosen
```
SELECT Mahasiswa.nim, Mahasiswa.nama, Mahasiswa.jenis_kelamin, Dosen.nama AS 'Dosen'
FROM Mahasiswa
LEFT JOIN Dosen ON Dosen.kd_ds=Mahasiswa.kd_ds;
```
![WhatsApp Image 2023-06-06 at 12 53 00](https://github.com/Muhamad-Raehan/basis-data-praktikum-5/assets/116246238/ec965747-926d-4b79-9abb-8f3bd5240f51)


3. JOIN table JadwalMengajar, Dosen, dan Matakuliah
```
SELECT jadwalMengajar.kd_mk, matakuliah.nama AS 'Mata kuliah', matakuliah.sks, Dosen.nama AS 'Dosen Pengampu'
FROM jadwalMengajar
JOIN Dosen ON jadwalMengajar.kd_ds = Dosen.kd_ds
JOIN matakuliah ON jadwalMengajar.kd_mk = matakuliah.kd_mk;
```
![WhatsApp Image 2023-06-06 at 12 53 18](https://github.com/Muhamad-Raehan/basis-data-praktikum-5/assets/116246238/37d6386a-3eea-4ffb-8354-0fda21ea29e4)


4. JOIN table JadwalMengajar, Dosen, dan Matakuliah
```
SELECT jadwalMengajar.kd_mk, matakuliah.nama AS 'Mata kuliah', matakuliah.sks, Dosen.nama AS 'Dosen Pengampu', jadwalMengajar.hari, jadwalMengajar.jam, jadwalMengajar.ruang
FROM jadwalMengajar
JOIN Dosen ON jadwalMengajar.kd_ds = Dosen.kd_ds
JOIN matakuliah ON jadwalMengajar.kd_mk = matakuliah.kd_mk;
```
![WhatsApp Image 2023-06-06 at 12 53 42](https://github.com/Muhamad-Raehan/basis-data-praktikum-5/assets/116246238/85db4784-74e2-400f-9076-6c9f1d0420ab)
