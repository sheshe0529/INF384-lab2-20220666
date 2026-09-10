1.1)
* Defecto 1: Ausencia de dependencia entre los jobs, lo que ocaciones que los jobs se ejecuten en paralelo (validar y publicar). Se manifiesta en el archivo .github/workflows/pipeline.yml en la línea 42.
* Defecto 2: Carga repetitiva de dependencias para cada ejecución en vivo, lo que podría tener versiones no deseadas. Se manifiesta en el archivo .github/workflows/pipeline.yml en la línea 26.
* Defecto 3: Falta de especificación de ramas, lo que hace que se publique en una rama no específica. Se manifiesta en el archivo .github/workflows/pipeline.yml en la línea 5.
* Defecto 4: Ausencia de caché en la preparación del entorno, lo que hace que se instalen todas las librerías de Python por cada ejecución, lo que hace que se demore. Se manifiesta en el archivo .github/workflows/pipeline.yml en la línea 21.
1.2) El defecto que explica la duración es la ausencia de caché, pues la carga de dependencias consume en total alrededor de 11 segundos, lo que podría reducir. A gran escala y con un nivel grande de dependencias, podría ser mayor impacto en los despliegues.
1.3) En el caso de mi grupo, el defecto de ausencia de dependencias podría reducir el lead time, porque se consideraban varios tiempos de validación entre aprobaciones manuales.
1.4) Lead Time para cambios debido a que esta métrica ayuda a medir el tiempo entre el primer commit a su llegada a producción, que es lo que se simula con "publicar". La otra posible puede ser la cantidad de fallos en los cambios, sin embargo, la que tiene un impacto real para explicar el tiempo y que se ataca el defecto, es Lead Time para Cambios.
1.5) El valor del LeadTime para CAMBIOS

Justificacion de version:
Desde el tag v1.2.0 hasta el HEAD solo se observan cambios de correccion y de documentacion/operacion de CI, con ningun tipo de cambio funcional nuevo de tipo feat ni breaking. Por ello, el incremento correcto es PATCH y la version pasa de 1.2.0 a 1.2.1; no corresponde mayor ni menor por ausencia de cambios mayores o nuevas funcionalidades compatibles.

