# Backup dan Restore Database MySQL

## Deskripsi
Project ini berisi langkah-langkah melakukan backup dan restore database MySQL menggunakan Command Prompt (CMD) pada XAMPP. Database yang digunakan adalah database **koperasi**.

## Tujuan
- Melakukan backup database MySQL.
- Mengembalikan database dari file backup.
- Memahami penggunaan perintah `mysqldump` dan `mysql`.

## Tools
- XAMPP
- MySQL/MariaDB
- Command Prompt (CMD)

## Backup Database

Masuk ke direktori MySQL:

```cmd
cd C:\xampp\mysql\bin
```

Lakukan backup database:

```cmd
mysqldump -u root -p koperasi > D:\Backup\koperasi.sql
```

Hasil backup akan tersimpan pada:

```text
D:\Backup\koperasi.sql
```

## Restore Database

Restore file backup ke database `db_restore`:

```cmd
mysql -u root -p -v db_restore < D:\Backup\koperasi.sql
```

## Verifikasi

Masuk ke MySQL:

```cmd
mysql -u root -p
```

Pilih database:

```sql
use db_restore;
```

Tampilkan tabel:

```sql
show tables;
```

Cek data:

```sql
select * from simpanan;
```

## Hasil

Database **koperasi** berhasil dibackup ke file `koperasi.sql` dan berhasil direstore ke database `db_restore`. Seluruh tabel dan data dapat digunakan kembali dengan baik.

## Kesimpulan

Backup dan restore database MySQL merupakan langkah penting untuk menjaga keamanan data. Dengan menggunakan `mysqldump` dan `mysql`, proses pencadangan serta pemulihan database dapat dilakukan dengan mudah melalui Command Prompt.

## Author

Asroful Awlya
