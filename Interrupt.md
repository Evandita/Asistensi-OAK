# Interrupt

## Komponen Interrupt

### Mask Register

Digunakan untuk **menyeleksi** sumber mana saja yang boleh mengirim sinyal interrupt ke CPU.

### IEN

Ketika IEN bernilai `1`, maka CPU berhak menerima sinyal interrupt. Jika IEN bernilai `0`, maka CPU tidak akan menerim sinyal interrupt sama sekali.

### INTACK

Sinyal yang berupa balasan dari CPU untuk **menerima** atau **menolak** interrupt.

### IVAD

Alamat yang menuju proses interrupt

### Bus Buffer

Tempat untuk menampung IVAD secara sementara, ketika sedang menunggu INTACK.

## Proses Interrupt

1. Ketika sinyal IVAD ingin dikirim ke CPU, maka tahan sebentar pada Bus Buffer untuk menunggu jawaban dari CPU apakah interrupt process akan dieksekusi atau tidak.

2. Apabila Interrupt dieksekusi, maka IVAD akan dikirimkan ke CPU.

3. PC beserta register-register lain yang sedang digunakan akan disimpan pada memory stack terlebih dahulu, sebelum ditimpa oleh IVAD.

4. CPU mengeksekusi proses Interrupt. Setelah selesai, CPU akan kembali ke proses semula dengan menggunakan data yang telah disimpan pada Memory Stack.