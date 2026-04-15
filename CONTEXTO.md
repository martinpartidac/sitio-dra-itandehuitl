# Contexto del proyecto — Sitio web Dra. Itandehuitl Arango Castillo

## Quién es la clienta

**Dra. Itandehuitl Arango Castillo** — Médica especialista en:
- **Alta Especialidad en Toxicología Clínica** — Hospital Juárez de México / UNAM (concluida feb 2025)
- **Especialista en Medicina de Urgencias** — Certificada por CONACEM, vigente 2023–2028
- **Profesora UNAM** — Colegio Mexicano de Medicina de Emergencias y Reanimación Avanzada (2024–presente)
- Consulta privada: **Hospital Ángeles Lindavista**, Ciudad de México
- Trabajo de base: **CMN La Raza, IMSS** (no mencionar en el sitio — el sitio es para su práctica privada)
- Miembro de **Redtox** (Red Nacional de Toxicología)
- Intereses académicos: fauna de ponzoña (arácnidos, serpientes, fauna marina), micología, intoxicaciones agudas
- Teléfono: `+52 81 1610 5778` (mismo número para Tel y WhatsApp)

Frase auténtica encontrada en su perfil Redtox:
> *"Para mí, cada animal venenoso es un mundo mágico que aún nos queda por explorar..."*

El sitio debe servir a **dos audiencias**:
1. Pacientes/familias en emergencia toxicológica
2. Médicos buscando interconsulta especializada

---

## Archivos del proyecto

```
/Users/luismartinpartida/Ita/
├── landing-v2.html               ← versión oscura (editorial, "National Geographic meets emergency medicine")
├── landing-dra-itandehuitl.html  ← versión clara (conservadora, misma info actualizada)
├── tarjetas.html                 ← Tarjetas de presentación — USAR OPCIÓN 1 (blanca/elegante)
├── guia-picadura-alacran.html    ← guía independiente (pendiente actualizar a estilo v2)
├── LOGO_01.png                   ← Logo oficial (navy + dorado, fondo blanco sólido)
├── LOGO_01_B.png                 ← Logo alternativo (misma versión, diferente export)
├── ita2.JPG                      ← Foto oficial (bata blanca, usar esta)
├── ita1.JPG                      ← Foto descartada (fondo distractor, sin bata)
└── CONTEXTO.md                   ← este archivo
```

Repositorio GitHub: `https://github.com/martinpartidac/sitio-dra-itandehuitl`

URLs en vivo:
- v2 (oscura): `https://martinpartidac.github.io/sitio-dra-itandehuitl/landing-v2.html`
- v1 (clara): `https://martinpartidac.github.io/sitio-dra-itandehuitl/landing-dra-itandehuitl.html`
- Tarjetas: solo local (no subidas a GitHub — contienen info privada)

---

## Tarjeta de presentación — Opción 1 (Blanca/Elegante) ← ELEGIDA

**Frente:**
- Fondo blanco, franja dorada superior
- Logo a la izquierda + separador dorado vertical
- Nombre en Playfair Display navy
- Especialidad en 2 líneas: `TOXICOLOGÍA CLÍNICA / MEDICINA DE URGENCIAS`
- Detalles: Hospital Ángeles Lindavista · CDMX / Redtox
- Ícono de teléfono dorado + `+52 81 1610 5778`

**Reverso:**
- Fondo navy oscuro, franja dorada superior
- Logo centrado grande (140px, invertido a blanco)
- `TOXICOLOGÍA CLÍNICA` en dorado
- Teléfono flanqueado por líneas doradas
- `ÁNGELES LINDAVISTA` en texto tenue

**Pendiente de logo:** `LOGO_01.png` tiene fondo blanco sólido — en el reverso navy el logo se invierte a blanco y se pierde el dorado. Para resultado óptimo solicitar al diseñador PNG con **fondo transparente**.

---

## Credential pills (sección "Quién soy") — landing-v2.html

```
● Hospital Ángeles Lindavista · CDMX
● Alta Especialidad Toxicología · UNAM
● Certificada CONACEM 2023–2028
● Profesora UNAM · Emergencias
● Redtox · Miembro Experto
```

---

## Estado del contenido

**Resuelto:**
- ✅ Teléfono real: `+52 81 1610 5778` — actualizado en los 3 archivos HTML
- ✅ Hospital correcto: Ángeles Lindavista (no CMN La Raza) en todos los archivos
- ✅ Especialidad correcta: ya es especialista titulada (no R2)
- ✅ Hero tagline: cambiada a versión sin sonar arrogante
- ✅ Tarjeta blanca elegida y diseño refinado

**Pendiente de la doctora:**
- Respuestas a las 6 preguntas para la sección "Quién soy":
  1. ¿Cuál fue el caso toxicológico que más te marcó y por qué?
  2. ¿Qué hace diferente tu enfoque al tratar intoxicaciones vs otros especialistas?
  3. ¿Por qué elegiste toxicología clínica después de urgencias?
  4. ¿Qué le dirías a un médico de primer contacto que enfrenta una picadura de alacrán grave?
  5. ¿Cuáles son los errores más comunes que ves en el manejo prehospitalario de intoxicaciones?
  6. ¿Qué animales de ponzoña considera más subestimados en México?

