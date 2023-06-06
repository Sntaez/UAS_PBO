# Ujian Akhir Semester PBO
Kelompok 14 :
* Merly Yuni Purnama    (G1A022006)
* Sinta Ezra Wati Gulo  (G1A022040)
* Anugrah Herianto      (G1A022068)

# Penjelasan Source Code
```py
import random # mengimpor modul random dari library 
import string # mengimpor modul string dari library
import tkinter as tk # mengimpor modul tkinter dan memberikan alias tk ke modul 
from tkinter import messagebox # mengimpor fungsi messagebox dari modul tkinter.
```
Kode di atas adalah kode untuk mengimport beberapa modul dan fungsi dari library tkinter. 
* Kode `import random` mengimpor modul random dari library Python. Modul ini berisi fungsi-fungsi yang berkaitan dengan angka acak (random number). Dengan mengimpor modul ini, kita dapat menggunakan fungsi-fungsi seperti `random.randint()` untuk menghasilkan angka acak. 
* Kode `import string` mengimpor modul string dari library Python. Modul ini berisi kumpulan fungsi-fungsi yang berkaitan dengan manipulasi string. Dengan mengimpor modul ini, kita dapat menggunakan fungsi-fungsi seperti `string.ascii_letters` atau `string.digits` untuk mendapatkan karakter alfabet atau angka.
* Kode `import tkinter as tk` mengimpor modul tkinter dan memberikan alias tk ke modul tersebut. Dimana tkinter adalah library standar Python untuk membuat antarmuka grafis (GUI). Dengan memberikan alias tk, kita dapat menggunakan tk sebagai prefix saat memanggil fungsi dan objek dari modul ini, misalnya `tk.Tk()` untuk membuat jendela utama aplikasi.
* Kode `from tkinter import messagebox` mengimpor fungsi messagebox dari modul tkinter. Fungsi messagebox digunakan untuk menampilkan kotak pesan pop-up dengan berbagai jenis pesan, seperti pesan informasi, peringatan, atau kesalahan kepada pengguna.

```py
def open_password_generator(): # deklarasi untuk sebuah fungsi membuka aplikasi password generator
    root.destroy() # memanggil metode destroy() pada objek root
    password_generator() # membuka jendela baru untuk menghasilkan password dengan memanggil fungsi
```
* Kode diatas adalah fungsi `open_password_generator()` untuk  menggabungkan langkah-langkah untuk menutup jendela utama aplikasi yang ada dan membuka jendela baru untuk menghasilkan password dalam aplikasi password generator.
* Kode `root.destroy()` yang memanggil metode `destroy()` pada objek root. root adalah objek utama dalam aplikasi GUI, yang telah dibuat sebelumnya menggunakan modul tkinter. Metode `destroy()` digunakan untuk menutup jendela utama aplikasi. Dengan memanggil `root.destroy()`, fungsi ini bertujuan untuk menutup jendela utama aplikasi sebelum membuka jendela baru.
* Kode `password_generator()` yang memanggil fungsi `password_generator()`. Tujuan dari pemanggilan ini adalah untuk membuka jendela baru yang khusus untuk menghasilkan password. Fungsi `password_generator()` kemungkinan besar akan menampilkan antarmuka pengguna atau melakukan operasi yang relevan dengan menghasilkan password secara interaktif.


    
    
    
