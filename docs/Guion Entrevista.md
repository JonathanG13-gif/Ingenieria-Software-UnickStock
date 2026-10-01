# Guion de entrevista — UnikStock


---

## 1. Preguntas por tramo


### Tramo 1 — Apertura
"Estoy armando un sistema para controlar el inventario de tiendas como la tuya, y esta plática me sirve para entender cómo trabajas hoy antes de diseñar nada. Lo que me cuentes ayuda a que el sistema resuelva problemas reales y no cosas que yo supongo. ¿Te parece bien si voy tomando notas mientras platicamos?"

R = "Sí, claro."

### Tramo 2 — Contexto
1. Cuéntame cómo es un día normal en la tienda, desde que abres hasta que cierras.
2. Además de atender a los clientes, ¿qué otras cosas tienes que hacer o decidir en la tienda durante la semana?

R= "Abro a las diez. Lo primero es acomodar lo que llegó el día anterior y ver qué se vendió. Entre semana entran como quince o veinticinco clientes, y los fines de semana más. Atiendo yo en el mostrador y, cuando hay mucho movimiento, me ayuda el vendedor de medio tiempo. Cierro como a las ocho de la noche."

R= "Decidir qué le compro a los proveedores y llevar las cuentas del negocio. También recibir la mercancía cuando llega."

### Tramo 3 — Proceso actual (cómo lo resuelves hoy)
3. Cuéntame de la última vez que un cliente pidió una talla o color y no supiste al momento si había o no. ¿Qué hiciste paso a paso?
R= "Hace unos días una clienta preguntó por una playera en talla M, en color negro. No me acordaba si me quedaba, así que fui al estante a buscarla y la dejé esperando en el mostrador. Revisé una por una las playeras de ese modelo hasta que la encontré. Tardé como cinco o seis minutos."

4. Cuéntame de la última vez que llegó mercancía nueva a la tienda. ¿Qué hiciste paso a paso, desde que la recibiste hasta que quedó lista para vender?
R = "Llegó un pedido grande de un proveedor y justo había clientes en la tienda. No podía dejarlos esperando, así que fui anotando en un papel lo que llegaba: qué era y cuántas piezas. Lo fui acomodando entre cliente y cliente. Ya en la noche, con calma, pasé lo del papel a la libreta. A veces se me olvida anotar algo o lo paso mal."


5. Piensa en la última vez que se te agotó un producto sin que te dieras cuenta. ¿Cómo te enteraste y qué pasó después con ese cliente?

R= "Una clienta pidió una gorra en un color y ya no tenía. Yo creía que todavía me quedaba una. Me enteré hasta que fui a buscarla y no estaba. Le ofrecí otro color, pero no le gustó y se fue sin comprar."



### Tramo 4 — Dolores
6. De todo lo que implica manejar la tienda, ¿qué parte te quita más tiempo o te genera más dolores de cabeza?

R= "Lo de revisar el estante cada vez que un cliente pregunta si tengo algo. Y que la libreta casi nunca cuadra con lo que realmente hay en la tienda."

### Tramo 5 — Excepciones
7. Cuéntame de una devolución reciente. ¿Qué hiciste con el producto y con el registro de esa venta?

R= "Un cliente regresó un collar que no le quedó. Revisé que estuviera bien y lo volví a poner en la vitrina. En la libreta anoté que lo habían devuelto, pero a veces se me pasa y el conteo ya no coincide."


8. Cuéntame de una vez que hayas vendido algo que, sin saberlo, ya no tenías en esa talla o color. ¿Qué pasó cuando te diste cuenta?

R= "Vendí una playera en una talla que creía tener. Cuando fui a sacarla del estante ya no estaba, porque no había anotado una venta anterior. Tuve que decirle al cliente que no la tenía. Le ofrecí buscarle otra talla, pero se molestó."

### Tramo 6 — Verificación de supuestos
Estas preguntas salen directo de las cosas que todavía tenía como "supuesto sin confirmar" en la especificación; cada supuesto se volvió una pregunta.

| Supuesto que tenía | Pregunta para verificarlo |
|---|---|
| No sabía si es una sola tienda o varias | ¿Cuántas ubicaciones o puntos de venta manejas actualmente? |
| No sabía si vendes también en línea | ¿Por dónde vendes tus productos hoy, además de la tienda física? |
| No sabía quién más opera el sistema aparte de ti | ¿Quiénes usan o usarían el sistema en el día a día, y qué hace cada uno? |
| No sabía qué tan grande es el catálogo | ¿Aproximadamente cuántos productos distintos manejas hoy en tu inventario? |
| No sabía si ya usas algún punto de venta (POS) | ¿Qué usas actualmente para cobrar una venta en la tienda? |

