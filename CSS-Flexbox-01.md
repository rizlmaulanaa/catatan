# CSS Note
## FLEXBOX
Flexbox (Flexible Box) adalah model tata letak dalam CSS yang memungkinkan desain tata letak responsif yang fleksibel tanpa menggunakan float atau positioning. Berikut ini adalah ringkasan singkat tentang Flexbox beserta beberapa contoh properti yang relevan:

### Display: 
Properti display digunakan untuk mendefinisikan apakah suatu elemen adalah flex container atau inline-flex container. Misalnya:
```CSS
.container {
  display: flex; /* atau inline-flex */
}
```
### Flex-direction: 
Properti ini menentukan arah utama (main-axis) dari flex items dalam flex container. Nilai-nilai yang mungkin:
row (default): Horisontal dari kiri ke kanan (LTR) atau kanan ke kiri (RTL).
column: Vertikal dari atas ke bawah. Contoh:
```CSS
.container {
  display: flex;
  flex-direction: row | row-reverse | column | column-reverse;
}
```
Berikut adalah penjelasan value dari properti flex-direction.

- Row: flex items akan disusun secara horizontal dari kiri ke kanan.
- Row-reverse: flex items akan disusun secara horizontal, tetapi berarah terbalik (kanan ke kiri).
- Column: flex items akan disusun secara vertikal dari atas ke bawah.
- Column-reverse: flex items akan disusun secara vertikal, tetapi dengan arah terbalik (bawah ke atas).

### Flex-wrap: 
Properti ini mengatur apakah flex items akan memenuhi satu baris atau dapat dibungkus ke baris berikutnya jika tidak cukup ruang. Nilai-nilai yang mungkin:
nowrap (default): Semua flex items dalam satu baris.
wrap: Flex items dapat dibungkus ke baris berikutnya. Contoh:
```CSS
.container {
  display: flex;
  flex-wrap: nowrap | wrap | wrap-reverse;
}
```
Berikut adalah penjelasan setiap value dari properti flex-wrap.

- nowrap: seluruh flex items hanya akan ditempatkan dalam satu baris meskipun sangat banyak jumlahnya.
- wrap: nilai ini menyebabkan flex items akan diletakkan ke baris yang baru (berikutnya) sehingga menjadi multiple lines.
- wrap-reverse: meskipun mirip dengan wrap, nilai ini akan menyebabkan beberapa flex items ditempatkan dengan menambahkan baris sebelumnya.

### Justify-content: 
Properti ini mengatur perataan flex items sepanjang sumbu utama. Beberapa nilai yang relevan:
flex-start (default): Flex items diperatakan ke awal sumbu utama.
flex-end: Flex items diperatakan ke akhir sumbu utama.
center: Flex items diperatakan di tengah sumbu utama. Contoh:
```CSS
.container {
  display: flex;
  justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly;
}
```
Berikut adalah penjelasan setiap value dari properti justify-content.

- Flex-start: peletakan child element akan dimulai dari main-start.
- Flex-end: peletakan child element dimulai dari main-end.
- Center: child element akan diletakkan di tengah parent child.
- Space-between: child element akan tersusun secara merata, elemen pertama berada di tepi main-start dan elemen kedua berada di tepi main-end. Jika child element lebih dari dua, elemen - - lainnya akan didistribusikan berada di tengah dengan jarak yang sama.
- Space-around: setiap child element akan memiliki panjang celah yang sama pada sisi horizontal.
- Space-evenly: setiap child element akan memiliki jarak yang setara, termasuk jarak ke tepi main-start dan main-end.
