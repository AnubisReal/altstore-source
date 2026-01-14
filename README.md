# AnubisReal AltStore Source

Repositorio oficial de AltStore para distribuir aplicaciones de AnubisReal.

## 📱 Agregar este Source a AltStore

Para agregar este source a tu AltStore Classic:

1. Abre **AltStore** en tu dispositivo iOS
2. Ve a la pestaña **Browse**
3. Toca el ícono **+** en la esquina superior derecha
4. Ingresa la siguiente URL:
   ```
   https://raw.githubusercontent.com/AnubisReal/altstore-source/main/apps.json
   ```
5. Toca **Add** y listo

## 🔧 Configuración del Repositorio

### Estructura de Archivos

```
altstore-source/
├── apps.json                 # Configuración principal del source
├── README.md                 # Este archivo
├── .gitignore               # Archivos ignorados por git
└── assets/                  # Assets de las aplicaciones
    ├── icons/               # Iconos de apps
    │   └── aio-icon.png
    ├── screenshots/         # Capturas de pantalla
    │   ├── screenshot1.png
    │   └── screenshot2.png
    └── news/                # Imágenes para noticias
        └── welcome.png
```

### Cómo Actualizar el Source

#### 1. Modificar apps.json

Edita el archivo `apps.json` con la información de tu aplicación:

- **name**: Nombre de tu app
- **bundleIdentifier**: `com.anubisreal.aio` (ya configurado)
- **developerName**: Tu nombre o nombre del desarrollador
- **subtitle**: Descripción corta
- **localizedDescription**: Descripción completa
- **versions**: Array de versiones disponibles

#### 2. Agregar el archivo .ipa

1. Sube tu archivo `.ipa` a GitHub Releases
2. Actualiza el `downloadURL` en `apps.json` con la URL del release
3. Actualiza el campo `size` con el tamaño del archivo en bytes
4. Opcional: Genera el hash SHA-256 y agrégalo al campo `sha256`

**Calcular SHA-256 del .ipa:**
```bash
# En macOS/Linux
shasum -a 256 tu-app.ipa

# En Windows (PowerShell)
Get-FileHash -Algorithm SHA256 tu-app.ipa
```

#### 3. Agregar Assets

- **Icono**: 512x512 px, formato PNG
- **Screenshots**: Resoluciones recomendadas de dispositivos iOS (1170x2532 para iPhone)
- Guarda los archivos en la carpeta `assets/` correspondiente
- Actualiza las URLs en `apps.json`

#### 4. Calcular el tamaño del .ipa

```bash
# En macOS/Linux
ls -l tu-app.ipa | awk '{print $5}'

# En Windows (PowerShell)
(Get-Item tu-app.ipa).length
```

### Hosting del Source

Este source está diseñado para ser alojado en **GitHub**. La URL del source será:

```
https://raw.githubusercontent.com/TU-USUARIO/altstore-source/main/apps.json
```

> **Nota**: Reemplaza `TU-USUARIO` con tu nombre de usuario de GitHub y asegúrate de que el repositorio sea público.

## 📝 Ejemplo de Versión

```json
{
  "version": "1.0.1",
  "date": "2026-01-15",
  "localizedDescription": "Nueva actualización con mejoras.\n\n• Nueva funcionalidad X\n• Mejoras en rendimiento\n• Corrección de bugs",
  "downloadURL": "https://github.com/AnubisReal/altstore-source/releases/download/v1.0.1/aio-1.0.1.ipa",
  "size": 10485760,
  "minOSVersion": "14.0",
  "sha256": "abc123def456..."
}
```

## 🎨 Personalización

### Colores

El campo `tintColor` acepta códigos hexadecimales de 6 caracteres (sin el #):
- Morado: `8A2BE2`
- Azul: `007AFF`
- Verde: `34C759`
- Rojo: `FF3B30`

### Noticias

Agrega noticias al array `news` en `apps.json` para mantener informados a tus usuarios sobre actualizaciones y anuncios.

## 🔗 Links Útiles

- [Documentación oficial de AltStore](https://faq.altstore.io/)
- [Formato de Source JSON](https://faq.altstore.io/distribute-your-apps/make-a-source)
- [AltStore en GitHub](https://github.com/rileytestut/AltStore)

## 📄 Licencia

Este repositorio es de código abierto. Puedes modificarlo según tus necesidades.

---

**Desarrollado por AnubisReal** 🚀
