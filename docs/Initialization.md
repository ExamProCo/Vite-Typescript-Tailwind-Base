## Initialize Vite.js

initialize a vite.js project in the current directory.
```sh
npm create vite@latest .
```

Options chosen:
```sh
◇  Current directory is not empty. Please choose how to proceed:
│  Ignore files and continue
│
◇  Package name:
│  vite-ts-tailwind-base
│
◇  Select a framework:
│  React
│
◇  Select a variant:
│  TypeScript
```

# Initialize Tailwind.css

```sh
npm install -D tailwindcss postcss autoprefixer
```

```sh
npx tailwindcss init -p
```
> This command didn't work on my system so I had to manually create the files below

tailwind.config.js

```sh
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```


postcss.config.js

```sh
export default {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
}
```

src/index.css

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Add Postcss

```sh
npm install -D @tailwindcss/postcss
```
