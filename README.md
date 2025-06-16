
# 📍 Panduan Install QGIS di Ubuntu 24.04 LTS

Dokumen ini memberikan langkah-langkah untuk menginstal **QGIS versi 3.14.x Pi** di Ubuntu 24.04 LTS.

---

## 🔧 1. Instal Alat Pendukung

```bash
sudo apt install gnupg software-properties-common
```

---

## 🔑 2. Tambahkan QGIS Signing Key

```bash
wget -qO - https://qgis.org/downloads/qgis-2020.gpg.key | sudo gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/qgis-archive.gpg --import

sudo chmod a+r /etc/apt/trusted.gpg.d/qgis-archive.gpg
```

> Ini penting agar sistem percaya pada paket QGIS yang diunduh dari repository resmi.

---

## 📦 3. Tambahkan Repository QGIS

```bash
sudo add-apt-repository "deb https://qgis.org/debian `lsb_release -c -s` main"
```

---

## 🔄 4. Perbarui Daftar Repository

```bash
sudo apt update
```

---

## 🧭 5. Instal QGIS

Untuk menginstal QGIS dan plugin GRASS:

```bash
sudo apt install qgis qgis-plugin-grass
```

Jika ingin sekaligus menginstal **QGIS Server**, gunakan:

```bash
sudo apt install qgis qgis-plugin-grass qgis-server
```

---

## ▶️ Menjalankan QGIS

Setelah instalasi selesai, jalankan aplikasi QGIS dengan perintah:

```bash
qgis
```

---

Semoga berhasil! 🚀
