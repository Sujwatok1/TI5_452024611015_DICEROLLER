# 🎲 Dice Roller

**Tugas Pemrograman Perangkat Bergerak**

Aplikasi Android sederhana untuk melempar dadu secara acak, dibangun menggunakan **Kotlin** dan **Jetpack Compose**.

---

## ✨ Fitur

- 🎲 **Lempar Dadu** — Tekan tombol "Roll" untuk menghasilkan angka dadu acak (1–6)
- 🖼️ **Gambar Dadu** — Menampilkan gambar dadu yang sesuai dengan hasil lemparan
- 📱 **UI Modern** — Menggunakan Jetpack Compose dengan Material Design 3
- 🎯 **Responsif** — Tampilan di tengah layar, cocok untuk berbagai ukuran perangkat

---

## 🛠️ Teknologi

| Komponen | Versi |
|----------|-------|
| Android Gradle Plugin | 9.1.0 |
| Kotlin | 2.2.10 |
| Compile SDK | 36 |
| Min SDK | 24 (Android 7.0) |
| Target SDK | 36 |
| Jetpack Compose BOM | 2026.02.01 |
| Material Design | 3 (Material3) |

---

## 📂 Struktur Proyek

```
Dice-Roller/
├── app/
│   ├── build.gradle.kts          # Konfigurasi build aplikasi
│   └── src/
│       └── main/
│           ├── AndroidManifest.xml
│           ├── java/com/example/diceroller/
│           │   └── MainActivity.kt   # Logika utama aplikasi
│           └── res/
│               ├── drawable/         # Gambar dadu (dice_1 s/d dice_6)
│               └── values/
│                   └── strings.xml   # String resource
├── build.gradle.kts              # Konfigurasi build root
├── settings.gradle.kts           # Pengaturan project
├── gradle/
│   └── libs.versions.toml        # Version catalog dependencies
├── gradlew / gradlew.bat         # Gradle wrapper
└── README.md                     # Dokumentasi proyek
```

---

## 🚀 Cara Menjalankan

### Prasyarat
- Android Studio (versi terbaru direkomendasikan)
- JDK 11 atau lebih tinggi
- Android SDK dengan API Level 36

### Langkah-langkah

1. **Clone repository**
   ```bash
   git clone https://github.com/NaufalAhnafussidqi/Dice-Roller.git
   cd Dice-Roller
   ```

2. **Buka di Android Studio**
   - Pilih **File → Open** dan arahkan ke folder proyek
   - Tunggu Gradle sync selesai

3. **Jalankan aplikasi**
   - Hubungkan perangkat Android atau buka emulator
   - Klik tombol **Run** (▶️) atau tekan `Shift + F10`

---

## 📝 Penjelasan Kode

### `MainActivity.kt`

File utama aplikasi yang berisi:

- **`DiceRollerApp()`** — Composable root yang mengatur tata letak utama
- **`DiceWithButtonAndImage()`** — Composable yang menampilkan:
  - **Image** — Gambar dadu sesuai hasil lemparan
  - **Spacer** — Jarak antara gambar dan tombol
  - **Button** — Tombol "Roll" untuk memicu lemparan dadu acak

### Logika Dadu

```kotlin
var result by remember { mutableStateOf(1) }

val imageResource = when (result) {
    1 -> R.drawable.dice_1
    2 -> R.drawable.dice_2
    3 -> R.drawable.dice_3
    4 -> R.drawable.dice_4
    5 -> R.drawable.dice_5
    else -> R.drawable.dice_6
}

Button(onClick = { result = (1..6).random() }) {
    Text(text = "Roll")
}
```

---

## 👤 Author

**Anasufi Ajwa Nazli Nailulhaq**

---

## 📄 Lisensi

Proyek ini dibuat untuk keperluan tugas pemrograman perangkat bergerak.
