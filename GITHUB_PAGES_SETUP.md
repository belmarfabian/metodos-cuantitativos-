# Cómo publicar este libro en GitHub Pages

## ✅ Ya está configurado

El proyecto ya está listo para GitHub Pages:
- ✅ El libro se compila en la carpeta `docs/`
- ✅ El archivo `.nojekyll` está en `docs/` (necesario para GitHub Pages)
- ✅ El `.gitignore` está configurado correctamente

---

## 📋 Paso 1: Crear repositorio en GitHub

1. Ve a https://github.com/new
2. Nombre del repositorio: `metodos-cuantitativos` (o el que prefieras)
3. Descripción: "Manual de Métodos Cuantitativos para Ciencias Políticas y Sociales"
4. **Público** (para que GitHub Pages funcione gratis)
5. **NO** marcar "Add a README file" (ya tienes uno)
6. Click en **"Create repository"**

---

## 📤 Paso 2: Subir el proyecto a GitHub

Abre Git Bash o terminal en la carpeta del proyecto y ejecuta:

```bash
# Navegar a la carpeta del proyecto
cd "g:/My Drive/Manual cuanti/metodos_cuantitativos"

# Inicializar repositorio git (si no está inicializado)
git init

# Agregar todos los archivos
git add .

# Primer commit
git commit -m "Primera versión del libro"

# Conectar con tu repositorio de GitHub (reemplaza TU_USUARIO)
git remote add origin https://github.com/TU_USUARIO/metodos-cuantitativos.git

# Cambiar a rama main (si es necesario)
git branch -M main

# Subir al repositorio
git push -u origin main
```

---

## 🌐 Paso 3: Activar GitHub Pages

1. Ve a tu repositorio en GitHub
2. Click en **"Settings"** (configuración)
3. En el menú lateral, click en **"Pages"**
4. En **"Source"**, selecciona **"Deploy from a branch"**
5. En **"Branch"**, selecciona:
   - Branch: **main**
   - Folder: **/docs**
6. Click en **"Save"**

GitHub comenzará a publicar tu libro. Esto toma 1-2 minutos.

---

## 🎉 Paso 4: Ver tu libro publicado

Tu libro estará disponible en:

```
https://TU_USUARIO.github.io/metodos-cuantitativos/
```

(Reemplaza `TU_USUARIO` con tu nombre de usuario de GitHub)

---

## 🔄 Actualizar el libro en el futuro

Cuando hagas cambios al libro:

```bash
# 1. Recompilar el libro (desde R/RStudio)
bookdown::render_book("index.Rmd", "bookdown::gitbook")

# 2. Agregar cambios a git
git add .

# 3. Hacer commit
git commit -m "Actualización: [describe los cambios]"

# 4. Subir a GitHub
git push
```

GitHub Pages se actualizará automáticamente en 1-2 minutos.

---

## 🛠️ Comandos útiles

### Ver estado de git
```bash
git status
```

### Ver historial de commits
```bash
git log --oneline
```

### Deshacer cambios no guardados
```bash
git checkout .
```

### Ver URL del repositorio remoto
```bash
git remote -v
```

---

## ⚠️ Notas importantes

1. **Archivos ignorados**: Los siguientes archivos NO se subirán a GitHub (están en `.gitignore`):
   - `_book/` (antigua carpeta de compilación)
   - `_bookdown_files/`
   - `*_cache/`
   - `packages.bib` (se genera automáticamente)

2. **Carpeta `docs/`**: Esta SÍ se sube a GitHub porque contiene el libro compilado para GitHub Pages.

3. **No modificar `docs/` manualmente**: Esta carpeta se regenera cada vez que compilas el libro.

4. **Privacidad**: El repositorio es público. Si hay datos sensibles, NO los incluyas.

---

## 🆘 Solución de problemas

### Error: "remote origin already exists"
```bash
git remote remove origin
git remote add origin https://github.com/TU_USUARIO/metodos-cuantitativos.git
```

### Error: "GitHub Pages no se ve bien"
- Verifica que `.nojekyll` esté en la carpeta `docs/`
- Hard refresh del navegador (Ctrl+F5)
- Espera 2-3 minutos para que GitHub Pages se actualice

### El libro no se actualiza en GitHub Pages
- Verifica que hiciste `git push`
- En GitHub, ve a Actions para ver si hay errores
- La actualización puede tardar hasta 5 minutos

---

## 📧 Contacto

**Autor:** Fabián Belmar
**Repositorio:** https://github.com/TU_USUARIO/metodos-cuantitativos (actualiza con tu URL real)

---

**Fecha de configuración:** 17 de noviembre de 2025
