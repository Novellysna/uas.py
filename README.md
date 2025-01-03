# Program Kalkulator sederhana
## Dokumentasi pembuatan program
https://youtube.com/shorts/1fwiqCNuDrY?si=8RGeCJ61y0AWC2VH

## flowchart 

```mermaid
flowchart TD
    A([Start]) --> B[Input Angka Pertama]
    B --> C[Input Angka Kedua]
    C --> D[Pilih Operasi]
    D --> E[Validasi Input]
    E --> F{Input Valid?}
    F -->|Tidak| B
    F -->|Ya| G[Lakukan Operasi]
    G --> H[Tampilkan Hasil]
    H --> I[Tanya Lanjutkan Perhitungan?]
    I -->|Ya| B
    I -->|Tidak| J([End])
```

## Penjelasan program
### 1. Class Operations: Kelas ini menangani operasi matematika dasar seperti penjumlahan, pengurangan, perkalian, dan pembagian. Setiap operasi disediakan sebagai metode statis.
### 2. Class InputValidation: Kelas ini digunakan untuk memvalidasi input dari pengguna, memastikan bahwa input yang diberikan adalah angka. Jika bukan angka, input akan ditolak.
### 3. Class Calculator: Kelas ini menangani alur kalkulator, termasuk meminta input pengguna, memilih operasi yang diinginkan, dan menampilkan hasil operasi.
### 4. Fungsi Main: Fungsi utama yang menjalankan program kalkulator. Pengguna akan diminta untuk memasukkan dua angka dan memilih operasi. Setelah selesai, pengguna dapat memilih untuk melakukan perhitungan lagi atau keluar.

## Fitur Program 
### 1. Validasi Input: Memastikan bahwa input yang dimasukkan oleh pengguna adalah angka yang valid.
### 2. Pilihan Operasi: Pengguna dapat memilih antara penjumlahan, pengurangan, perkalian, atau pembagian.
### 3. Looping: Program akan terus berjalan hingga pengguna memilih untuk keluar setelah menyelesaikan perhitungan.

## Demo program kalkulator sederhana

```python
def kalkulator():
    print("Selamat datang di Kalkulator Sederhana!")
    print("Pilih operasi yang ingin Anda lakukan:")
    print("1. Penjumlahan (+)")
    print("2. Pengurangan (-)")
    print("3. Perkalian (*)")
    print("4. Pembagian (/)")

    try:
        pilihan = int(input("Masukkan pilihan (1/2/3/4): "))

        if pilihan in [1, 2, 3, 4]:
            angka1 = float(input("Masukkan angka pertama: "))
            angka2 = float(input("Masukkan angka kedua: "))

            if pilihan == 1:
                hasil = angka1 + angka2
                print(f"Hasil dari {angka1} + {angka2} = {hasil}")
            elif pilihan == 2:
                hasil = angka1 - angka2
                print(f"Hasil dari {angka1} - {angka2} = {hasil}")
            elif pilihan == 3:
                hasil = angka1 * angka2
                print(f"Hasil dari {angka1} * {angka2} = {hasil}")
            elif pilihan == 4:
                if angka2 != 0:
                    hasil = angka1 / angka2
                    print(f"Hasil dari {angka1} / {angka2} = {hasil}")
                else:
                    print("Error: Pembagian dengan nol tidak diperbolehkan!")
        else:
            print("Pilihan tidak valid. Silakan coba lagi.")
    except ValueError:
        print("Input tidak valid. Harap masukkan angka.")

# Memulai program kalkulator
kalkulator()

```
## Output Program
```
PS C:\Users\novellysna\Desktop\New Delhi> & "C:/Users/novellysna/AppData/Local/Programs/Python/Python313/python.exe" "e:/program kalkulator sederhana uas"
Selamat datang di Kalkulator Sederhana!
Masukkan angka pertama: 5 
Masukkan angka kedua: 5

Pilih operasi:
1. Penjumlahan (+)
2. Pengurangan (-)
3. Perkalian (*)
4. Pembagian (/)
Masukkan pilihan (1/2/3/4): 3
```

## penjelasan output
Dengan struktur modular dan OOP ini, kalkulator menjadi lebih terorganisir dan mudah untuk dikembangkan lebih lanjut jika diperlukan. Anda bisa menambahkan lebih banyak fitur, seperti operasi matematika lainnya atau menyimpan riwayat perhitungan
