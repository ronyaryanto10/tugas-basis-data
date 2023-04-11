# Tugas-Basis-Data

1. Buat sebuah database dengan nama latihan2!
``` 
CREATE DATABASE latihan1;
```
![bdata 1](https://user-images.githubusercontent.com/115356128/229334957-bac06184-b49b-4fd3-b0c4-f241e0881d68.png)
![bdatas 1](https://user-images.githubusercontent.com/115356128/229594312-acff43e8-3d15-43be-a38e-6b16341393c0.png)


2. Buat sebuah tabel dengan nama biodata (nama, alamat) didalam
database latihan1!
```
CREATE TABLE siswa (nama VARCHAR(100), alamat TEXT);
```
![bdatas 2](https://user-images.githubusercontent.com/115356128/229595191-3753c350-57ad-47ae-a877-d87314700bc2.png)


3. Tambahkan sebuah kolom keterangan (varchar 15), sebagai kolom
terakhir!
```
ALTER TABLE siswa ADD COLUMN keterangan varchar(15) AFTER alamat;
```
![bdatas 3](https://user-images.githubusercontent.com/115356128/229597145-eff6bd8e-3036-485a-8773-8aff59a7f55a.png)


4. Tambahkan kolom id (int 11) di awal (sebagai kolom pertama)!
```
ALTER TABLE siswa ADD COLUMN id int(11) First;
```
![bdatas4](https://user-images.githubusercontent.com/115356128/229598116-7598a5c7-a14a-4ff6-b503-039f6d140c1a.png)


5. Sisipkan sebuah kolom dengan nama phone (varchar 15) setelah
kolom alamat!
```
ALTER TABLE siswa ADD COLUMN phone varchar(15) after alamat;
```
![bdatas 5](https://user-images.githubusercontent.com/115356128/229598786-4eb06698-c012-4dd3-b0c7-e7c1ddf9c2c0.png)


6. Ubah tipe data kolom id menjadi char(11)!
```
ALTER TABLE siswa MODIFY COLUMN id VARCHAR(11);
```
![bdatas 6](https://user-images.githubusercontent.com/115356128/229599451-b87eaf7c-1875-4dd1-b90b-632e43b60803.png)


7. Ubah nama kolom phone menjadi hp (varchar 20)!
```
ALTER TABLE siswa CHANGE COLUMN phone hp varchar(20);
```
![bdatas 7](https://user-images.githubusercontent.com/115356128/229600016-7bedd0da-b4a6-47c9-a7ea-ccff74239c21.png)


8. Tambahkan kolom email setelah kolom hp
```
ALTER TABLE siswa ADD COLUMN email text after hp;
```
![bdatas 8](https://user-images.githubusercontent.com/115356128/229600459-677b3f99-2f8c-46dc-8c87-d88a4d4e80df.png)


9. Hapus kolom keterangan dari tabel!
```
alter table siswa drop keterangan;
```
![bdatas 9](https://user-images.githubusercontent.com/115356128/229600871-754a8080-c1b6-45c8-ab50-1f703d5fcd7e.png)


10. Ganti nama tabel menjadi data_mahasiswa!
```
alter table siswa rename data_mahasiswa;
```
![bdatas 10](https://user-images.githubusercontent.com/115356128/229601653-07aabf6a-03d2-4c0d-bc4c-2bb2997c8ac0.png)


11. Ganti nama field id menjadi nim!
```
ALTER TABLE data_mahasiswa CHANGE COLUMN id nim varchar(11);
```
![bdatas 11](https://user-images.githubusercontent.com/115356128/229602818-8f1dcfc4-8fc6-42af-a378-ce20fdfb9e73.png)


12. Jadikan nim sebagai PRIMARY KEY!
```
ALTER TABLE data_mahasiswa ADD PRIMARY KEY(nim);
```
![bdatas 12](https://user-images.githubusercontent.com/115356128/229603322-447124dd-198f-4a7f-930d-e765c5ef803e.png)


13. Jadikan kolom email sebagai UNIQUE KEY
```
ALTER TABLE data_mahasiswa ADD CONSTRAINT email unique KEY(email);
```
![bdatas 13](https://user-images.githubusercontent.com/115356128/229603650-d7cb191a-6229-46a3-af59-af1678a85361.png)


14. Hasil akhir

![bdata 14](https://user-images.githubusercontent.com/115356128/229335067-6f9423e3-aa30-4d59-8326-7fe6d6739f6e.png)


# Evaluasi dan pertanyaan
1. Apa maksud dari int (11)?
```
int (11) nunjukkan bahwa kolom memiliki tipe data bilangan bulat (integer) dengan ukuran 11 digit 
```

2. Ketika kita melihat struktur tabel dengan perintah desc, ada kolom Null yang
berisi Yes dan No. Apa maksudnya ?
```
Jika kolom "Null" adalah "YES", itu berarti kolom tersebut diizinkan untuk memiliki nilai NULL.

Jika kolom "Null" adalah "NO", maka kolom tersebut tidak diizinkan untuk memiliki nilai NULL
```
