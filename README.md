# Postulaciones a cargos — Club Rotaract

Web para que los socios conozcan los cargos del club y se postulen al inicio de cada mandato.
Pensada como **primer paso tecnológico** del club: gratis, sin servidores que mantener y **heredable** para las futuras generaciones.

## ¿Cómo funciona?

- La web (un solo archivo `index.html`) muestra los cargos de la junta directiva y los comités.
- Cada cargo tiene un botón **"Postularme"** que abre un **Google Form**.
- Todas las postulaciones quedan automáticamente en una **hoja de Google** que controla la directiva.
- Está publicada gratis con **GitHub Pages**.

## Para el presidente / administrador

Toda la configuración está en el bloque **CONFIG** al final de `index.html`. No hace falta saber programar:

1. Crea el Google Form de postulaciones (ver [`guia-postulaciones.md`](guia-postulaciones.md)).
2. Pega el enlace del formulario en `FORM_URL`.
3. Ajusta el nombre del club, el año del mandato y la lista de cargos si lo necesitas.
4. Guarda y sube el cambio a GitHub. La web se actualiza sola.

## Heredar al próximo mandato

El próximo presidente solo tiene que:
1. Actualizar `mandato` y, si cambian, los cargos en `index.html`.
2. Crear su propio Google Form y pegar el nuevo `FORM_URL`.

Nada caduca ni se borra entre mandatos, porque no hay base de datos ni costos.

## Fuentes de los cargos

Estructura basada en el Plan de Liderazgo para Clubes de Rotary International
(cinco comités permanentes: Administración, Membresía, Imagen Pública, Proyectos de Servicio y La Fundación Rotaria)
y en la estructura estándar de junta directiva de los clubes Rotaract.
