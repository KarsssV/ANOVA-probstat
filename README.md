# ANOVA

## Pengantar ANOVA (Analysis of Variance)

**ANOVA (Analysis of Variance)** adalah metode statistik yang digunakan untuk menguji apakah terdapat perbedaan **rata-rata** dari dua kelompok atau lebih. ANOVA sangat berguna dalam **eksperimen atau penelitian komparatif** di mana kita ingin mengetahui pengaruh suatu variabel terhadap hasil atau outcome.

### Intuisi Dasar

Alih-alih membandingkan kelompok satu per satu (dengan uji-t yang berisiko meningkatkan Type I Error), ANOVA memungkinkan kita menguji **semua kelompok secara bersamaan**, kemudian dilanjutkan (jika perlu) dengan **post-hoc test** seperti Tukey HSD untuk mengetahui kelompok mana yang berbeda.

### Asumsi ANOVA

1. **Independensi**: Data antar kelompok bersifat independen.
2. **Normalitas**: Data dalam masing-masing kelompok terdistribusi normal.
3. **Homoskedastisitas**: Varians antar kelompok relatif sama.

---

## Jenis-Jenis ANOVA

### 1. One-Way ANOVA (ANOVA Satu Arah)

#### Deskripsi:
Digunakan ketika kita ingin menguji pengaruh **satu variabel kategorikal (faktor)** terhadap satu variabel numerik (respon).

#### Contoh:
Menguji apakah **jenis pupuk** (Organik, Kimia, Campuran) memengaruhi **tinggi tanaman**.

#### Model:

![Screenshot 2025-06-12 150846](https://github.com/user-attachments/assets/2ee20579-f51a-42a6-8a05-a6a5332e48c6)

---

### 2. Two-Way ANOVA (ANOVA Dua Arah)

#### Deskripsi:
Digunakan ketika kita ingin menguji pengaruh **dua variabel kategorikal (faktor A dan B)** terhadap satu variabel numerik.

#### Contoh:
Mengukur pengaruh **jenis pupuk** dan **jenis tanaman** terhadap **tinggi tanaman**.

#### Interaksi:
Two-way ANOVA juga bisa mengevaluasi **interaksi antara dua faktor** — apakah efek salah satu faktor tergantung pada level faktor lainnya.

#### Model:

![Screenshot 2025-06-12 151157](https://github.com/user-attachments/assets/e0a0d73f-3a81-4b3a-8e9d-06d8f94c8f60)

---

### 3. Repeated Measures ANOVA

#### Deskripsi:
Digunakan ketika **pengukuran dilakukan berulang pada subjek yang sama**, misalnya pengukuran mingguan terhadap pasien.

#### Contoh:
Mengukur tingkat stres seseorang setelah terapi selama 3 minggu berturut-turut.

#### Perbedaan dengan One-Way ANOVA:
- Subjek **tidak independen** antar waktu → korelasi perlu diperhitungkan.
- Biasanya memerlukan struktur data **long format**.

---

### 4. MANOVA (Multivariate ANOVA)

#### Deskripsi:
Perluasan dari ANOVA ketika terdapat **lebih dari satu variabel dependen**.

#### Contoh:
Mengukur pengaruh jenis diet terhadap **berat badan** dan **kadar kolesterol** secara bersamaan.

## Studi Kasus
Contoh studi kasus dapat dilihat pada link berikut ini:

[ANOVA-Colab](https://colab.research.google.com/drive/1M_FVmONHZm7K9naaBKl0rBhBBNNhAdgg?usp=sharing) 

---

## Catatan Tambahan

| Tipe ANOVA         | Faktor Independen | Faktor Interaksi | Variabel Dependen | Repeated Measure |
|--------------------|-------------------|------------------|-------------------|------------------|
| One-Way ANOVA      | 1                 | ❌               | 1                 | ❌               |
| Two-Way ANOVA      | 2                 | Opsional         | 1                 | ❌               |
| Repeated ANOVA     | 1 (atau lebih)    | ❌               | 1                 | ✅               |
| MANOVA             | ≥1                | Opsional         | ≥2                | ❌               |

---

## Referensi

- Montgomery, D. C. (2020). *Design and Analysis of Experiments*
- McDonald, J. H. (2014). *Handbook of Biological Statistics*
- [SciPy Documentation – ANOVA](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.f_oneway.html)
- [Statsmodels Documentation](https://www.statsmodels.org/stable/anova.html)

---


