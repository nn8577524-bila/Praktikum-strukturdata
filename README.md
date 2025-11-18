
# **Implementasi Stack dan Queue di Python**

Dokumentasi ini menjelaskan implementasi dasar struktur data **Stack** dan **Queue** menggunakan bahasa Python.
Keduanya menggunakan tipe data **list**, karena Python menyediakan operasi yang efisien seperti `append()`, `pop()`, dan indexing.
Implementasi struktur data Stack dan Queue menggunakan tipe data list Python sangat membantu dalam memahami prinsip dasarnya: LIFO (Last-In, First-Out) untuk Stack dan FIFO (First-In, First-Out) untuk Queue.


##  **1. Stack (LIFO — Last In, First Out)**

Stack adalah struktur data linear yang menerapkan prinsip LIFO (Last-In, First-Out). Ini berarti elemen yang terakhir dimasukkan ke dalam tumpukan adalah elemen pertama yang akan dikeluarkan.

###  **Membuat Stack**

```python
stack = []
```

###  **Push (Menambah Elemen ke Stack)**

```python
stack.append('A')
stack.append('B')
stack.append('C')
print("Stack:", stack)
```

**Output:**

```
Stack: ['A', 'B', 'C']
```

###  **Pop (Menghapus Elemen Teratas)**

```python
element = stack.pop()
print("Pop:", element)
```

**Output:**

```
Pop: C
```

###  **Peek (Melihat Elemen Teratas Tanpa Menghapus)**

```python
topElement = stack[-1]
print("Peek:", topElement)
```

**Output:**

```
Peek: B
```

###  **Cek Apakah Stack Kosong**

```python
isEmpty = not bool(stack)
print("isEmpty:", isEmpty)
```

**Output:**

```
isEmpty: False
```

###  **Ukuran Stack**

```python
print("Size:", len(stack))
```

**Output:**

```
Size: 2
```


##  **2. Queue (FIFO — First In, First Out)**

Queue adalah struktur data linear yang menerapkan prinsip FIFO (First-In, First-Out). Ini berarti elemen yang pertama dimasukkan ke dalam antrian adalah elemen pertama yang akan dikeluarkan.
###  **Membuat Queue**

```python
queue = []
```

###  **Enqueue (Menambah Elemen ke Queue)**

```python
queue.append('A')
queue.append('B')
queue.append('C')
print("Queue:", queue)
```

**Output:**

```
Queue: ['A', 'B', 'C']
```

###  **Dequeue (Menghapus Elemen Depan)**

```python
element = queue.pop(0)
print("Dequeue:", element)
```

**Output:**

```
Dequeue: A
```

###  **Peek (Melihat Elemen Depan Tanpa Menghapus)**

```python
frontElement = queue[0]
print("Peek:", frontElement)
```

**Output:**

```
Peek: B
```

###  **Cek Apakah Queue Kosong**

```python
isEmpty = not bool(queue)
print("isEmpty:", isEmpty)
```

**Output:**

```
isEmpty: False
```

###  **Ukuran Queue**

```python
print("Size:", len(queue))
```

**Output:**

```
Size: 2
```


##  **Ringkasan Output Program**

### **Stack**

```
Stack: ['A', 'B', 'C']
Pop: C
Peek: B
isEmpty: False
Size: 2
```

### **Queue**

```
Queue: ['A', 'B', 'C']
Dequeue: A
Peek: B
isEmpty: False
Size: 2
```


##  **Struktur Data yang Digunakan**

* `append()` ➝ menambah elemen
   Metode ini berfungsi untuk menambahkan satu elemen baru ke akhir list, yang sangat efisien ($O(1)$) dan berguna sebagai operasi Push (Stack) atau Enqueue (Queue).
* `pop()` ➝ menghapus elemen (terakhir / berdasarkan index)
   Metode ini menghapus dan mengembalikan elemen; jika tanpa indeks, ia menghapus elemen terakhir ($O(1)$) untuk Pop Stack, namun jika menggunakan pop(0), ia menghapus elemen pertama ($O(n)$) untuk Dequeue Queue.
* indexing `[0]` dan `[-1]` ➝ melihat elemen depan/teratas
  Dengan indexing, kita dapat mengakses elemen pertama ([0]) atau elemen terakhir ([-1]) dalam waktu konstan ($O(1)$) untuk operasi Peek tanpa menghapus elemen tersebut.
* `len()` ➝ menghitung jumlah elemen
  Fungsi ini secara cepat mengembalikan total jumlah elemen yang ada dalam list, yang berguna untuk mengetahui ukuran Stack atau Queue saat ini ($O(1)$).
* `bool(list)` ➝ mengecek apakah list kosong
  list kosong dianggap False, sehingga pengecekan kondisi ini adalah cara paling ringkas untuk memverifikasi apakah Stack atau Queue kosong sebelum melakukan operasi penghapusan.

## **Kesimpulan**

Implementasi struktur data **Stack** dan **Queue** menggunakan tipe data **`list`** Python adalah metode yang sederhana untuk memahami prinsip dasar kedua struktur data tersebut, meskipun memiliki batasan kinerja yang signifikan pada Queue.
* **Stack** diimplementasikan secara **efisien** karena memanfaatkan operasi `append()` untuk **Push** dan `pop()` untuk **Pop**. 
* Kedua operasi ini memiliki kompleksitas waktu **konstan ($O(1)$)**, menjadikannya ideal karena interaksi Stack hanya terjadi di satu ujung (`tail` atau akhir list).
* **Queue** juga menggunakan `append()` untuk **Enqueue** ($O(1)$) tetapi mengandalkan `pop(0)` untuk operasi **Dequeue**.
* Operasi **Dequeue** ini memiliki kompleksitas waktu **linear ($O(n)$)** karena penghapusan elemen di awal list memerlukan pergeseran semua elemen yang tersisa di memori. 
* Hal ini membuat implementasi Queue dengan `list` **tidak efisien** untuk volume data besar atau aplikasi yang membutuhkan kinerja tinggi.
Untuk implementasi Queue yang optimal dalam konteks performa, **modul `collections.deque`** lebih disarankan karena dirancang untuk menjamin operasi Dequeue dan Enqueue di kedua ujung tetap berjalan dalam waktu **konstan ($O(1)$)**.



