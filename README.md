# Video Automate: web legal

Static legal website for Video Automate (privacy policy and terms of use), in Spanish and English.

Video Automate es una herramienta de uso personal que publica vídeos verticales generados con IA en las cuentas propias de su titular (YouTube Shorts, Instagram Reels y TikTok) y lee sus métricas. Las plataformas cuyas API usa piden una política de privacidad y unas condiciones públicas, y este repositorio las aloja.

Se publica con GitHub Pages en https://ackyer.github.io/video-automate-legal/

| Español | English | Contenido |
|---|---|---|
| `index.html` | `en.html` | Qué es la herramienta, quién la usa y contacto |
| `privacidad.html` | `privacy.html` | Política de privacidad |
| `terminos.html` | `terms.html` | Condiciones de uso |

## Antes de publicar

Las páginas llevan el marcador `{{CORREO_CONTACTO}}` donde va el correo de contacto público. Mientras siga en alguna página, no hay que publicarla. Para sustituirlo:

```
CORREO='...'   # el correo público de contacto
sed -i "s|{{CORREO_CONTACTO}}|$CORREO|g" *.html
```

## Reglas

- HTML y CSS en línea. Sin scripts, sin analítica, sin fuentes ni recursos externos. Los únicos enlaces externos son las políticas y los ajustes de las plataformas.
- Las URL llevan el nombre del archivo (por ejemplo, `/privacidad.html`) para evitar redirecciones.
- Si cambia lo que hace la herramienta, actualizar el texto y la fecha de última actualización en las dos versiones.
- Si TikTok pide verificar la propiedad de las URL, su archivo de firma se añade en la raíz de este repositorio.
- Este repositorio es público: no subir claves, tokens ni datos personales.
