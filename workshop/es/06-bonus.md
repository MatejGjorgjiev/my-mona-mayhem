<!-- l10n-sync: source-file="workshop/06-bonus.md" -->
# 🎉 Bonus y extensiones

---

¡Has creado una aplicación de batallas de GitHub completamente funcional! Ahora puedes ir más allá con estos **desafíos abiertos**.

<!-- track:vscode:start -->
Usa **Agent Mode** para todos los desafíos: describe lo que quieres y deja que Copilot te ayude a crearlo.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Usa Copilot CLI para todos los desafíos: combina el contexto de `@file`, `/plan`, el modo normal y `/review` según sea necesario.
<!-- track:cli:end -->

---

## 🏆 Desafío 1: Pancarta del ganador

Cuando se carguen los dos gráficos de contribuciones, compara los totales y anuncia quién ha ganado.

**Qué crear:**
- Comparar las contribuciones totales de ambos usuarios
- Mostrar **"🏆 {username} WINS! 🏆"** con un estilo festivo si hay un ganador claro
- Mostrar **"🤝 IT'S A TIE! 🤝"** si los totales son iguales
- Añadir animación o confeti para darle más ambiente

**Sugerencia de prompt:**
> After both users' contribution data loads, compare total contributions and display a winner banner. Show "🏆 {username} WINS! 🏆" if one user has more contributions, or "🤝 IT'S A TIE! 🤝" if equal. Make it visually exciting with CSS animations.

---

## 🏆 Desafío 2: Contador de rachas

Calcula y muestra la racha más larga de contribuciones consecutivas de cada usuario.

**Qué crear:**
- Analizar los datos de contribuciones día a día
- Encontrar la secuencia más larga de días consecutivos con al menos una contribución
- Mostrar de forma destacada la duración de la racha de cada usuario
- Resaltar quién tiene la racha más larga

**Sugerencia de prompt:**
> Add a streak counter feature that analyzes each user's contribution data to find their longest consecutive contribution streak. Display "🔥 Longest Streak: X days" for each user below their contribution graph.

---

## 🏆 Desafío 3: Historial de batallas

Guarda los resultados de las batallas para que los usuarios puedan consultar sus enfrentamientos anteriores.

**Qué crear:**
- Guardar cada resultado en `localStorage` (nombres de usuario, totales, ganador y fecha y hora)
- Añadir una sección **"Recent Battles"** debajo del área de batalla principal
- Mostrar los últimos 5–10 enfrentamientos y sus resultados
- Añadir un botón "Clear History"

**Sugerencia de prompt:**
> Save battle results to localStorage after each comparison. Add a "Recent Battles" section that displays the last 10 battles with usernames, contribution totals, the winner, and when the battle happened. Include a "Clear History" button.

---

## 🏆 Desafío 4: Efectos de sonido

Añade sonidos de arcade retro con Web Audio API, sin archivos externos.

**Qué crear:**
- Sonido de **moneda insertada** al hacer clic en "Battle!"
- Sonido de **potenciación** cuando los resultados se carguen correctamente
- Sonido de **explosión** si se produce un error (usuario no encontrado o error de API)
- Botón para silenciar y activar el sonido

**Sugerencia de prompt:**
> Add retro arcade sound effects using the Web Audio API (no audio files). Play a coin insert sound on battle start, a power-up sound when results load, and an explosion sound on errors. Generate the sounds programmatically with oscillators and gain nodes. Include a mute toggle.

---

## 🏆 Desafío 5: Secuencia de batalla animada

Crea suspense con una cuenta atrás dramática antes de revelar los resultados.

**Qué crear:**
- Al hacer clic en "Battle!", mostrar una superposición a pantalla completa
- Animar: **"3..."** → **"2..."** → **"1..."** → **"⚡ FIGHT! ⚡"**
- A continuación, mostrar los gráficos de contribuciones con una entrada espectacular
- Usar animaciones CSS o temporizadores de JavaScript

**Sugerencia de prompt:**
> Add an animated battle sequence when the user clicks "Battle!". Show a countdown overlay: "3..." then "2..." then "1..." then "⚡ FIGHT! ⚡" with each step lasting about 1 second. After the countdown, reveal the results with a slide-in animation.

