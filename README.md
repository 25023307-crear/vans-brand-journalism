# Vans — El medio es el mensaje

Sitio web académico de **Brand Journalism** sobre Vans como empresa de calzado. La experiencia presenta su historia, relación con el skateboarding, producto representativo, proceso de fabricación, materiales, beneficios, comunidad, fuentes y datos de identificación del estudiante.

## Tecnologías

- React 19
- TypeScript
- Vite
- Tailwind CSS 4
- Lucide React
- GitHub Pages mediante GitHub Actions

## Requisitos

- Node.js 20 o superior
- pnpm 10 o npm compatible
- Git

## Ejecutar localmente

```bash
pnpm install
pnpm dev
```

Abre la URL local que muestre Vite, normalmente `http://localhost:3000`.

## Comprobar y compilar

```bash
pnpm check
pnpm build
pnpm preview
```

La compilación final se genera en `dist/`.

## Publicar en GitHub Pages automáticamente

1. Crea un repositorio nuevo en GitHub.
2. Sube todo el contenido de este proyecto a la rama `main`.
3. En GitHub, abre **Settings → Pages**.
4. En **Build and deployment**, selecciona **GitHub Actions**.
5. El archivo `.github/workflows/deploy.yml` compilará y publicará el sitio automáticamente después de cada `push` a `main`.
6. La URL será parecida a:

   `https://TU-USUARIO.github.io/NOMBRE-DEL-REPOSITORIO/`

### Comandos para subir el proyecto

```bash
git init
git add .
git commit -m "Publicar sitio académico de Vans"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/NOMBRE-DEL-REPOSITORIO.git
git push -u origin main
```

El workflow usa `VITE_BASE_PATH` para que las imágenes y recursos funcionen dentro de una URL de repositorio. Si se utiliza un repositorio de usuario con URL `TU-USUARIO.github.io`, cambia el valor de `VITE_BASE_PATH` en el workflow a `/`.

## Estructura importante

```text
client/
  public/images/       Imágenes locales del sitio
  src/pages/Home.tsx   Contenido y estructura de la página
  src/index.css        Diseño visual responsive
  src/App.tsx          Entrada de la aplicación
.github/workflows/     Publicación automática en GitHub Pages
vite.config.ts         Configuración portable de Vite
package.json           Scripts y dependencias
CREDITS.md             Créditos de imágenes y fuentes
```

## Nota sobre el formulario

El formulario de participación funciona como interacción visual en el navegador y muestra un mensaje de confirmación. No guarda respuestas en un servidor porque esta versión es un sitio estático. Para almacenar respuestas, conecta el formulario a Formspree, Google Forms o un backend propio.

## Nota académica

El sitio fue preparado como entrega académica. Vans es una marca de VF Corporation. El sitio no es oficial ni representa una relación comercial con Vans.
