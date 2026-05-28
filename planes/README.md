# Planes recibidos

Acá se guardan los PDFs de los planes trimestrales que presenta cada área.

## Flujo

1. El director de cada área completa el formulario en la web (su área queda
   precargada según con qué usuario entra).
2. Mientras escribe, el borrador se guarda solo en su navegador (no se pierde
   si cierra y vuelve a entrar en la misma computadora).
3. Al terminar aprieta **"Enviar al CEO"** → el navegador genera el PDF del plan
   y lo descarga (elegir *Guardar como PDF* en el diálogo de impresión).
4. El director te manda ese PDF.
5. Vos (o Claude) lo sumás a esta carpeta `planes/` y hacés commit:

   ```
   git add planes/Plan-Creatividad-Q2-2026.pdf
   git commit -m "Plan de Creatividad Q2 2026"
   git push
   ```

Una vez commiteado, el PDF queda accesible desde el sitio en:
`https://facundocouyet.github.io/cascaradireccion-/planes/<archivo>.pdf`

## Por qué este paso es manual

El sitio es estático (GitHub Pages, sin servidor). El navegador no puede
escribir archivos en el repositorio por su cuenta. Para automatizar la
recepción habría que sumar un backend o un servicio externo (ej: Formspree
para que lleguen por mail, o Google Sheets). Si en algún momento querés eso,
se puede agregar.

## Convención de nombres

`Plan-<Area>-Q<n>-<año>.pdf` — ej: `Plan-Contenido-Q2-2026.pdf`
