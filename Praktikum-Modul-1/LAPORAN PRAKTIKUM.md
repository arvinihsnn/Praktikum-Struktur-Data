# <h1 align="center">Laporan Praktikum Modul 1 - Codeblocks IDE & Pengenalan Bahas C++ (Bagian Pertama)</h1>
<p align="center">Arvin Ihsan Fatih - 109082500050</p>

## Dasar Teori
Bahasa C++ adalah bahasa peningkatan dari bahasa C dan bisa dipakai untuk membuat berbagai macam program atau aplikasi[1].

### A. Struktur Dasar Program C++<br/>
Bentuk atau struktur dasar program yang dibuat dengan C++ terdiri dari tiga bagian:
#### 1. Bagian include
#### 2. Bagian namespace
#### 3. Bagian fungsi[2].

### B. Struktur Kontrol Perabangan dan Perulangan<br/>
#### 1. Percabangan: Percabangan akan mampu membuat program berpikir dan menentukan tindakan sesuai dengan logika/kondisi yang kita berikan. Pada pemrograman C++, terdapat 6 bentuk percabangan: Percabangan if, Percabangan if/else, Percabangan if/else/if, Percabangan Switch/Case, Percabangan dengan Operator Ternary, dan Percabangan Bersarang (Nested)[3].
#### 2. Perulangan: Perulangan akan membantu kita mengeksekusi kode yang berulang-ulang, berapapun yang kita mau. Ada empat macam bentuk perulangan pada C++: Blok Perulangan For, Perulangan While pada C++, Perulangan Do/While pada C++, dan Perulangan Bersarang (Nested Loop)[4].

## Guided 

### 1.

```C++
#include <iostream>
using namespace std;
int main() {
 cout << "hello world" << endl;
 return 0;
}
```
Program ini merupakan program sederhana untuk menampilkan teks. Menggunakan cout untuk mencetak kalimat "hello world", dan endl untuk berpindah ke baris baru. Program ini bertujuan untuk mengenalkan struktur dasar kode C++ dan fungsi input-output dasar.

### 2.

```C++
#include <iostream>
using namespace std;
int main() {
  int inp;
  cin >> inp;
  cout << "nilai = " << inp;
  return 0;
}
```
Program ini berfungsi untuk menerima inputan angka dari pengguna dan menampilkannya kembali ke layar. Variabel inp bertipe data int digunakan untuk menyimpan angka bilangan bulat yang dimasukkan melalui perintah cin. Setelah angka diinputkan, program mencetak teks "nilai = " diikuti dengan nilai variabel inp tersebut menggunakan perintah cout.

### 3.

```C++
#include <iostream>
using namespace std;
int main() {
  int W, X, Y; float Z;
  X = 7; Y = 3; W = 1;
  Z = (X + Y) / (Y + W);
  cout<< "Nilai z = " << Z << endl;
  return 0;
}
```
Program ini dibuat untuk mempelajari operasi aritmatika dasar dan penggunaan tipe data dalam C++. Variabel W, X, dan dideklarasikan bertipe int untuk menyimpan nilai bilangan bulat, sedangkan Z bertipe float untuk menyimpan hasil perhitungan. Program melakukan penjumlahan dan pembagian matematika (7 + 3) / (3 + 1) yang menghasilkan nilai 10 / 4 = 2.5, lalu mencetak hasilnya ke layar menggunakan perintah cout.

## Unguided 

### 1. Buatlah program yang menerima input-an dua buah bilangan bertipe float, kemudian memberikan output-an hasil penjumlahan, pengurangan, perkalian, dan pembagian dari dua bilangan tersebut.

