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

## 4. Basic Utility (1)

### Spacing & Sizing

|                                                 Style | Class                                                  |
| ----------------------------------------------------: | ------------------------------------------------------ |
|       [Padding](https://tailwindcss.com/docs/padding) | p-2 px-2 py-2 pt-2 pr-2 pb-2 pl-2 ...                  |
|         [Margin](https://tailwindcss.com/docs/margin) | m-2 mx-2 my-2 mt-2 mr-2 mb-2 ml-2 ...                  |
|   [Space Between](https://tailwindcss.com/docs/space) | space-x-2 space-y-2 ...                                |
|           [Width](https://tailwindcss.com/docs/width) | w-2 w-auto w-1/2 w-full w-screen w-min w-max w-fit ... |
|   [Min-Width](https://tailwindcss.com/docs/min-width) | min-w-0 min-w-full min-w-min min-w-max min-w-fit ...   |
|   [Min-Width](https://tailwindcss.com/docs/min-width) | min-w-0 min-w-full min-w-min min-w-max min-w-fit       |
|   [Max-Width](https://tailwindcss.com/docs/max-width) | max-w-0 max-w-full max-w-max max-w-max max-w-fit ...   |
|         [Height](https://tailwindcss.com/docs/height) | h-2 h-auto h-1/2 h-full h-screen h-min h-max h-fit ... |
| [Min-Height](https://tailwindcss.com/docs/min-height) | min-h-0 min-h-full min-h-min min-h-max min-h-fit       |
| [Max-Height](https://tailwindcss.com/docs/max-height) | max-h-0 max-h-full max-h-max max-h-max max-h-fit ...   |

### Typography

- [Font-family](https://tailwindcss.com/docs/font-family)
- [Font-size](https://tailwindcss.com/docs/font-size)
- [Font-smoothing](https://tailwindcss.com/docs/font-smoothing)
- [Font-style](https://tailwindcss.com/docs/font-style)
- [Font-weight](https://tailwindcss.com/docs/font-weight)
- [Text-align](https://tailwindcss.com/docs/text-align)
- ...

### Colors

- [Text-color](https://tailwindcss.com/docs/text-color)
- [Background-color](https://tailwindcss.com/docs/background-color)
- [Gradient-color-stops](https://tailwindcss.com/docs/gradient-color-stops)
- ...

<p align="right"><a href="#catatanrangkumanku-saat-belajar">Go 🔝</a></p>
