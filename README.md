# 📱 Guardias HPC 2026

Aplicación web progresiva (PWA) para gestionar el calendario de guardias del Hospital Psiquiátrico de Campeche.

## 🚀 Archivos para Subir a GitHub

### Archivos Principales (OBLIGATORIOS):
1. **index.html** - Aplicación principal con botón de actualización incluido
2. **sw.js** - Service Worker (versión v3)
3. **manifest.json** - Configuración de la PWA

### Archivos de Iconos (OPCIONALES pero recomendados):
Si tienes los iconos, súbelos también:
- icon-72.png
- icon-96.png
- icon-128.png
- icon-144.png
- icon-152.png
- icon-192.png
- icon-384.png
- icon-512.png

## 📦 Cómo Subir a GitHub

### Opción 1: Interfaz Web (Más Fácil)

1. Ve a tu repositorio: https://github.com/HP-Camp/HPC2026
2. Para cada archivo:
   - Si existe: haz clic → editar (lápiz) → seleccionar todo → pegar nuevo contenido
   - Si no existe: Add file → Upload files → arrastra el archivo
3. Haz commit de cada cambio

### Opción 2: Git desde Terminal

```bash
# Clona el repositorio (si no lo tienes)
git clone https://github.com/HP-Camp/HPC2026.git
cd HPC2026

# Copia los archivos nuevos aquí
# (copia index.html, sw.js, manifest.json)

# Agrega los cambios
git add index.html sw.js manifest.json

# Haz commit
git commit -m "Update app to v3 with update button"

# Sube a GitHub
git push origin main
```

## ✨ Características Nuevas

### Botón de Actualización
- Ubicado en la esquina inferior derecha
- Color morado con gradiente
- Al tocarlo: limpia caché y actualiza automáticamente
- Puedes eliminarlo después de que todos actualicen

### Service Worker v3
- Gestión mejorada de caché
- Actualización automática
- Funciona offline

## 🔄 Actualizar en el Celular

Después de subir los archivos:

### Método 1: Reinstalar PWA (Más efectivo)
1. Mantén presionado el ícono de la app
2. Eliminar app
3. Safari → tu página → Compartir → Agregar a pantalla de inicio

### Método 2: Usar el botón de actualización
1. Abre la app
2. Toca el botón morado "Actualizar app"
3. Confirma
4. Espera a que recargue

### Método 3: Limpiar caché de Safari
1. Ajustes → Safari
2. Borrar historial y datos de sitios web
3. Vuelve a abrir la app

## 📝 Notas Importantes

- **Espera 1-2 minutos** después de hacer push para que GitHub Pages actualice
- El **botón de actualización** es temporal, puedes eliminarlo después
- Para eliminar el botón: edita `index.html` y borra el código entre los comentarios `<!-- BOTÓN DE ACTUALIZACIÓN -->` y `<!-- FIN BOTÓN DE ACTUALIZACIÓN -->`

## 🎯 Futuras Actualizaciones

Cada vez que hagas cambios importantes:

1. Edita `sw.js`
2. Cambia la línea 3:
   ```javascript
   const CACHE_VERSION = 'v4';  // incrementa: v3 → v4 → v5
   ```
3. Haz commit y push
4. Los usuarios verán la actualización automáticamente

## 🆘 Soporte

Si algo no funciona:
1. Verifica que todos los archivos estén en la raíz del repositorio (no en carpetas)
2. Asegúrate que GitHub Pages esté activado en Settings → Pages
3. La URL debe ser: https://hp-camp.github.io/HPC2026/

## 📊 Estructura de Archivos

```
HPC2026/
├── index.html          ← Aplicación principal
├── sw.js              ← Service Worker
├── manifest.json      ← Config PWA
├── icon-72.png        ← Iconos (opcionales)
├── icon-96.png
├── icon-128.png
├── icon-144.png
├── icon-152.png
├── icon-192.png
├── icon-384.png
└── icon-512.png
```

---

¿Preguntas? Revisa la sección de Issues en GitHub o contacta al administrador.
