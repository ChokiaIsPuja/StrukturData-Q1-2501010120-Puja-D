# StrukturData-Q1-2501010120-Puja-D
## Identitas

- Nama: Kadek Puja Arya Putra
- NIM: 2501010120
- Kelas: D

---

## 1. Array vs Singly Linked List (Akses Data)

Array dapat diakses dalam waktu **O(1)** karena elemen disimpan di **memori kontinu**, sehingga alamat elemen bisa dihitung langsung menggunakan rumus offset dari base address.

Singly Linked List membutuhkan waktu **O(n)** karena data disimpan di **memori non-kontinu**, sehingga harus melakukan traversal dari head sampai node yang dituju melalui pointer `next`.

---

## 2. Kapan Linked List Lebih Efisien

Linked List lebih unggul pada operasi **insert dan delete di awal atau tengah data**.

- Array: perlu shifting elemen → O(n)
- Linked List: cukup ubah pointer → O(1) (jika node sudah diketahui)

Namun, pencarian posisi tetap O(n), sehingga keunggulan utama ada pada manipulasi node, bukan akses data.

---

## 3. Doubly Linked List

Struktur node terdiri dari:
- data
- pointer `next`
- pointer `prev`

Kelebihan:
- Bisa traversal dua arah
- Delete node lebih mudah

Kekurangan:
- Lebih boros memori karena ada tambahan pointer `prev`

---

## 4. Circular Linked List

Circular Linked List adalah linked list di mana node terakhir menunjuk kembali ke head, bukan NULL.

Contoh penggunaan:
- Round-robin scheduling pada sistem operasi
- Sistem antrian berputar (game turn-based)

Keunggulan: iterasi bisa berlanjut tanpa reset dari awal.

---

## 5. Dynamic Array (Python List)

Saat `append()` dilakukan:

- Jika kapasitas masih cukup → operasi O(1)
- Jika penuh:
  1. Membuat array baru dengan ukuran lebih besar
  2. Menyalin semua elemen lama (O(n))
  3. Menambahkan elemen baru

Meskipun ada resize O(n), secara rata-rata tetap **amortized O(1)**.

