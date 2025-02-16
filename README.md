# README

## Proyek Laravel dengan Tailwind CSS, Flowbite, dan NPM

### Persyaratan
Pastikan Anda telah menginstal perangkat lunak berikut sebelum memulai:
- PHP (>= 8.0)
- Composer
- Node.js & npm
- Laravel (>= 11)
- TablePlus
- Laragon atau Herd
- MySQL atau PostgreSQL (opsional, tergantung kebutuhan database)

### Instalasi
```sh
# Kloning repositori
git clone https://github.com/username/proyek-laravel.git
cd proyek-laravel

# Instal dependensi PHP dengan Composer
composer install

# Buat file konfigurasi .env
cp .env.example .env

# Generate aplikasi key
php artisan key:generate

# Migrasi dan seeding database (opsional)
php artisan migrate --seed

# Instal dependensi frontend menggunakan npm
npm install

# Instal Tailwind CSS dan Flowbite
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
npm install flowbite
```

### Konfigurasi Tailwind CSS
Edit file `tailwind.config.js` untuk menambahkan Flowbite:
```js
module.exports = {
  content: [
    "./resources/**/*.blade.php",
    "./resources/**/*.js",
    "./resources/**/*.vue",
    "./node_modules/flowbite/**/*.js"
  ],
  theme: {
    extend: {},
  },
  plugins: [require('flowbite/plugin')],
}
```

### Kompilasi Aset Frontend
```sh
# Untuk mode pengembangan
npm run dev

# Untuk produksi
npm run build
```

### Jalankan Server Lokal
```sh
php artisan serve
```
Akses proyek melalui `http://127.0.0.1:8000`

### Penggunaan
```sh
# Membuat model dan migrasi
php artisan make:model NamaModel -m

# Melihat daftar rute
php artisan route:list

# Menjalankan mode pengawasan untuk perubahan frontend
npm run watch
```

### Lisensi
Proyek ini menggunakan lisensi [MIT](LICENSE).

