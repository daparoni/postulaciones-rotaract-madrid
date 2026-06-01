# Guía: crear el formulario y controlar las postulaciones

Esta guía explica, paso a paso y sin tecnicismos, cómo dejar la web lista para recibir postulaciones.

## Paso 1 — Crear el Google Form (gratis)

1. Entra a [forms.google.com](https://forms.google.com) con la cuenta del club.
2. Crea un formulario nuevo. Título sugerido: **"Postulación a cargos — Club Rotaract 2026–2027"**.
3. Agrega estas preguntas (puedes ajustarlas):
   - **Nombre completo** (texto corto) — obligatoria
   - **Correo / WhatsApp de contacto** (texto corto) — obligatoria
   - **Puesto al que te postulas** (desplegable) — obligatoria
     - Pon como opciones todos los cargos: Presidente, Vicepresidente, Secretario, Tesorero, Macero, Administración del club, Membresía, Imagen pública, Proyectos de servicio, La Fundación Rotaria, etc.
   - **¿Por qué te postulas? / ¿Qué propones?** (párrafo) — obligatoria
   - **Tiempo en el club / experiencia previa** (párrafo) — opcional

## Paso 2 — Obtener el enlace y pegarlo en la web

1. En el formulario, pulsa **Enviar** → pestaña del **enlace** 🔗 → **Acortar URL** → **Copiar**.
2. Abre `index.html`, busca el bloque **CONFIG** (al final) y pega el enlace en:
   ```
   FORM_URL: "https://forms.gle/TU-ENLACE",
   ```
3. Guarda y sube el cambio a GitHub.

## Paso 3 — (Opcional) Pre-rellenar el puesto automáticamente

Para que al pulsar "Postularme" en un cargo el formulario ya traiga ese puesto seleccionado:

1. En el formulario: menú **⋮** (arriba a la derecha) → **Obtener enlace prerrellenado**.
2. Selecciona en la pregunta "Puesto" cualquier opción y pulsa **Obtener enlace**.
3. Copia el enlace. En él verás algo como `entry.123456=Presidente`.
4. Reemplaza el nombre del puesto por `{{PUESTO}}` y pégalo en `FORM_URL_PRELLENADO`. Ejemplo:
   ```
   FORM_URL_PRELLENADO: "https://docs.google.com/forms/d/e/XXXX/viewform?usp=pp_url&entry.123456={{PUESTO}}",
   ```

## Paso 4 — Controlar las postulaciones

1. En el formulario, abre la pestaña **Respuestas**.
2. Pulsa el icono verde de **Hojas de cálculo** para volcar todo a una hoja de Google.
3. Ahí ves, filtras y exportas (a Excel) todas las postulaciones por cargo, en tiempo real.

## Cerrar las postulaciones

Cuando termine el periodo, en el formulario desactiva **"Aceptar respuestas"**. La web seguirá visible como referencia.