```C++
#include <iostream>
using namespace std;

int main() {
 float bil1, bil2;

 cout << "bilangan pertama : ";
 cin >> bil1;
 cout << "bilangan kedua : ";
 cin >> bil2;

 cout << "Penjumlahan (" << bil1 << " + " << bil2 << ") = " << bil1 + bil2 << endl;
 cout << "Pengurangan (" << bil1 << " - " << bil2 << ") = " << bil1 - bil2 << endl;
 cout << "Perkalian   (" << bil1 << " * " << bil2 << ") = " << bil1 * bil2 << endl;
 cout << "Pembagian (" << bil1 << " / " << bil2 << ") = " << bil1 / bil2 << endl;
 return 0;
}
```
### Output Unguided 1 : bilangan pertama : 20 
bilangan kedua : 2
Penjumlahan (20 + 2) = 22
Pengurangan (20 - 2) = 18
Perkalian   (20 * 2) = 40
Pembagian   (20 / 2) = 10

bilangan pertama : 6
bilangan kedua : 7
Penjumlahan (6 + 7) = 13
Pengurangan (6 - 7) = -1
Perkalian   (6 * 7) = 42
Pembagian   (6 / 7) = 0.857143

##### Output 1
![Screenshot Output Unguided 1_1](https://github.com/arvinihsnn/Praktikum-Struktur-Data/blob/main/Praktikum-Modul-1/Output-Unguided-1-1.png)

##### Output 2
![Screenshot Output Unguided 1_2](https://github.com/arvinihsnn/Praktikum-Struktur-Data/blob/main/Praktikum-Modul-1/Ouput-Unguided-1-2.png)

Program ini bertujuan untuk membuat kalkulator aritmatika dasar yang menerima input dua bilangan bertipe float. Nilai yang dimasukkan pengguna disimpan ke dalam variabel bil1 dan bil2, kemudian program langsung menghitung serta menampilkan hasil penjumlahan, pengurangan, perkalian, dan pembagian.

### 2. Buatlah sebuah program yang menerima masukan angka dan mengeluarkan output nilai angka tersebut dalam bentuk tulisan. Angka yang akan di-input-kan user adalah bilangan bulat positif mulai dari 0 s.d 100.

```C++
#include <iostream>
#include <string>
using namespace std;

int main() {
 int angka;
 string satuan[] = {"nol", "satu", "dua", "tiga", "empat", "lima", "enam", "tujuh", "delapan", "sembilan", "sepuluh", "sebelas"};

 cin >> angka;

 cout << angka << " : ";

 if (angka <= 11) {
 cout << satuan[angka] << endl;
 } else if (angka < 20) {
 cout << satuan[angka % 10] << " belas" << endl;
 } else if (angka < 100) {
 cout << satuan[angka / 10] << " puluh ";
 if (angka % 10 != 0) {
 cout << satuan[angka % 10];
 }
 cout << endl;
 } else if (angka == 100) {
 cout << "seratus" << endl;
 }

 return 0;
}
```
### Output Unguided 2 : 67
67 : enam puluh tujuh

100
100 : seratus

##### Output 1
![Screenshot Output Unguided 2_1](https://github.com/arvinihsnn/Praktikum-Struktur-Data/blob/main/Praktikum-Modul-1/Output-Unguided-2-1.png)

##### Output 2
![Screenshot Output Unguided 2_2](https://github.com/arvinihsnn/Praktikum-Struktur-Data/blob/main/Praktikum-Modul-1/Output-Unguided-2-2.png)

Program ini memproses input angka dan mencetak sebutan atau ejaannya secara langsung. Array satuan menyimpan kata dasar untuk angka 0 sampai 11. Kondisi if-else digunakan untuk menentukan apakah angka tersebut masuk kelompok satuan/belasan (di bawah 20), puluhan (di bawah 100), atau angka 100.

### 3. Buatlah program yang dapat memberikan input dan output sbb. Input: 3
Output:
3 2 1 * 1 2 3
2 1 * 1 2
1 * 1
*

```C++
#include <iostream>
using namespace std;

int main() {
 int n;

 cout << "input: ";
 cin >> n;

 cout << "output:" << endl;

 for (int i = n; i >= 1; i--) {

 for (int s = 0; s < n - i; s++) {
 cout << " ";
 }

 for (int j = i; j >= 1; j--) {
 cout << j << " ";
 }

 cout << "* ";

 for (int j = 1; j <= i; j++) {
 cout << j;
 if (j != i) {
 cout << " ";
 }
 }
 cout << endl;
 }

 for (int s = 0; s < n; s++) {
 cout << " ";
 }
 cout << "*" << endl;

 return 0;
}
```
### Output Unguided 3 : input: 6
output:
6 5 4 3 2 1 * 1 2 3 4 5 6
 5 4 3 2 1 * 1 2 3 4 5
  4 3 2 1 * 1 2 3 4
   3 2 1 * 1 2 3
    2 1 * 1 2
     1 * 1
      *

input: 15
output:
15 14 13 12 11 10 9 8 7 6 5 4 3 2 1 * 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15
 14 13 12 11 10 9 8 7 6 5 4 3 2 1 * 1 2 3 4 5 6 7 8 9 10 11 12 13 14
  13 12 11 10 9 8 7 6 5 4 3 2 1 * 1 2 3 4 5 6 7 8 9 10 11 12 13
   12 11 10 9 8 7 6 5 4 3 2 1 * 1 2 3 4 5 6 7 8 9 10 11 12
    11 10 9 8 7 6 5 4 3 2 1 * 1 2 3 4 5 6 7 8 9 10 11
     10 9 8 7 6 5 4 3 2 1 * 1 2 3 4 5 6 7 8 9 10
      9 8 7 6 5 4 3 2 1 * 1 2 3 4 5 6 7 8 9
       8 7 6 5 4 3 2 1 * 1 2 3 4 5 6 7 8
        7 6 5 4 3 2 1 * 1 2 3 4 5 6 7
         6 5 4 3 2 1 * 1 2 3 4 5 6
          5 4 3 2 1 * 1 2 3 4 5
           4 3 2 1 * 1 2 3 4
            3 2 1 * 1 2 3
             2 1 * 1 2
              1 * 1
               *

##### Output 1
![Screenshot Output Unguided 3_1](https://github.com/arvinihsnn/Praktikum-Struktur-Data/blob/main/Praktikum-Modul-1/Output-Unguide-3-1.png)

##### Output 2
![Screenshot Output Unguided 3_2](https://github.com/arvinihsnn/Praktikum-Struktur-Data/blob/main/Praktikum-Modul-1/Output-Unguide-3-2.png)

Program ini mencetak pola angka bertingkat berdasarkan nilai n yang dimasukkan. Menggunakan perulangan for, program mencetak spasi untuk menggeser posisi, diikuti deret angka menurun, tanda bintang di bagian tengah, dan deret angka menaik. Pada bagian paling akhir, program mencetak satu tanda bintang tunggal di posisi tengah sebagai penutup pola.

## Kesimpulan
Praktikum ini memberikan saya pemahaman mendasar mengenai dasar-dasar pemrograman C++. Melalui tugas unguided ini, pemahaman terhadap penggunaan variabel, tipe data (int, float, string), operator matematika, percabangan (if-else), serta perulangan bersarang (nested loop) berhasil diimplementasikan dengan baik untuk menyelesaikan tugas modul 1 ini.

## Referensi
<br>[1] Ahmad Muhardian. (2019). Belajar C++ #01: Pengenalan Bahasa C++ untuk Pemula. Petani Kode. Diakses pada 27 September 2026 melalui https://www.petanikode.com/cpp-untuk-pemula/.
<br>[2] Ahmad Muhardian. (2015). Belajar C++ #03: Sintak Dasar C++ yang Harus Kamu Pahami!. Petani Kode. Diakses pada 27 September 2026 melalui https://www.petanikode.com/cpp-sintaks/.
<br>[3] Ahmad Muhardian. (2018). Belajar C++ #07: Memahami 6 Macam Bentuk Blok Percabangan pada C++. Petani Kode. Diakses pada 27 September 2026 melalui https://www.petanikode.com/cpp-percabangan/.
<br>[4] Ahmad Muhardian. (2019). Belajar C++ #08: Memahami Blok Perulangan di C++. Petani Kode. Diakses pada 27 September 2026 melalui https://www.petanikode.com/cpp-perulangan/.