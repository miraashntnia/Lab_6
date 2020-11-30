```
                                                 MIRA SHINTANIA
                                                   312010290
                                                    TI.20.B2

```




# **Tugas Praktikum 6**
Membuat program dengan mengaplikasikan penggunaan fungsi yang akan menampikan daftar nilai mahasiswa, dengan ketentuan:
- Fungsi tambah() untuk menambah data
- Fungsi tampilkan() untuk menampilkan data
- Fungsi hapus(nama) untuk menghapus data berdasarkan nama
- Fungsi ubah(nama) untuk mengubah data berdasarkan nama
- Membuat Flowchart

## **Source Code**
Berikut source code lengkapnya: https://github.com/miraashntnia/Lab_6/blob/master/Tugas%20Praktikum%206.py

## **Penjelasan**

1. Membuat Dictionary dan Looping dengan menggunakan source code sebagai berikut:
```
dataMhs = {}                                                                                     ## Membuat Dictionary kosong
print("==================================================================")
print("|                  PROGRAM INPUT NILAI MAHASISWA                 |")
print("==================================================================")

while True:                                                                                      ## LOOPING AKTIF
    c = input("\nA)dd, E)dit, D)elete L)ist, Q)uit: ")                                           ## Membuat Menu
```

2. Membuat Fungsi **Tambah** untuk menambahkan data dengan source code sebagai berikut:
```
    if (c.lower() == 'a'):                                                                       ## MENU TAMBAH DATA
        print("\n=========================")
        print("| TAMBAH DATA MAHASISWA |")
        print("=========================")
        nama          = input("Masukkan Nama        : ")                                         ## Menginput Nama
        nim           = input("Masukkan NIM         : ")                                         ## Menginput NIM
        nilaiTugas    = int(input("Masukkan Nilai Tugas : "))                                    ## Menginput Nilai Tugas
        nilaiUts      = int(input("Masukkan Nilai UTS   : "))                                    ## Menginput Nilai UTS
        nilaiUas      = int(input("Masukkan Nilai UAS   : "))                                    ## Menginput Nilai UAS
        nilaiAkhir    = (0.30 * nilaiTugas) + (0.35 * nilaiUts) + (0.35 * nilaiUas)              ## Menghitung Nilai Akhir
        dataMhs[nama] = nim, nilaiTugas, nilaiUts, nilaiUas, nilaiAkhir                          ## Menambahkan data yang sudah diinput ke Dictionary
        print("\nData Berhasil Ditambahkan!")
```

3. Membuat Fungsi **Tampilkan** untuk menampilkan data dengan source code sebagai berikut:
```
    elif (c.lower() == 'l'):                                                                    ## MENU TAMPILKAN DATA
        if dataMhs.items():                                                                     ## Mengambil items dari Dictionary
            print("\n                      DAFTAR NILAI MAHASISWA                    ")
            print("==================================================================")
            print("| No |     Nama     |    NIM    | Tugas |  UTS  |  UAS  |  Akhir |")
            print("==================================================================")
            i = 0
            for x in dataMhs.items():
                i += 1
                print("| {6:2} | {0:12s} | {1:9s} | {2:5} | {3:5} | {4:5} | {5:6} |".format(x[0], x[1][0], x[1][1], x[1][2], x[1][3], x[1][4], i))  ## Format tabel
            print("==================================================================")
        else:
            print("\n                      DAFTAR NILAI MAHASISWA                    ")
            print("==================================================================")
            print("| No |     Nama     |    NIM    | Tugas |  UTS  |  UAS  |  Akhir |")
            print("==================================================================")
            print("|                          TIDAK ADA DATA!                       |")
            print("==================================================================")        ## Jika data masih kosong, akan muncul pesan tsb.
```

4. Membuat Fungsi **Hapus** untuk menhapus data berdasarkan nama dengan source code sebagai berikut:
```
    elif (c.lower() == 'd'):                                                                    ## MENU HAPUS DATA BERDASARKAN NAMA
        nama = input("Masukkan Nama:  ")                                                        ## Masukkan nama yang akan didelete
        if nama in dataMhs.keys():                                                              ## Mengambil keys dari Dictionary
            del dataMhs[nama]                                                                   ## Menghapus data yang dipilih
            print("Data Telah dihapus!")
        else:
            print("Data Mahasiswa Tidak Ada".format(nama))                                      ## Jika data tidak ditemukan, akan muncul perintah tsb.
```

5. Membuat Fungsi **Ubah** Untuk mengubah data berdasarkan nama dengan source code sebagai berikut:
```
    elif (c.lower() == 'e'):                                                                     ## MENU UBAH DATA BERDASARKAN NAMA
        print("\n=======================")
        print("| EDIT DATA MAHASISWA |")
        print("=======================")
        nama = input("Masukkan Nama: ")                                                          ## Cari nama yang akan diedit
        if nama in dataMhs.keys():                                                               ## Mengambil key dari Dictionary
            nim           = input("Masukkan NIM Baru         : ")                                ## Menginput NIM baru
            nilaiTugas    = int(input("Masukkan Nilai Tugas Baru : "))                           ## Menginput Nilai Tugas Baru
            nilaiUts      = int(input("Masukkan Nilai UTS Baru   : "))                           ## Menginput Nilai UTS Baru
            nilaiUas      = int(input("Masukkan Nilai UAS Baru   : "))                           ## Menginput Nilai UAS Baru
            nilaiAkhir    = (0.30 * nilaiTugas) + (0.35 * nilaiUts) + (0.35 * nilaiUas)          ## Menghitung Nilai Akhir Baru
            dataMhs[nama] = nim, nilaiTugas, nilaiUts, nilaiUas, nilaiAkhir                      ## Mengupdate data ke Dictionary
            print("\nData Berhasil Di Update!")
        else:                                                                                    
            print("Data tidak ditemukan!")                                                       ## Jika nama tidak ditemukan maka muncul perintah tsb.
```

6. Menu **Keluar** untuk keluar dari program dengan source code sebagai berikut:
```
    elif (c.lower() == 'q'):                                                                   ## MENU KELUAR
        print("\n Mira Shintania \n 312010290 \n TI.20.B.2")
        break                                                                                  ## Mengakhiri LOOPING

    else:
        print("Pilih menu yang tersedia: ")                                                    ## Jika menu yang dipilih tidak valid, akan muncul pesan tsb.
 ```
## **FLOWCHART**

![github](https://github.com/miraashntnia/Lab_6/blob/master/FLOWCHART.jpg)

## **Hasil Output**

- **Tambah Data**

![github](https://github.com/miraashntnia/Lab_6/blob/master/Hasil%20Output/MENU%20TAMBAH%20DATA.png)

- **Tampilkan Data**

![github](https://github.com/miraashntnia/Lab_6/blob/master/Hasil%20Output/MENU%20TAMPILKAN%20DATA.png)

- **Ubah Data Berdasarkan Nama**

![github](https://github.com/miraashntnia/Lab_6/blob/master/Hasil%20Output/MENU%20UBAH%20DATA%20BERDASARKAN%20NAMA.png)

- **Hapus Data Berdasarkan Nama**

![github](https://github.com/miraashntnia/Lab_6/blob/master/Hasil%20Output/MENU%20HAPUS%20DATA%20BERDASARKAN%20NAMA.png)

