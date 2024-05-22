# Instalasi MysQL

## Menggunakan termux

1. Buka Aplikasi Termux
2. Ketik "termux-setup-storage"
3. Ketik izinkan/allow access
4. Lakukan update atau upgrade paket. Ketik "pkg update && upgrade -y"
5. jika ada informasi untuk melanjutkan instalasi ketik "y"
6. Hasil aplikasi mariadb dengan mengetik "pkg install mariadb"
7. Ketika proses berhenti dan ada pilihan "y/n" ketik saja "y" untuk melanjutkan proses penginstalan
8. ketik "mysqld_safe" untuk memberi keamanan.
9. Ketik CNTRL+Z agar bisa ngesave datanya.

# Referensi Link Vidio YouTube

https://youtu.be/dmhJQ4zs_WY?si=yLCNgx8ZNHbEbFDx

# QUERY

Perintah `mysql -u root` digunakan untuk masuk ke client MySQL dengan menggunakan nama pengguna "root". Ini akan memungkinkan Anda untuk terhubung ke server MySQL dan mengeksekusi perintah SQL atau mengelola basis data yang terhubung dengan akun "root".

## HASIL
![[Screenshot_20240504_203335.jpg]]
## ANALISIS

Perintah mysql -u root digunakan untuk mengakses server MySQL menggunakan akun pengguna "root" dari baris perintah (command line). Analisis dari perintah ini akan tergantung pada apa yang ingin Anda ketahui atau lakukan setelah masuk ke dalam server MySQL dengan akun "root".

## Kesimpulan

Perintah "mysql -u root" digunakan untuk masuk ke dalam server database MySQL menggunakan pengguna (user) "root". Dengan demikian, Anda akan dapat mengakses dan mengelola database MySQL menggunakan hak akses penuh yang dimiliki oleh pengguna root.

# Insert

## Insert 1 Data

### Struktur

```mysql
insert into nama_table
    values ("nilai1","nilai2","nilai3","nilai4");
```

### Contoh

```mysql
insert into pelanggan
     values (1,"hansar","hans",0895333405540);
```

### Hasil 

![Insert 1 data](satudata.jpg)

### Analisis

- `INSERT INTO karyawan` : Ini menentukan nama tabel dimana data akan dimasukkan, dalam hal ini, "karyawan".
    
- `VALUES ("1", "ardiansya", "ardi", "0895333405540")`: Ini menentukan nilai yang akan dimasukkan ke dalam setiap kolom tabel. Nilai yang diberikan adalah untuk kolom sesuai urutan kemunculannya di tabel.
    
- 1 untuk kolom pertama,
    
- "hansar" untuk kolom kedua,
    
- "hans" untuk kolom ketiga,
    
- 0895333405540 untuk kolom keempat.
    

Akan menyisipkan baris baru ke dalam tabel "karyawan" dengan nilai yang ditentukan.

### Kesimpulan

Kesimpulan dari perintah `INSERT INTO pelanggan VALUES (1, "hansar", "hans", "0895333405540");` adalah data karyawan dengan ID 1, nama "ardiansya", nama panggilan "ardi", dan nomor telepon "0895333405540" telah dimasukkan ke dalam tabel karyawan.

## Insert >1 Data

### Struktur

```mysql
insert into nama_table 
     values ("nilai1","nilai2","nilai3","nilai4"),
("nilai1","nilai2","nilai3","nilai4"),
("nilai1","nilai2","nilai3","nilai4");
```

### Contoh

```mysql
insert into pelanggan
    values (2,"farhan","far",08431279465),
(3,"fadhilamir","fadil",08846379542),
(4,"alfazari","raihan",08613452764);
```

### Hasil

![[Screenshot_20240504_205738.jpg]]
### Analisis 

- Perintah: `INSERT INTO karyawan`
- Data yang dimasukkan:
    - Set 1: ("2654", "farhan", "far", "089753627153")
    - Set 2: ("2541", "raihan", "han", "08527383654")
    - Set 3: ("2331", "fadhil", "fadil", "08964321759")
- Tabel Tujuan: `karyawan`
- Kolom yang diisi:
    - `id_pelanggan`: Nilai dari kolom ini adalah "2654", "2541", dan "2331" untuk masing-masing set data.
    - `nama_depan`: Nilai dari kolom ini adalah "farhan", "raihan", dan "fadhil" untuk masing-masing set data.
    - `nama_belakang`: Nilai dari kolom ini adalah "far", "han", dan "fadil" untuk masing-masing set data.
    - `no_telp`: Nilai dari kolom ini adalah "089753627153", "08527383654", dan "08964321759" untuk masing-masing set data.

### Kesimpulan

Adalah bahwa query tersebut berhasil memasukkan tiga baris data baru ke dalam tabel pelanggan dengan informasi yang terperinci mengenai setiap karyawan, termasuk ID, nama depan, nama belakang, dan nomor telepon mereka.

## Menyebut Kolom

### Struktur

```mysql
insert into nama_table
    (kolom1,kolom2) values ("nilai1","nilai2");
```

