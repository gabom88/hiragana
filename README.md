# かな — Japanese Kana Flashcards

Mini aplicación web para estudiar y practicar **hiragana y katakana mediante flashcards interactivas**.

Está diseñada para sesiones rápidas de estudio y práctica, con diferentes modos de juego, seguimiento del progreso y selección personalizada de los caracteres.

Todo vive en **un solo archivo HTML**: sin dependencias, sin instalación, sin conexión y sin enviar nada a ningún servidor.

Puedes probarlo online aquí 👉 https://gabom88.github.io/hiragana/

![HTML](https://img.shields.io/badge/HTML-1%20archivo-orange)
![Sin dependencias](https://img.shields.io/badge/dependencias-ninguna-brightgreen)
![Offline](https://img.shields.io/badge/offline-sí-blue)
![Caracteres](https://img.shields.io/badge/kana-208-blueviolet)


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

También permite escuchar individualmente cualquier carácter, palabra u oración.

Depende de las voces instaladas en el sistema operativo. En equipos sin voz japonesa disponible, la aplicación lo indica en lugar de fallar en silencio.

### 📚 Explorador de caracteres

Permite consultar todos los caracteres disponibles.

Al seleccionar uno se abre su ficha, que muestra:

* El carácter dentro de una **cuadrícula de práctica** estilo *renshūchō*, con la cruz punteada de referencia.
* Romanización, nivel actual, aciertos y errores.
* Reproducción de pronunciación.

La ficha ofrece tres vistas:

| Vista               | Qué muestra                                              |
| ------------------- | -------------------------------------------------------- |
| **Trazos**          | El glifo con el orden de trazos numerado                 |
| **Impreso**         | La forma impresa habitual                                |
| **Dibujar**         | Lienzo táctil para trazar sobre el glifo atenuado        |

Los números de trazo aparecen únicamente en esta ficha. Las flashcards usan siempre la tipografía japonesa del sistema, sin numeración, para no dar pistas visuales durante la práctica.

Los **caracteres combinados** (きゃ, シュ, ちょ…) se muestran en grande sin cuadrícula: son dos bloques y su orden de trazos es el de sus componentes por separado, no el de una unidad.

### ✏️ Modo dibujar

Lienzo sobre la cuadrícula para practicar el trazo con el dedo o un stylus.

* Funciona con dedo, ratón y stylus mediante *pointer events*.
* El glifo con el orden de trazos queda debajo, atenuado, para calcar encima.
* Suavizado con curvas cuadráticas; en móvil se recogen las posiciones intermedias que el navegador agrupa, para que la línea no salga a tramos.
* Botones **Deshacer** y **Borrar**.
* Los trazos se guardan en coordenadas normalizadas, así que girar el dispositivo no los deforma.

No hay reconocimiento automático de escritura: evaluar si el trazo es correcto necesitaría un modelo que no cabe en un archivo autónomo. La autoevaluación es visual.

### 💬 Palabras

Vocabulario escribible solo con kana, agrupado en **9 categorías y 90 palabras**:

Saludos y cortesía · Números del 1 al 10 · Días y tiempo · Colores · Comida y bebida · Animales · Familia y personas · Cosas del día a día · Préstamos en katakana

Cada entrada muestra el kana, la romanización y el significado en español, y se puede escuchar.

### 🗨️ Oraciones

Frases de uso diario agrupadas por situación: **8 categorías y 70 oraciones**.

Saludos y despedidas · Presentarse · Cortesía y disculpas · Preguntas básicas · En un restaurante o tienda · Cuando no entiendes · Moverse por la ciudad · Frases del día a día

Se eligieron frases que en el uso real se escriben en kana (ありがとうございます, ただいま, がんばって), evitando aquellas que normalmente llevan kanji, para no acostumbrar la vista a una forma que luego no se encuentra.

Las oraciones llevan **espacios entre palabras**. El japonés escrito no los usa, pero sin kanji una frase corrida resulta ilegible para quien empieza; es la misma convención que emplean los materiales de nivel inicial, y la propia pantalla lo advierte.

### 💾 Copia de seguridad

El avance vive en el navegador, así que borrar los datos del sitio lo elimina. La app incluye una pantalla propia para exportarlo e importarlo.

**Exportar**: copia al portapapeles o descarga un `.json` con la fecha en el nombre. Si la API del portapapeles no está disponible (habitual al abrir el archivo con `file://`), recurre a la selección manual del texto.

**Importar**: pegando el contenido o eligiendo un archivo, con dos modos.

| Modo             | Comportamiento                                                                                            |
| ---------------- | --------------------------------------------------------------------------------------------------------- |
| **Combinar**     | Conserva, carácter por carácter, la versión con más práctica acumulada; se queda con el mejor récord de cada modo y con la unión de los días practicados |
| **Reemplazar**   | Descarta el avance actual y deja el de la copia                                                            |

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

Utiliza el almacenamiento disponible del navegador, con `localStorage` como alternativa, por lo que **no necesita una base de datos ni un servidor**.

No hay cuentas ni analítica, y no se realiza ninguna petición de red.

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

La fuente de orden de trazos va **subseteada e incrustada en base64** dentro del CSS: 177 glifos —hiragana y katakana completos, incluidos los pequeños y el alargador `ー`— en formato WOFF, unos 58 KB antes de codificar. Por eso la aplicación funciona sin conexión y sigue siendo un único archivo, de aproximadamente 156 KB en total.

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

| Tecla | Acción               |
| ----- | -------------------- |
| `1`   | Seleccionar opción 1 |
| `2`   | Seleccionar opción 2 |
| `3`   | Seleccionar opción 3 |
| `4`   | Seleccionar opción 4 |
| `Esc` | Salir de la partida  |

En respuestas escritas, `Enter` permite enviar la respuesta.

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
* Caracteres que necesitan repaso.

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
