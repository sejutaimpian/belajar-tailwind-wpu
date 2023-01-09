# Catatan/Rangkumanku saat belajar

<details>
  <summary>Daftar Isi</summary>
  <ol>
    <li>
        <a href="#1-apa-itu-tailwindcss">Apa itu TailwindCSS</a>
    </li>
    <li>
        <a href="#2-kenapa-tailwindcss">Kita Butuh Prettier</a>
    </li>
    <li>
        <a href="#3-instalasi-dan-konfigurasi">Instalasi dan Konfigurasi</a>
    </li>
  </ol>
</details>

## 1. Apa itu TailwindCSS

- TailwindCSS: A utility-first CSS framework packed with classes.
  `Rapidly build modern websites without ever leaving your HTML.`
- Utility-first CSS merujuk kepada class-class yang terdapat pada Tailwind hanya class utility, dan bukan component.

```
// Contoh Utility CSS
<button class='p-2 rounded'>Login</button>

// Contoh Component CSS
<button class='btn'>Login</button>
```

- Features

  - Interactivity

  ```
  <button class='p-2 rounded hover:bg-sky-600'>Login</button>
  ```

  - Responsive Design

  ```
  <button class='p-2 rounded md:p-4'>Login</button>
  ```

  - Dark Mode

  ```
  <button class='p-2 rounded dark:bg-gray-800'>Login</button>
  ```

  - Reusablity
  - Custom Style
  - Functions & Directives

<p align="right"><a href="#catatanrangkumanku-saat-belajar">Go 🔝</a></p>

## 2. Kenapa TailwindCSS

- Latar belakang dibuatnya Tailwindcss

<p align="right"><a href="#catatanrangkumanku-saat-belajar">Go 🔝</a></p>

## 3. Instalasi dan Konfigurasi

- Didalam dokumentasinya, Tailwind menyediakan 4 tabs untuk berbagai cara instalasi.
- Jika untuk belajar, boleh menggunakan play CDN, dan ini tidak cocok untuk production.
- Jika menggunakan framework, pilih tabs Framework Guide.
- Untuk Instalasi Tailwind tersendiri, bisa menggunakan Tailwind CLI
- Karena kita akan menggunakan npm untuk instalasinya, maka sebaiknya `npm init -y` terlebih dahulu

Install Tailwind dan Buat file Tailwind config

```
npm install -D tailwindcss
npx tailwindcss init
```

Konfigurasi path Tailwind

```
content: ["./public/**/*.{html,js}"],
```

Start the Tailwind CLI build process

```
npx tailwindcss -i ./src/css/input.css -o ./public/css/style.css --watch
```

Buat file index.html di folder public lalu importkan css tailwind yang style.css

```
<link rel="stylesheet" href="css/style.css">
```

Tailwind siap digunakan

- Memindahkan command tailwind watch ke dalam package.json

```
// Package.json
"scripts": {
    "dev": "npx tailwindcss -i ./src/css/input.css -o ./public/css/style.css --watch"
},

// Pemanggilan
npm run dev
```

- File Tailwind dapat diminify

```
npx tailwindcss -o ./public/css/final.css --minify
```

<p align="right"><a href="#catatanrangkumanku-saat-belajar">Go 🔝</a></p>
