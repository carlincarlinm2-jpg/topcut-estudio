# TopCut Estudio: cómo subirlo a Vercel

Es un sitio estático: un solo `index.html`. No necesita servidor ni base de datos; los videos se procesan en el navegador de cada persona.

## Opción A: sin programar (con GitHub)
1. Crea un repositorio nuevo en github.com (por ejemplo `topcut`).
2. En el repositorio, "Add file" → "Upload files" y arrastra `index.html` y `vercel.json`. Haz commit.
3. Entra a vercel.com → "Add New…" → "Project" → importa ese repositorio.
4. Framework Preset: **Other**. No cambies nada más y pulsa **Deploy**.
5. Vercel te da un enlace `https://tu-proyecto.vercel.app`. Cada vez que cambies el archivo en GitHub, se vuelve a publicar solo.

## Opción B: con la terminal
```
npm i -g vercel
cd carpeta-donde-descomprimiste
vercel        # la primera vez te pide iniciar sesión
vercel --prod
```

## Notas
- La exportación rápida usa WebCodecs: funciona en Chrome y Edge actuales (escritorio y Android) y en Safari reciente. Vercel sirve con HTTPS, que es obligatorio para esa función.
- Si un navegador no tiene el codificador rápido, la app graba en tiempo real automáticamente.
- Formatos recomendados para los clips: MP4 (H.264) o WebM. Los .MOV en HEVC de iPhone pueden no abrir en Chrome de Windows.
