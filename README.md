# <i>Face Mask Detection</i> (Deteksi Masker Muka)
<p align="center">
  <img src="https://github.com/Soedirman-Machine-Learning/face-mask-detection/blob/main/logo-md1png.png" width="256" height="256">
  <br>
  <b>Logo Aplikasi Deteksi Masker Muka</b>
</p>

## Penjelasan Singkat
Aplikasi ini dibuat untuk melakukan deteksi pemakaian masker muka secara <i>real-time</i> menggunakan metode <i>deep learning</i>. Program dalam proyek ini menggunakan kombinasi antara algoritma CNN (<i>Convolutional Neural Network</i>) dan algoritma deteksi wajah. Program CNN dibuat menggunakan infrastruktur <i>Google Colaboratory</i> dengan bahasa pemrograman <i>Python</i> dan menggunakan <i>Framework Keras</i> dan TensorFlow yang kemudian disimpan dalam bentuk <i>file Jupyter Notebooks</i> “.ipynb”. File dari program tersebut disimpan ke layanan repositori <i>web development</i> pada <i>Platform Github</i>.
<i>Dataset</i> pelatihan dan validasi disimpan pada <i>Github</i> dengan dua macam kelas (with_mask dan without_mask) yang didapatkan dari Github milik Chandrikadeb7 (https://github.com/chandrikadeb7/Face-Mask-Detection/tree/master/dataset). Jumlah <i>dataset</i> yang digunakan yaitu 3835 dengan rincian 1916 gambar berkelas <i>with_mask</i> dan 1919 <i>without_mask</i>. Sedangkan <i>dataset</i> pengujian yang terdapat pada file "face-detector.zip".
Program klasifikasi dengan algoritma CNN menggunakan dua macam arsitektur, yaitu arsitektur MobileNetV2 dan VGG16Net. Sedangkan untuk algoritma deteksi wajah menggunakan <i>caffe model</i> SSD <i>ResNet10</i> dan <i>library</i> MTCNN.

Setelah dilakukannya validasi, model dari hasil pengujian tersebut dapat disimpan dan dikonversi ke dalam bentuk <i>file Tensorflow Lite</i> ".tflite". File tersebut nantinya digunakan sebagai model yang dapat diimpor ke <i>Android Studio</i> yang tentunya juga mengimpor <i>library tensorflow</i> pada build.gradle di dalam <i>project Android Studio</i>. Kemudian dibuat aplikasi Android untuk deteksi masker muka dengan menggunakan fasilitas kamera pada perangkat <i>Smartphone Android</i>.

Pengujian dilakukan pada dua media yaitu pada infrastruktur Google Colaboratory dan pada aplikasi Android.

## Pelatihan dan Pembuatan Model pada <i>Google Colaboratory</i>
1. Klik salah satu file Jupyter Notebooks (.ipynb) pada repositori ini
2. Klik ikon "Open with Colab"
3. Masuk ke <i>Google Colab</i> dengan akun Google Anda
4. Klik menu "Runtime" kemudian pilih "Run All" atau tekan <b>Ctrl+F9</b> pada keyboard
5. Tunggu prosesnya hingga selesai (sekitar 5 sampai 10 menit, tergantung koneksi internet dan spesifikasi komputer Anda)
6. Unduh model (.tflite) yang sudah didapat dari proses pelatihan
7. Model tersebut nantinya dapat digunakan pada aplikasi Android.

## <i>Video</i> Hasil Pelatihan dan Pengujian pada <i>Google Colaboratory</i>
Dapat dilihat pada <i>link</i> berikut : 

## Aplikasi <i>Android</i>
Karena ukuran <i>file</i> yang hanya dapat diunggah pada <i>Github</i> maksimal 25 MB maka untuk ukuran <i>file</i> yang lebih besar dari 25 MB disimpan di penyimpanan <i>Google Drive</i>.
1. Model <i>TensorFlow Lite</i> dapat diunduh di <i>link</i> berikut : 
2. Aplikasi <i>Android</i>-nya dapat diunduh pada <i>link</i> : https://github.com/Soedirman-Machine-Learning/face-mask-detection/blob/main/aplikasi%20android/Face%20Mask%20Detection/apk/Deteksi-Masker-Muka-DL.apk

## Penggunaan Aplikasi Android
### Menggunakan Kamera
1. Download aplikasinya di dalam folder Output pada repositori ini. Pada halaman : https://github.com/Soedirman-Machine-Learning/face-mask-detection/blob/main/aplikasi%20android/Face%20Mask%20Detection/apk/Deteksi-Masker-Muka-DL.apk
2. Buka Aplikasi Deteksi Masker Muka kemudian pilih menu "DETEKSI".
3. Setelah terbuka menu tersebut arahkan kamera ke obyek wajah yang akan dideteksi (jarak kamera dengan obyek dapat mencapai 150 cm).
4. Hasil prediksi dan label akan muncul secara <i>real-time</i> dalam persentase (% diurutkan dari yang tertinggi). Persentase tertinggi merupakan hasil prediksi yang paling mendekati/mirip.
5. Waktu <i>inference time</i> pada setiap ponsel dapat berbeda. Pada ponsel Mi A1, <i>inference time</i> terbaik yaitu pada 110 ms sehingga dapat dikatakan bahwa hasil prediksi akurat.



### Informasi Aplikasi
1. Buka Aplikasi
2. Klik menu "TENTANG"
3. Terbuka informasi dari aplikasi