### Tramo 7 — Cierre
"Déjame decirte con mis palabras lo que entendí de cómo trabajas hoy, y tú me corriges donde me haya equivocado." (Resumir en voz alta lo entendido.)
"¿Hay algo que no te pregunté y que debí preguntarte?"

R = "Sí, así es más o menos. Nada más agregaría que lo de la mercancía en el papel me pasa seguido cuando hay mucha gente, y de ahí salen la mayoría de mis errores."

### Revisión de las preguntas
Repasé las 8 preguntas de los tramos 2 al 5 y las 5 de verificación: ninguna se contesta con un simple sí/no y ninguna sugiere la respuesta, así que las dejé tal cual.

---

## 2. Bitácora de la entrevista


**Lo que se confirmó tal cual lo tenía pensado:**
- Es una sola tienda física, sin ventas en línea ni otras sucursales.
- Solo dos personas usan el sistema en el día a día: yo y mi vendedor de medio tiempo. Él vende, pero no decide qué se reabastece; esa parte sigue siendo solo mía.
- El catálogo ronda los 150 productos distintos entre las cuatro categorías (ropa, relojes, collares, gorras).
- No uso ningún sistema de punto de venta. Cobro con una terminal bancaria sencilla y llevo las cuentas aparte en una libreta.

**Un supuesto que resultó falso:**
- Yo traía la idea de que en algún momento iba a necesitar dejar contemplado el manejo de más de una sucursal, aunque fuera a futuro. Al hacer la entrevista quedó claro que eso ni siquiera está en mis planes cercanos, así que lo quité por completo del alcance en vez de dejarlo como algo "fuera de alcance por ahora" — simplemente no aplica.

**Algo que apareció sin que lo esperara:**
- Cuando llega un pedido grande de un proveedor justo mientras hay clientes en el mostrador, la mercancía nueva se queda anotada en un papel para capturarla al sistema más tarde con calma, y a veces se me olvida anotar algo o lo capturo mal después. No había pensado en ese momento específico como una fuente de error. Lo tomé en cuenta para que el registro de entrada de mercancía no pida demasiados datos ni sea lento, porque si lo es, se me sigue quedando todo en el papel.

---

## 3. Ficha de dominio


**Ficha de dominio · Unik Syle**

**Quién eres**
Eres el dueño o dueña de Unik Syle, una tienda de ropa y accesorios (ropa, relojes, collares, gorras). Llevas el negocio tú mismo desde hace cuatro años. Atiendes el mostrador, decides qué se compra a los proveedores y llevas las cuentas. Tienes un vendedor de medio tiempo que te ayuda en las horas de más movimiento.

**Cómo es tu día**
Abres a las diez, acomodas lo que llegó el día anterior y revisas qué se vendió. Entre quince y veinticinco clientes al día entre semana, más los fines de semana. Cuando llega mercancía nueva de un proveedor, a veces coincide con clientes en el mostrador y no alcanzas a acomodarla toda de inmediato.

**Reglas que conoces y no vas a decir si no te preguntan**
- Solo tienes una tienda física; no vendes en línea ni tienes otras sucursales.
- Aparte de ti, solo el vendedor de medio tiempo atiende el mostrador; él vende pero no decide qué reabastecer.
- Manejas alrededor de 150 productos distintos entre las cuatro categorías, contando todas las variantes de talla, color y modelo.
- Para cobrar usas una terminal bancaria sencilla; no tienes ningún sistema de punto de venta, solo la terminal y una libreta para anotar.

**Una excepción que ocurre a veces**
Cuando llega un pedido grande de un proveedor y hay clientes esperando al mismo tiempo, anotas la mercancía nueva en un papel para capturarla después con calma, y algunas veces se te olvida anotar algo o lo capturas mal.

**Lo que te molesta de cómo trabajas hoy**
Cuando un cliente pregunta si tienes una talla o color específico, tienes que ir físicamente al estante a revisar, y a veces lo dejas esperando varios minutos. La libreta donde llevas las cuentas casi nunca cuadra exactamente con lo que hay en el estante.
