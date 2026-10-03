# Flujo de Agenda · Propuesta

Sitio estático de dos páginas, con la marca KBZ aplicada. No usa framework ni necesita build.

```
index.html          Flujo paso a paso         →  /
diagramas.html      Diagramas de flujo        →  /diagramas
assets/             Monograma, wordmark e íconos
vercel.json         URLs limpias, cabeceras y caché
```

## Publicar en Vercel

**Opción A: CLI**

```bash
npm i -g vercel
cd flujo-agenda
vercel          # vista previa
vercel --prod   # producción
```

Cuando pregunte por el framework, elige **Other**. Deja vacíos el build command y el output directory.

**Opción B: desde Git**

1. Sube esta carpeta a un repositorio de GitHub o Bitbucket.
2. En vercel.com → Add New → Project, importa el repositorio.
3. Framework Preset: **Other**. Sin build command. Output directory: la raíz.

## Notas

- La página está marcada `noindex` (en la meta y en la cabecera `X-Robots-Tag`) porque es un borrador para el cliente. Quítalo de los dos lugares si quieres que Google la indexe.
- Las fuentes vienen de Google Fonts y los diagramas usan Mermaid desde cdnjs, así que la página necesita conexión a internet.
- Para probar en local: `npx serve .` y abre http://localhost:3000.
