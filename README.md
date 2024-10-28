# Fungsi untuk menghitung total harga tiket
def hitung_harga_tiket():
    # Meminta input dari pengguna
    tipe_tiket = input("Masukkan tipe tiket (reguler/VIP): ").lower()
    status_member = input("Apakah Anda memiliki kartu member? (ya/tidak): ").lower()

    # Menentukan harga tiket berdasarkan tipe
    if tipe_tiket == "reguler":
        harga_tiket = 40000
    elif tipe_tiket == "vip":
        harga_tiket = 150000
    else:
        print("Tipe tiket tidak valid!")
        return  # Pastikan untuk mengembalikan dari fungsi jika tipe tidak valid
    
    # Menghitung diskon jika pengguna adalah member
    diskon = 0.2 if status_member == "ya" else 0
    total_harga = harga_tiket * (1 - diskon)

    # Menampilkan total harga
    print(f"Total harga yang harus dibayar: Rp{total_harga:.2f}")

# Memanggil fungsi
hitung_harga_tiket()
