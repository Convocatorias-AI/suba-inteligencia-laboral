# Suba Inteligencia Laboral — prototipo de demostración

Prototipo navegable del modelo territorial de inteligencia laboral con IA para la localidad de Suba,
preparado por la Universidad del Rosario (Proyecto Ítaca · URSTEAM · Dirección de Desarrollo) para la
convocatoria **Cities Deliver: AI Solutions for Public Services**.

## Qué es

Una sola página HTML, sin dependencias de servidor, que recorre el flujo de SUBA Inteligencia Laboral:

**Caso guiado de Marta.** Para entender el proceso con una persona, el menú abre con un caso paso a paso: una empresa de Suba
registra una vacante de auxiliar administrativa, Marta sube su hoja de vida, la IA detecta que solo le falta Power BI, le arma
un curso validado por la Universidad del Rosario, actualiza su perfil, envía su hoja de vida con consejos de entrevista y la
empresa la contrata. Cada paso abre la pantalla real del agente que actúa.

Además, el prototipo recorre:

1. registro de personas y empresas con consentimiento (Ley 1581 de 2012) y repositorio único de cuatro fuentes,
   normalizadas con ESCO y CUOC (PostgreSQL con pgvector y almacenamiento de objetos);
2. orquestador multiagente de los agentes 1 a 6, con base de conocimiento RAG que cita sus fuentes y trazabilidad de cada decisión;
3. Agente 1 (mercado laboral) y Agente 2 (perfil de talento), con GPT-6 Luna y GPT-6.1 Terra para el 10 % más difícil;
4. Agente 3: motor de coincidencias que combina similitud semántica y reglas explícitas, con corrección del orientador;
5. tres decisiones consecutivas y cuatro rutas: A (Agente 5), B (Agente 4), D (Agente 6) y C (formación externa);
6. seguimiento de contratación y permanencia, panel del empleador, copiloto de empleabilidad y Agente 8;
7. tablero de impacto (postulaciones, formación, contratación y permanencia) que alimenta la Fase III.

Las coincidencias, las rutas y los ciclos de retorno (B → acompañamiento laboral, C → Agente 2, sin empleo → Agente 3)
se calculan en vivo en el navegador.

## Qué NO es

Las vacantes, los perfiles y las cifras son **sintéticos**. Las respuestas de los agentes son **simuladas**
con reglas locales: no hay un modelo de inteligencia artificial en ejecución, ni datos de personas reales,
ni conexión a fuentes externas. El prototipo no presta servicios de empleo.

## Publicación

El sitio se publica con GitHub Pages desde la rama `main`, carpeta raíz. `index.html` es autocontenido
(los logos institucionales van incrustados), así que basta con copiar ese archivo para actualizarlo.

## Actualizar

El prototipo y los diagramas se generan desde la carpeta de trabajo del proyecto:

- `python herramientas/generar_diagramas.py` regenera `assets/arquitectura-tecnica.svg` y `assets/flujo-decision.svg`;
- `python herramientas/prototipo/ensamblar.py` arma `prototipo-suba-inteligencia-laboral.html`.

1. Reemplazar `index.html` por la versión nueva del prototipo.
2. `git add -A && git commit -m "Actualiza el prototipo" && git push`.

GitHub Pages republica en uno o dos minutos.
