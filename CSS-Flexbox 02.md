# Align & GAP Flexbox
## Align-Items
Properti ini memiliki perilaku menempatkan flex items sepanjang cross axis.<br>
Bayangkan bahwa tingkah laku dari properti ini mirip dengan properti justify-content,<br>
tetapi mengatur child element dalam satu baris pada cross axis. 

```CSS
.container {
  display: flex;
  align-items: stretch | flex-start | flex-end | center | baseline;
}
```
Berikut adalah penjelasan setiap value dari properti align-items.

- Stretch: melebar hingga memenuhi container dalam cross axis. Setiap child element akan memiliki nilai height yang sama, meskipun isi konten berbeda.
- Flex-start: setiap child element akan memiliki ukuran height sesuai dengan isi konten serta seluruhnya akan berada di tepi cross-start.
- Flex-end: setiap child element akan memiliki ukuran height sesuai dengan isi konten serta seluruhnya akan berada di tepi cross-end.
- Center: setiap child element memiliki ukuran height sesuai dengan isi konten dan secara vertikal posisi elemen berada di tengah.
- Baseline: nilai pada asalnya akan menyerupai flex-start. Namun, jika konten pertama pada masing-masing child element memiliki ukuran height yang berbeda, 
child element lainnya akan menyesuaikan posisinya secara cross axis dari cross-start.

## Align-content
Properti ini melakukan perataan terhadap flex items pada setiap baris dalam cross-axis. Tingkah laku properti ini hampir mirip dengan properti justify-content yang mengatur tata letak flex items di sisi main axis.

Hal yang perlu diperhatikan adalah penggunaan properti ini hanya akan berpengaruh pada multi-line flex container dan properti flex-wrap dilibatkan. Flex container yang hanya memiliki single line tidak akan memiliki efek diterapkannya properti align content.
```CSS
.container {
  display: flex;
  align-content: flex-start | flex-end | center | space-between | space-around | space-evenly;
}
```
Berikut adalah penjelasan setiap value dari properti ini.

- Normal (default): Jika kita tidak menerapkan value pada align content, flex items akan diposisikan secara default.
- Flex-start: flex items ditata pada permulaan flex container.
- Flex-end: flex items ditata pada akhir flex container.
- Center: flex items diposisikan di tengah flex container.
- Space-between: flex items akan disebar secara merata, item pertama akan diposisikan pada cross-start dan item terakhir akan diposisikan pada cross-end.
- Space-around: flex items akan disebar secara merata dengan jarak celah yang sama juga.
- Space-evenly: flex items akan disebar secara merata dengan jarak yang merata juga.
## GAP
Sering kali kita ingin memberikan jarak atau celah pada flex items. Biasanya kita akan mengandalkan properti margin dalam hal ini. Namun, ada cara yang lebih efektif, yaitu menggunakan properti gap.
```CSS
.container {
  display: flex;
  gap: 1rem; /* diterapkan secara vertikal dan horizontal dengan nilai yang sama */
  gap: 1rem 2rem; /* diterapkan secara vertikal dan horizontal */
  row-gap: 1rem; /* diterapkan secara horizontal */
  column-gap: 1rem; /* diterapkan secara vertikal */
}
```
