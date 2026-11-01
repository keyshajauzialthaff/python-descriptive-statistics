# python-descriptive-statistics
# Modul Statistik Deskriptif Python: Ukuran Pemusatan dan Penyebaran Data

Repositori ini berisi *package* atau modul Python sederhana yang dikembangkan untuk melakukan perhitungan statistika deskriptif secara otomatis, mencakup **ukuran pemusatan** dan **ukuran penyebaran data**. Proyek ini dibuat untuk mempermudah analisis data numerik secara efisien dan akurat.

---

## Struktur Direktori

```text
.
├── ukuran_pemusatan.py     # Modul untuk menghitung ukuran pemusatan data
├── ukuran_penyebaran.py    # Modul untuk menghitung ukuran penyebaran data
├── python-descriptive-statistics.pdf 
└── README.md               # Dokumentasi proyek
```

---

## Fitur & Modul

### 1. Modul Pemusatan (`ukuran_pemusatan.py`)
* **Rata-rata (Mean):** Menghitung nilai tengah dari seluruh data.
* **Median:** Menentukan nilai tengah dari data yang telah diurutkan (mendukung jumlah data ganjil maupun genap).
* **Modus:** Menentukan nilai yang paling sering muncul dalam data.
* **Kuartil (Q1 & Q3):** Menghitung batas bawah (25%) dan batas atas (75%) distribusi data.

### 2. Modul Penyebaran (`ukuran_penyebaran.py`)
* **Nilai Minimum & Maksimum:** Menentukan batas terkecil dan terbesar dalam data.
* **Range (Rentang):** Selisih antara nilai maksimum dan minimum.
* **Varians:** Mengukur seberapa jauh data tersebar dari nilai rata-rata.
* **Standar Deviasi:** Akar kuadrat dari varians dalam satuan asli data.

---

## Panduan Penggunaan (*User Guide*)

Berikut adalah contoh cara mengimpor dan menggunakan modul ini dalam skrip Python atau Google Colab:

### 1. Import Modul
Pastikan file modul (`ukuran_pemusatan.py` dan `ukuran_penyebaran.py`) berada pada direktori yang sama atau dapat diakses melalui path sistem (`sys.path`).

```python
import ukuran_pemusatan
import ukuran_penyebaran
import random

# Membuat data numerik acak sebagai contoh
data = [random.randint(10, 100) for _ in range(10)]
print("Data:", data)
```

### 2. Memanggil Fungsi Ukuran Pemusatan
```python
print("Rata-rata:", ukuran_pemusatan.mean(data))
print("Median:", ukuran_pemusatan.median(data))
print("Modus:", ukuran_pemusatan.modus(data))
print("Q1:", ukuran_pemusatan.kuartil(data, 1))
print("Q3:", ukuran_pemusatan.kuartil(data, 3))

# Atau menggunakan fungsi agregasi ringkasan
print(ukuran_pemusatan.ukuran_pemusatan(data))
```

### 3. Memanggil Fungsi Ukuran Penyebaran
```python
print("Nilai Minimum:", ukuran_penyebaran.nilai_minimum(data))
print("Nilai Maksimum:", ukuran_penyebaran.nilai_maksimum(data))
print("Range:", ukuran_penyebaran.rentang(data))
print("Varians:", ukuran_penyebaran.varians(data))
print("Standar Deviasi:", ukuran_penyebaran.standar_deviasi(data))

# Atau menggunakan fungsi agregasi ringkasan
print(ukuran_penyebaran.ukuran_penyebaran(data))
```
