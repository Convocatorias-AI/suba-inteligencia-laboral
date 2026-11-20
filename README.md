# Suba Inteligencia Laboral — prototipo de demostración

Prototipo navegable del modelo territorial de inteligencia laboral con IA para la localidad de Suba,
preparado por la Universidad del Rosario (Proyecto Ítaca · URSTEAM · Dirección de Desarrollo) para la
convocatoria **Cities Deliver: AI Solutions for Public Services**.

## Qué es

Una sola página HTML, sin dependencias de servidor, que recorre:

- los cinco agentes de la Fase II (mercado laboral, perfil de talento, brechas y coincidencias, aprendizaje, acompañamiento);
- el panel del empleador (publicar vacante, candidatos anonimizados, retroalimentación con motivo);
- el tablero de seguimiento de la Fase III (indicadores contra línea base, embudo, equidad y calidad).

Los puntajes de coincidencia y las rutas A/B/C se calculan en vivo en el navegador.

## Qué NO es

Las vacantes, los perfiles y las cifras son **sintéticos**. Las respuestas de los agentes son **simuladas**
con reglas locales: no hay un modelo de inteligencia artificial en ejecución, ni datos de personas reales,
ni conexión a fuentes externas. El prototipo no presta servicios de empleo.

## Publicación

El sitio se publica con GitHub Pages desde la rama `main`, carpeta raíz. `index.html` es autocontenido
(los logos institucionales van incrustados), así que basta con copiar ese archivo para actualizarlo.

## Actualizar

1. Reemplazar `index.html` por la versión nueva del prototipo.
2. `git add -A && git commit -m "Actualiza el prototipo" && git push`.

GitHub Pages republica en uno o dos minutos.
