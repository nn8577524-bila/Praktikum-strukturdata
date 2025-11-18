📌 README – Queue (Antrian)
🧠 Konsep Dasar Queue

Queue atau Antrian adalah struktur data yang cara kerjanya seperti antrean di dunia nyata:
➡️ Yang datang duluan, dilayani duluan.
Istilah kerennya yaitu FIFO (First In, First Out).
🧾 Penjelasan Kode
queue = []

# Enqueue
queue.append('A')
queue.append('B')
queue.append('C')
print("Queue: ", queue)

# Dequeue
element = queue.pop(0)
print("Dequeue: ", element)

# Peek
frontElement = queue[0]
print("Peek: ", frontElement)

# isEmpty
isEmpty = not bool(queue)
print("isEmpty: ", isEmpty)
🔍 Operasi-operasi pada Queue
| Operasi           | Penjelasan                                            |
| ----------------- | ----------------------------------------------------- |
| `append()`        | Memasukkan data ke antrian (**enqueue**)              |
| `pop(0)`          | Mengambil & menghapus data paling depan (**dequeue**) |
| `queue[0]`        | Melihat data terdepan tanpa menghapus (**peek**)      |
| `not bool(queue)` | Mengecek apakah queue kosong                          |
| `len(queue)`      | Mengecek total data dalam antrian                     |
📝 Alur Singkat Eksekusi

Tambahkan A, B, C → ['A', 'B', 'C']

Dequeue: ambil elemen pertama → 'A'

Queue sekarang → ['B', 'C']

Peek hasilnya 'B'

Queue tidak kosong → False

Ukuran queue → 2

📌 README – Stack (Tumpukan)
🧠 Konsep Dasar Stack

Stack atau Tumpukan adalah struktur data yang cara kerjanya seperti menyusun piring:
➡️ Yang ditaruh terakhir, diambil paling pertama.
Istilah kerennya yaitu LIFO (Last In, First Out).

🧾 Penjelasan Kode
stack = []

# Push
stack.append('A')
stack.append('B')
stack.append('C')
print("Stack: ", stack)

# Pop
element = stack.pop()
print("Pop: ", element)

# Peek 
topElement = stack[-1]
print("Peek: ", topElement)

# isEmpty
isEmpty = not bool(stack)
print("isEmpty: ", isEmpty)

# Size
print("Size :", len(stack))

🔍 Operasi-operasi pada Stack
| Operasi           | Penjelasan                                          |
| ----------------- | --------------------------------------------------- |
| `append()`        | Menambah data ke paling atas (**push**)             |
| `pop()`           | Mengambil & menghapus data terakhir (**pop**)       |
| `stack[-1]`       | Melihat data paling atas tanpa menghapus (**peek**) |
| `not bool(stack)` | Mengecek apakah stack kosong                        |
| `len(stack)`      | Mengecek total data dalam stack                     |

📝 Alur Singkat Eksekusi

Push A, B, C → ['A', 'B', 'C']

Pop menghapus 'C'

Stack sekarang → ['A', 'B']

Peek hasilnya 'B'

Stack tidak kosong → False

Ukuran stack → 2

🆚 Perbedaan Inti Stack vs Queue
| Struktur  | Prinsip                   | Ilustrasi        |
| --------- | ------------------------- | ---------------- |
| **Queue** | FIFO (First In First Out) | Antri beli tiket |
| **Stack** | LIFO (Last In First Out)  | Menumpuk piring  |




# Size
print("Size: ", len(queue))
