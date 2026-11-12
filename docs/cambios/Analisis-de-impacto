# Análisis de impacto de SC-001

## Solicitud que se analiza

'quien registro la venta', pedida por Lalo, dupla de revision el 12 de noviembre de 2026.

## Traducción a términos del sistema

Lo pedido: "que en el historial de ventas se vea quién registró cada venta".

Traducido a UnikStock: la clase Usuario, que dejé fuera de mi diagrama de clases, tiene que entrar con su nombre y su rol. La clase Venta tiene que guardar quién la registró, unida a un solo Usuario. El sistema necesita saber quién lo está usando en el momento de registrar la venta. Y el caso de uso CU-07 muestra un dato más.

## Impacto directo

| Artefacto | Unidad | Qué hay que cambiar |
|---|---|---|
| Requisito RF-001 Descontar stock al vender | 2 | Al registrar la venta se guarda también quién la registró |
| Requisito RF-008 Mostrar historial de ventas por día | 2 | Cada venta muestra quién la registró; las anteriores muestran "sin dato" |
| Requisito nuevo RF-010 Identificar a quien usa el sistema | 2 | Escribirlo: el sistema sabe si lo usa el dueño o el vendedor |
| Caso de uso CU-01 Registrar venta | 2 | Nueva precondición: ya se sabe quién usa el sistema |
| Caso de uso CU-07 Consultar historial de ventas por día | 2 | El resultado muestra una columna más |
| Diagrama de clases | 4 | Entra Usuario (nombre y rol) y una relación de Venta con un solo Usuario |
| Diagrama de secuencia | 4 | Todavía no tengo uno de UnikStock en el repositorio. Cuando lo haga, "registrar venta" tendrá un mensaje para saber quién es |
| Diagrama de componentes C4 (nivel 3) | 3 | Aparece un módulo nuevo, Usuarios. Ventas le pregunta quién es, sin leer sus tablas |

## Impacto indirecto

| Artefacto | Unidad | Por qué se ve afectado |
|---|---|---|
| Registro de decisión ADR-001 | 3 | La decisión de monolito modular sigue válida, pero su texto dice tres módulos y ahora serían cuatro. No lo edito: escribo un ADR-002 que registra el módulo nuevo |
| Diagrama de contenedores C4 | 3 | Sin impacto: siguen siendo App web, Servidor y Base de datos |
| Diagrama de contexto C4 | 3 | Sin impacto: las personas y los sistemas externos son los mismos |
| Máquina de estados | 4 | Sin impacto: no tengo una de UnikStock y el cambio no agrega estados |
| RNF-USA-002 (máximo 3 pasos por venta) | 2 | Si pidiera identificarse en cada venta, lo rompería. Por eso la persona se identifica una sola vez al abrir el sistema |
| Análisis de sustantivos | 4 | Usuario quedó descartado por estar fuera del sistema, y esa razón ya no es cierta |
| Especificación, secciones 1 y 2 (alcance y usuarios) | 2 | Hay que revisar si dicen que el sistema no maneja usuarios |
| Tabla de trazabilidad | 2 | Cambian las filas de RF-001 y RF-008, y falta la de RF-010 |
| Prototipo en Figma | 2 | Las pantallas de venta e historial no muestran al usuario |
| Ventas ya registradas | — | No tienen usuario guardado. Muestro "sin dato" y no invento quién fue |
| Pruebas | — | Hay que repetir las de RF-001, RF-006 y RF-008 |
| RNF-CON-001 (stock real y mostrado) | 2 | Sin impacto: el stock se calcula igual |
| RNF-REN-001 (respuesta en menos de 5 segundos) | 2 | Sin impacto esperado: el historial lee una columna más |
| RNF-DIS-001, RNF-FLE-001 y RNF-USA-001 | 2 | Sin impacto |

## Lo que queda sin tocar

- Los requisitos RF-002 a RF-007 y RF-009.
- Las entradas de mercancía y las devoluciones: no muestran quién las registró.
- El cálculo del stock, el nivel mínimo y las búsquedas.
- Las tablas de productos y variantes.
- Los diagramas C4 de contexto y de contenedores.

## Riesgos

- Si el dueño y el vendedor comparten el mismo dispositivo y no cambian de usuario, el dato sería falso. Probabilidad media.
- Si pidiera identificarse en cada venta, rompería el límite de 3 pasos. Probabilidad baja, porque la identificación es una sola vez al abrir.
- Que el módulo Usuarios crezca después con contraseñas y permisos, que nadie pidió. Probabilidad media.
- De no hacerlo: seguir sin pista para encontrar el origen de un descuadre de stock.

## Alternativas consideradas

1. **Identificarse una vez al abrir el sistema y guardar el usuario en cada venta.** Implica un módulo nuevo (Usuarios), cuesta unas 13 horas y deja pendientes los permisos por rol. Me inclino por esta.
2. **Elegir quién registra la venta en cada venta, con una lista.** Es más simple y no necesita módulo nuevo (unas 7 horas), pero agrega un paso a cada venta y se puede equivocar al elegir.

## Estimación de esfuerzo

| Concepto | Esfuerzo |
|---|---|
| Cambios de diseño y documentación | 4 horas |
| Implementación | 6 horas |
| Pruebas | 3 horas |
| **Total** | **13 horas** |

**De dónde sale este número.** Lo comparé con RF-005 Registrar devolución, que también agrega un registro unido a otra pieza. Esperé algo más grande porque aquí aparece un módulo nuevo y hay que actualizar más documentos.

Supuse que solo hay dos usuarios fijos (dueño y vendedor), que no hay contraseñas y que las ventas anteriores quedan sin usuario. Dejé fuera mostrar quién registró entradas y devoluciones, permisos distintos por rol y reportes por vendedor.

## Recomendación

Aceptar, con dos condiciones, que la persona se identifique una sola vez por sesión, para no romper RNF-USA-002, y que el módulo nuevo quede registrado en un ADR-002. Es un cambio perfectivo de costo moderado, y la parte indirecta (documentos y pruebas) pesa casi lo mismo que la directa.
