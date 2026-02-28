Nama        : Intania Mustofa  
No Presensi : 145  
Keterangan  : Tugas Week 2 Differential Expression Analysis (GEO2R)  
GEO accession : GSE18090

<p align="center"><b>“Gene Expression Profiling During Early Acute Febrile Stage of Dengue Infection Can Predict The Disease Outcome”</b></p>

### A. Pendahuluan

<p>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Infeksi dengue merupakan penyakit akibat virus dengue yang dapat berkembang
menjadi bentuk ringan (Dengue Fever/DF) maupun berat (Dengue Hemorrhagic
Fever/DHF). Pada fase akut awal (early acute febrile stage), perubahan ekspresi gen pada
sel darah perifer dapat mencerminkan respons imun tubuh serta berpotensi menjadi
biomarker prediktif terhadap luaran klinis.
</p>

<p>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Dataset GSE18090 yang tersedia di database Gene Expression Omnibus (GEO) berisi
data ekspresi gen pasien dengue pada fase akut awal. Analisis ini bertujuan untuk
mengidentifikasi gen-gen yang mengalami perubahan ekspresi signifikan (Differentially
Expressed Genes/DEGs) serta menginterpretasikan kaitannya dengan kondisi biologis
infeksi dengue.
</p>

### B. Metode
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1\) Dataset

<p>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Dataset yang digunakan adalah GSE18090 dari Gene Expression Omnibus (GEO)
dengan judul "<i>Gene Expression Profiling During Early Acute Febrile Stage of Dengue
Infection Can Predict The Disease Outcome</i>". Dataset ini berisi data ekspresi gen dari
sampel darah pasien yang terinfeksi virus dengue pada fase demam akut awal.
Platform: Affymetrix Human Genome U133 Plus 2.0 Array
</p>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2\) Pembagian kelompok

<p>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Sampel dibagi menjadi dua kelompok untuk analisis komparatif:
</p>

- Group 1: DF + DHF
- Group 2: ND (Kontrol)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3\) Parameter

<p>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Analisis differential expression dilakukan menggunakan GEO2R dengan parameter
sebagai berikut:
</p>

a. Metode statistik: limma (Linear Models for Microarray Data)  
b. Multiple testing correction: Benjamini-Hochberg (False Discovery Rate/FDR)
Kriteria signifikansi:
- Adjusted p-value (adj.P.Val) < 0.05
- Log fold change (logFC) > 1 atau < -1 (menunjukkan perubahan ekspresi
minimal 2x lipat)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4\) Replikasi Analisis

<p>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Untuk memastikan reproducibility dan konsistensi hasil, analisis dilakukan sebanyak 3
kali replikasi dengan langkah-langkah yang identik:
</p>

- Replikasi 1: Analisis awal dengan parameter standar
- Replikasi 2: Pengulangan analisis dengan parameter yang sama untuk verifikasi
- Replikasi 3: Konfirmasi akhir untuk memastikan konsistensi pola ekspresi gen
Ketiga replikasi diharapkan menunjukkan gen-gen signifikan yang konsisten dengan
arah perubahan ekspresi (up-regulated atau down-regulated) yang sama.

### C. Hasil dan interpretasi
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1. Hasil Analisis Differential Expression

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Berdasarkan analisis GEO2R dengan kriteria adj.P.Val < 0.05, &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ditemukan 7 probe sets yang menunjukkan perubahan ekspresi &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;signifikan.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Tabel 1. Differentially Expressed Genes dari analisis GEO2R
<img width="984" src="https://raw.githubusercontent.com/Intania3110/Tugas_2/main/Differentially%20Expressed%20Genes%20dari%20analisis%20GEO2R.png">

Keterangan: LogFC dengan warna merah menunjukkan up-regulated genes, warna biru menunjukkan
down-regulated genes.

#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. Ringkasan Statistik DEG
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Dari analisis yang dilakukan, diperoleh ringkasan sebagai berikut:
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Total gen signifikan (adj.P.Val < 0.05): 7 probe sets

