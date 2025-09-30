# Tugas 2

## Modul 1: Mengenal pemrograman Kotlin dengan menggunakan Array, List, Looping dan penggunaan Konstruktor pada Class dan Setter-Getter

###Membuat Array dan List
  Pada bagian ini anda akan mencoba untuk menuliskan Array dan List kemudian menampilkannya dengan menggunakan looping. Berikut ini merupakan langkah-langkah yang dilakukan:
## 1. Langkah pertama silahkan tulis kode program berikut ini:

```
fun main() {
    val school = listOf("mackerel", "trout", "halibut")
    val myList = mutableListOf("tuna", "salmon", "shark")
    myList.remove("shark")
    
    println(school)
    println(myList)
}
```
OUTPUT
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/8cb15b3a-7efe-4440-aa58-8ff5dcabcc29" />




## 2. Menampilkan Looping Pada Program Diatas.

```
fun main() {
    val school = listOf("mackerel", "trout", "halibut")
    
    val myList = mutableListOf("tuna", "salmon", "shark")
	myList.remove("shark")
    
    println(school)
    println(myList)
    
    println("Print data using Looping")
    
    var i=0
    for (element in school) {
        i++
    	println("$i: $element")
	}
    
    
}
```

OUTPUT
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/f19ac366-3a2c-4f32-a3bf-db9822d1f02b" />



### Membuat Konstruktor pada Class
Pada bagian ini anda akan mencoba untuk menuliskan Konstruktor pada Class dan menambahkan setter-getter didalamnya. Berikut ini merupakan langkah-langkah yang dilakukan:

## 1. Langkah pertama silahkan tulis kode program berikut ini:

```
class Aquarium (var length: Int = 100, var width: Int = 20, var height: Int = 40) {
    init {
        println("aquarium initializing")
    }
    init {
        println("Volume: ${width * length * height / 1000} liters")
    }
    
}

fun main() {
        val aquarium1 = Aquarium()
        val aquarium2 = Aquarium(width = 25)
        val aquarium3 = Aquarium(height = 35, length = 110)
        val aquarium4 = Aquarium(width = 25, height = 35, length = 110)
}
```

OUTPUT
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/ed80e336-67d4-43e6-85b8-f53ea5e278c1" />


## 2. Langkah selanjutnya kita akan menambahkan konstruktor dengan cara lain yakni menggunakan constructor seperti program dibawah ini.

```
class Aquarium (var length: Int = 100, var width: Int = 20, var height: Int = 40) {
    init {
        println("aquarium initializing")
    }
    init {
        println("Volume: ${width * length * height / 1000} liters")
    }
    
    constructor(numberOfFish: Int) : this() {
        val tank = numberOfFish * 2000 * 1.1
        println("Tank: $tank")
    }
}
   
    fun main() {
        val aquarium1 = Aquarium()
        val aquarium2 = Aquarium(width = 25)
        val aquarium3 = Aquarium(height = 35, length = 110)
        val aquarium4 = Aquarium(width = 25, height = 35, length = 110)        
        val aquarium5 = Aquarium(numberOfFish = 29)
 }
```

OUTPUT
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/91f5d4fc-6a5e-4f4f-b803-1293869076f1" />


## 3. Langkah selanjutnya kita akan menambahkan setter-getter seperti program dibawah ini:

```
class Aquarium (val length: Int = 100, val width: Int = 20, var height: Int = 40) {
    
    var volume: Int
    get() = width * height * length / 1000
    set(value) {
        height = (value * 1000) / (width * length)
    }
    
    init {
        println("aquarium initializing")
    }
    init {
        // 1 liter = 1000 cm^3
        println("Volume: ${width * length * height / 1000} liters")
    }
    
    constructor(numberOfFish: Int) : this() {
        // 2,000 cm^3 per fish + extra room so water doesn't spill
        val tank = numberOfFish * 2000 * 1.1
        println("Tank: $tank")
    }
    
    fun printSize() {
    	println("Width: $width cm " +
            "Length: $length cm " +
            "Height: $height cm ")
        
        // 1 liter = 1000 cm^3
        println("Volume: $volume liters")
    }
    
}
   
    fun main() {
        val aquarium1 = Aquarium()
        aquarium1.printSize()
        // default height and length
        val aquarium2 = Aquarium(width = 25)
        aquarium2.printSize()
        // default width
        val aquarium3 = Aquarium(height = 35, length = 110)
        aquarium3.printSize()
        // everything custom
        val aquarium4 = Aquarium(width = 25, height = 35, length = 110)
        aquarium4.printSize()
        val aquarium5 = Aquarium(numberOfFish = 29)
        aquarium5.printSize()
   }
```

OUTPUT
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/388e7ea8-6454-4cc7-b318-0ee60efe7c53" />


## Modul 2: Menjalankan aplikasi pada Device Android

## 1. Langkah Pertama
butki pengerjaan:
<img width="1351" height="864" alt="image" src="https://github.com/user-attachments/assets/62c3b2a7-15fe-467d-9edb-bff0ce31aef4" />


## 2. Langkah Selanjutnya
bukti pengerjaan:
<img width="1351" height="864" alt="image" src="https://github.com/user-attachments/assets/82e17ac9-3381-4ffc-a36a-01ee3d1b32b5" />


## Modul 3: Mengenal struktur proyek pada pembuatan aplikasi Android

Di dalam modul ini saya belajar mengenal struktur proyek Android yaitu:
1. Resources (layout, gambar, string, warna, media)
2. Components (activities, services, helper classes)
3. Manifest (informasi setting/runtime)
4. Build configuration (APK version di Gradle)

## Modul 4: Mencatat Log pada aplikasi Android

Dari modul ini saya belajar cara menggunakan Logcat untuk menampilkan log dengan kode Log.d("Tag","Pesan") agar bisa memantau jalannya aplikasi.

## Modul 5: Membuat Interactive UI dengan View

Dari modul ini saya jadi mengetahui cara membuat proyek baru dalam contoh pada modul di proyek ini di beri nama "helloFellas".
