# 📍 Panduan Install QGIS di Ubuntu 24.04 LTS

Dokumen ini memberikan langkah-langkah untuk menginstal QGIS (versi 3.14.x Pi) di Ubuntu 24.04 LTS.

---

## 🔧 1. Instal Alat Pendukung

```bash
sudo apt install gnupg software-properties-common

🔑 2. Tambahkan QGIS Signing Key

wget -qO - https://qgis.org/downloads/qgis-2020.gpg.key | sudo gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/qgis-archive.gpg --import

sudo chmod a+r /etc/apt/trusted.gpg.d/qgis-archive.gpg

    Ini penting agar sistem percaya pada paket QGIS yang diunduh dari repository resmi.

📦 3. Tambahkan Repository QGIS

sudo add-apt-repository "deb https://qgis.org/debian `lsb_release -c -s` main"

🔄 4. Perbarui Daftar Repository

sudo apt update

🧭 5. Install QGIS

sudo apt install qgis qgis-plugin-grass

    Kalau ingin install QGIS Server juga, tambahkan qgis-server:

sudo apt install qgis qgis-plugin-grass qgis-server

▶️ Menjalankan QGIS

Setelah instalasi selesai, jalankan aplikasi dengan mengetik:

qgis


