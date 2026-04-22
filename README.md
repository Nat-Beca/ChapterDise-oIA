# 🎨 Muro del Equipo — Git Workshop

Bienvenide al workshop de Git para diseñadores. Al final de esta sesión, habrás aprendido a clonar un repositorio, hacer cambios y subir tu contribución. Además, el resultado de todos juntos será esta página: **un muro con la tarjeta de cada persona del equipo**.

---

## 🚀 Tu misión

Agregar **tu propia tarjeta** al muro. Cada tarjeta tiene:
- Tu nombre y rol
- Tu color(es) favorito(s)
- Un dato curioso tuyo
- Un arte SVG único — generado con ayuda de Claude ✨

---

## 📋 Paso a paso

### 1. Clonar el repositorio

```bash
git clone <url-del-repo>
cd git-workshop
```

### 2. Crear tu rama

```bash
git checkout -b tarjeta/tu-nombre
```

> Ejemplo: `git checkout -b tarjeta/nataly`

### 3. Generar tu arte con Claude

Abre [claude.ai](https://claude.ai) y usa este prompt (personalízalo con tus datos):

```
Genera un SVG animado de 120x120px para una tarjeta de perfil.
Mi color favorito es [TU COLOR].
El arte debe reflejar algo sobre mí: [UNA PALABRA QUE TE DESCRIBA].
Solo devuelve el código SVG, sin explicaciones.
El SVG debe funcionar inline en HTML.
```

Copia el SVG que te dé Claude — lo usarás en el siguiente paso.

### 4. Agregar tu tarjeta al `index.html`

Abre `index.html` y busca el comentario:

```html
<!-- AGREGA TU TARJETA AQUÍ ↓ -->
```

Pega este bloque justo después y personalízalo:

```html
<article class="card" id="tu-nombre">
  <div class="card-art" style="background: linear-gradient(135deg, #COLOR1, #COLOR2);">
    <!-- Pega aquí el SVG que te generó Claude -->
  </div>
  <div class="card-info">
    <span class="card-role">TU ROL</span>
    <h2 class="card-name">Tu Nombre</h2>
    <p class="card-fact">Un dato curioso o frase que te represente.</p>
  </div>
</article>
```

### 5. Ver tu cambio en el navegador

Abre `index.html` directo en tu navegador — no necesitas servidor. ¡Verifica que se ve bien!

### 6. Guardar tu cambio con Git

```bash
# Ver qué archivos cambiaste
git status

# Agregar el archivo al commit
git add index.html

# Crear el commit con un mensaje descriptivo
git commit -m "feat: agrega tarjeta de [tu nombre]"

# Subir tu rama
git push origin tarjeta/tu-nombre
```

### 7. Crear un Pull Request

Ve al repositorio en GitHub y crea un Pull Request de tu rama hacia `main`. Pon como título: **"Tarjeta de [Tu Nombre]"**.

---

## 💡 Tips

| Situación | Solución |
|-----------|----------|
| No sé qué colores usar | Abre [coolors.co](https://coolors.co) y genera una paleta |
| Quiero otro tipo de arte | Pídele a Claude "un SVG de [flores / geometría / ondas / constelaciones]" |
| Git me pide usuario/contraseña | Usa un token de acceso personal (te lo explica el facilitador) |
| Hay conflicto en el PR | No entres en pánico — es normal y lo resolvemos juntos |

---

## 🏆 Comandos Git que aprendiste hoy

```
git clone      → Descargar un repositorio
git checkout   → Cambiar de rama (o crear una nueva con -b)
git status     → Ver qué archivos cambiaron
git add        → Preparar cambios para el commit
git commit     → Guardar los cambios con un mensaje
git push       → Subir tus cambios a GitHub
```

---

*Workshop facilitado por el equipo de Design Ops · Avaldigitallabs*
