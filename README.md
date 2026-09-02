# ひらがな — Japanese Hiragana Flashcards

Mini aplicación web para estudiar y practicar **hiragana japonés mediante flashcards interactivas**.

Está diseñada para sesiones rápidas de estudio y práctica, con diferentes modos de juego, seguimiento del progreso y selección personalizada de los caracteres.

## ✨ Características

### 📖 Modo Estudio

Modo de práctica sin límite de tiempo.

* Flashcards de hiragana.
* Preguntas en ambas direcciones:

  * `か → ka`
  * `ka → か`
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

### 📊 Sistema de progreso

Cada carácter tiene su propio nivel de dominio.

El nivel aumenta al responder correctamente y disminuye cuando se comete un error.

El progreso se muestra mediante un **mapa de dominio**, permitiendo identificar rápidamente qué caracteres están:

* Sin practicar
* Nuevos
* En proceso
* Dominados

Un carácter se considera dominado al alcanzar el nivel necesario dentro del sistema de progreso.

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

### 🔤 Grupos de caracteres

La aplicación incluye tres grupos:

| Grupo      | Caracteres |
| ---------- | ---------: |
| Básicos    |         46 |
| Dakuten    |         25 |
| Combinados |         33 |

Los grupos pueden activarse o desactivarse desde **Ajustes**.

Por defecto se comienza únicamente con los 46 hiragana básicos.

### 🔊 Pronunciación

Incluye lectura en voz alta utilizando la API de síntesis de voz del navegador.

* Voz japonesa `ja-JP`.
* Puede activarse o desactivarse desde Ajustes.
* También permite escuchar individualmente cualquier carácter desde el explorador de caracteres.

### 📚 Explorador de caracteres

Permite consultar todos los caracteres disponibles.

Al seleccionar uno se muestra:

* Hiragana en tamaño grande.
* Romanización.
* Nivel actual.
* Número de aciertos.
* Número de errores.
* Reproducción de pronunciación.

### 🏆 Récords

Los récords se almacenan de acuerdo con la configuración de cada modo.

Por ejemplo:

* Time Attack — 60 segundos
* Time Attack — 120 segundos
* Survival — 20 tarjetas / 5 segundos

De esta manera, cada configuración tiene su propio récord.

### 🌙 Modo oscuro

Incluye tres opciones de apariencia:

* Automático
* Claro
* Oscuro

En modo automático se adapta a la configuración de apariencia del sistema operativo.

### 💾 Guardado automático

La aplicación guarda automáticamente:

* Configuración.
* Progreso de cada carácter.
* Récords.

Utiliza el almacenamiento disponible del navegador, con `localStorage` como alternativa, por lo que **no necesita una base de datos ni un servidor**.

## 🚀 Uso

No requiere instalación ni dependencias.

Simplemente abre:

```text
hiragana flashcards.html
```

en un navegador moderno.

También puede alojarse directamente como una página estática, por ejemplo mediante **GitHub Pages**.

## 🛠️ Tecnologías

El proyecto está construido utilizando únicamente tecnologías web estándar:

* HTML5
* CSS3
* JavaScript
* Web Speech API
* LocalStorage

No utiliza frameworks ni librerías externas.

## 📱 Diseño

La interfaz está diseñada para funcionar especialmente bien en dispositivos móviles, pero también puede utilizarse desde un ordenador.

Incluye:

* Diseño responsive.
* Interfaz optimizada para pantallas táctiles.
* Atajos de teclado.
* Animaciones y retroalimentación visual.
* Soporte para `prefers-reduced-motion`.
* Adaptación automática al modo oscuro.

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

## 🎯 Objetivo

El objetivo del proyecto es proporcionar una herramienta **simple, rápida y sin distracciones** para memorizar hiragana, priorizando los caracteres que el usuario todavía no domina.

No requiere cuentas, conexión a internet, servidores ni sistemas externos para guardar el progreso.

---



Este proyecto puede modificarse y adaptarse libremente según las necesidades de estudio.
