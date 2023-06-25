Penanggung jawab : Muhammad Rifaldi Dwimahendra (F55120049)  

Nama anggota kelompok :  
Rizky Kaligis (F55120036)   
Moh. Raihan Dirga Putra Lamadjido (F55120045)  
Bernadeth Putri Meo (F55120047)  
Muhammad Rifaldi Dwimahendra (F55120049)  
Ghea Erlita Tahendung (F55120050)  

Penjelasan Program :
Program ini adalah program Deep Learning yang menggunakan TensorFlow dan Keras untuk membuat dan melatih model hingga dapat digunakan untuk memprediksi person / nama dan gendernya.
pada program ini, digunakan drive.mount() untuk menghubungkan ke dataset yang berada pada google drive, kemudian image ImageDataGenerator untuk augmentasi data, kemudian model dibuat 
dengan teknik Deep Learning menggunakan arsitektur Deep Convolutional Neural Network (DCNN) pada TensorFlow dan Keras dengan dua output yaitu person_output dan Gender_output.
kemudian model dikompilasi dengan optimizer, loss function dan matrics. kemudian ditambahkan callback yang berfungsi untuk menyimpan model dengan val accuracy tertinggi saat pelatihan model
dan melakukan early stop jika selama 20 epoch val accuracy tidak mendapat peningkatan. model dilatih dengan jumlah langkah yang akan dilakukan pada setiap epoch pelatihan ama dengan total jumlah data gambar dibagi dengan ukuran batch
dan jumlah langkah yang akan dilakukan pada setiap epoch evaluasi sama seperti pada jumlah langkah pada setiap epoch pelatihan.  

link dataset : https://drive.google.com/drive/folders/1-aSo27sCkvpv1t0Chi1UhLGCWLt7TSr5?usp=drive_link

How to run :
Import library yang diperlukan menggunakan drive.mount('/content/gdrive').
Tentukan direktori data train dan data validasi.
buat generator data train dan data validasi .
konfigurasi model DCNN (VGG16).
Tentukan layer output untuk klasifikasi gender dan klasifikasi person.
Kompilasi model dengan loss function, optimizer dan evaluation matrics yang sesuai.
Tentukan callback untuk menyimpan model terbaik dan menghentikan pelatihan jika terjadi overfitting.
Latih model menggunakan fungsi fit() dengan data dari generator data train dan generator data validasi,tentukan jumlah epoch train dan epoch validasi.
Tampilkan grafik akurasi menggunakan Matplotlib.
load data yang akan menjadi data untuk testing / predict, preproces data citra sebelum dilakukan predict dan lakukan testing dengan model yang telah dilatih
menggunakan fungsi model.predict()  dan tampilkan hasil predict berupa citra dan caption hasil predict menggunakan matplotlib.pyplot.

