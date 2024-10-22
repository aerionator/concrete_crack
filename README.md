# concrete_crack
Test CNN for Concrete Crack Images for Classification

Perbedaam Test Model Pertama vs Test Model Kedua

1. Input Image Size:
First Model: Resizes images ke 227x227.
Second Model: Resizes images ke 128x128.
Note: Ukuran gambar yang lebih kecil dapat mempercepat proses setiap epoch.

2. Batch Size:
First Model: Menggunakan batch size of 32.
Second Model: Menggunakan batch size of 64.
Note: Batch yang lebih besar dapat mempercepat training namun butuh memori yang lebih banyak.

3. Convolutional Layers:
First Model: Punya dua convolutional layers dengan filter 32 dan 64.
Second Model: Punya tiga convolutional layers dengan filter 16, 32, and 64.
Pooling Layers: Kedua model menggunakan MaxPooling2D setelah convolutional layer.

4. Fully Connected Layers:
First Model: Menggunakan satu dense layer dengan 64 unit.
Second Model: Menggunakan satu dense layer dengan 128 unit.

5. Dropout Layer:
First Model: Tidak menggunakan dropout layer.
Second Model: Menggunakan Dropout layer dengan rate 0.5 untuk mencegah terjadinya overfitting.

6. Optimizer & Learning Rate:
First Model: Menggunakan Adam optimizer (default).
Second Model: Menggunakan Adam optimizer dengan learning rate rendah yaitu 0.0001.

7. Callbacks:
First Model: Tidak menggunakan callbacks.
Second Model: Menggunakan EarlyStopping (untuk menghentikan training jika validation loss tidak membaik) dan ModelCheckpoint (untuk menyimpan model dengan performa terbaik berdasarkan validation loss).

8. Augmentation & Additional Layers:
Second Model: Menggunakan langkah augmentation seperti shear_range dan zoom_range (tidak digunakan di model pertama). 

9. Model Visualization:
First Model: Tidak menggunakan visualisasi untuk training dan validasi accuracy dan loss.
Second Model: Menggunakan visualisaisi untuk training accuracy dan loss.

10. Result :

First Model:
Dari epoch 1-10.
Tingkat accuracy maupun validasi accuracy tidak lebih dari 50%.
Tingkat loss dan validasi loss cukup tinggi yaitu 69%.
Setiap proses epoch memakan waktu setidaknya 30 menit.

Second Model:
Dari epoch 1-10.
Tingkat accuracy terus meningkat hingga 99%, begitu pula dengan validasi accuracy.
Tingkat loss terus menurun hingga 3%, sementara validasi loss mencapai sekitar 1%-4%.
Setiap proses epoch memakan waktu setidaknya 5-10 menit.
