# LogisTech — Modelo operativo de la plataforma interna

Presentación interactiva sobre la reestructuración del modelo operativo de la IDP de LogisTech: liderazgo dual Two-in-a-Box (PPM y Tech Lead), curación 80/20 con dos golden paths (microservicios Node.js y PostgreSQL gestionado), política de rutas propias para los equipos de datos, entrega desacoplada del portal y del plano de control, InnerSourcing con un solo propietario por activo y retiro de Jenkins por adopción pull. Elaborada para Arquitectura de Plataformas (ARTI-4219), Universidad de los Andes.

[Ver la presentación interactiva](https://raparram.github.io/LogisTech/)

## Archivo de entrega y revisión local

`index.html` contiene el documento completo, con los cinco autores, estilos, scripts y diagramas SVG integrados. Es el archivo único de entrega. Las fuentes web tienen alternativas locales, así que el contenido también se puede consultar sin conexión. `LogisTech.html` es únicamente un acceso mediante iframe y necesita `index.html` a su lado.

Para revisar la rama descargada, abre `index.html` en un navegador o ejecuta `python3 -m http.server 8765` desde el repositorio y visita <http://localhost:8765/>. El enlace público de arriba muestra la versión publicada en GitHub Pages.

La portada abre con una simulación: un despliegue por la ruta pavimentada, la caída del portal y de la API sin interrumpir la entrega, y la ruta propia del equipo de datos. La vista inicial muestra una síntesis por bloque. Los apartados desplegables conservan roles, golden paths, política de atípicos, mecanismo de contingencia, matriz de fallos, modelo de contribución y plan de deprecación. En «Contenido», el botón «Mostrar análisis completo» abre todos los apartados. Los enlaces directos a una sección detallada abren su apartado automáticamente. Al imprimir se abren todos los apartados.

## Correspondencia con la rúbrica

| Criterio | Evidencia en el documento |
| --- | --- |
| Two-in-a-Box y curación 80/20 | Bloque I: quién asume PPM y TL, tabla de fronteras de decisión con un solo dueño por decisión y regla de desempate (1.1); demanda de 30 equipos, dos golden paths con su contrato y lo que queda fuera (1.2); comunicado oficial de dos párrafos para datos, sin penalizaciones y con operación propia (1.3). |
| Arquitectura fuera de la ruta crítica y resiliencia | Bloque II: diagrama lógico con plano de control separado de la ruta de entrega, mecanismo paso a paso para compilar, probar y desplegar sin portal ni API, e interfaz dual (2.1); matriz de fallos F1–F6, dependencias residuales y break-glass auditado (2.2); game day y SLO separados (2.3). |
| InnerSourcing, adopción pull y deuda técnica | Bloque III: RFC, controles automáticos y revisión por CODEOWNERS; enrutamiento de la guardia según el origen de la falla y acuerdos de propiedad, soporte y ciclo de vida del template React (3.1); retiro de Jenkins en tres pasos con condiciones de avance, ventana de superposición y palancas de atracción (3.2). |
| Estructura y rigor conceptual | Síntesis del comité, simulación de portada, diagrama vinculado con la matriz, hoja de ruta de 13 semanas, trazabilidad de las tres crisis, madurez CNCF, riesgos, supuestos y referencias. |

El diagrama editable está en `diagramas/tobe-resiliencia.drawio`. Sus identificadores F1–F6 corresponden al SVG incorporado en `index.html` y a la matriz 2.2; cualquier cambio debe conservar esa correspondencia.
