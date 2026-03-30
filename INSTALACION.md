# 🚀 GUÍA DE INSTALACIÓN - PASO A PASO

## 📦 Archivos que Debes Subir

### ✅ Archivos OBLIGATORIOS (3):
1. **index.html** - La aplicación completa (con botón de actualización incluido)
2. **sw.js** - Service Worker versión 3
3. **manifest.json** - Configuración de la PWA

### 📱 Archivos OPCIONALES:
- Iconos (icon-72.png, icon-96.png, etc.) - Si ya los tienes, manténlos. Si no, no son críticos.

---

## 🎯 MÉTODO RÁPIDO: Reemplazar 3 Archivos

### Paso 1: Ir a GitHub
1. Abre tu navegador
2. Ve a: **https://github.com/HP-Camp/HPC2026**
3. Inicia sesión si es necesario

---

### Paso 2: Reemplazar index.html

#### 2.1 Abrir el archivo
1. Haz clic en **`index.html`** en la lista de archivos
2. Haz clic en el **ícono del lápiz** ✏️ (Edit this file)

#### 2.2 Reemplazar contenido
1. Presiona **Cmd+A** (seleccionar todo)
2. Presiona **Delete** (borrar todo)
3. Abre el archivo **`index.html`** que descargaste
4. **Cmd+A** → **Cmd+C** (copiar todo)
5. Regresa a GitHub
6. **Cmd+V** (pegar)

#### 2.3 Guardar
1. Baja hasta "Commit changes"
2. Escribe: `Update index.html with update button`
3. Haz clic en **"Commit changes"**
4. Confirma en el diálogo

---

### Paso 3: Reemplazar sw.js

#### 3.1 Abrir el archivo
1. Regresa a la página principal del repo
2. Haz clic en **`sw.js`**
3. Haz clic en el **ícono del lápiz** ✏️

#### 3.2 Reemplazar contenido
1. **Cmd+A** → **Delete**
2. Abre el archivo **`sw.js`** que descargaste
3. **Cmd+A** → **Cmd+C**
4. Regresa a GitHub
5. **Cmd+V**

#### 3.3 Guardar
1. Commit message: `Update service worker to v3`
2. **"Commit changes"**

---

### Paso 4: Reemplazar manifest.json

#### 4.1 Abrir el archivo
1. Regresa a la página principal
2. Haz clic en **`manifest.json`**
3. Haz clic en el **ícono del lápiz** ✏️

#### 4.2 Reemplazar contenido
1. **Cmd+A** → **Delete**
2. Abre **`manifest.json`** descargado
3. **Cmd+A** → **Cmd+C**
4. Regresa a GitHub
5. **Cmd+V**

#### 4.3 Guardar
1. Commit message: `Update manifest.json`
2. **"Commit changes"**

---

## ⏰ Esperar

**Espera 2-3 minutos** para que GitHub Pages actualice.

Verás que el último commit dice "now" o hace unos minutos en la página principal.

---

## 📱 Actualizar en el iPhone

### ✅ OPCIÓN 1: Reinstalar la App (MÁS EFECTIVA)

1. Busca el ícono de **"Guardias HPC"** en tu pantalla de inicio
2. **Mantén presionado** el ícono (2-3 segundos)
3. Toca **"Eliminar App"**
4. Confirma **"Eliminar"**
5. Abre **Safari**
6. Ve a: `https://hp-camp.github.io/HPC2026/`
7. **Espera** a que cargue completamente
8. Toca el botón **Compartir** 📤 (centro inferior)
9. Desplázate y toca **"Agregar a pantalla de inicio"**
10. Toca **"Agregar"**

✅ **¡Listo! Ahora tienes la versión actualizada**

---

### ✅ OPCIÓN 2: Usar el Botón de Actualización

1. Abre la app desde la pantalla de inicio
2. Busca el **botón morado** en la esquina inferior derecha
3. Dice: **"Actualizar app"**
4. Tócalo
5. Confirma en el diálogo
6. Espera a que recargue

---

### ✅ OPCIÓN 3: Limpiar Caché de Safari

1. Ve a **Ajustes** del iPhone
2. Desplázate y toca **Safari**
3. Desplázate hasta encontrar **"Borrar historial y datos de sitios web"**
4. Tócalo
5. Confirma **"Borrar historial y datos"**
6. Abre Safari
7. Ve a tu página: `https://hp-camp.github.io/HPC2026/`

---

## ✅ Verificar que Funcionó

Después de actualizar, verifica:

1. **El botón morado debe aparecer** en la esquina inferior derecha
2. **Los datos deben ser los más recientes**
3. **La app debe funcionar sin problemas**

---

## 🗑️ Eliminar el Botón (Opcional - Después)

Una vez que todos hayan actualizado (en unos días), puedes eliminar el botón:

1. Edita **`index.html`** en GitHub
2. Busca: `<!-- BOTÓN DE ACTUALIZACIÓN -->`
3. **Elimina** todo desde ahí hasta: `<!-- FIN BOTÓN DE ACTUALIZACIÓN -->`
4. Guarda el cambio
5. Incrementa la versión en **`sw.js`** a `v4`

---

## 🆘 Solución de Problemas

### No veo el botón morado
- Espera 3-5 minutos más
- Elimina y reinstala la app
- Verifica que subiste el `index.html` correcto

### La app no se actualiza
- Prueba con OPCIÓN 1 (Reinstalar)
- Es el método más confiable

### Error al subir archivos
- Verifica que estés en la rama correcta (main)
- Asegúrate de tener permisos de escritura
- Intenta refrescar la página de GitHub

---

## 📊 Checklist Final

- [ ] Subí `index.html`
- [ ] Subí `sw.js`
- [ ] Subí `manifest.json`
- [ ] Esperé 2-3 minutos
- [ ] Eliminé la app del iPhone
- [ ] Reinstalé la app desde Safari
- [ ] Veo el botón morado
- [ ] Los datos son correctos
- [ ] Todo funciona bien

---

¡Éxito! 🎉

Si tienes dudas, revisa el archivo README.md incluido.
