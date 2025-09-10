# To-do Mini App

## 📖 Deskripsi
Aplikasi Flutter sederhana untuk mencatat daftar tugas (to-do).  
Fitur utama:
- Menambahkan tugas baru.
- Menandai tugas selesai/belum selesai.
- Menghapus tugas.
- Melihat daftar detail tugas di layar terpisah.

Tujuan aplikasi ini adalah mempraktikkan:
1. Perbedaan **Stateless** dan **Stateful** widget.
2. **State management** dengan `provider`.
3. Membuat **widget tree** yang rapi dan terstruktur.
4. Memisahkan kode ke dalam folder `models`, `providers`, `widgets`, dan `screens`.

---

## 🌳 Diagram Widget Tree (Sederhana)

lib/
 ├── main.dart
 ├── models/
 │     └── todo.dart      ✅ model doang, simple
 ├── providers/
 │     └── todo_provider.dart
 ├── widgets/
 │     ├── add_todo_dialog.dart
 │     └── todo_item.dart

Alasan

---

## ⚙️ Pendekatan State Management

- **Dipilih:** `Provider` dengan `ChangeNotifierProvider`  
- **Alasan:**
  1. `Provider` adalah paket resmi Flutter, sederhana, dan direkomendasikan untuk pemula.
  2. Cocok untuk aplikasi kecil seperti to-do, karena hanya ada satu model data (`Todo`).
  3. Memisahkan **logic state** (tambah, hapus, toggle) dari **UI**, sehingga kode lebih bersih dan mudah dibaca.
  4. UI otomatis **rebuild** setiap kali ada perubahan pada daftar todo, tanpa perlu memanggil `setState` manual di banyak tempat.
  5. `Consumer` hanya me-rebuild widget tertentu yang butuh update, lebih efisien daripada full rebuild.

---

## 📂 Struktur Project

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/acd58702-0751-4d93-b538-8f0dbd472bad" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d925d42c-83ec-4bb7-90b0-40965003926a" />


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b17ebb5e-3156-44c0-83d6-5b284d5e54d2" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/500cc1dc-b01c-4d86-8ab4-67a7c02174ba" />