- Up-regulated genes (logFC > 1): 3 probe sets

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1\) 236191_at (logFC = 2.40)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2\) POLR1A/222704_at (logFC = 1.96)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3\) MLEC/200616_s_at (logFC = 1.51)

- Down-regulated genes (logFC < -1): 4 probe sets

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1\) 1559394_a_at (logFC = -2.60)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2\) OLFM1/205591_at (logFC = -2.02)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3\) MIB2/228261_at (logFC = -1.00)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4\) FAM134A/222129_at (logFC = -0.98)

#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3. Interpretasi Biologis

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Up regulated genes:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;a. POLR1A (RNA polymerase I subunit A): Gen ini terlibat dalam transkripsi rRNA.
Peningkatan ekspresi POLR1A dapat mengindikasikan peningkatan aktivitas
sintesis protein sebagai respons terhadap infeksi virus, yang diperlukan untuk
produksi protein imun dan respons seluler terhadap stress.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;b. MLEC (Malectin): Protein ini terlibat dalam quality control protein di retikulum
endoplasma (ER). Peningkatan ekspresinya dapat menunjukkan aktivasi ER stress
response akibat replikasi virus dengue yang intensif dalam sel host.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Down regulated genes:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;a. OLFM1 (Olfactomedin 1): Meskipun fungsi spesifiknya dalam respons imun masih
belum sepenuhnya dipahami, OLFM1 telah dikaitkan dengan regulasi pertumbuhan
sel dan diferensiasi. Penurunan ekspresinya dapat berkaitan dengan modulasi
respons imun atau perubahan dalam homeostasis seluler selama infeksi dengue.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;b. MIB2 (Mindbomb E3 Ubiquitin Protein Ligase 2): Gen ini terlibat dalam jalur
ubiquitinasi protein dan regulasi Notch signaling. Penurunan ekspresinya dapat
mempengaruhi respons inflamasi dan diferensiasi sel imun.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;c. FAM134A (Family with Sequence Similarity 134 Member A): Protein ini terlibat
dalam reticulophagy (degradasi selektif retikulum endoplasma melalui autophagy).
Penurunan ekspresinya dapat berkaitan dengan strategi virus untuk menghindari
degradasi atau mengeksploitasi jalur autophagic untuk replikasi.

#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4. Konsistensi Replikasi
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Analisis yang dilakukan sebanyak tiga kali replikasi menunjukkan hasil yang konsisten.
Gen-gen yang teridentifikasi signifikan muncul dengan pola yang sama pada setiap
replikasi, dengan arah perubahan ekspresi up and down regulation, nilai statistic dan
logFC yang konsisten.

### D. Kesimpulan
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Analisis differential expression menggunakan GEO2R pada dataset GSE18090 berhasil
mengidentifikasi 7 probe sets yang menunjukkan perubahan ekspresi signifikan (adj.P.Val
< 0.05) pada pasien dengue fase demam akut awal. Dari jumlah tersebut, 3 gen mengalami
up-regulation dan 4 gen mengalami down-regulation.  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Gen-gen yang teridentifikasi terlibat dalam berbagai proses biologis penting termasuk
stress response (MLEC, POLR1A), immune modulation (MIB2), dan autophagy regulation
(FAM134A). Perubahan ekspresi gen-gen ini mencerminkan kompleksitas respons host
terhadap infeksi virus dengue dan berpotensi sebagai biomarker untuk memprediksi
outcome penyakit. Analisis yang dilakukan dengan tiga kali replikasi menunjukkan
konsistensi hasil yang baik, mengindikasikan reliabilitas temuan ini. Signature ekspresi gen
pada fase awal infeksi dapat memberikan insight valuable untuk stratifikasi risiko pasien
dan memfasilitasi intervensi klinis yang lebih dini dan targeted.

<p align="center"><b>LAMPIRAN</b></p>

<img width="984" src="https://raw.githubusercontent.com/Intania3110/Tugas_2/main/Gambar_1.png">

<img width="984" src="https://raw.githubusercontent.com/Intania3110/Tugas_2/main/Gambar_2.png">
