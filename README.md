# Enkapsulasi dalam Java 🚀

### 📚 **Deskripsi**
Enkapsulasi adalah konsep fundamental dalam **Pemrograman Berorientasi Objek (OOP)** yang memungkinkan pengembang melindungi data dari akses dan modifikasi langsung dari luar objek. Dengan enkapsulasi, kita dapat menyembunyikan implementasi detail suatu objek dan hanya menyediakan antarmuka yang aman untuk mengakses atau memodifikasinya.

Proyek ini menunjukkan cara penggunaan enkapsulasi dalam bahasa Java dengan contoh kelas `Person` yang menyimpan data pribadi seseorang, seperti nama, jenis kelamin, dan umur. Setiap atribut bersifat **private** dan hanya dapat diakses melalui metode **getter** dan **setter**.

### 🛠 **Fitur**
- **Getter & Setter**: Untuk mengakses dan memodifikasi atribut yang terenksapsulasi.
- **Validasi Input**: Cek nilai input yang diberikan ke `setter` untuk menjaga integritas data.
- **Output Terformat**: Menampilkan hasil informasi dengan format yang terstruktur.

### 🚩 **Kode Utama**
```java
// Class Person
public class Person {
    private String nama;
    private char jenisKelamin;
    private int umur;

    // Constructor
    public Person(String nama, char jenisKelamin, int umur) {
        this.nama = nama;
        this.jenisKelamin = jenisKelamin;
        this.umur = umur;
    }

    // Getter dan Setter dengan validasi
    public String getNama() { return nama; }
    public void setNama(String nama) { this.nama = nama; }

    public char getJenisKelamin() { return jenisKelamin; }
    public void setJenisKelamin(char jenisKelamin) {
        if (jenisKelamin == 'L' || jenisKelamin == 'P') {
            this.jenisKelamin = jenisKelamin;
        } else {
            System.out.println("Jenis kelamin tidak valid! Masukkan 'L' atau 'P'.");
        }
    }

    public int getUmur() { return umur; }
    public void setUmur(int umur) {
        if (umur > 0) {
            this.umur = umur;
        } else {
            System.out.println("Umur harus lebih besar dari 0.");
        }
    }
    
    public void tampilkanInfo() {
        System.out.println("Nama: " + this.nama);
        System.out.println("Jenis Kelamin: " + this.jenisKelamin);
        System.out.println("Umur: " + this.umur);
    }
}


// Class Main
public class Main {
    public static void main(String[] args) {
        // Membuat objek Person
        Person person = new Person("Anton", 'L', 32);

        // Tampilkan data awal
        System.out.println("Data Awal:");
        person.tampilkanInfo();

        // Mengubah nilai dengan setter
        person.setNama("Riko");
        person.setJenisKelamin('P');
        person.setUmur(21);

        // Tampilkan data setelah perubahan
        System.out.println("\nData Setelah Diubah:");
        person.tampilkanInfo();
        
        // Mencoba input invalid
        System.out.println("\nMencoba input yang tidak valid:");
        person.setJenisKelamin('X');
        person.setUmur(-5);
    }
}
```

### 🧩 **Bagaimana Cara Kerjanya?**

1. **Enkapsulasi Data**: Atribut dalam class `Person` bersifat `private`, artinya mereka hanya bisa diakses melalui metode `getter` dan `setter`. Ini melindungi data dari akses langsung dari luar class.

2. **Validasi Input**: Setter untuk `jenisKelamin` dan `umur` dilengkapi dengan validasi input. Hanya input yang valid yang akan diterima:
   - `jenisKelamin` harus berupa 'L' (Laki-laki) atau 'P' (Perempuan).
   - `umur` harus lebih besar dari 0.

3. **Error Handling**: Jika input tidak valid, program akan menampilkan pesan kesalahan:
   - Jika jenis kelamin yang dimasukkan bukan 'L' atau 'P', akan muncul pesan: "Jenis kelamin tidak valid! Masukkan 'L' atau 'P'."
   - Jika umur yang dimasukkan kurang dari atau sama dengan 0, akan muncul pesan: "Umur harus lebih besar dari 0."


### 📦 **Cara Menjalankan Program**

1. **Clone repository ini**:
   ```bash
   git clone https://github.com/username/repository-name.git

2. **Compile file:**

```bash
javac Person.java Main.jav
```

3.**Jalankan program:**

```bash
java Main
```

📊 Output
Berikut ini adalah contoh output yang dihasilkan dari program:

```bash
Salin kode
Data Awal:
Nama: Anton
Jenis Kelamin: L
Umur: 32

Data Setelah Diubah:
Nama: Riko
Jenis Kelamin: P
Umur: 21

Mencoba input yang tidak valid:
Jenis kelamin tidak valid! Masukkan 'L' atau 'P'.
Umur harus lebih besar dari 0.
```

### 💡 **Penjelasan**

- **Getter** dan **Setter** melindungi atribut pribadi dari manipulasi langsung, memberikan pengembang kontrol penuh atas bagaimana data dimanipulasi.
- Validasi dalam setter menjamin bahwa data yang disimpan tetap konsisten dan sesuai dengan aturan yang ditetapkan.
- **Enkapsulasi** ini berguna untuk menjaga integritas data dan meningkatkan keamanan dalam aplikasi besar.

### 👨‍💻 **Kontributor**

- [Lintang Rafi Adhi](https://github.com/LintangRafiAdhi) 😊



### **Penjelasan Format**:
1. **Blok kode**: Menggunakan tiga backticks (\`\`\`) untuk menandai blok kode agar tampilan perintah terminal dan output lebih terstruktur.
2. **Instruksi langkah demi langkah**: Disusun dalam urutan yang jelas untuk memudahkan pengguna dalam menjalankan program.
3. **Output Program**: Ditampilkan secara utuh agar pembaca tahu apa yang diharapkan ketika menjalankan kode.

