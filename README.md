# Tugas Praktikum { Pertemuan ke 12 } <img src=https://logos-download.com/wp-content/uploads/2016/05/MySQL_logo_logotype.png width="130px" >


|**Nama**|**NIM**|**Kelas**|**Matkul**|
|----|---|-----|------|
|Samuel Damatta Tindaon|312310462|TI.23.A.5|Basis Data|

# Soal Latihan Praktikum 

![T1](https://github.com/SamuelTindaon/MTSQL5/assets/147571483/e55bc2fb-937c-41a1-b02c-c5b0a8ae3e1c)

![T2](https://github.com/SamuelTindaon/MTSQL5/assets/147571483/679f7f4e-9050-4a7b-b1f4-a216c933a87d)

![T3](https://github.com/SamuelTindaon/MTSQL5/assets/147571483/16f98ee4-23f2-4acf-8774-ea9de10bec15)

![T4](https://github.com/SamuelTindaon/MTSQL5/assets/147571483/a1cd9e2e-ed64-48d8-bd23-2dd9014a87a0)

![T5](https://github.com/SamuelTindaon/MTSQL5/assets/147571483/5edf4a36-b01a-49d3-97a0-43045ce13aac)

## Latihan

- Lakukan JOIN table Mahasiswa dan Dosen.
- Lakukan JOIN tabel Matakuliah dan Dosen.
- Lakukan JOIN table JadwalMengajar, Dosen, dan Matakuliah.
- Lakukan JOIN tabel KrsMahasiswa, Mahasiswa, Matakuliah, dan Dosen.

## Buat Script SQL JOIN Table berdasarkan skema data diatas.

```
INSERT INTO mahasiswa VALUES
    (1812345, 'Ari Santoso', 'L', '1999-10-11', NULL, 'Bekasi', NULL, NULL, 'DS002'),
    (1823456, 'Dina Marlina', 'P', '1998-11-20', NULL, 'Jakarta', NULL, NULL, NULL),
    (1834567, 'Rahmat Hidayat', 'L', '1999-05-10', NULL, 'Bekasi', NULL, NULL, NULL),
    (1845678, 'Jaka Sampurna', 'L', '2000-10-19', NULL, 'Cikarang', NULL, NULL, NULL),
    (1856789, 'Tia Lestari', 'P', '1999-02-15', NULL, 'Karawang', NULL, NULL, NULL),
    (1867890, 'Anton Sinaga', 'L', '1998-06-22', NULL, 'Bekasi', NULL, NULL, NULL),
    (1912345, 'Listia Nastiti', 'P', '2001-10-23', NULL, 'Jakarta', NULL, NULL, NULL),
    (1923456, 'Amira Jarisa', 'P', '2001-01-24', NULL, 'Karawang', NULL, NULL, 'DS004'),
    (1934567, 'Laksana Mardito', 'L', '1999-04-14', NULL, 'Cikarang', NULL, NULL, NULL),
    (1945678, 'Jura Marsina', 'P', '2000-05-10', NULL, 'Cikarang', NULL, NULL, NULL),
    (1956789, 'Dadi Martani', 'L', '2001-08-29', NULL, 'Bekasi', NULL, NULL, 'DS005'),
    (1967890, 'Bayu Laksono', 'L', '1999-07-22', NULL, 'Cikarang', NULL, NULL, 'DS004');

SELECT*FROM Mahasiswa;
`````
Output :
![H1](https://github.com/SamuelTindaon/MTSQL5/assets/147571483/b0be9b84-9223-4a3b-811d-b9cff363c35a)

`````
insert into dosen values
    ("DS001", "Nofal Arianto"),
    ("DS002", "Ario Talib"),
    ("DS003", "Ayu Rahmadina"),
    ("DS004", "Ratna Kumala"),
    ("DS005", "Vika Prasetyo");

SELECT*FROM Dosen;

`````
Output :
![H2](https://github.com/SamuelTindaon/MTSQL5/assets/147571483/a60f99fe-1800-484d-bed8-31675d5d7ba1)

`````
INSERT INTO Matakuliah VALUES
('MK001', 'Algoritma Dan Pemrogaman', 3),
('MK002', 'Praktikum Algoritma Dan Pemrograman', 1),
('MK003', 'Teknologi Basis Data', 3),
('MK004', 'Praktikum Teknologi Basis Data', 1),
('MK005', 'Pemrograman Dasar', 3),
('MK006', 'Pemrograman Berorientasi Objek', 3),
('MK007', 'Struktur Data', 3),
('MK008', 'Arsitektur Komputer', 2);

SELECT * FROM Matakuliah;
`````
Output :
![H3](https://github.com/SamuelTindaon/MTSQL5/assets/147571483/997e109e-414b-4ddd-b1df-1d0d57131918)

`````
INSERT INTO JadwalMengajar VALUES
('MK001', 'DS002', 'Senin', '10:00:00', '102'),
('MK002', 'DS002', 'Senin', '13:00:00', 'Lab. 01'),
('MK003', 'DS001', 'Selasa', '08:00:00', '201'),
('MK004', 'DS001', 'Rabu', '10:00:00', 'Lab. 02'),
('MK005', 'DS003', 'Selasa', '10:00:00', 'Lab. 01'),
('MK006', 'DS004', 'Kamis', '09:00:00', 'Lab. 03'),
('MK007', 'DS005', 'Rabu', '08:00:00', '102'),
('MK008', 'DS005', 'Kamis', '13:00:00', '201');

SELECT*FROM JadwalMengajar;
`````
Output :
![H4](https://github.com/SamuelTindaon/MTSQL5/assets/147571483/3811a3e4-4244-470b-9527-6c99836e6e48)

`````
INSERT INTO KRSMahasiswa VALUES
(1823456, 'MK001', 'DS002', 3, NULL),
(1823456, 'MK002', 'DS002', 1, NULL),
(1823456, 'MK003', 'DS001', 3, NULL),
(1823456, 'MK004', 'DS001', 3, NULL),
(1823456, 'MK007', 'DS005', 3, NULL),
(1823456, 'MK008', 'DS005', 3, NULL);

SELECT * FROM KRSMahasiswa;
`````
Output :
![H5](https://github.com/SamuelTindaon/MTSQL5/assets/147571483/8beaf992-dc8d-44fd-a7f6-75a01fb8c273)

# Latihan
- JOIN table Mahasiswa dan Dosen
`````
SELECT Mahasiswa.nim, Mahasiswa.nama, Mahasiswa.jk, Dosen.nama AS "Dosen PA"
FROM Mahasiswa INNER JOIN Dosen ON Dosen.kd_ds = Mahasiswa.kd_ds;
`````
Output :
![J1](https://github.com/SamuelTindaon/MTSQL5/assets/147571483/ea062d7a-f0ad-4886-8433-134065290893)

- LEFT JOIN table Mahasiswa dan Dosen
`````
SELECT Mahasiswa.nim, Mahasiswa.nama, Mahasiswa.jk, Dosen.nama AS "Dosen PA"
FROM Mahasiswa LEFT JOIN Dosen ON Dosen.kd_ds = Mahasiswa.kd_ds;
`````
Output:
![J2](https://github.com/SamuelTindaon/MTSQL5/assets/147571483/1fac1f7a-4162-45e3-a504-5acec8f99415)

- JOIN table JadwalMengajar, Dosen, dan Matakuliah
`````
SELECT Matakuliah.kd_mk, Matakuliah.nama, Matakuliah.sks, Dosen.nama AS "Dosen Pengampu"
FROM JadwalMengajar
LEFT JOIN Matakuliah ON JadwalMengajar.kd_mk = Matakuliah.kd_mk
LEFT JOIN Dosen ON JadwalMengajar.kd_ds = Dosen.kd_ds;
`````
Output:
![J3](https://github.com/SamuelTindaon/MTSQL5/assets/147571483/7f0a62c2-6e01-4983-a69e-5cae0ca19103)

- JOIN table JadwalMengajar, Dosen, dan Matakuliah
`````
SELECT Matakuliah.kd_mk, Matakuliah.nama, Matakuliah.sks, Dosen.nama AS "Dosen Pengampu", JadwalMengajar.hari, JadwalMengajar.jam, JadwalMengajar.ruang
FROM JadwalMengajar
LEFT JOIN Matakuliah ON JadwalMengajar.kd_mk = Matakuliah.kd_mk
LEFT JOIN Dosen ON JadwalMengajar.kd_ds = Dosen.kd_ds;
`````
Output :
![J4](https://github.com/SamuelTindaon/MTSQL5/assets/147571483/63562883-dabe-4a00-8bda-8b04739566c9)

- JOIN tabel KRSMahasiswa, Mahasiswa, Matakuliah, dan Dosen
`````
SELECT Mahasiswa.nim, Mahasiswa.nama AS "nama", Dosen.nama AS "Dosen PA", Matakuliah.nama AS "Matakuliah", Matakuliah.sks, Dosen.nama AS "Dosen Pengampu"
FROM KRSMahasiswa
JOIN Mahasiswa ON KRSMahasiswa.nim = Mahasiswa.nim
JOIN Matakuliah ON KRSMahasiswa.kd_mk = Matakuliah.kd_mk
JOIN Dosen ON KRSMahasiswa.kd_ds = Dosen.kd_ds;
`````
Output :
![J5](https://github.com/SamuelTindaon/MTSQL5/assets/147571483/eda1429c-f9d5-41c8-83dc-3b1f83cd18fa)

## SELESAI <img align="center" alt="Ikhsan-Python" height="40" width="45" src="https://em-content.zobj.net/source/microsoft-teams/337/student_1f9d1-200d-1f393.png"> <img align="center" alt="Ikhsan-Python" height="40" width="45" src="https://em-content.zobj.net/thumbs/160/twitter/348/flag-indonesia_1f1ee-1f1e9.png"
