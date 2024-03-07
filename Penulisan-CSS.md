# Aturan penulisan css

## TYPE ELEMENT SELECTOR
untuk penulisan selector seperti : header,nav,div,span, dan element lainnya
tulis dengan format berikut
```CSS
span {
  color: red;
}
```

## CLASS selector
untuk penulisan class seperti : <header class="navbar-container> dan lain sebagainya
```CSS
.navbar-container {
  backgound-color: blue;
}
```

## Kombinasi Element+class
untuk penulisan seperti ini syntax harus berada pada line yang sama dan menunjukkan nilai spesifik 
misal untuk kode berikut =  <header class="navbar-container>
kita bisa menulisnya dengan
```CSS
/*tidak boleh ada spasi saat penulisan ELEMENT.Class contoh = header.navbar-container*/
header.navbar-container{
    display: flex;
    justify-content: space-around;
    align-items: center;

    z-index: 9999; /* z-index agar navbar selalu berada pada lapisan/tumpukan teratas*/
```
bisa juga dengan beberapa class atau list sekaligus berikut beberapa contohnya
```CSS
header.navbar-container .nav-list ul{
    padding-left: 0;
    
    display: flex;
    justify-content: center;
    gap: 2rem 1rem;
}

header.navbar-container .nav-list li{
    list-style-type: none;
}
/*ini efek saat navigasi diarahkan dengan cursor*/
header.navbar-container .nav-list li a{
    padding: 0.5rem 1.5rem;
    border-radius: 5px;

    text-decoration: none;
    font-size: 1.05rem;
    font-weight: 500;
    color: black;

    transition: all 0.2 ease-in-out; /*durasi transisi cursor hover*/
}
/*ini efek saat navigasi diarahkan dengan cursor*/
header.navbar-container .nav-list li:hover a{
    background-color: #425c77;
    color: white;
}
```
## ID SELECTOR
ini untuk penulisan ID misal = ```<div id="special"> ```
```CSS
#special {
  background-color: skyblue;
}
```

## Atribut selector
Attribute selector merupakan cara menetapkan target elemen berdasarkan sebuah atribut yang digunakan atau bahkan bisa lebih spesifik dengan nilainya. Contohnya sebagai berikut.
```CSS
/* <a> element yang menerapkan href attribute */
a[href] {
  color: blue;
}

/* <a> element yang menerapkan nilai pada href dengan awalan "#" */
a[href^='#'] {
  background-color: gold;
}

/* <a> element yang menerapkan nilai pada href yang mengandung teks "example" */
a[href*='example'] {
  background-color: silver;
}

/* <a> element yang menerapkan nilai pada href yang mengandung teks "insensitive" tidak mementingkan huruf kapital*/
a[href*='insensitive' i] {
  color: cyan;
}

/* <a> element yang menerapkan nilai pada href dengan akhiran ".org" */
a[href$='.org'] {
  color: red;
}
```
Dari kode di atas, terlihat banyak sekali kondisi yang dapat diterapkan pada attribut selector. Agar dapat lebih mudah memahaminya, mari kita rangkum dalam sebuah tabel.<br>
### attr = a <br> 
Syntax	Description
- [attr] Menargetkan elemen yang menerapkan atribut attr.

- [attr=value] Menargetkan elemen yang menerapkan atribut attr dengan nilai value.

- [attr~=value] Menargetkan elemen yang menerapkan atribut attr dan salah satu nilainya adalah value.

- [attr^=value] Menargetkan elemen yang menerapkan atribut attr dan nilainya diawali dengan nilai value.

- [attr$=value] Menargetkan elemen yang menerapkan atribut attr dan nilainya diakhiri dengan value.

- [attr*=value] Menargetkan elemen yang menerapkan atribut attr dan nilainya mengandung value.

## Universal Selector
Universal selector digunakan untuk diterapkan pada seluruh elemen. Namun, selector ini juga bisa secara spesifik menargetkan sebuah elemen dengan menggabungkannya bersama selector yang lain. Berikut contohnya.
```CSS
  /* Menargetkan seluruh tipe elemen */
* {
  color: green;
}

/* Menargetkan seluruh tipe elemen yang mengandung nilai "en" pada atribut lang */
*[lang^='en'] {
  font-style: italic;
}

/* Menargetkan seluruh tipe elemen yang memiliki nilai "warning" pada atribut class */
*.warning {
  color: red;
}

/* Menargetkan seluruh tipe elemen yang memiliki nilai "content" pada atribut id */
*#content {
  border: 1px solid blue;
  padding: 20px;
}
```
