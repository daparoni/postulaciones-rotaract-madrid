# Guía: conectar el formulario y ver las postulaciones

El formulario de postulación ya está **dentro de la página** (al pulsar "Postularme" en cualquier cargo se abre con tu diseño).
Solo falta conectarlo a **Formspree** para que las postulaciones se guarden y te lleguen. Es gratis y se hace una sola vez.

## Paso 1 — Crear el formulario en Formspree (gratis)

1. Entra a [formspree.io](https://formspree.io) y crea una cuenta (puedes usar tu correo de Google).
2. Pulsa **+ New form**. Ponle un nombre, por ejemplo "Postulaciones Rotaract".
3. Indica el correo donde quieres recibir las postulaciones.
4. Formspree te dará una URL como `https://formspree.io/f/abcdwxyz`.
   El **ID** es la última parte: `abcdwxyz`.

## Paso 2 — Pegar el ID en la web

1. Abre `index.html` y busca el bloque **CONFIG** (al final del archivo).
2. Pega tu ID entre las comillas:
   ```
   FORMSPREE_ID: "abcdwxyz"
   ```
3. Guarda y sube el cambio a GitHub. ¡Listo! Las postulaciones ya se envían.

> Mientras `FORMSPREE_ID` esté vacío, el formulario muestra un aviso y no envía nada (modo prueba).

## Paso 3 — Ver y controlar las postulaciones

- Cada postulación te llega por **correo** y queda guardada en el **panel de Formspree**.
- En el panel puedes ver todas las postulaciones, filtrarlas por cargo y **exportarlas a CSV/Excel**.
- Cada envío incluye: **puesto**, **nombre y apellido** y **por qué se postula**.

## Límites del plan gratuito

El plan gratis de Formspree permite alrededor de **50 envíos al mes**, suficiente para una elección.
Si esperas muchísimas postulaciones, puedes crear varios formularios o subir de plan.

## Cerrar las postulaciones

Cuando termine el periodo, en Formspree puedes **desactivar el formulario** (Form → Settings).
La web seguirá visible como referencia.

## Heredar al próximo mandato

El próximo presidente solo crea su propio formulario en Formspree, pega el nuevo `FORMSPREE_ID`
y actualiza el año del mandato y los cargos en `index.html`. Nada caduca entre mandatos.
