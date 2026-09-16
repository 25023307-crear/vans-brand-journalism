# Vans — El medio es el mensaje

Sitio web académico de **Brand Journalism** sobre Vans como empresa de calzado. El proyecto presenta la historia de la marca, su relación con el skateboarding, el modelo Old Skool, el proceso de fabricación, los materiales, los beneficios del producto, la comunidad, las fuentes de investigación y los datos de identificación académica de José Antonio Lorenzo Mora.

## 1. Requisitos previos

Antes de comenzar, instala las siguientes herramientas:

| Herramienta | Versión recomendada | Uso |
|---|---:|---|
| Node.js | 20 o superior | Ejecutar el entorno de desarrollo y las herramientas frontend |
| pnpm | 10.4.1 o superior | Instalar dependencias y ejecutar scripts |
| Git | Versión reciente | Clonar y administrar el repositorio |
| Navegador web | Chrome, Edge, Firefox o Safari actualizado | Visualizar el sitio |

También puedes utilizar **npm** si no tienes pnpm, aunque el proyecto está configurado originalmente para pnpm.

Para comprobar si ya tienes las herramientas instaladas, ejecuta:

```bash
node --version
pnpm --version
git --version
```

Si no tienes pnpm, instálalo con:

```bash
corepack enable
corepack prepare pnpm@10.4.1 --activate
```

## 2. Clonar el repositorio

Abre una terminal y cambia a la carpeta donde quieras guardar el proyecto. Después ejecuta:

```bash
git clone https://github.com/25023307-crear/vans-brand-journalism.git
cd vans-brand-journalism
```

Para confirmar que estás dentro del proyecto correcto, ejecuta:

```bash
git remote -v
git branch --show-current
```

La rama principal debe ser `main` y el remoto debe apuntar a:

```text
https://github.com/25023307-crear/vans-brand-journalism.git
```

> **Importante:** el repositorio es privado. Para clonarlo necesitas iniciar sesión en GitHub mediante Git Credential Manager, una clave SSH o un token personal con permisos de lectura.

## 3. Instalar las dependencias

Desde la carpeta raíz del proyecto, ejecuta:

```bash
pnpm install
```

Este comando instala React, Vite, TypeScript, Tailwind CSS, Lucide React y las demás dependencias declaradas en `package.json`.

Si utilizas npm, puedes ejecutar:

```bash
npm install
```

No es necesario instalar paquetes manualmente uno por uno.

## 4. Ejecutar el sitio en modo desarrollo

Inicia el servidor local con:

```bash
pnpm dev
```

También puedes utilizar:

```bash
npm run dev
```

Vite mostrará una dirección parecida a la siguiente:

```text
http://localhost:3000/
```

Abre esa dirección en tu navegador. El sitio utiliza **Hot Module Replacement**, por lo que los cambios en los archivos se reflejan automáticamente sin reiniciar el servidor.

Para detener el servidor, regresa a la terminal y presiona:

```text
Ctrl + C
```

## 5. Archivos principales del proyecto

La estructura más importante es la siguiente:

```text
vans-brand-journalism/
├── client/
│   ├── index.html                 Documento HTML principal
│   ├── public/
│   │   └── images/                Imágenes locales del sitio
│   │       ├── vans-hero.jpg
│   │       ├── vans-process.jpg
│   │       ├── vans-community.jpg
│   │       ├── store-front.jpg
│   │       ├── store-display.jpg
│   │       └── store-visit.jpg
│   └── src/
│       ├── App.tsx                Entrada de la aplicación React
│       ├── index.css              Sistema visual y diseño responsive
│       ├── main.tsx               Punto de montaje de React
│       ├── pages/
│       │   └── Home.tsx            Contenido completo de la página
│       ├── components/             Componentes reutilizables
│       ├── contexts/               Contextos de la aplicación
│       ├── hooks/                  Hooks personalizados
│       └── lib/                    Funciones auxiliares
├── docs/
│   └── investigacion-vans.md       Documento de investigación académica
├── .github/workflows/
│   └── deploy.yml                 Flujo opcional de GitHub Pages
├── CREDITS.md                     Fuentes y créditos de imágenes
├── package.json                   Scripts y dependencias
├── pnpm-lock.yaml                 Versiones bloqueadas de dependencias
├── tsconfig.json                  Configuración de TypeScript
└── vite.config.ts                 Configuración de Vite
```

## 6. Comprobar el código

Antes de entregar o publicar cambios, ejecuta la comprobación de TypeScript:

```bash
pnpm check
```

El resultado correcto debe terminar sin errores de TypeScript.

Si utilizas npm:

```bash
npm run check
```

## 7. Crear una compilación de producción

Genera una versión optimizada del sitio con:

```bash
pnpm build
```

El resultado se guarda en la carpeta:

```text
dist/
```

Para previsualizar localmente esa compilación, ejecuta:

```bash
pnpm preview
```

Después abre la dirección que muestre Vite, normalmente:

```text
http://localhost:4173/
```

La secuencia recomendada antes de publicar es:

```bash
pnpm install
pnpm check
pnpm build
pnpm preview
```

## 8. Modificar el contenido

La mayor parte del contenido editorial se encuentra en:

```text
client/src/pages/Home.tsx
```

