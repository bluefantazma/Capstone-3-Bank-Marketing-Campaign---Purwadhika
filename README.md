**<p style="font-size:20px;">Bank Marketing Campaign Model</p>**

**Business Problem Understanding**

Bank X adalah salah satu bank yang menawarkan produk simpanan, pinjaman dan lain-lain kepada nasabah. saat ini bank X sedang membutuhkan analisa terhadap customer base-nya untuk membuat program marketing yang tepat sasaran.

**Problem Statement**

Program marketing yang tidak tepat sasaran dapat menimbulkan kerugian antara lain biaya pemasaran yang terbuang lebih besar, serta kerugian jangka panjang akibat tidak mampunya bank untuk mengakuisisi nasabah yang tepat sasaran.

**Goals**

Tujuan dari analisis dan modeling ini adalah untuk mengetahui profil nasabah yang memiliki kemungkinan lebih tinggi untuk menempatkan dananya di bank (deposit). Dengan adanya analisis modeling yang akurat, bank dapat mengalokasikan anggaran promosi dengan lebih efisien untuk menyasar nasabah yang memiliki profil dengan kemungkinan tertinggi untuk menempatkan dana.

**Analytic Approach:**

Untuk melakukan hal tersebut, kita akan mencoba untuk membangun sebuah model untuk memprediksi nasabah yang cendrung tertarik untuk menempatkan dana.
Metode yang dilakukan adalah supervised learning karena datanya sudah memiliki label, dalam hal ini adalah penempatan dana.

Adapun metode supervised learning yang digunakan adalah jenis klasifikasi yang akan membantu perusahaan untuk dapat menganalisis efektivitas program pemasaran sebelumnya dengan memeriksa hal-hal antara lain:
- jumlah / berapa kali nasabah dihubungi
- waktu kontak terakhir dilakukan
- hasil program sebelumnya
- respon calon nasabah.

- **Metric Evaluation**

Sasaran analisis adalah sebagai berikut: 

0: Tidak (Tidak berkenan untuk menempatkan dana) 

1: Ya (bermaksud untuk membuka rekening dana)

**Type I Error | False Positive** : ketika sistem memprediksi minat nasabah untuk menempatkan dana, namun pada kenyataannya, mereka tidak bermaksud melakukannya, hal tersebut berarti program pemasaran sia-sia karena nasabah tersebut memiliki kecenderungan untuk tidak menempatkan dana.

**Type II Error | False Negative** : ketika sistem memprediksi bahwa nasabah tidak tertarik untuk menempatkan dana, namun pada kenyataannya, mereka ingin menempatkan dana, hasilnya adalah bahwa bank akan kehilangan potensi keuntungan dari nasabah tersebut.

**Kesimpulan**
==============

**Precision dan Recall**: Precision untuk kelas 1 (71%) lebih tinggi daripada recall untuk kelas 1 (62%), yang menunjukkan bahwa model lebih baik dalam memprediksi bahwa nasabah akan menempatkan dana, tetapi sering kali melewatkan nasabah yang sebenarnya bermaksud menempatkan dana (Type II Error lebih tinggi).

**F1-Score**: F1-score untuk kedua kelas cukup seimbang, menunjukkan bahwa model memiliki kinerja yang cukup baik secara keseluruhan, meskipun ada ruang untuk perbaikan.

**Accuracy:** Akurasi 70% menunjukkan kinerja yang cukup baik, tetapi model masih bisa ditingkatkan terutama untuk meningkatkan recall pada kelas 1.

**Type I Error dan Type II Error:** Tingginya Type II Error (false negatives) berarti bank mungkin kehilangan peluang dari nasabah yang sebenarnya tertarik menempatkan dana. Di sisi lain, Type I Error (false positives) berarti ada beberapa usaha pemasaran yang sia-sia untuk nasabah yang tidak berminat.


**Contoh Simulasi**
====

Misalkan Bank memiliki target nama 1000 orang yang telah diproses menggunakan model ini, dan 1 nama diasumsikan memakan biaya Rp10.000 untuk menghubunginya (biaya pulsa). Model memiliki Type I error sebesar 23%. Maka jumlah biaya yang mungkin terbuang adalah:

23% x 1.000 (nasabah) x 10.000 (rupiah) = 2.300.000

Sedangkan apabila bank salah memilih nama nasabah yang seharusnya dapat melakukan pembukaan rekening namun tidak dihubungi, kerugiannya adalah sebagai berikut, dengan asumsi keuntungan yang diterima (misal dari biaya rekening bulanan sebesar 15.000 tiap nasabah selama 1 bulan)
Model memiliki Type II error sebesar 37%, maka jumlah keuntungan yang mungkin tidak jadi didapatkan adalah:

Potensi Pendapatan = 37% x 1000 (nasabah) x 15000 (rupiah) x 12 (bulan) = 66.600.000
Biaya pemasaran = 37% x 1000 (nasabah) x 10000 (rupiah) = 3.700.000
Potensi Pendapatan yang tidak jadi didapat = 62.900.000

**Kesimpulan**
==============

**Precision dan Recall**: Precision untuk kelas 1 (71%) lebih tinggi daripada recall untuk kelas 1 (62%), yang menunjukkan bahwa model lebih baik dalam memprediksi bahwa nasabah akan menempatkan dana, tetapi sering kali melewatkan nasabah yang sebenarnya bermaksud menempatkan dana (Type II Error lebih tinggi).

**F1-Score**: F1-score untuk kedua kelas cukup seimbang, menunjukkan bahwa model memiliki kinerja yang cukup baik secara keseluruhan, meskipun ada ruang untuk perbaikan.

**Accuracy:** Akurasi 70% menunjukkan kinerja yang cukup baik, tetapi model masih bisa ditingkatkan terutama untuk meningkatkan recall pada kelas 1.

**Type I Error dan Type II Error:** Tingginya Type II Error (false negatives) berarti bank mungkin kehilangan peluang dari nasabah yang sebenarnya tertarik menempatkan dana. Di sisi lain, Type I Error (false positives) berarti ada beberapa usaha pemasaran yang sia-sia untuk nasabah yang tidak berminat.


**Contoh Simulasi**
====

Misalkan Bank memiliki target nama 1000 orang yang telah diproses menggunakan model ini, dan 1 nama diasumsikan memakan biaya Rp10.000 untuk menghubunginya (biaya pulsa). Model memiliki Type I error sebesar 23%. Maka jumlah biaya yang mungkin terbuang adalah:

23% x 1.000 (nasabah) x 10.000 (rupiah) = 2.300.000

Sedangkan apabila bank salah memilih nama nasabah yang seharusnya dapat melakukan pembukaan rekening namun tidak dihubungi, kerugiannya adalah sebagai berikut, dengan asumsi keuntungan yang diterima (misal dari biaya rekening bulanan sebesar 15.000 tiap nasabah selama 1 bulan)
Model memiliki Type II error sebesar 37%, maka jumlah keuntungan yang mungkin tidak jadi didapatkan adalah:

Potensi Pendapatan = 37% x 1000 (nasabah) x 15000 (rupiah) x 12 (bulan) = 66.600.000
Biaya pemasaran = 37% x 1000 (nasabah) x 10000 (rupiah) = 3.700.000
Potensi Pendapatan yang tidak jadi didapat = 62.900.000
