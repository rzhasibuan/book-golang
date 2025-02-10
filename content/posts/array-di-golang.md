---
date: '2025-02-10T10:08:00+07:00'
draft: false
title: 'Array di golang '
tags: ['golang', 'system design']
---


## Daftar Isi

1. [Pendahuluan](#pendahuluan)
2. [Deklarasi dan Inisialisasi Array](#deklarasi-dan-inisialisasi-array)
3. [Akses Elemen Array](#akses-elemen-array)
4. [Iterasi Array](#iterasi-array)
5. [Modifikasi Array](#modifikasi-array)
6. [Panjang Array](#panjang-array)
7. [Array sebagai Parameter Fungsi](#array-sebagai-parameter-fungsi)
8. [Perbedaan Array dan Slice](#perbedaan-array-dan-slice)
9. [Kesimpulan](#kesimpulan)
10. [Daftar Pustaka](#daftar-pustaka)

---

## Pendahuluan

Array adalah struktur data yang digunakan untuk menyimpan sekumpulan elemen dengan tipe data yang sama di dalam Golang. Array memiliki ukuran tetap yang tidak dapat diubah setelah dideklarasikan.

---

## Deklarasi dan Inisialisasi Array

Di Golang, array dapat dideklarasikan dengan menentukan panjangnya dan tipe datanya.

```go
package main
import "fmt"

func main() {
    var angka [5]int // Array dengan panjang 5
    fmt.Println(angka) // Output: [0 0 0 0 0]
}
```

Array juga dapat diinisialisasi saat deklarasi:

```go
angka := [5]int{1, 2, 3, 4, 5}
fmt.Println(angka) // Output: [1 2 3 4 5]
```

---

## Akses Elemen Array

Elemen dalam array dapat diakses dengan indeks:

```go
angka := [5]int{10, 20, 30, 40, 50}
fmt.Println(angka[2]) // Output: 30
```

---

## Iterasi Array

Menggunakan perulangan `for` untuk menelusuri elemen array:

```go
angka := [5]int{1, 2, 3, 4, 5}
for i := 0; i < len(angka); i++ {
    fmt.Println(angka[i])
}
```

Menggunakan `range`:

```go
for index, value := range angka {
    fmt.Printf("Indeks %d: %d\n", index, value)
}
```

---

## Modifikasi Array

Elemen dalam array dapat dimodifikasi dengan mengakses indeksnya:

```go
angka := [3]int{10, 20, 30}
angka[1] = 50
fmt.Println(angka) // Output: [10 50 30]
```

---

## Panjang Array

Panjang array dapat diperoleh dengan `len()`:

```go
angka := [4]int{5, 10, 15, 20}
fmt.Println(len(angka)) // Output: 4
```

---

## Array sebagai Parameter Fungsi

Array dapat digunakan sebagai parameter fungsi, tetapi akan dikirim sebagai salinan:

```go
func cetakArray(arr [3]int) {
    fmt.Println(arr)
}

func main() {
    angka := [3]int{1, 2, 3}
    cetakArray(angka)
}
```

---

## Perbedaan Array dan Slice

Array memiliki ukuran tetap, sedangkan slice adalah referensi ke bagian array dengan ukuran yang dapat berubah.

```go
var arr = [5]int{1, 2, 3, 4, 5} // Array
var slice = arr[1:4]            // Slice dari array
fmt.Println(slice)               // Output: [2 3 4]
```

---

## Kesimpulan

Array di Golang adalah struktur data dengan ukuran tetap yang dapat menyimpan elemen dengan tipe data yang sama. Untuk ukuran yang dinamis, lebih baik menggunakan slice.

---

## Daftar Pustaka

1. The Go Programming Language Specification - [https://golang.org/ref/spec](https://golang.org/ref/spec)
2. Effective Go - [https://golang.org/doc/effective\_go.html](https://golang.org/doc/effective_go.html)
3. Go by Example - [https://gobyexample.com](https://gobyexample.com)


