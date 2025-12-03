# Tugas Frontend: React Fundamental (Show Data & Logic)

Repository ini berisi latihan dasar React.js menggunakan CDN. Fokus utama project ini adalah mempelajari cara manipulasi data array, rendering list (looping), dan penerapan logika kondisional (If-Else) di dalam komponen JSX.

## 📝 Implementasi Fitur

Berdasarkan instruksi latihan, berikut adalah fitur yang telah diselesaikan:

### 1. Show Data (Rendering Lists)
* Menambahkan properti gambar (`imgUrl`) pada data array.
* Menggunakan method `.map()` untuk me-looping data produk.
* Menampilkan gambar dan detail produk secara dinamis ke UI.

### 2. Conditional Rendering (Logic If-Else)
* Menambahkan properti `brand` pada data.
* Membuat logika deteksi Sistem Operasi (OS) otomatis:
    * Jika Brand **"Apple"** → OS set ke **"iOS"**.
    * Selain itu → OS set ke **"Android"**.
* Menampilkan label OS pada kartu produk.

---

## 💻 Cuplikan Kode (Snippet)

Logika utama untuk penentuan OS dan rendering gambar:

```javascript
function Product({ name, price, brand, imgUrl }) {
    // Logic menentukan OS
    let os = "";
    if (brand === "Apple") {
        os = "iOS";
    } else {
        os = "Android";
    }

    return (
        <div className="card">
            <img src={imgUrl} alt={name} />
            <h3>{name}</h3>
            <p>Brand: {brand} | OS: <b>{os}</b></p>
            {/* Logic harga & diskon lainnya... */}
        </div>
    );
}