En ese archivo puedes modificar:

- Títulos y subtítulos.
- Historia de Vans.
- Descripción del Old Skool.
- Pasos del proceso de fabricación.
- Beneficios funcionales y emocionales.
- Datos de identificación académica.
- Enlaces a fuentes y redes sociales.
- Texto de botones y llamadas a la acción.

Los estilos están en:

```text
client/src/index.css
```

Las imágenes se encuentran en:

```text
client/public/images/
```

Cuando reemplaces una imagen, conserva el mismo nombre de archivo o actualiza la constante correspondiente al inicio de `Home.tsx`.

## 9. Actualizar el proyecto desde GitHub

Si ya tienes una copia local y quieres descargar los cambios más recientes:

```bash
git checkout main
git pull origin main
pnpm install
pnpm dev
```

## 10. Guardar y subir cambios

Después de modificar el proyecto, revisa los archivos cambiados:

```bash
git status
git diff
```

Valida y compila:

```bash
pnpm check
pnpm build
```

Después crea un commit y súbelo a GitHub:

```bash
git add .
git commit -m "Actualizar contenido del sitio Vans"
git push origin main
```

Es recomendable utilizar mensajes de commit claros, por ejemplo:

```text
Actualizar datos académicos
Agregar fotografías del estudiante
Corregir diseño responsive
Actualizar fuentes de investigación
```

## 11. Publicar con GitHub Pages

El proyecto incluye un workflow en:

```text
.github/workflows/deploy.yml
```

Para utilizarlo:

1. Abre el repositorio en GitHub.
2. Entra a **Settings**.
3. Selecciona **Pages**.
4. En **Build and deployment**, elige **GitHub Actions**.
5. Verifica que el workflow pueda ejecutarse en la rama `main`.
6. Revisa la pestaña **Actions** para confirmar el resultado.

Para un repositorio llamado `vans-brand-journalism`, la dirección esperada sería parecida a:

```text
https://25023307-crear.github.io/vans-brand-journalism/
```

El workflow utiliza `VITE_BASE_PATH` para que los recursos locales funcionen dentro de la ruta del repositorio.

> **Nota sobre permisos:** si GitHub rechaza la subida del workflow, la credencial utilizada necesita el permiso `workflow`. En ese caso, sube primero el código sin el workflow o autoriza el permiso adicional en GitHub.

> **Nota sobre repositorios privados:** la disponibilidad de GitHub Pages para repositorios privados depende del plan de GitHub y de la configuración de la cuenta. Si GitHub no permite publicar este repositorio privado, cambia su visibilidad a pública o utiliza una cuenta/plan compatible.

## 12. Solución de problemas frecuentes

### El comando `pnpm` no existe

Activa Corepack e instala la versión recomendada:

```bash
corepack enable
corepack prepare pnpm@10.4.1 --activate
```

### El puerto 3000 está ocupado

Detén el proceso que utiliza el puerto o ejecuta Vite con otro puerto:

```bash
pnpm dev -- --port 3001
```

Después abre:

```text
http://localhost:3001/
```

### Las imágenes no aparecen

Confirma que existan los seis archivos dentro de:

```text
client/public/images/
```

También verifica que `Home.tsx` utilice rutas con `import.meta.env.BASE_URL` y que los nombres de los archivos coincidan exactamente, incluyendo mayúsculas y minúsculas.

### La compilación falla después de cambiar una imagen

Revisa que la imagen no esté corrupta y que tenga formato `.jpg` o `.png`. Después ejecuta:

```bash
pnpm check
pnpm build
```

### GitHub Pages muestra una pantalla en blanco

Revisa que el workflow haya terminado correctamente en **Actions** y que `VITE_BASE_PATH` tenga el nombre correcto del repositorio. Para un repositorio de proyecto debe incluir la ruta, por ejemplo:

```text
/vans-brand-journalism/
```

### GitHub solicita autenticación al clonar

El repositorio es privado. Configura una clave SSH o utiliza GitHub CLI:

```bash
gh auth login
gh repo clone 25023307-crear/vans-brand-journalism
```

## 13. Alcance del formulario

El formulario de participación funciona como una interacción visual en el navegador y muestra un mensaje de confirmación. Esta versión es un sitio estático y no guarda respuestas en una base de datos. Para almacenar participaciones reales, conecta el formulario con Formspree, Google Forms, Netlify Forms o un backend propio.

## 14. Créditos y uso académico

Las fuentes y créditos de imágenes están documentados en [`CREDITS.md`](./CREDITS.md). La investigación complementaria se encuentra en [`docs/investigacion-vans.md`](./docs/investigacion-vans.md).

Vans, Old Skool, Sidestripe y otros nombres de producto son marcas de sus respectivos titulares. Este proyecto es una entrega académica independiente y no es un sitio oficial de Vans.

## 15. Datos de identificación incluidos

| Campo | Información |
|---|---|
| Estudiante | José Antonio Lorenzo Mora |
| Matrícula | 25023307 |
| Asesor | Mtro. Daniel Rivera Nieto |
| Módulo | Creación de marca y posicionamiento |
| Reto | Reto 3 · El medio es el mensaje |
| Fecha | 15 de septiembre de 2026 |