---

## 🏆 Desafío 6: Leyenda de contribuciones

Añade una leyenda de escala de color que coincida con la paleta del gráfico de contribuciones.

**Qué crear:**
- Una leyenda horizontal con los niveles de intensidad de las contribuciones
- Etiquetas desde **"Less"** hasta **"More"**
- Usar la paleta de colores de la respuesta de la API de contribuciones de GitHub
- Colocarla cerca de los gráficos

**Sugerencia de prompt:**
> Add a contribution legend below the graphs showing the color scale from the API's color palette. Display a row of colored squares ranging from "Less" (lightest) to "More" (darkest), matching the actual contribution level colors returned by the API.

---

## 🏆 Desafío 7: Compartir resultados

Permite que los usuarios compartan los resultados de sus batallas con un solo clic.

**Qué crear:**
- Un botón **"📋 Share Results"** que aparezca después de una batalla
- Copiar al portapapeles un resumen de texto con formato
- Incluir los nombres de usuario, los totales de contribuciones y el ganador
- Mostrar brevemente el mensaje de confirmación "Copied!"

**Sugerencia de prompt:**
> Add a "📋 Share Results" button that copies a formatted battle summary to the clipboard. The summary should include both usernames, their contribution totals, and who won. Use the Clipboard API and show a brief "Copied to clipboard!" confirmation.

---

<!-- track:cli:start -->
## 💻 Extras del CLI

Si quieres explorar más funciones de Copilot CLI después del taller principal:

- Usa `copilot -p "Write a conventional commit message for the current git diff"` para generar una respuesta rápida que puedas pegar en Git.
- Ejecuta `/share file` para guardar la sesión como Markdown y consultarla más adelante.
- Usa `/session` y `/session plan` para consultar cómo el CLI registra el trabajo actual.
<!-- track:cli:end -->

## 🎊 ¡Enhorabuena!

¡Has completado el taller **Mona Mayhem: GitHub Battle**! Esto es lo que has conseguido:

### Lo que has creado

- ✅ Una **aplicación web de varias páginas** a partir de una especificación de diseño
- ✅ Una **página de inicio** con temática de arcade retro y diseño adaptable
- ✅ Una **arena de batalla** que obtiene y compara datos reales de contribuciones de GitHub
- ✅ **Gráficos de contribuciones interactivos** con niveles de actividad diferenciados por colores
- ✅ Mejoras de **gestión de errores, estados de carga y accesibilidad**
- ✅ Un **diseño adaptable** para distintos dispositivos

### Lo que has practicado

| Habilidad | Práctica |
|---|---|
| **Ingeniería de contexto** | Proporcionar a Copilot los archivos, las instrucciones y las restricciones adecuadas |
| **Planificación** | Generar y refinar planes de implementación antes de programar |
| **Programación agéntica** | Delegar a Copilot tareas de varios pasos y archivos |
| **Iteración de diseño** | Partir de una dirección visual y refinarla hasta lograr un resultado pulido |
| **Disciplina de revisión** | Inspeccionar los cambios generados por IA antes de confirmarlos |

### 🚀 Sigue aprendiendo

- 📺 [Canal de YouTube de VS Code](https://www.youtube.com/@code) — Consejos, tutoriales y novedades
- 📖 [Documentación de GitHub Copilot](https://docs.github.com/en/copilot) — Documentación y guías oficiales
- 💻 [Documentación de GitHub Copilot CLI](https://docs.github.com/en/copilot/how-tos/copilot-cli) — Instalación, comandos slash y prácticas recomendadas
- 🌟 [Awesome GitHub Copilot](https://github.com/stefanprodan/awesome-github-copilot) — Recursos y ejemplos de la comunidad
- 🛠️ [Talleres de Copilot Dev Days](https://github.com/github/copilot-dev-days) — Más talleres prácticos

---

## 🙏 ¡Gracias!

¡Gracias por participar en este taller! Has comprobado cómo GitHub Copilot puede acelerar todas las fases del desarrollo, desde la planificación y el diseño hasta la implementación y el pulido. Las técnicas que has practicado sirven para cualquier proyecto, framework y escala. ¡Ahora crea algo increíble! 🚀
