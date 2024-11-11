<div align="center">
    <a href="https://github.com/beryllwithcode/golang-study">
    <img src="https://cdn.icon-icons.com/icons2/2699/PNG/512/golang_logo_icon_171073.png" alt="Logo" width="150" height="150">
    </a>
    <h1 align="center">Study Golang</h1>
    <p align="center">This repository contains about learning Go programming language</p>
</div>

## Fundamental Golang
<h3>Hello World</h3>
Sample code Hello World in Golang:

  ```go
    package main

    // Import Package fmt
    import "fmt"

    func main() {
    //Print "Hello, World!" on console
    fmt.println("Hello, World!")
    }
   ```
- Di Go, setiap program adalah bagian dari paket. kata kunci ``package``. Dalam contoh ini, Program milik ``main`` package. 
- ``import ("fmt")`` bertujuan untuk mengimport file yang termasuk dalam ``fmt`` package.
- ``fmt.println()`` adalah fungsi yang tersedia dari ``fmt`` package. Ini digunakan untuk menampilkan/mencetak text. Dalam contoh kita, hasil output nya akan menghasilkan Hello, World!

<h3>Compile File Go-lang</h3>
<h4>(Go source) -> (Compiler) -> (Executable Binary)</h4>

Untuk compile suatu file dapat menjalankan perintah: <br>
``go build nama_file.go`` <br>
atau jika ingin menjalankan suatu file tanpa compile, jalankan perintah: <br>
``go run nama_file.go``

<h3>Tipe data</h3> 

- Number (Integer, Float)
```go
    func main() {
	    fmt.Println("one", 1) //output: one, 1
	    fmt.Println("two", 2) //output: two, 2
	    fmt.Println("one point six", 1.6) //output: one point six, 1.6
    }
```
- Boolean (True or False)
```go
    func main() {
        fmt.Println(true) //output: true
        fmt.Println(false) //output: false
    }
```
- Alias
<table>
    <tr>
        <th>Tipe</th>
        <th>Alias</th>
    </tr>
    <tr>
        <td>byte</td>
        <td>uint8</td>
    </tr>
    <tr>
        <td>rune</td>
        <td>int32</td>
    </tr>
    <tr>
        <td>any</td>
        <td>interface{}</td>
    </tr>
</table>

- String 
    <p>1. String adalahh tipe data dari kumpulan karakter</p>
    <p>2. Tipe data String di Go-Lang diwakili dengan kata kunci string</p>
    <p>3. Nilai data string di Go-Lang selalu dimulai dan di akhiri dengan (tanda kutip ganda)-> "Ini string" <-(Tanda kutip ganda)</p>
```go
    func main() {
        fmt.Println("Beryll") //output: Beryll
        fmt.Println("Pradana") //output: Pradana
        fmt.Println("Ramadhan") //output: Ramadhan
    }
```

<h3>Variable</h3> <br>

- Variable adalah tempat untuk menyimpan suatu data. <br>
Untuk membuat variable, kita dapat menggunakan keyword ``var``, kemudian di ikuti dengan nama variable dan tipe data.
```go
// Example 1

    func main() {
        //Declaration Variable
        var name string
        var age int

        //Assign value to variable name & age
        name = "Beryll Pradana Ramadhan"
        age = 21

        //Print value of variable
        fmt.Println(name) //output: Beryll Pradana Ramadhan
        fmt.Println(age) //output: 21
    }
```
```go
// Example 2

    func main() {
        //Assign value to variable name & age
        name := "Beryll Pradana Ramadhan"
        age := 21

        //Print value of variable
        fmt.Println(name) //output: Beryll Pradana Ramadhan
        fmt.Println(age) //output: 21
```
```go
// Example 3

    func main() {
        //Declaration Variable
	var born, now

	//Assign value to Variable born & now
	born = 2003
	now = 2024

	//Print value of Variable
	fmt.Println("I was born on ", born) //output: I was born on 2003
	fmt.Println("My age is ", now - born) //output: My age is 21
```

- Multi Variable
Go mendukung metode deklarasi banyak secara bersamaan, caranya adalah dengan menuliskan variable nya dengan pembatas tanda koma ( , ). Untuk pengisian value nya juga bisa secara bersamaan.
```go
// Example 1

	var first, second, third string
	first, second, third = "satu", "dua", "tiga" 
```
Dengan menggunakan teknik type inference, deklarasi multi variable bisa dilakukan untuk variable-variable yang memiliki tipe data yang berbeda.
```go
// Example 2

	var one, isFriday, twoPointTwo, say
	one, isFriday, twoPointTwo, say := 1, true, 2.2, "hello!"	
```

- Reserved Variable
Variable _(Underscore), Go punya aturan yang cukup unik yang dimana mengharuskan harus menggunakan semua variable yang telah di deklarasikan, jika tidak maka akan terjadi error. Reserved Varianle biasa dimanfaatkan untuk menampung nilai yang tidak dipakai. Bisa di bilang variable ini merupakan keranjang sampah.
```go
_ = "Study Jam Golang"
_ = "Belajar Golang itu Mudah!"
name, _ = "Beryll", "Belajar Golang"
```

- Variable Declaration Using Keyword ``new``
Fungsi ``new()`` digunakan untuk membuat variable pointer dengan tipe data tertentu. Nilai data default nya akan menyesuaikan dengan tipe datanya.
```go
name := new(string)

fmt.Println(name) //output: 0x2081a220
fmt.Pritnln(*name) //output: ""
```
Variable ``name`` menampung data bertipe pointer string. Jika ditampilkan yang muncul bukanlah nilai melainkan alamat memori nilai tersebut (dalam bentuk notasi heksadesimal). Untuk menampilkan nilai aslinya, variable tersebut perlu di Dereference terlebih dahulu, caranya dengan menuliskan tanda asterisk ( * ) sebelum nama variabel.


<a href="https://dasarpemrogramangolang.novalagung.com/A-tipe-data.html">Click untuk penjelasan lengkap nya!</a>
