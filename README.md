# PseudoIDE

**PseudoIDE** — editor e intérprete de pseudocódigo en español, 100% en el navegador, pensado para introducir a alumnos en la programación sin necesidad de instalar nada.

Se ejecuta completamente en el cliente (HTML + CSS + JavaScript vanilla, sin backend ni dependencias externas).

**🔗 Pruébalo online, sin instalar nada: [yfenchehr.github.io/pseudocodigo_ide](https://yfenchehr.github.io/pseudocodigo_ide/)**

## Finalidad

Proyecto con fin estrictamente docente: ofrecer a profesores y alumnos una herramienta ligera para practicar la lógica de programación (variables, condicionales, bucles) usando pseudocódigo en español, antes de dar el salto a un lenguaje de programación real.

Es un proyecto público y sin ánimo de lucro. Cualquier centro educativo, docente o estudiante puede usarlo, modificarlo y distribuirlo libremente.

## Público objetivo

- Alumnos que se inician en programación (secundaria, bachillerato, primeros cursos universitarios).
- Docentes que buscan una herramienta lista para usar en clase, sin instalación ni configuración.

## Características

- Editor con numeración de líneas, autoindentado e indicador de posición (línea/columna).
- Barra de inserción rápida de estructuras: `INICIO...FIN`, `SI...ENTONCES`, `MIENTRAS...HACER`, `PARA...HASTA`, `LEER`, `MOSTRAR`, etc.
- Intérprete de pseudocódigo en español (ver referencia del lenguaje más abajo).
- Panel de variables en tiempo real mientras se ejecuta el programa.
- Consola de salida con entrada de datos interactiva durante la ejecución (`LEER`).
- Aviso de líneas no reconocidas con su número de línea: las erratas no fallan en silencio.
- Protección anti-bucle-infinito (límite global de pasos y de iteraciones en `MIENTRAS`), con la página siempre respondiendo — la ejecución cede el hilo al navegador periódicamente.
- Botón **⏹ Detener** para interrumpir una ejecución en curso.
- Autoguardado del contenido del editor en el navegador (`localStorage`): recargar la página no pierde el trabajo.
- Atajo de teclado **Ctrl+Enter** (o Cmd+Enter) para ejecutar.
- Diseño adaptable: en pantallas estrechas el editor y la consola se apilan en vertical.
- Tres misiones/ejercicios precargados a modo de práctica gamificada:
  - 🔐 **Escape Room algorítmico** — bucles, condiciones y entrada de datos.
  - 🚀 **Control de nave espacial** — simulación con `MIENTRAS` y estado.
  - 🎄 **La Cena de Navidad** — juego de decisiones: 6 rondas con 3 opciones cada una y 4 finales distintos según lo que elijas.

## Cómo usarlo

La forma más rápida es entrar directamente en **[yfenchehr.github.io/pseudocodigo_ide](https://yfenchehr.github.io/pseudocodigo_ide/)** desde cualquier navegador (ordenador, tablet o Chromebook de clase). No requiere instalación, cuenta ni conexión constante: una vez cargada la página, funciona sin conexión.

También puedes descargar el repositorio y abrir `index.html` directamente en el navegador (doble clic), o servirlo con cualquier servidor estático.

## Referencia del lenguaje

| Instrucción | Ejemplo | Descripción |
|---|---|---|
| `INICIO` / `FIN` | — | Delimitan el programa |
| `// comentario` | `// esto no se ejecuta` | Comentario de línea |
| `variable = expr` | `total = 5 + 3` | Asignación |
| `MOSTRAR expr` | `MOSTRAR 'Total: ' + total` | Imprime en la consola |
| `LEER var` | `LEER edad` | Pide un valor al usuario (pausa la ejecución) |
| `SI cond ENTONCES` … `SI NO` … `FIN_SI` | `SI edad >= 18 ENTONCES` | Condicional (el `SI NO` es opcional; admite anidamiento) |
| `MIENTRAS cond HACER` … `FIN_MIENTRAS` | `MIENTRAS x < 10 HACER` | Bucle condicional |
| `PARA var = a HASTA b HACER` … `FIN_PARA` | `PARA i = 1 HASTA 5 HACER` | Bucle contado |
| `PARA var EN [lista] HACER` … `FIN_PARA` | `PARA caja EN [A, B, C] HACER` | Bucle sobre una lista |
| `ACTIVAR var` | `ACTIVAR alarma` | Pone la variable a `VERDADERO` |
| `EMITIR expr` | `EMITIR 'señal enviada'` | Imprime un mensaje destacado |
| `TERMINAR` | — | Finaliza el programa inmediatamente |

**Expresiones:** números, cadenas entre comillas (`'texto'` o `"texto"`), `VERDADERO`/`FALSO`, operadores `+ - * /` (el `+` concatena si hay texto), paréntesis.
**Comparadores:** `=`, `<>` o `!=`, `<`, `>`, `<=`, `>=`.
**Conectores lógicos:** `Y`, `O` (con la precedencia habitual: `Y` liga más fuerte que `O`).
Los nombres de variable admiten tildes y `ñ`, y no distinguen mayúsculas de minúsculas.

## Uso pedagógico del propio código fuente

Además de usarse como herramienta en clase, el propio fichero `index.html` puede servir como material didáctico en sí mismo. Es un único archivo, sin build ni dependencias, con un intérprete de pseudocódigo completo implementado a mano: tokenizador, evaluador de expresiones y condiciones, y un ejecutor recursivo de bloques (`SI`, `MIENTRAS`, `PARA`). Para alumnos más avanzados (o de asignaturas de compiladores/lenguajes), es un ejemplo real y legible de cómo funciona por dentro un intérprete sencillo.

## Estado del proyecto

Prototipo funcional (MVP) en desarrollo activo.

## Licencia

Distribuido bajo licencia [MIT](LICENSE). Puedes usarlo, copiarlo, modificarlo y redistribuirlo libremente, incluso en contextos educativos institucionales, manteniendo el aviso de copyright original.

## Contribuciones y reporte de errores

Al ser un proyecto público y sin ánimo de lucro, las contribuciones de la comunidad docente y de desarrolladores son bienvenidas.

Si encuentras un error, tienes una sugerencia o quieres proponer una mejora (por ejemplo, una nueva misión), abre un [Issue](https://github.com/YfencheHR/pseudocodigo_ide/issues) en este repositorio. Si quieres aportar código directamente, puedes abrir un Pull Request.

## Autor y contacto

Proyecto mantenido por Yfenche. Para dudas, sugerencias o colaboraciones: yfenchehr@gmail.com

## Nota sobre el desarrollo

Este proyecto se ha desarrollado con ayuda de inteligencia artificial (Claude, de Anthropic), tanto para la programación como para la documentación. Se indica por transparencia, especialmente al tratarse de un recurso educativo.
