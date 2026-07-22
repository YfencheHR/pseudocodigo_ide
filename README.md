# pseudocodigo_ide

**PseudoIDE** — editor e intérprete de pseudocódigo en el navegador, pensado para introducir a alumnos en la programación sin necesidad de instalar nada.

Se ejecuta 100% en el cliente (HTML + CSS + JavaScript vanilla, sin backend ni dependencias externas). Basta con abrir `index.html` en cualquier navegador.

## Finalidad

Proyecto con fin estrictamente docente: ofrecer a profesores y alumnos una herramienta ligera para practicar la lógica de programación (variables, condicionales, bucles) usando pseudocódigo en español, antes de dar el salto a un lenguaje de programación real.

Es un proyecto público y sin ánimo de lucro. Cualquier centro educativo, docente o estudiante puede usarlo, modificarlo y distribuirlo libremente.

## Público objetivo

- Alumnos que se inician en programación (secundaria, bachillerato, primeros cursos universitarios).
- Docentes que buscan una herramienta lista para usar en clase, sin instalación ni configuración.

## Características

- Editor con numeración de líneas, autoindentado e indicador de posición (línea/columna).
- Barra de inserción rápida de estructuras: `INICIO...FIN`, `SI...ENTONCES`, `MIENTRAS...HACER`, `PARA...HASTA`, `LEER`, `MOSTRAR`, etc.
- Intérprete de pseudocódigo en español con soporte de variables, condicionales (`SI`/`SI NO`), bucles (`MIENTRAS`, `PARA`), entrada de datos interactiva (`LEER`) y salida por consola (`MOSTRAR`).
- Panel de variables en tiempo real mientras se ejecuta el programa.
- Consola de salida con entrada de datos interactiva durante la ejecución.
- Protección anti-bucle-infinito (límite de pasos totales y de iteraciones en `MIENTRAS`).
- Tres misiones/ejercicios precargados a modo de práctica gamificada: Escape Room algorítmico, Control de nave espacial y La Cena de Navidad.

## Cómo usarlo

Abre `index.html` directamente en el navegador (doble clic, o sírvelo con cualquier servidor estático). No requiere instalación, compilación ni conexión a internet.

## Estado del proyecto

Prototipo inicial (MVP) en desarrollo activo.

## Licencia

Distribuido bajo licencia [MIT](LICENSE). Puedes usarlo, copiarlo, modificarlo y redistribuirlo libremente, incluso en contextos educativos institucionales, manteniendo el aviso de copyright original.

## Contribuciones

Al ser un proyecto público y sin ánimo de lucro, las contribuciones de la comunidad docente y de desarrolladores son bienvenidas. (Guía de contribución detallada, próximamente.)
