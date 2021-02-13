# <i>Face Mask Detection</i> (Deteksi Masker Muka)
<p align="center">
  <img src="https://github.com/Soedirman-Machine-Learning/face-mask-detection/blob/main/logo-md1png.png" width="150" height="150">
  <br>
  <b>Logo Aplikasi Deteksi Masker Muka</b>
</p>

## Penjelasan Singkat
Aplikasi ini dibuat untuk melakukan deteksi pemakaian masker muka secara <i>real-time</i> menggunakan teknik <i>deep learning</i>. Program dalam proyek ini menggunakan kombinasi antara algoritma CNN (<i>Convolutional Neural Network</i>) dan algoritma deteksi wajah. Program CNN dibuat menggunakan infrastruktur <i>Google Colaboratory</i> dengan bahasa pemrograman <i>Python</i> dan menggunakan <i>Framework Keras</i> dan TensorFlow yang kemudian disimpan dalam bentuk <i>file Jupyter Notebooks</i> “.ipynb”. File dari program tersebut disimpan ke layanan repositori <i>web development</i> pada <i>Platform Github</i>.
<i>Dataset</i> pelatihan dan validasi disimpan pada <i>Github</i> dengan dua macam kelas (<i>with_mask</i> dan <i>without_mask</i>) yang didapatkan dari Github milik Chandrikadeb7 (https://github.com/chandrikadeb7/Face-Mask-Detection/tree/master/dataset). Jumlah <i>dataset</i> untuk pelatihan yaitu 3835 gambar dengan rincian 1916 gambar berkelas <i>with_mask</i> dan 1919 <i>without_mask</i>. Sedangkan <i>dataset</i> pengujian yang terdapat pada file "face-detector.zip" hasil dari kamera Mi A1 dan website https://unsplash.com/.
Program klasifikasi dengan algoritma CNN menggunakan dua macam arsitektur, yaitu arsitektur MobileNetV2 dan VGG16Net. Sedangkan untuk algoritma deteksi wajah menggunakan <i>caffe model</i> SSD <i>ResNet10</i> dan <i>library</i> MTCNN.

Setelah dilakukan validasi dan evaluasi, model dari hasil pengujian tersebut dapat disimpan dan dikonversi ke dalam bentuk <i>file Tensorflow Lite</i> ".tflite". File tersebut akan digunakan sebagai model untuk aplikasi <i>Android Studio</i> pada bagian folder <i>assets</i>, selain itu mengimpor <i>library tensorflow</i> dan <i>ML Kit Face Recognition</i> pada build.gradle di dalam <i>project Android Studio</i>. Kemudian dibuat aplikasi Android untuk deteksi masker muka dengan menggunakan fasilitas kamera pada perangkat <i>Smartphone Android</i>.

Pengujian dilakukan pada dua media yaitu pada infrastruktur <i>Google Colaboratory</i> dan pada aplikasi Android.

## Pelatihan dan Pembuatan Model pada <i>Google Colaboratory</i>
1. Klik salah satu file antara "Full_Face_Mask_Detection_MobileNetV2.ipynb" atau "Full_Face_Mask_Detection_VGG16Net.ipynb".
2. Klik ikon "Open with Colab"
3. Masuk ke <i>Google Colab</i> dengan akun Google Anda
4. Klik menu "Runtime" kemudian pilih "Run All" atau tekan <b>Ctrl+F9</b> pada keyboard
5. Tunggu prosesnya hingga selesai (sekitar 5 sampai 10 menit, tergantung koneksi internet dan spesifikasi komputer Anda)
6. Anda dapat juga melakukan <i>run</i> pada setiap <i>cell</i> atau baris yang ada agar dapat lebih memperhatikan prosesnya
6. Setelah selesai pelatihan, unduh model (.tflite) yang sudah didapat dari proses pelatihan
7. Model tersebut nantinya dapat digunakan pada aplikasi Android

## Pengujian Deteksi menggunakan Model pada <i>Google Colaboratory</i>
1. Setelah Anda sudah sampai pada bagian mengunduh model (.tflite). Anda dapat mencoba menggunakan model dengan melakukan deteksi.
2. Ada dua pilihan model deteksi wajah (SSD <i>ResNet10</i> dan <i>library</i> MTCNN)
3. Run setiap baris yang ada dan ikuti prosesnya, Anda akan mencoba deteksi pada
   a) Deteksi pada Gambar yang tersedia pada file "face-detector.zip"
   b) Deteksi secara <i>realtime</i> perframe
   c) Deteksi secara <i>realtime</i>
4. Nikmati dan amati proses pengujiannya, selamat mencoba!

## Aplikasi <i>Android</i>
<p align="center">
  <img src="https://github.com/Soedirman-Machine-Learning/face-mask-detection/blob/main/Aplikasi-Android.gif" width="240" height="427">
  <br>
  <b>Simulasi</b>
</p>

1. Model <i>TensorFlow Lite</i> dapat diunduh di <i>link</i> berikut : https://github.com/Soedirman-Machine-Learning/face-mask-detection/blob/main/mask_model.tflite
2. Aplikasi <i>Android</i>-nya dapat diunduh pada <i>link</i> : https://github.com/Soedirman-Machine-Learning/face-mask-detection/blob/main/aplikasi%20android/Face%20Mask%20Detection/apk/Deteksi-Masker-Muka-DL.apk

## Penggunaan Aplikasi Android
### Menggunakan Kamera
1. Download aplikasinya di dalam folder Output pada repositori ini. Pada halaman : https://github.com/Soedirman-Machine-Learning/face-mask-detection/blob/main/aplikasi%20android/Face%20Mask%20Detection/apk/Deteksi-Masker-Muka-DL.apk
2. Berikan izin kamera untuk aplikasi ini.
3. Buka Aplikasi Deteksi Masker Muka kemudian pilih menu "DETEKSI".
4. Deteksi dapat menggunakan kamera depan dan kamera belakang.
5. Setelah terbuka menu deteksi arahkan kamera ke obyek wajah yang akan dideteksi (jarak kamera dengan obyek dapat mencapai 150 cm).
6. Hasil prediksi dan label akan muncul secara <i>real-time</i> dalam persentase (% diurutkan dari yang tertinggi). Persentase tertinggi merupakan hasil prediksi yang paling mendekati/mirip.
7. Waktu <i>inference time</i> pada setiap ponsel dapat berbeda. Pada ponsel Mi A1, <i>inference time</i> terbaik yaitu pada 110 ms sehingga dapat dikatakan bahwa hasil prediksi akurat.

### Informasi Aplikasi
1. Buka Aplikasi
2. Klik menu "TENTANG"
3. Terbuka informasi dari aplikasi
