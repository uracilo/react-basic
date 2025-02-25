# 🚀 Proyecto con Vite + React + TypeScript

Este documento proporciona los primeros pasos para configurar un proyecto web usando Vite, React y TypeScript.

## 📌 Requisitos previos
Antes de comenzar, asegúrate de tener instalado lo siguiente en tu sistema:
- [Node.js](https://nodejs.org/) (versión recomendada: LTS)
- [npm](https://www.npmjs.com/)
- [Git](https://git-scm.com/)

## 🌍 Crear un repositorio en GitHub
Para administrar tu código en GitHub, sigue estos pasos:

1. Accede a [GitHub](https://github.com/) e inicia sesión.
2. Haz clic en `New Repository` para crear un nuevo repositorio.
3. Asigna el nombre `fiesta-de-cumpleanios` y elige la opción `Public` o `Private`, según prefieras.
4. No selecciones ninguna opción de inicialización (`README.md`, `.gitignore`, etc.).
5. Haz clic en `Create repository`.
6. Copia el enlace del repositorio recién creado.

## 🛠️ Crear el proyecto
Ejecuta el siguiente comando en tu terminal para crear un nuevo proyecto con Vite:

```sh
npm create vite@latest fiesta-de-cumpleanios --template react-ts
```

Esto generará una estructura básica del proyecto con React y TypeScript.

## 📂 Estructura del proyecto
Después de la instalación, tu proyecto tendrá la siguiente estructura:

```
fiesta-de-cumpleanios/
│── node_modules/
│── public/
│── src/
│   │── App.tsx
│   │── main.tsx
│   │── assets/
│   │── components/
│── .gitignore
│── index.html
│── package.json
│── tsconfig.json
│── vite.config.ts
```

## 📦 Instalar dependencias
Dirígete a la carpeta del proyecto e instala las dependencias:

```sh
cd fiesta-de-cumpleanios
npm install
```

### 📌 Agregar Bootstrap
Para incluir Bootstrap en el proyecto, instala los paquetes necesarios:

```sh
npm install bootstrap
```

Luego, importa Bootstrap en `main.tsx`:

```ts
import 'bootstrap/dist/css/bootstrap.min.css';
import 'bootstrap/dist/js/bootstrap.bundle.min';
```

## 🔗 Vincular el repositorio con GitHub
Después de haber creado el repositorio en GitHub, enlázalo con tu proyecto local:

```sh
cd fiesta-de-cumpleanios
git init
```

Agrega el repositorio remoto:

```sh
git remote add origin git@github.com:tu-usuario/fiesta-de-cumpleanios.git
```

Añade los archivos y realiza el primer commit:

```sh
git add .
git commit -m "Primer commit"
```

Sube los cambios al repositorio en GitHub:

```sh
git branch -M main
git push -u origin main
```

## 🚀 Ejecutar el servidor de desarrollo
Para iniciar el servidor de desarrollo, usa:

```sh
npm run dev
```

Esto iniciará un servidor en `http://localhost:5173/` (por defecto).

## 🛠 Configuración adicional
### 🏗️ Configuración de alias
Para definir alias en `tsconfig.json` y `vite.config.ts`, agrega lo siguiente:

**`tsconfig.json`**:
```json
{
  "compilerOptions": {
    "baseUrl": "./",
    "paths": {
      "@components/*": ["src/components/*"]
    }
  }
}
```

**`vite.config.ts`**:
```ts
import { defineConfig } from 'vite';
import react from '@vitejs/plugin-react';
import path from 'path';

export default defineConfig({
  plugins: [react()],
  resolve: {
    alias: {
      '@components': path.resolve(__dirname, 'src/components')
    }
  }
});
```

## 📦 Construcción para producción
Para generar una versión optimizada del proyecto, ejecuta:

```sh
npm run build
```

El código optimizado estará en la carpeta `dist/`.

## 🔧 Desplegar el proyecto
Puedes desplegar el contenido de `dist/` en cualquier hosting estático como:
- Vercel
- Netlify
- GitHub Pages

## 🎉 ¡Listo!
Ahora tienes un proyecto en React con TypeScript y Vite configurado. ¡Disfruta codificando! 🚀

