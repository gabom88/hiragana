# かな — Japanese Kana Flashcards

Mini aplicación web para estudiar y practicar **hiragana y katakana mediante flashcards interactivas**.

Está diseñada para sesiones rápidas de estudio y práctica, con diferentes modos de juego, seguimiento del progreso y selección personalizada de los caracteres.

Todo vive en **un solo archivo HTML**: sin dependencias, sin instalación, sin conexión y sin enviar nada a ningún servidor.

Puedes probarlo online aquí 👉 https://gabom88.github.io/hiragana/

![HTML](https://img.shields.io/badge/HTML-1%20archivo-orange)
![Sin dependencias](https://img.shields.io/badge/dependencias-ninguna-brightgreen)
![Offline](https://img.shields.io/badge/offline-sí-blue)
![Caracteres](https://img.shields.io/badge/kana-208-blueviolet)
![Contenido](https://img.shields.io/badge/palabras%20y%20frases-396-yellow)


## ✨ Características

### 📖 Modo Estudio

Modo de práctica sin límite de tiempo.

* Flashcards de hiragana y katakana.
* Preguntas en ambas direcciones:

  * `か → ka`
  * `ka → か`
  * Mezclado
* Opción múltiple.
* Respuesta escrita mediante teclado.
* Repetición de los caracteres que se fallan.
* Sistema de dominio por carácter.
* Contador de aciertos y racha.

El sistema selecciona con mayor frecuencia los caracteres que tienen un menor nivel de dominio, ayudando a reforzar los que más cuestan.

**No hay avance automático.** Tras responder, la tarjeta se queda en pantalla el tiempo que haga falta para mirar el error, y aparecen dos botones:

* **Practicar este carácter** abre la ficha completa del carácter, con su cuadrícula, su orden de trazos y el lienzo para dibujarlo, sin salir de la partida.
* **Siguiente** continúa. Con teclado, `Enter` o la barra espaciadora hacen lo mismo.

Time Attack y Survival sí avanzan solos, porque ahí el reloj está corriendo.

### ⏱️ Time Attack

Modo contrarreloj para intentar conseguir la mayor puntuación posible.

* Duración configurable.
* Las tarjetas aparecen continuamente.
* **+100 puntos** por respuesta correcta.
* Bonificación por responder rápidamente.
* Bonificación por mantener una racha.
* **−20 puntos** por respuesta incorrecta.
* Registro del récord según la duración seleccionada.

### 💥 Survival

Modo de supervivencia en el que cada tarjeta tiene un tiempo limitado.

* Selección de **10, 20 o 30 tarjetas**.
* Tiempo configurable por tarjeta.
* Barra de tiempo visible.
* **+100 puntos** por acierto.
* Bonificación según el tiempo restante.
* **−50 puntos** por fallo o por quedarse sin tiempo.
* Registro de récords según la configuración utilizada.

### 🔁 Para repasar

Los caracteres fallados no se pierden al terminar la partida. La pantalla de inicio muestra los **10 más recientes**, del último fallo hacia atrás y sin repetidos.

Tanto ahí como en el resumen final de cualquier modo, cada carácter es pulsable y abre su ficha para practicarlo en el momento.

### 🎯 Distractores por parecido visual

Las opciones falsas no salen al azar. Se eligen entre los caracteres que de verdad se confunden, que es donde está el error real del estudiante.

La app combina dos fuentes:

* **Pares confundibles por su forma**: ぬ/め, れ/わ/ね, さ/ち/き, は/ほ, シ/ツ/ソ/ン, ク/タ/ケ, ワ/ウ/フ, ル/レ…
* **Familias del mismo kana base**, deducidas automáticamente al descomponer el carácter y retirar el dakuten: か/が, き/ぎ/きゃ/きゅ/きょ/ぎゃ/ぎゅ/ぎょ…

Cada carácter acaba con unos 4 parecidos de media. Por tarjeta entran **como máximo dos** distractores parecidos y el resto se completa al azar; si fueran siempre los tres, el patrón se volvería adivinable.

Se puede desactivar desde **Ajustes**.

### 📊 Sistema de progreso

Cada carácter tiene su propio nivel de dominio.

El nivel aumenta al responder correctamente y disminuye cuando se comete un error.

El progreso se muestra mediante un **mapa de dominio**, permitiendo identificar rápidamente qué caracteres están:

* Sin practicar
* Nuevos
* En proceso
* Dominados

Un carácter se considera dominado al alcanzar el nivel necesario dentro del sistema de progreso.

### 🔥 Racha de días y calendario

Un día queda marcado en cuanto se responde una tarjeta, usando la **fecha local** del dispositivo.

* Racha actual, mejor racha y días totales.
* Calendario de las últimas **18 semanas**, con el día de hoy remarcado.
* Si todavía no has practicado hoy, la racha **no se rompe** hasta que acabe el día. La pantalla de inicio avisa de que falta la sesión.

### 📝 Diferentes formas de responder

Puedes elegir entre:

* **Opción múltiple**
* **Escribir con el teclado**

Cuando se utiliza la respuesta escrita, la aplicación acepta diferentes romanizaciones equivalentes, por ejemplo:

* `shi` / `si`
* `tsu` / `tu`
* `chi` / `ti`
* `fu` / `hu`
* `ja` / `jya`

Las preguntas en dirección `ka → か` siempre se responden por opción múltiple, ya que escribir kana requeriría un teclado japonés.

Cuando hiragana y katakana están activos a la vez, en esa dirección los distractores se restringen al mismo silabario que la tarjeta y el enunciado indica cuál se pide (*¿Qué katakana es?*). De lo contrario, `ka` tendría dos respuestas correctas.

### 🔤 Grupos de caracteres

La aplicación incluye seis grupos, activables por separado desde **Ajustes**:

| Silabario | Grupo      | Caracteres |
| --------- | ---------- | ---------: |
| Hiragana  | Básicos    |         46 |
| Hiragana  | Dakuten    |         25 |
| Hiragana  | Combinados |         33 |
| Katakana  | Básicos    |         46 |
| Katakana  | Dakuten    |         25 |
| Katakana  | Combinados |         33 |

**208 caracteres en total.** Por defecto se comienza únicamente con los 46 hiragana básicos.

### 🔊 Pronunciación

Lectura en voz alta mediante la API de síntesis de voz del navegador, con varios ajustes finos:

* **Selector de voz**: lista todas las voces `ja-*` instaladas en el sistema. En un mismo Android puede haber dos o tres con calidad muy distinta.
* **Velocidad**: lenta, normal o rápida. Una sílaba suelta a velocidad normal suele salir cortada.
* **Tabla de excepciones**: los motores de voz leen `は`, `へ` y `を` como partículas gramaticales (*wa*, *e*, *o*), lo cual es incorrecto al enseñar la lectura del carácter. La app los sustituye internamente por su katakana equivalente (`ハ`, `ヘ`, `ヲ`). La sustitución solo actúa cuando el texto es exactamente ese carácter suelto, así que dentro de una frase `これは なんですか` se sigue leyendo *kore wa*, que es lo correcto.
* Botón de prueba en Ajustes.

También permite escuchar individualmente cualquier carácter, palabra, oración o entrada del diccionario propio.

Depende de las voces instaladas en el sistema operativo. En equipos sin voz japonesa disponible, la aplicación lo indica en lugar de fallar en silencio.

### 📚 Explorador de caracteres

Permite consultar todos los caracteres disponibles.

Al seleccionar uno se abre su ficha, que muestra:

* El carácter dentro de una **cuadrícula de práctica** estilo *renshūchō*, con la cruz punteada de referencia.
* Romanización, nivel actual, aciertos y errores.
* Reproducción de pronunciación.

La ficha ofrece tres vistas:

| Vista       | Qué muestra                                       |
| ----------- | ------------------------------------------------- |
| **Trazos**  | El glifo con el orden de trazos numerado          |
| **Impreso** | La forma impresa habitual                         |
| **Dibujar** | Lienzo táctil para trazar sobre el glifo atenuado |

Los números de trazo aparecen únicamente en esta ficha. Las flashcards usan siempre la tipografía japonesa del sistema, sin numeración, para no dar pistas visuales durante la práctica.

Los **caracteres combinados** (きゃ, シュ, ちょ…) se muestran en grande sin cuadrícula: son dos bloques y su orden de trazos es el de sus componentes por separado, no el de una unidad.

Esta misma ficha se abre desde el modo Estudio, desde el resumen de la partida y desde la lista de repaso del inicio.

### ✏️ Modo dibujar

Lienzo sobre la cuadrícula para practicar el trazo con el dedo o un stylus.

* Funciona con dedo, ratón y stylus mediante *pointer events*.
* El glifo con el orden de trazos queda debajo, atenuado, para calcar encima.
* En móvil se recogen las posiciones intermedias que el navegador agrupa, para que la línea no salga a tramos.
* Botones **Deshacer** y **Borrar**.
* Los trazos se guardan en coordenadas normalizadas, así que girar el dispositivo no los deforma.

**Paleta de 8 colores** configurable desde Ajustes. El primero es tinta que sigue el tema: negra en modo claro, blanca en oscuro.

**Trazos estilizados**, activables desde Ajustes, hacen dos cosas:

* Dibujan con curvas **Catmull-Rom** convertidas a Bézier cúbicas, que pasan por cada punto llegando con la tangente del vecino, sin esquinas.
* Al levantar el dedo, simplifican el trazo con **Ramer-Douglas-Peucker**, que descarta las muestras casi colineales responsables de los micro-bultos del dedo. La limpieza va al soltar y no durante el trazo, para que la línea no baile mientras dibujas.

No hay reconocimiento automático de escritura: evaluar si el trazo es correcto necesitaría un modelo que no cabe en un archivo autónomo. La autoevaluación es visual.

### 💬 Palabras

Vocabulario escribible solo con kana, agrupado en **19 categorías y 232 palabras**:

Palabras esenciales · Saludos y cortesía · Números · Días y tiempo · Colores · Comida y bebida · En el konbini · En la estación · En el hotel · Lugares · Verbos básicos · Adjetivos útiles · Direcciones · El cuerpo y la salud · El clima · Animales · Familia y personas · Cosas del día a día · Préstamos en katakana

Cada entrada muestra el kana, la romanización y el significado en español, y se puede escuchar.

### 🗨️ Oraciones

Frases de uso diario agrupadas por situación: **15 categorías y 164 oraciones**.

Saludos y despedidas · Presentarse · Cortesía y disculpas · Preguntas básicas · Cuando no entiendes · En el konbini · En un restaurante · Alergias y comida especial · En el tren y el metro · En el aeropuerto · En el hotel · De compras · Preguntar el camino · Emergencias y salud · Frases del día a día

Las categorías de viaje incluyen también **lo que te van a decir a ti**, no solo lo que dices tú. En el konbini aparecen las preguntas de caja (`ふくろは ごりようですか`, `あたためますか`, `おはしは おつけしますか`) junto a las respuestas útiles, empezando por `だいじょうぶです`, que funciona como un «no, gracias».

Se eligieron frases que en el uso real se escriben en kana (ありがとうございます, ただいま, がんばって), evitando aquellas que normalmente llevan kanji, para no acostumbrar la vista a una forma que luego no se encuentra.

Las oraciones llevan **espacios entre palabras**. El japonés escrito no los usa, pero sin kanji una frase corrida resulta ilegible para quien empieza; es la misma convención que emplean los materiales de nivel inicial, y la propia pantalla lo advierte.

### 📓 Diccionario propio

Además del contenido incluido, puedes añadir tus propias palabras. Se pegan en bloque, una por línea:

```text
おはよう, ohayou, Buenos días
ねこ, Gato
がっこう, gakkou, Escuela
```

**La pronunciación es opcional.** Si la omites y el japonés está escrito solo en kana, se calcula sola y aparece marcada como `auto`. La transliteración es determinista y cubre `っ` (duplica la consonante siguiente), `ん` ante vocal (`hon'ya`), el alargador `ー` y los combinados.

Con kanji la app pide la pronunciación en lugar de inventarla: leer 今日 requiere un analizador morfológico con diccionario, de varios megabytes, y aun así la lectura es ambigua según el contexto.

Cuando una línea trae tres campos, el del medio solo se toma como pronunciación si de verdad lo parece: se compara con el romaji que la app puede generar. Así `ねこ, Gato, minino` no confunde «Gato» con una lectura, y la traducción puede llevar comas sin romperse.

Cada entrada se escucha y se elimina individualmente, y el diccionario completo se puede vaciar de una vez.

### 💾 Copia de seguridad

El avance vive en el navegador, así que borrar los datos del sitio lo elimina. La app incluye una pantalla propia para exportarlo e importarlo, accesible desde el inicio y desde **Ajustes**.

**Exportar**: copia al portapapeles o descarga un `.json` con la fecha en el nombre. Si la API del portapapeles no está disponible (habitual al abrir el archivo con `file://`), recurre a la selección manual del texto.

**Importar**: pegando el contenido o eligiendo un archivo, con dos modos.

| Modo           | Comportamiento                                                                                                                                          |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Combinar**   | Conserva, carácter por carácter, la versión con más práctica acumulada; se queda con el mejor récord de cada modo y con la unión de los días practicados |
| **Reemplazar** | Descarta el avance actual y deja el de la copia                                                                                                          |

La copia completa incluye configuración, progreso, récords, días practicados, caracteres pendientes de repaso y el diccionario propio.

El **diccionario también se exporta e importa por separado**, por si quieres compartir solo tu lista de palabras. Al importarlo se añaden las que falten y se respetan las que ya tengas con el mismo japonés.

La importación valida el archivo y descarta claves que no correspondan a kana conocidos, además de sanear los valores fuera de rango.

### 🏆 Récords

Los récords se almacenan de acuerdo con la configuración de cada modo.

Por ejemplo:

* Time Attack — 60 segundos
* Time Attack — 120 segundos
* Survival — 20 tarjetas / 5 segundos

De esta manera, cada configuración tiene su propio récord.

### 🎚️ Contraste de la cuadrícula

El grosor visual de la cuadrícula es configurable desde Ajustes, con tres niveles: **tenue, media y marcada**, y una vista previa en vivo.

La tinta de las líneas se invierte según el tema —negra en claro, blanca en oscuro— de modo que la cuadrícula se mantiene legible en modo oscuro en lugar de desaparecer.

### 🌙 Modo oscuro

Incluye tres opciones de apariencia:

* Automático
* Claro
* Oscuro

En modo automático se adapta a la configuración de apariencia del sistema operativo.

### 💽 Guardado automático

La aplicación guarda automáticamente:

* Configuración.
* Progreso de cada carácter.
* Récords.
* Días practicados.
* Caracteres pendientes de repaso.
* Diccionario propio.

Utiliza el almacenamiento disponible del navegador, con `localStorage` como alternativa, por lo que **no necesita una base de datos ni un servidor**.

No hay cuentas ni analítica, y no se realiza ninguna petición de red.

Borrar el progreso desde Ajustes no toca el diccionario propio.

## 🚀 Uso

No requiere instalación ni dependencias.

Simplemente abre:

```text
hiragana flashcards.html
```

En móvil conviene añadirlo a la pantalla de inicio: se abre a pantalla completa y se comporta como una aplicación nativa.

## 🛠️ Tecnologías

El proyecto está construido utilizando únicamente tecnologías web estándar:

* HTML5
* CSS3
* JavaScript
* Web Speech API
* Canvas 2D y Pointer Events
* LocalStorage

No utiliza frameworks ni librerías externas.

La fuente de orden de trazos va **subseteada e incrustada en base64** dentro del CSS: 177 glifos —hiragana y katakana completos, incluidos los pequeños y el alargador `ー`— en formato WOFF, unos 58 KB antes de codificar. Por eso la aplicación funciona sin conexión y sigue siendo un único archivo, de aproximadamente 188 KB en total.

Toda la romanización del contenido incluido está **generada con el mismo conversor que usa el diccionario**, en lugar de escrita a mano, de modo que las 396 entradas son consistentes con lo que la app calcularía y no puede haber erratas de tecleo.

## 📱 Diseño

La interfaz está diseñada para funcionar especialmente bien en dispositivos móviles, pero también puede utilizarse desde un ordenador. Sigue convenciones visuales de iOS.

Incluye:

* Diseño responsive.
* Interfaz optimizada para pantallas táctiles.
* Atajos de teclado.
* Animaciones y retroalimentación visual.
* Soporte para `prefers-reduced-motion`.
* Adaptación automática al modo oscuro.
* Respeto del `safe-area-inset` en pantallas con notch.

La aplicación limita el contenido principal a un ancho de aproximadamente 520 px para conservar una experiencia similar a una aplicación móvil.

## ⌨️ Atajos de teclado

Durante las preguntas de opción múltiple:

| Tecla             | Acción                            |
| ----------------- | --------------------------------- |
| `1` … `4`         | Seleccionar la opción             |
| `Enter` / `Espacio` | Continuar tras responder, en Estudio |
| `Esc`             | Salir de la partida               |

En respuestas escritas, `Enter` envía la respuesta y, una vez corregida, pasa a la siguiente. Con la ficha de un carácter abierta, `Esc` la cierra.

## 📈 Estadísticas

Al finalizar una sesión se muestra un resumen con:

* Tarjetas respondidas.
* Aciertos.
* Fallos.
* Precisión.
* Mejor racha.
* Tiempo medio por acierto.
* Duración de la sesión.
* Puntos perdidos por errores.
* Caracteres que necesitan repaso, pulsables para practicarlos.

## 🌐 Compatibilidad

Navegadores modernos de escritorio y móvil.

La síntesis de voz incluye varios ajustes para Safari e iOS: una locución muda en el primer toque, ya que iOS exige un gesto del usuario antes de permitir hablar; reintentos al cargar la lista de voces, que llega tarde y a veces vacía; una pausa entre `cancel()` y `speak()`, porque encadenarlos en el mismo ciclo deja la cola bloqueada; y `resume()` si el sintetizador queda en pausa.

## 🎯 Objetivo

El objetivo del proyecto es proporcionar una herramienta **simple, rápida y sin distracciones** para memorizar kana, priorizando los caracteres que el usuario todavía no domina.

No requiere cuentas, conexión a internet, servidores ni sistemas externos para guardar el progreso.

## 🙏 Créditos

Los diagramas de orden de trazos provienen de **KanjiStrokeOrderFont**, de Ulrich Apel y los proyectos Wadoku y AAAA, distribuida bajo una licencia de tipo BSD. El subset incrustado conserva ese crédito dentro de la propia aplicación, y el `LICENCE.txt` original se incluye en el repositorio.

## 📄 Licencia

El código de la aplicación puede modificarse y adaptarse libremente según las necesidades de estudio. La fuente incrustada mantiene su licencia original.
