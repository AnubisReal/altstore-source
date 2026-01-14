# Imágenes de Noticias

Coloca aquí las imágenes para las noticias que aparecerán en AltStore.

## Especificaciones

- **Tamaño**: 1600x900 px (relación 16:9 recomendada)
- **Formato**: PNG o JPG
- **Tamaño de archivo**: Recomendado < 500KB

## Archivos

Nombra tus imágenes de forma descriptiva:
- `welcome.png` - Imagen de bienvenida (ya configurada)
- `update-1.0.1.png` - Para anuncio de actualización
- `feature-announcement.png` - Para nuevas características
- etc.

## Uso

Las imágenes de noticias se configuran en la sección `news` del archivo `apps.json`:

```json
{
  "title": "Título de la noticia",
  "identifier": "identificador-unico",
  "caption": "Descripción corta",
  "date": "2026-01-14",
  "tintColor": "8A2BE2",
  "imageURL": "https://raw.githubusercontent.com/TU-USUARIO/altstore-source/main/assets/news/tu-imagen.png",
  "notify": false
}
```

## Consejos

- Usa imágenes atractivas y profesionales
- Mantén un estilo visual consistente
- Optimiza las imágenes para web
- Usa `notify: true` solo para noticias importantes
