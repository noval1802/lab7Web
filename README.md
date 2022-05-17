# Pembuatan Web Server dari Menu XAMPP

## Langkah Langkah Menggunakan XMPP Dengan Menggunakan Format Dokumen (.php)

### Menjalankan Web Server

Untuk menjalankan web server dari menu XAMPP Control

![xmpp](asset/img/xmppServer.png)

### Memulai PHP

Buat folder **lab7_php_dasar** pada root directory web server **(c:\xampp\htdocs)**.

![htdocs](asset/img/htdocs.png)
Kemudian untuk mengakses directory tersebut pada web server dengan mengakses URL: http://localhost/lab7_php_dasar/

![localhost](asset/img/localhost.png)

### PHP Dasar

Buat file baru dengan nama _dasar.php_ pada directory tersebut. Kemudian buat kode seperti berikut.

```php
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>PHP Dasar</title>
</head>
<body>
    <h1>Belajar PHP Dasar</h1>
    <?php
        echo "Hello world";
    ?>
</body>
</html>
```

Kemudian untuk mengakses hasilnya melali URL: http://localhost/lab7_php_dasar/dasar.php

![dasarPHP](asset/img/dasarPHP.png)

### Variable PHP

Menambahkan variable pada program.

```php
<?php
       $nim = "312010049";
       $nama = 'Abdul Aziz Anaoval';
       echo "NIM : " . $nim . "<br>";
       echo "Nama : $nama";
   ?>
```

![variablePHP](asset/img/variablePHP.png)

### predifine Variable $\_GET

```php
<?php
echo 'Selamat Datang ' . $_GET['nama'];
?>
```

Untuk mengaksesnya gunakan URL:
http://localhost/lab7_php_dasar/latihan2.php?nama=Noval

![predifineVariableGET](asset/img/predifineVariableGET.png)

### Membuat Form Input

```php
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Latihan 2 PHP</title>
</head>

<body>
    <h2>Form Input</h2>

    <form method="post">
        <label>Nama: </label>
        <input type="text" name="nama">
        <input type="submit" value="kirim">
    </form>
    <?php
    echo 'Selamat Datang ' . $_GET['nama'];
    ?>
</body>

</html>
```

![FormInput](asset/img/FormInput.png)

### Oprator

```php
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <?php
    $gaji = 1000000;
    $pajak = 0.1;
    $thp = $gaji - ($gaji * $pajak);
    echo "Gaji sebelum pajak = Rp. $gaji <br>";
    echo "Gaji yang dibawa pulang = Rp. $thp";
    ?>

</body>

</html>
```
![oprator_gaji](asset/img/oprator.png)

### Kondisi IF

```php
  <h2>Kondisi IF</h2>
    <?php
    $nama_hari = date("l");
    if ($nama_hari == "Sunday") {
        echo "Minggu";
    } elseif ($nama_hari == "Monday") {
        echo "Senin";
    } else {
        echo "Selasa";
    }
    ?>
```
![Kondisi_if](asset/img/Kondisi_if.png)

### Kondisi Switch

```php
<?php
    $nama_hari = date("1");
    switch ($nama_hari) {
        case "Sunday":
            break;
            echo "minggu";
            break;
        case "Monday":
            echo "Senin";
            break;
        case "Tuesday":
            echo "Selasa";
            break;
        default:
            echo "Sabtu";
    }
    echo"/$nama_hari";
    ?>
```
![Kondisi_Switch](asset/img/Kondisi_switch.png)

### Pengulangan For

```php
<?php
    echo "Perulangan 1 sampai 10 <br />";
    for ($i = 1; $i <= 10; $i++) {
        echo "Perulangan ke: " . $i . '<br />';
    }
    echo "Perulangan Menurun dari 10 ke 1 <br />";
    for ($i = 10; $i >= 1; $i--) {
        echo "Perulangan ke: " . $i . '<br />';
    }
    ?>
```
![Pengulangan_for](asset/img/Pengulangan_for.png)

### Pengulangan While 

```php
<?php
    echo "Perulangan 1 sampai 10 <br />";
    $i = 1;
    while ($i <= 10) {
        echo "Perulangan ke: " . $i . '<br />';
        $i++;
    }
    ?>
```
![Pengulangan_while](asset/img/Pengulangan_while.png)

### Pengulangan Dowhile

```php
 </h2>
    <?php
    echo "Perulangan 1 sampai 10 <br />";
    $i = 1;
    do {
        echo "Perulangan ke: " . $i . '<br />';
        $i++;
    } while ($i <= 10);
    ?>
```
![Pengulangan_dowhile](asset/img/Pengulangan_dowhile.png)

# Pertanyaan dan Tugas

Buatlah program PHP sederhana dengan menggunakan form input yang menampilkan nama, tanggal lahir dan pekerjaan. Kemudian tampilkan outputnya dengan menghitung umur berdasarkan inputan tanggal lahir. Dan pilihan pekerjaan dengan gaji yang berbeda-beda sesuai pilihan pekerjaan.
