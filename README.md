# Vite React SWC TS Tailwind Template

["Hello, World" Preview](https://bissakov.github.io/react-calculator/)

### Installation

```bash
git clone https://github.com/bissakov/vite-react-swc-ts-tailwind-template.git
```

### Reproduce template

1. Create React template with SWC and TypeScript:

```bash
npm create vite@latest vite-react-swc-ts-tailwind-template --template react-swc-ts
cd vite-react-swc-ts-tailwind-template
npm install
```

2. Install TailwindCSS:

```bash
npm install -D tailwindcss postcss autoprefixer prettier prettier-plugin-tailwindcss
npx tailwindcss init -p
```

3. Configure the template paths inside the tailwind.config.js file:

```js
/** @type {import('tailwindcss').Config} */
export default {
  content: ["./src/**/*.{js,jsx,ts,tsx}"],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

4. Set up the Tailwind directives inside the ./src/styles/index.css file:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

5. Set the correct base in vite.config.js

```ts
import { defineConfig } from "vite";
import react from "@vitejs/plugin-react-swc";

// https://vitejs.dev/config/
export default defineConfig({
  base: "/vite-react-swc-ts-tailwind-template/",
  plugins: [react()],
});
```

6. Create Actions workflow for GitHub Pages.
