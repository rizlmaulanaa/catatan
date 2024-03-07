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
  flex-direction: row | row-reverse | column | column-reverse;
}
```

### Flex-wrap: 
Properti ini mengatur apakah flex items akan memenuhi satu baris atau dapat dibungkus ke baris berikutnya jika tidak cukup ruang. Nilai-nilai yang mungkin:
nowrap (default): Semua flex items dalam satu baris.
wrap: Flex items dapat dibungkus ke baris berikutnya. Contoh:
```CSS
.container {
  flex-wrap: nowrap | wrap | wrap-reverse;
}
```

### Justify-content: 
Properti ini mengatur perataan flex items sepanjang sumbu utama. Beberapa nilai yang relevan:
flex-start (default): Flex items diperatakan ke awal sumbu utama.
flex-end: Flex items diperatakan ke akhir sumbu utama.
center: Flex items diperatakan di tengah sumbu utama. Contoh:
```CSS
.container {
  justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly | start | end | left | right;
}
```
