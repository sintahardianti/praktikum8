# Praktikum 8

### Nama : Sinta Hardianti Wijaya

### NIM : 312210342

### Kelas : TI.22.A3

## Soal Tugas Praktikum

<img width="607" alt="soal prak8" src="https://user-images.githubusercontent.com/115516473/206854662-00d4ad39-79d2-435d-849d-9f7bd13ac83d.png">

## > Buat dictionary kosong terlebih dahulu

```     mahasiswa = {} ```

## > Buat menu program utama

```
    def menu():
        print("\n")
        print("====================================================")
        print("      \t\t Program input nilai       ")
        print("====================================================\n")

        x = input("[(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar]: ")
        print("\n")

        if x == 'L':
            show()
        elif x == 'T':
            add()
        elif x == 'U':
            update()
        elif x == 'H':
            delete()
        elif x == 'C':
            search()
        elif x == 'K':
            print("==========================================================================")
            print('\n')
            print("> You exit the code                        ")
            print("\n")
            print("==========================================================================")

            exit()

        else:
            print("            KODE YANG ANDA MASUKKAN TIDAK VALID !!!!!!!!!!!")

    // Saya menggunakan perulangan while-true agar program terus berjalan hingga berhenti
    while True:
        menu()
  ```
  
  ## > Kode program untuk menambahkan data
  
  ```
      def add():
        print("Tambah Data")
        nama = input("Nama\t         : ")
        nim = input("NIM\t         : ")
        uts = int(input("Nilai UTS\t : "))
        uas = int(input("Nilai UAS\t : "))
        tugas = int(input("Nilai Tugas\t : "))
        akhir = (tugas * 30 / 100) + (uts * 35 / 100) + (uas * 35 / 100)
        mahasiswa[nama] = nim, tugas, uts, uas, akhir
   ```
   
   ## > Kode program untuk melihat data 
   
   ```
       def show():
        if mahasiswa.items():
            print("Daftar Nilai")
            print("=================================================================================")
            print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
            print("=================================================================================")
            i = 0
            for a in mahasiswa.items():
                i += 1
                print("| {no:2d} | {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} |      {5:6.2f} |"
                    .format(a[0][: 14], a[1][0], a[1][1], a[1][2], a[1][3], a[1][4], no=i))
            print("=================================================================================")

        else:
            print("Daftar Nilai")
            print("=================================================================================")
            print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
            print("=================================================================================")
            print("|                                TIDAK ADA DATA                                 |")
            print("=================================================================================")
   ```
   
   ## > Kode program untuk mengubah data
   
   ```
       def update():
        print("Ubah Data")
        nama = input("Masukkan Nama : ")
        if nama in mahasiswa.keys():
            nim = input("NIM\t : ")
            uts = int(input("Nilai UTS\t : "))
            uas = int(input("Nilai UAS\t : "))
            tugas = int(input("Nilai Tugas\t : "))
            akhir = (tugas * 30 / 100) + (uts * 35 / 100) + (uas * 35 / 100)
            mahasiswa[nama] = nim, tugas, uts, uas, akhir

        else:
            print("Nama tidak ditemukan ")
  ```
  
  ## > Kode program untuk menghapus data
  
  ```
      def delete():
        print("Hapus Data")
        nama = input("Masukkan Nama : ")

        if nama in mahasiswa.keys():
            del mahasiswa[nama]

        else:
            print("Nama tidak ditemukan")
  ```
  
  ## > Kode program untuk mencari data
  
  ```
      def search():
        print("Cari Data")
        a = input("Masukkan Nama : ")
        if a in mahasiswa.keys():
            print("===========================================================================")
            print("|      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir   |")
            print("===========================================================================")
            print("| {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} |     {5:6.2f} |"
                .format(a, mahasiswa[a][0], mahasiswa[a][1], mahasiswa[a][2], mahasiswa[a][3], mahasiswa[a][4]))
            print("===========================================================================")

        else:
            print("=================================================================================")
            print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
            print("=================================================================================")
            print("|                          DATA TIDAK DITEMUKAN                                 |")
            print("=================================================================================")
```
  
## > Outputnya :
  
  ![outputpraktikum8](https://user-images.githubusercontent.com/115516473/206898558-9d49c62e-1c46-407f-9c52-8caf95006f5c.png)

## T) untuk tambah data

![prak8-1](https://user-images.githubusercontent.com/115516473/206898919-079403c4-e7f0-420d-8c50-e63d75f206c3.png)

## L) untuk melihat data yang baru saja ditambahkan

![prak8-2](https://user-images.githubusercontent.com/115516473/206899032-1b77318b-bc11-4ec8-aec3-495d711f5bd5.png)

## H) untuk menghapus data 

![prak8-3](https://user-images.githubusercontent.com/115516473/206899110-56680759-2ae5-4e05-92ce-cd2f364b0b53.png)

data sudah terhapus

## C) untuk mencari data

![prak8-4](https://user-images.githubusercontent.com/115516473/206899243-118251f6-6e6c-44f5-a8ff-98d57cabccbc.png)

data tidak ditemukan karena tadi sudah dihapus

## K) untuk keluar dari program

![prak8-5](https://user-images.githubusercontent.com/115516473/206899320-7a829d7e-cdd7-4f9a-accb-f8703d02ce88.png)

## > Flowchartnya :

<img width="543" alt="flowchart prak8" src="https://user-images.githubusercontent.com/115516473/206899371-35df9579-e5b7-4412-8451-17aace56bc0a.png">

# Selesai