### Contoh

```mysql
insert into pelanggan
(nama_depan,id_pelanggan) values ("agus","5");
```

### Hasil

![insert Lebih kecil](lebihkecil.jpg)

### Analisis

- `INSERT INTO pelanggan`: Ini adalah pernyataan SQL yang menunjukkan bahwa kita ingin menyisipkan data ke dalam tabel bernama `karyawan`.
    
- `(nama_depan, nama_belakang)`: Bagian ini menentukan kolom-kolom di mana data akan dimasukkan. Dalam hal ini, kolom yang ditentukan adalah `nama_depan` dan `nama_belakang`.
    
- `VALUES ("agus", "5")`: Ini adalah nilai yang ingin dimasukkan ke dalam kolom yang telah ditentukan sebelumnya. `"agus"` akan dimasukkan ke dalam kolom `nama_asli`, dan `"5"` akan dimasukkan ke dalam kolom `nama_belakang`.
    

Jadi, secara keseluruhan, query ini akan menambahkan sebuah baris baru ke dalam tabel `pelanggan` dengan nilai `"agus"` untuk kolom `nama_depan` dan nilai `"5"` untuk kolom `nama_belakang`.

### Kesimpulan

Query ini merupakan sebuah perintah SQL untuk memasukkan data baru ke dalam tabel `pelanggan`. Data yang dimasukkan adalah `nama_depan "agus"` dan `nis_karyawan "5".`

# Update (data)

## Struktur

```mysql
update nama_tabel set nama_kolom1"nilai1" where nama_kolom2"nilai2;
```

## Contoh

```mysql
update pelanggan set no_telp="086451334044" where nama_belakang="4";
```

## Hasil

![Update](update.jpg)

## Analisis

- `UPDATE pelanggan`: Bagian ini menentukan tabel yang akan diperbarui, yaitu "karyawan" dalam hal ini.
    
- `SET no_telp="086451334044"`: Bagian ini menetapkan nilai kolom "no_telp" menjadi "086451334044" untuk record yang sesuai dengan kondisi yang ditentukan pada klausa WHERE.
    
- `WHERE nama_belakang="4"`: Bagian ini menentukan kondisi yang harus dipenuhi oleh catatan agar dapat diperbarui. Dalam hal ini, memperbarui record dimana nilai pada kolom "nis_karyawan" sama dengan "4".

## Kesimpulan

sebuah perintah SQL untuk mengubah nilai kolom nama_depan menjadi "hansar" di dalam tabel karyawan dimana nama_belakang memiliki nilai "4". Kesimpulannya, perintah tersebut bertujuan untuk memperbarui data karyawan dengan nama_belakang tertentu dengan no_telp "086451334044".

# Delete (Hapus baris data)

## Struktur

```mysql
DELETE FROM nama_tabel WHERE nama_kolom"nilai";
```

## Contoh

```mysql
DELETE FROM pelanggan WHERE id_pelanggan="3";
```

## Hasil

![[Screenshot_20240504_213116.jpg]]

## Analisis

**Perintah:** `DELETE FROM pelanggan`

- Ini adalah perintah untuk menghapus data dari tabel "karyawan".

**Kondisi WHERE:** `id_pelanggan=3

- Ini adalah klausa WHERE yang menentukan kriteria untuk baris-baris yang akan dihapus. Dalam hal ini, baris akan dihapus jika nilai kolom "nis_karyawan" sama dengan 3.

**Tabel:** `pelanggan`

- Ini adalah nama tabel yang akan dihapus barisnya.

## Kesimpulan

Perintah SQL di atas menghapus baris data dari tabel "pelanggan" di mana nilai kolom "id_pelanggan" sama dengan "3". Kesimpulannya, program ini digunakan untuk menghapus informasi pelanggan dengan nomor identitas "3" dari basis data.

# Hapus Tabel

## Struktur

```mysql
drop table nama_table;
```

## Contoh

```mysql
drop table pelanggan;
```

## Hasil

![Hapus](hapus.jpg)

## Analisis

"drop table pelanggan;" adalah tentang perintah SQL untuk menghapus tabel bernama "pelanggan" dari database.

1. **Drop Table**: Ini adalah perintah SQL yang digunakan untuk menghapus tabel dari database.
    
2. **Pelanggan**: Ini adalah nama tabel yang akan dihapus.
    

Jadi, secara keseluruhan, query tersebut akan menghapus tabel bernama "pelanggan" dari database yang sedang digunakan. Dengan melakukan ini, semua data yang ada dalam tabel tersebut akan dihapus dan struktur tabelnya akan dihapus dari database.

## Kesimpulan

Query "DROP TABLE pelanggan;" akan menghapus tabel bernama "pelanggan" dari database. Ini adalah perintah SQL yang digunakan untuk menghapus tabel beserta semua data yang terkait dengan tabel tersebut dari database. Proses ini bersifat permanen, artinya setelah tabel dihapus, data yang ada di dalamnya tidak dapat dikembalikan lagi kecuali jika backup telah dibuat sebelumnya.






