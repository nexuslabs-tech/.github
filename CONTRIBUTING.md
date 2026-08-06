# Contribuir a los proyectos de Nexus Labs

Gracias por ayudar a mejorar un proyecto de Nexus Labs. Las contribuciones se
evalúan por su corrección, evidencia, mantenibilidad y adecuación a la
arquitectura del repositorio afectado.

## Antes de realizar un cambio

1. Leé el archivo README del repositorio y toda instrucción local para
   contribuciones o agentes.
2. Buscá trabajos relacionados en las incidencias y solicitudes de cambios
   existentes.
3. Para un cambio no trivial, abrí o referenciá una incidencia que defina el
   problema y el resultado esperado.
4. Mantené el alcance lo suficientemente acotado como para validarlo y revertirlo
   de forma segura.

Las instrucciones específicas de cada repositorio prevalecen cuando son más
estrictas que este documento.

## Ramas y confirmaciones

Usá ramas de corta duración con un prefijo descriptivo:

- `feat/` para comportamiento nuevo.
- `fix/` para correcciones.
- `docs/` para cambios exclusivos de documentación.
- `refactor/` para cambios estructurales que preservan el comportamiento.
- `test/` para cambios exclusivos de pruebas.
- `chore/` para mantenimiento.

Priorizá confirmaciones acotadas y mensajes en modo imperativo. Se recomiendan
los prefijos de Confirmaciones Convencionales, por ejemplo `feat:`, `fix:`,
`docs:`, `test:` y `chore:`.

No mezcles formato, contenido generado o limpieza sin relación con un cambio
funcional, salvo que la solicitud explique explícitamente ese alcance.

## Requisitos de evidencia

Cada solicitud de cambios debe explicar:

- Qué cambió y por qué.
- Qué supuestos se realizaron.
- Qué comandos o verificaciones se ejecutaron.
- Qué resultados se observaron, incluidos fallos o limitaciones.
- Cuál es el riesgo operativo y el camino de reversión.
- Si se requiere documentación o migración del entorno de ejecución.

Adjuntá capturas, registros, trazas y mediciones sólo cuando respalden de manera
material la afirmación realizada. Eliminá secretos y datos personales.

## Separación entre código fuente y ejecución

Nunca confirmes estado de ejecución ni datos locales de una máquina, incluidos:

- Bases de datos SQLite y sus archivos `-wal` o `-shm`.
- Registros, cachés, archivos de bloqueo creados por servicios en ejecución o
  resultados temporales.
- Copias de seguridad, instantáneas de memoria, datos exportados de usuarios o
  paquetes de evidencia generados.
- Credenciales, tokens, claves privadas, valores de `.env` o configuración local
  de herramientas.

Los archivos de bloqueo del proyecto que definen dependencias reproducibles son
artefactos del código fuente y deben permanecer versionados. Los bloqueos del
entorno de ejecución no deben versionarse.

## Flujo de solicitudes de cambios

1. Actualizá tu rama desde la rama predeterminada.
2. Ejecutá los comandos de validación y del arnés documentados por el repositorio.
3. Completá la plantilla con evidencia concreta.
4. Esperá las verificaciones automáticas requeridas.
5. Resolvé las conversaciones de revisión antes de fusionar.
6. Priorizá la fusión condensada, salvo que exista una razón para preservar cada
   confirmación individual.

El trabajo asistido por inteligencia artificial es bienvenido, pero la persona
autora sigue siendo responsable de cada cambio. El estado del repositorio, las
verificaciones ejecutables y la documentación primaria son las fuentes de
verdad, no los resúmenes generados ni la memoria de un modelo.

## Seguridad

No divulgues una posible vulnerabilidad en una incidencia pública. Seguí
[`SECURITY.md`](SECURITY.md) y utilizá el canal privado de seguridad del
repositorio afectado.
