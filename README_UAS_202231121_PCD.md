
# UAS_PCD_202231121_PRAKTIKUM

import cv2 // mengimport opencv pada phyton
import matplotlib.pyplot as plt //mengimpor modul pyplot dari pustaka Matplotlib, untuk mennampilkan plot 

img = cv2.imread('desti.jpg') //untuk membaca dan memuat citra dari file dengan nama 'desti.jpg'

cv2.imshow("Menampilkan Gambar Tepi", img) // fungsi dari OpenCV yang digunakan untuk menampilkan citra dalam sebuah jendela dan diberikan nama "Menampilkan Gambar Tepi"
cv2.waitKey(0) // fungsi yang menunggu input dari keyboard,membuat jendela tetap terbuka dan tidak langsung tertutup setelah ditampilkan.
cv2.destroyAllWindows() //fungsi yang menutup semua jendela yang dibuka oleh OpenCV.

gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY) //parameter yang menentukan bahwa konversi dari BGR (format warna OpenCV) ke grayscale dilakukan
blurred = cv2.GaussianBlur(gray, (5, 5), 1.4) //menerapkan filter Gaussian untuk mengurangi noise pada citra.
contours, hierarchy = cv2.findContours(edges, cv2.RETR_TREE, cv2.CHAIN_APPROX_SIMPLE) //pengambilan kontur yang mengambil semua kontur dan membuat hierarki lengkap.
contour_image = image.copy()
cv2.drawContours(contour_image, contours, -50, (0, 255, 0), 5) //membuat salinan dari citra asli untuk menggambar kontur.

##Menampilkan Gambar Output Gamabar 1
plt.figure(figsize=(10, 5)) //digunakan untuk membuat sebuah figure baru dengan ukuran tertentu dalam Matplotlib

plt.subplot(1, 2, 1) //membuat subplot baru dalam figure Matplotlib,subplot ini adalah yang pertama dalam grid 1x2 (satu baris, dua kolom.
plt.title('Gambar Asli') //menambahkan judul pada subplot
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB)) //digunakan untuk menampilkan citra dalam subplot.

plt.subplot(1, 2, 2) //membuat subplot baru dalam figure Matplotlib,subplot ini adalah yang pertama dalam grid 1x2 (satu baris, dua kolom dan urutan gambar 2
plt.title('Canny Edge Detection') //menambahkan judul pada subplot, dengan nama Canny Edge Detection.
plt.imshow(edges, cmap='gray') //menampilkan citra dalam subplot

plt.show() //menampilkan figure yang berisi semua subplot yang telah ditambahkan

##Menampilkan Gambar Output 2
plt.figure(figsize=(15, 5)) //Membuat figure baru dengan ukuran 15 inci lebar dan 5 inci tinggi. Ini akan menjadi kanvas untuk menampilkan subplot

plt.subplot(1, 3, 1) //Mengatur subplot pertama dalam grid 1x3 (satu baris dengan tiga kolom dengan urutan gambar pertama)
plt.title('Gambar Asli') //Menambahkan judul "Gambar Asli"
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB)) //Menampilkan gambar asli yang telah diubah dari format BGR ke RGB. Matplotlib menggunakan format RGB, sedangkan OpenCV menggunakan BGR

plt.subplot(1, 3, 2)// Mengatur subplot kedua dalam grid 1x3 dengan urutan gambar ke 2
plt.title('Canny Edge Detection') //Menambahkan judul "Canny Edge Detection"
plt.imshow(edges, cmap='gray') //Menampilkan hasil deteksi tepi dengan metode Canny dalam skala keabuan (cmap='gray')

plt.subplot(1, 3, 3) //Mengatur subplot ketiga dalam grid 1x3 dengan urutan gambar ke3
plt.title('Countours Detection') //Menambahkan judul "Countours Detection" 
plt.imshow(cv2.cvtColor(contour_image, cv2.COLOR_BGR2RGB)) //Menampilkan gambar dengan kontur yang telah digambar di atasnya, diubah dari format BGR ke RGB

plt.show() //Menampilkan semua subplot dalam satu figure








## Demo

Insert gif or link to demo