**Pendiente técnico:**
- PNG del logo con fondo transparente (solicitar al diseñador)
- Actualizar `guia-picadura-alacran.html` al estilo de v2
- Definir dominio real (placeholder actual: `https://draita.mx/`)
- Decidir entre v1 (clara) y v2 (oscura) para presentar a la doctora

---

## Diseño de landing-v2.html (versión oscura)

### Estética
- "National Geographic meets emergency medicine" — editorial, oscuro, impactante
- NO cambiar a fondo claro
- NO fondos alternados por sección — usar solo bordes sutiles

### Variables CSS principales
```css
--bg: #070d1a        /* fondo base */
--bg-2: #0d1627      /* secciones alternas */
--bg-3: #111e35      /* cards / acordeón */
--text: #eef2ff
--teal: #14b8a6
--blue: #3b82f6
--emergency: #e11d48
--strip-h: 48px
--nav-h: 68px
```

### Fuentes
- **Playfair Display** — headings editoriales (italic para énfasis)
- **Inter** — cuerpo y UI

### Estructura de secciones
1. `emergency-strip` — franja roja fija en top, z-index 2000, teléfono de emergencia
2. `nav` — transparente sobre hero → sólido al hacer scroll
3. `#hero` — headline "Cuando el veneno *no puede esperar.*" + foto circular + 2 CTAs
4. `#quien` — pull quote + bio + credential pills
5. `#especialidades` — 4 tarjetas (fauna ponzoña, tox marina, micología, intox agudas)
6. `#proceso` — 3 pasos: Contacta → Evaluación → Atención
7. `#guia` — acordeón de emergencia (picadura alacrán, mordedura serpiente, intox oral, inhalación)
8. `#contacto` — solo teléfono + WhatsApp (sin formulario)
9. `footer` — nombre, especialidades, año

### CTAs del hero
- **Rojo** (pulse animation): "Tengo una emergencia — Llamar ahora" → `tel:`
- **Azul** (outline): "Soy médico — Solicitar interconsulta" → `#contacto`

### Mobile breakpoints
| Breakpoint | Qué cambia |
|---|---|
| 900px | Hero: 1 columna, foto arriba, `min-height: auto` |
| 768px | Quién soy: 1 columna; comilla grande se reduce |
| 720px | Especialidades: 1 columna |
| 680px | Proceso: 1 columna |
| 560px | Acordeón: columnas do/don't en 1 col |
| 520px | Contacto: botones full-width apilados |
| 480px | Strip: oculta texto, solo botón; badges flotantes ocultos; comilla 3.5rem |

---

## Decisiones técnicas

- HTML/CSS/JS puro — sin frameworks, sin librerías externas
- Todo CSS inline en `<style>`, todo JS al final en `<script>`
- `clamp()` para tipografía fluida
- Iconos: SVG inline únicamente
- Schema.org `Physician` estructurado en `<head>`
- Open Graph tags para compartir en redes

---

## Bugs corregidos (historial)

- **v1 — X visible en nav desktop**: el botón de cerrar menú móvil se mostraba en desktop. Fix: agregar `.nav-close-item { display: none; }` fuera del media query.
- **v2 — comilla decorativa demasiado grande en móvil**: reducida con media queries a 3.5rem en ≤480px.
- **v2 — hero ocupaba 100vh en móvil**: cambiado a `min-height: auto` en ≤900px.
- **v2 — badges flotantes se salían en móvil**: ocultos en ≤480px.
- **v1 — texto invisible en sección contacto**: clase `hero-tagline` tenía color blanco (para hero oscuro) pero se reutilizaba en contacto (fondo claro). Fix: `section .hero-tagline { color: var(--text-secondary); }`.

---

## Cosas que NO hacer

- No mencionar CMN La Raza ni IMSS en el sitio (es su trabajo institucional, no su práctica privada)
- No cambiar el diseño oscuro de v2 a uno claro
- No agregar formulario de contacto (solo teléfono/WhatsApp)
- No usar fondos de color por sección (solo `var(--bg)`, `var(--bg-2)`, `var(--bg-3)`)
- No agregar imágenes de stock — solo `ita2.JPG`
- No usar librerías externas (React, Bootstrap, Alpine, etc.)

---

## Cómo publicar cambios en GitHub Pages

```bash
cd /Users/luismartinpartida/Ita
git add landing-v2.html landing-dra-itandehuitl.html tarjetas.html CONTEXTO.md
git commit -m "Descripción del cambio"
git push
```

El sitio se actualiza en 1-2 minutos. Forzar recarga con `Cmd+Shift+R`.

> El remote `origin` ya está configurado, no hace falta setup adicional.
