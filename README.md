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

```py
def open_password_generator(): # deklarasi untuk sebuah fungsi membuka aplikasi password generator
    root.destroy() # memanggil metode destroy() pada objek root
    password_generator() # membuka jendela baru untuk menghasilkan password dengan memanggil fungsi

def password_generator(): # deklarasi untuk sebuah fungsi membuat jendela aplikasi password generator 
    
    def generate_password(): # deklarasi untuk sebuah fungsi dipanggil ketika tombol "Generate" dijepret oleh pengguna
        
        length = length_entry.get() # mengambil nilai yang dimasukkan oleh pengguna pada length_entry dan menyimpannya dalam variabel length
        try:
            length = int(length) # nilai length dikonversi menjadi integer 
            if length > 10: # memeriksa apakah panjang password yang dimasukkan oleh pengguna lebih besar dari 10
                messagebox.showerror("Error", "Panjang password maksimal adalah 10!")
            else:
                characters = string.ascii_letters + string.digits + string.punctuation # membuat string characters yang berisi kombinasi
                password = ''.join(random.choice(characters) for _ in range(length)) # menggunakan perulangan for untuk memilih karakter secara acak
                password_label.config(text="Password: " + password) # Mengatur teks label
        except ValueError:
            messagebox.showerror("Error", "Silahkan masukkan angka sebagai panjang password!")
    
    # Inisialisasi jendela utama (root) menggunakan tk.Tk()        
    root = tk.Tk()
    root.title("UAS PBO KELOMPOK 14 - Password Generator")

    # Background color
    root.configure(bg="black")

    # Header
    header_label = tk.Label(root, text="Welcome to Random Password Generator", font=("Times New Roman", 20), bg="black", fg="white")
    header_label.pack(pady=20)

    # Password Length
    length_frame = tk.Frame(root, bg="black") # Membuat objek frame 
    length_frame.pack() # Mengatur tata letak (layout) frame

    length_label = tk.Label(length_frame, text="Silahkan masukkan angka panjang password! : ", font=("Times New Roman", 10), bg="black", fg="white") # Membuat objek label
    length_label.pack(side=tk.LEFT, padx=10) # Mengatur tata letak (layout) label 

    length_entry = tk.Entry(length_frame, font=("Times New Roman", 10)) # Membuat objek Entry (length_entry) 
    length_entry.pack(side=tk.LEFT, padx=10) # Mengatur tata letak (layout) input field 

    # Generate Button
    generate_button = tk.Button(root, text="Generate", font=("Times New Roman", 10), bg="gray", command=generate_password)
    generate_button.pack(pady=10)

    # Password Display
    password_label = tk.Label(root, text="Password:", font=("Times New Roman", 14), bg="black", fg="white")
    password_label.pack(pady=10)

    # Kode ini menjalankan siklus utama aplikasi Tkinter
    root.mainloop()
```
Kode tersebut merupakan definisi dari fungsi `password_generator()`, yang bertanggung jawab untuk membuat jendela aplikasi pembuat password. Berikut adalah penjelasan untuk setiap baris kode dalam fungsi tersebut:
* `def password_generator()` bertujuan untuk membuat jendela aplikasi pembuat password.
* `def generate_password()` yang akan dipanggil ketika tombol "Generate" diklik oleh pengguna. Fungsi ini berisi logika untuk menghasilkan password secara acak.
* `length = length_entry.get()` akan mengambil nilai yang dimasukkan oleh pengguna pada `length_entry`, yaitu panjang password yang diinginkan, dan menyimpannya dalam variabel `length`.
* `length = int(length)` akan mengonversi nilai length menjadi integer. Hal ini dilakukan karena nilai yang diambil dari length_entry awalnya dalam bentuk string.
* `if length > 10: ... else: ...` akan memeriksa apakah panjang password yang dimasukkan oleh pengguna lebih besar dari 10. Jika lebih besar dari 10, maka akan muncul pesan kesalahan menggunakan `messagebox.showerror()`. Jika tidak, maka akan dilakukan proses pembuatan password.
* `characters = string.ascii_letters + string.digits + string.punctuation` akan membuat string characters yang berisi kombinasi dari huruf alfabet (besar dan kecil), angka, dan tanda baca.
* `password = ''.join(random.choice(characters) for _ in range(length))` akan menggunakan perulangan for untuk memilih karakter secara acak dari characters, sebanyak length kali. Kemudian, karakter-karakter tersebut digabungkan menjadi string password menggunakan metode `join()`.
* `password_label.config(text="Password: " + password)` akan mengatur teks dari `password_label` dengan menambahkan string "Password: " diikuti dengan nilai password.
* Inisialisasi jendela utama `(root)` dengan kode di bawah deklarasi fungsi adalah inisialisasi jendela utama aplikasi menggunakan `tk.Tk()`. Ini membuat objek root yang merupakan instance dari kelas Tk dari modul tkinter. Jendela utama ini akan menampilkan antarmuka aplikasi pembuat password.
* Pengaturan tampilan jendela utama yaitu pengaturan tampilan jendela utama, seperti memberikan judul jendela, mengatur warna latar belakang, dan menambahkan label serta tombol ke dalam jendela.
* `root.mainloop()` akan menjalankan siklus utama aplikasi Tkinter. Ini akan memperbarui dan menampilkan jendela aplikasi, serta menangani peristiwa yang terjadi di dalamnya.



    
    
    
