# 📤 INSTRUCCIONES PARA SUBIR ARCHIVOS A GITHUB

## Archivo a Reemplazar:
✅ **sw.js** (Service Worker con nueva versión de caché)

---

## 🎯 OPCIÓN 1: Editar Directamente en GitHub (MÁS RÁPIDO)

### Paso 1: Ir a tu repositorio
1. Abre: https://github.com/HP-Camp/HPC2026

### Paso 2: Editar sw.js
1. Haz clic en el archivo **`sw.js`**
2. Haz clic en el **ícono del lápiz** (✏️) arriba a la derecha que dice "Edit this file"
3. **Selecciona TODO** el contenido (Cmd+A en Mac)
4. **Borra** todo el contenido
5. **Copia** el contenido del archivo `sw.js` que te descargaste
6. **Pega** en el editor de GitHub

### Paso 3: Hacer Commit
1. Baja hasta el final de la página
2. En "Commit changes" escribe: `Update service worker to v3`
3. Haz clic en **"Commit changes"**
4. Confirma en el diálogo que aparece

### Paso 4: Esperar
- Espera **1-2 minutos** para que GitHub Pages actualice

---

## 🎯 OPCIÓN 2: Subir Archivo Completo

### Paso 1: Eliminar el archivo anterior
1. Ve a tu repositorio: https://github.com/HP-Camp/HPC2026
2. Haz clic en **`sw.js`**
3. Haz clic en el **ícono de tres puntos** (⋯) o ícono de basura
4. Selecciona **"Delete file"**
5. Escribe mensaje: `Delete old sw.js`
6. Haz clic en **"Commit changes"**

### Paso 2: Subir el nuevo archivo
1. Ve a la página principal del repositorio
2. Haz clic en **"Add file"** → **"Upload files"**
3. **Arrastra** el archivo `sw.js` que descargaste
4. O haz clic en **"choose your files"** y selecciona `sw.js`
5. Escribe mensaje: `Add updated service worker v3`
6. Haz clic en **"Commit changes"**

---

## 📱 Después de Subir: Actualizar en el iPhone

### Método 1: Recargar sin caché (Safari)
1. Abre **Safari** en tu iPhone
2. Ve a tu página: `https://hp-camp.github.io/HPC2026/`
3. Toca y **mantén presionado** el botón de recargar (⟳) por 2 segundos
4. Si no aparece menú, desliza hacia abajo desde la barra de direcciones
5. Toca **"Recargar"** varias veces

### Método 2: Limpiar caché de Safari
1. Ve a **Ajustes** → **Safari**
2. Desplázate hacia abajo
3. Toca **"Borrar historial y datos de sitios web"**
4. Confirma
5. Abre Safari y ve a tu página de nuevo

### Método 3: Reinstalar la PWA (Si está en pantalla de inicio)
1. Mantén presionado el **ícono de la app** en la pantalla de inicio
2. Toca **"Eliminar app"**
3. Abre **Safari**
4. Ve a: `https://hp-camp.github.io/HPC2026/`
5. Toca el botón **Compartir** (cuadro con flecha hacia arriba)
6. Desplázate y toca **"Agregar a pantalla de inicio"**
7. Toca **"Agregar"**

---

## ✅ Verificar que Funcionó

Después de actualizar, verifica:
1. Los datos mostrados deben ser los más recientes
2. En la consola de Safari (si conectas tu iPhone al Mac) deberías ver:
   ```
   [SW] Instalando versión: v3
   [SW] Activando versión: v3
   ```

---

## ⚠️ Si NO se actualiza después de 5 minutos:

Agrega este código temporal al final de tu `index.html` (antes de `</body>`):

```html
<!-- BOTÓN DE EMERGENCIA - ELIMINAR DESPUÉS DE USAR -->
<button onclick="forceUpdate()" style="position:fixed;bottom:20px;right:20px;z-index:9999;background:#FF3B30;color:white;padding:15px 20px;border:none;border-radius:10px;font-size:16px;font-weight:bold;box-shadow:0 4px 12px rgba(0,0,0,0.3);">
  🔄 Actualizar App
</button>

<script>
function forceUpdate() {
  if (confirm('¿Limpiar caché y actualizar la app?')) {
    if ('serviceWorker' in navigator) {
      navigator.serviceWorker.getRegistrations().then(registrations => {
        registrations.forEach(registration => {
          registration.unregister();
        });
      });
      
      caches.keys().then(cacheNames => {
        return Promise.all(
          cacheNames.map(cacheName => caches.delete(cacheName))
        );
      }).then(() => {
        alert('✅ Caché limpiado. La página se recargará.');
        window.location.reload(true);
      });
    }
  }
}
</script>
```

Este botón rojo aparecerá en la esquina inferior derecha. Los usuarios pueden tocarlo para forzar la actualización.

---

## 🎓 Para Futuras Actualizaciones:

Cada vez que hagas cambios importantes:

1. Edita `sw.js`
2. Cambia la línea 3:
   ```javascript
   const CACHE_VERSION = 'v4';  // v3 → v4 → v5, etc.
   ```
3. Sube el archivo
4. Los usuarios verán la actualización automáticamente (o tendrán que recargar una vez)

---

## 🆘 ¿Necesitas Ayuda?

Si algo no funciona:
1. Verifica que el archivo `sw.js` esté en la raíz del repositorio (no en una carpeta)
2. Asegúrate que GitHub Pages esté activado
3. Revisa que la URL sea: `https://hp-camp.github.io/HPC2026/`
4. Espera al menos 2-3 minutos después de subir

---

¡Mucha suerte! 🚀
