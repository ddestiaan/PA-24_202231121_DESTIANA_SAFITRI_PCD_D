# TEORI CANNY DAN CONTOUR DETECTION


## ABSTRAK
Karena teknologi pengukuran 3D telah banyak digunakan dalam industri manufaktur, deteksi tepi dalam gambar kedalaman memainkan peran penting dalam aplikasi visi komputer . Dalam makalah ini, kami telah mengusulkan proses deteksi tepi dalam gambar kedalaman berdasarkan penghalusan berbasis gambar dan operasi morfologi . Dalam metode ini kami telah menggunakan prinsip penyaringan Median , yang memiliki fitur terkenal untuk properti pelestarian tepi . Deteksi tepi dilakukan berdasarkan prinsip deteksi Tepi Canny dan diimprovisasi dengan operasi morfologi , yang direpresentasikan sebagai kombinasi erosi dan dilatasi. Kemudian, kami membandingkan hasil kami dengan beberapa metode yang ada dan menunjukkan bahwa metode ini menghasilkan hasil yang lebih baik. Namun, metode ini bekerja dalam aplikasi multiframe dengan framerate yang efektif. Dengan demikian, teknik ini akan membantu mendeteksi tepi dengan kuat dari gambar kedalaman dan berkontribusi untuk mempromosikan aplikasi dalam gambar kedalaman seperti deteksi objek, segmentasi objek, dan lainnya.

Deteksi kontur adalah langkah lanjutan yang sering mengikuti deteksi tepi, dengan tujuan untuk mengidentifikasi batas-batas bentuk dan struktur dalam citra. Metode deteksi kontur, seperti algoritma Suzuki dan Abe, sering digunakan untuk mengikuti dan mendefinisikan kontur yang telah diidentifikasi oleh algoritma Canny. Kontur yang terdeteksi dapat digunakan dalam berbagai aplikasi, mulai dari pengenalan objek hingga pemetaan fitur dalam citra.

### Kata Kunci : Canny Edge Detection, Deteksi Tepi, Deteksi Kontur, Pengolahan Citra, Visi Komputer, Ekstraksi Fitur

## PROSES algoritma
### CANNY EDGE DETECTION
 - Proses algoritma deteksi Canny Edge :
1. Smoothing : Untuk menghilangkan noise pada gambar, dilakukan operasi smoothing atau blurring.

2. Menemukan gradien : Setelah memperoleh gradien gambar, tepian harus ditandai hanya pada area di mana besaran besar diperoleh.

3. Penekanan non-maksimum : Hanya nilai maksimum lokal yang harus dianggap sebagai tepi.

4. Ambang batas ganda : Tepi prospektif ditentukan oleh ambang batas ganda.

5. Pelacakan tepi dengan histeresis : Setelah menekan semua tepi yang tidak terhubung ke tepi yang sangat pasti atau kuat, tepi tersebut akan dianggap sebagai tepi akhir.

- Proses algoritma deteksi CONTOUR

1. Deteksi objek
2. Segmentasi gambar
3. Menggambar Kontur
4. Pengolahan Lanjutan (Opsional)

## POINT
1. Canny Edge Detection adalah metode deteksi tepi yang efektif melalui proses pengurangan noise, perhitungan gradien, penekanan non-maximum, dan penerapan ambang batas ganda.
2. Deteksi Kontur mengidentifikasi batas objek yang terdeteksi dan memberikan informasi untuk analisis lebih lanjut, seperti pengenalan bentuk dan pemetaan fitur.
3. Kombinasi kedua teknik ini mendukung berbagai aplikasi dalam pengolahan citra, memberikan alat yang kuat untuk ekstraksi fitur dan analisis visual.

## KESIMPULAN
Secara keseluruhan, Canny Edge Detection dan deteksi kontur adalah komponen penting dalam pengolahan citra modern. Canny Edge Detection memberikan dasar yang kuat untuk deteksi tepi yang akurat, sedangkan deteksi kontur memperluas analisis dengan menyoroti batas-batas objek dan fitur-fitur penting dalam citra. Kombinasi kedua teknik ini memungkinkan pengembangan solusi yang lebih baik dan lebih efektif dalam berbagai bidang aplikasi teknologi, dari visi komputer hingga pemantauan lingkungan.

## JURNAL TERKAIT
https://ieeexplore.ieee.org/abstract/document/6885761/
https://ieeexplore.ieee.org/abstract/document/5557884/

## Deployment

To deploy this project run

```bash
  npm run deploy
```


# UTS_PCD_202231121_LAPORAN

import cv2 // mengimport opencv pada phyton
import matplotlib.pyplot as plt //mengimpor modul pyplot dari pustaka Matplotlib, untuk mennampilkan plot 
import numpy as np //mengimpor pustaka NumPy sebagai np
## Appendix

Any additional information goes here

