# Cache

Salah satu jenis memori pada komputer yang dimana data-datanya paling mungkin digunakan oleh CPU. Sekitar 80% kemungkinan akses memori oleh CPU dapat dipenuhi pada memori Cache.

Memori pada komputer dibuat secara hirarki, karena faktor biaya dan panas. Apabila memori komputer seluruhnya terbuat dari cache, maka akan sangat mahal dan mudah panas.

## Cache Mapping

### Direct Mapping

Main memory akan dibagi menjadi blok-blok yang seukuran dengan Cache System. Setiap index pada alamat Cache hanya boleh disimpan data dari Main Memory dengan index blok yang sama juga. Sebagai contoh:

index 1 pada cache hanya boleh disimpan data dari index 1 blok apapun main memory, dan index N pada cache hanya boleh disimpan data dari index N blok apapun main error.

Keunggulan dari Direct Mapping adalah kesederhanaannya.

Kelemahan dari Direct Mapping adalah ketika terdapat lebih dari 1 blok dengan indeks sama yang ingin menyimpan data pada cache memory. Sebagai contoh:

Apabila index **1** blok 1 main memory dan index **1** blok 2 ingin menyimpan pada cache memory, maka akan terjadi tabrakan data.

### Associative Mapping

Main memory dapat menyimpan data pada cache memory secara bebas tanpa dibatasi aturan-aturan tertentu.

Keunggulan dari Associative Mapping adalah menyelesaikan masalah dari Direct Mapping.

Kelemahan dari Associative Mapping adalah menyebabkan proses searching data pada Cache lebih lama.

### Set Associative Mapping

Mirip seperti Direct Mapping, hanya saja setiap indeks pada Cache Memory dapat menyimpan lebih dari 1 data. Hal ini dapat terwujud dengan membagi seluruh indeks cache memori menjadi beberapa set yang lebih kecil.

## Replacement Algorithm

Replacement Algorithm adalah algoritma pada Cache Memory yang digunakan untuk memilih data mana yang akan dibuang untuk membersihkan tempat agar data baru dapat masuk.

### Least Recently Used

Membuang data yang tidak digunakan paling lama

### Least Frequently Used

Membuang data yang paling jarang digunakan

### FIFO (First In First Out)

Membuang data paling tua dalam Cache

### LIFO (Last In First Out)

Membuang data paling muda dalam Cache

## Write Policy

Hubungan penyimpanan data antara CPU, Cache, dan Main Memory.

### Write Through

Tiap kali CPU ingin mengakses data dari alamat tertentu, maka Cache dan Main Memory selalu terlibat. Hal ini menyebabkan kepadatan lalu lintas data.

### Write Back

Tiap kali CPU ingin mengakses data dari alamat tertentu, Cache selalu terlibat dan Main Memory **hanya** terlibat jika terjadi Replacement Algorithm pada data di Cache. 

## Istilah Cache Lainnya

### Cache Coherence

Istilah yang mendeskripsikan ketika data yang sama terdapat pada cache yang berbeda di dalam sistem multiprocessor.

### Locality of Reference

Bagian data yang dipredeksi akan sering dibutuhkan oleh CPU, sehingga akan disimpan pada Cache.