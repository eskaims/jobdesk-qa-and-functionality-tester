## SOAL TEST - QA & FUNCTIONALITY TESTER ##

Silahkan cermati & analisa proses flow dibawah ini:

1. Terdapat aplikasi penjualan berbasis mobile yang digunakan oleh salesman untuk menginput data pesanan atas toko-toko yang dia kunjungi.
2. Data yang diinput oleh salesman mencakup:
    - Memilih kode toko yang dikunjungi
    - Memilih Kode produk yang dipesan oleh toko
    - Mengisi Qty produk yang diinginkan oleh toko
    - Catatan / remark pesanan (optional)
3. Data pesanan yang diinput salesman di aplikasi mobile, dikirim melalui API ke server sehingga bisa di cek oleh admin penjualan untuk di follow up lebih lanjut
4. Admin penjualan dapat melihat list pesanan yang sudah diinput oleh salesman, 
    - Jika jumlah qty produk yang dipesan lebih kecil dari jumlah qty produk digudang secara sistem, maka dia akan menandai nomor-nomor pesanan tsb untuk disiapkan oleh admin gudang.
    - Jika ada produk yang qty pesanan nya lebih besar dari qty produk digudang secara sistem, maka admin penjualan akan menandai nomor-nomor pesanan tsb agar diproses dengan qty yang tersedia, dan selisih qtynya dibuatkan menjadi dokumen pesanan baru.
5. Nomor-nomor pesanan yang sudah ditandai oleh admin sales untuk diproses oleh admin gudang akan diverifikasi ketersediaan stok fisik digudang. 
    - Jika stok di gudang dapat memenuhi jumlah qty pesanan, maka admin gudang akan menandai nomor-nomor pesanan dengan kriteria tersebut untuk di cetak dokumen surat jalannya, kemudian produk di gudang dipindahkan ke area staging sebelum dinaikkan ke mobil untuk pengiriman.
    - Jika stok di gudang tidak dapat memenuhi qty pesanan, maka admin gudang akan menandai nomor-nomor pesanan dengan kriteria tersebut sebagai "dokumen dengan stok tidak cukup".
6. Nomor pesanan yang sudah diproses pengiriman akan diverifikasi oleh admin gudang ketika driver kembali ke gudang. 
    - Jika pesanan diterima oleh toko secara full qty, maka pesanan tersebut ditandai oleh admin gudang untuk kemudian diproses bagian fakturis
    - Jika pesanan diterima sebagian oleh toko, maka admin gudang akan menginput nilai qty kembali untuk tiap produk
    - Jika pesanan ditolak oleh toko, maka nomor pesanan ditandai sebagai dokumen yang dibatalkan



Dari proses flow tersebut, Anda diminta untuk membuat:
1. TDD dengan metode / tools yang Anda kuasai
2. BDD dengan metode / tools yang Anda kuasai
3. Simulasikan dalam bentuk dokumen Laporan Hasil Test secara lengkap (normal skenario & negatif skenario) yang mencakup functional test, performance test, dan integration test.


