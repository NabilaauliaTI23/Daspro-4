# Daspro-4
# Membuat fungsi untuk merekap barang
def rekap_barang():
    # Inisialisasi list untuk menyimpan barang
    daftar_barang = []

    # Loop untuk menginput nama dan harga beli setiap barang
    while True:
        nama_barang = input("Masukkan nama barang: ")
        harga_beli = int(input("Masukkan harga beli (dalam rupiah): "))

        # Menghitung harga jual (harga beli dikali 10/100)
        harga_jual = harga_beli * 10 / 100

        # Menambahkan informasi barang ke dalam list
        daftar_barang.append((nama_barang, harga_beli, harga_jual))

        # Menanyakan apakah ingin menambah barang lagi
        tambah_barang = input("Apakah Anda ingin menambah barang lagi? (y/n): ")
        if tambah_barang.lower() != 'y':
            break

    # Menampilkan rekapan list barang yang sudah dimasukkan
    print("Rekap Barang:")
    for barang in daftar_barang:
        print("Nama Barang:", barang[0])
        print("Harga Beli:", "Rp", barang[1])
        print("Harga Jual:", "Rp", barang[2])
        print()

# Memanggil fungsi rekap_barang
rekap_barang()
