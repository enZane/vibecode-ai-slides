---
title: ¿Estás programando o apostando?
info: |
  ## ¿Estás programando o apostando?
  Estrategias de trabajo con IA para una mejor experiencia de vibecoding.

  Comparando el uso de IA con el póker: ¿azar o estrategia?

drawings:
  persist: true
transition: slide-left
mdc: true
layout: cover
---

<!-- Timing: 0:00-0:30 (30 seconds) - Opening hook -->

<div class="absolute inset-0 w-full h-full">

<div class="card top-3 text-right">
<h1 class="!text-5xl">
Una más y ya!
</h1>
<h3 class="!text-4xl ml-16">
Vibecoding con IA: ¿Azar o estrategia?
</h3>
</div>

<img src="/cards_nextjs.png" alt="Cartas de herramientas de IA" class="w-full h-auto object-cover absolute inset-0 -z-2">


</div>

<style>
  :root {
  --primary-900: hsl(256, 43%, 7%);
  --primary-800: hsl(240, 24%, 13%);
    
  --primary-600: hsl(252, 9%, 22%);
  --primary-500: hsl(259, 13%, 28%);
  --primary-400: hsl(254, 22%, 32%);

  --primary-300: hsl(251, 13%, 68%);
  --primary-200: hsl(240, 15%, 76%);
  --primary-100: hsl(240, 21%, 88%);

  --neutral-100: hsl(0, 0%, 100%);

  --accent-400: hsl(93, 60%, 69%);

  --text-1: var(--neutral-100);
  --text-2: var(--primary-100);
  --text-3: var(--primary-200);

  --surface-1: var(--primary-900);
  --surface-2: var(--primary-800);
  --surface-3: var(--primary-700);

  --border-1: var(--primary-500); /* top */
  --border-2: var(--primary-600); /* bottom */
}
  .card {
  --border-width: 1px;
  padding: 2rem;
  border-radius: 1rem;
  position: relative;
  color: white;
  background: hsl(from var(--surface-3) hsl / 0.25);
  backdrop-filter: blur(12px);
}
.card::before {
  content: "";
  position: absolute;
  z-index: -1;
  inset: 0;
  border-radius: inherit;
  border: var(--border-width) solid transparent;
  background: linear-gradient(var(--border-1), var(--border-2)) border-box;
  mask: linear-gradient(black, black) border-box,
    linear-gradient(black, black) padding-box;
  mask-composite: subtract;
}
  .slidev-page .slidev-page-1 {
    position: unset;
  }
  div {
    padding: 0;
  }
</style>

---
layout: center
transition: slide-up
---

<!-- Timing: 0:30-1:00 (30 seconds) - Agenda -->

# Agenda 📋

- 🎯 **La realidad**: IA como azar vs estrategia
- 🃏 **El paralelismo**: Póker y desarrollo con IA
- 🔧 **Las herramientas**: PRDs, MCP, y Cursor rules
- 🎵 **Vibecoding intencional**: Cómo hacerlo bien
- 💭 **Reflexión**: Qué decisión tomas hoy


---
transition: slide-up
---

<!-- Timing: 1:00-2:00 (60 seconds) - Audience engagement + AI tools showcase -->

<div>
  <h1
    :initial="{ y: -100, opacity: 0 }"
   class="text-4xl font-bold text-center w-full">
    ¿Quién aquí ha usado ChatGPT más de 5 veces esta semana? 🙋‍♀️
  </h1>
</div>

  <FallingCard
    name="Cursor"
    v-click
    iconBg="bg-blue-400/20"
    textColor="text-blue-400"
    :initial="{ x: 50, rotate: -25 }"
    :enter="{ y: 80, x: 30, rotate: -15, opacity: 1 }"
  />
  <FallingCard
    name="Copilot"
    v-click
    iconBg="bg-green-400/20"
    textColor="text-green-400"
    :initial="{ x: 230, rotate: 15 }"
    :enter="{ y: 200, x: 150, rotate: 10, opacity: 1 }"
  />
  <FallingCard
    name="v0"
    v-click
    iconBg="bg-white/20"
    textColor="text-white"
    :initial="{ x: 360, rotate: -20 }"
    :enter="{ y: 100, x: 300, rotate: -8, opacity: 1 }"
  />
  <FallingCard
    name="Lovable"
    v-click
    iconBg="bg-pink-400/20"
    textColor="text-pink-400"
    :initial="{ x: 440, rotate: 20 }"
    :enter="{ y: 240, x: 420, rotate: 12, opacity: 1 }"
  />
  <FallingCard
    name="Claude"
    v-click
    iconBg="bg-orange-400/20"
    textColor="text-orange-400"
    :initial="{ x: 590, rotate: -10 }"
    :enter="{ y: 70, x: 600, rotate: -5, opacity: 1 }"
  />
  <FallingCard
    name="Fusion"
    v-click
    iconBg="bg-purple-400/20"
    textColor="text-purple-400"
    :initial="{ x: 600, rotate: -50 }"
    :enter="{ y: 220, x: 700, rotate: -20, opacity: 1 }"
  />

---
layout: image
transition: fade
---

<!-- La realidad del desarrollo con IA hoy -->

<div class="pl-42 w-full h-full">
  <Tweet id="1925478344147050760" />
</div>

---
transition: slide-right
---

<div class="text-2xl mt-4 ml-2 flex flex-col items-start">

<h1 class="font-bold text-red-500">
The war is over.
</h1>

<img  src="https://i.chzbgr.com/full/9917713920/h377F5AC4/redmond-wa-azure-performance-team-august-2017-present-office-365-foundation-engineering-see-more" alt="Meme sobre el fin de la guerra IA vs Desarrolladores" class="max-w-md self-center" />
</div>




---
layout: section
---

<!-- Timing: 2:30-3:30 (60 seconds) - Problem identification -->

## ¿Pero, quién no ha tenido ese momento de...

<div v-click class="mt-4 text-3xl italic text-primary py-3">

_"Otra vez, ¿por qué no me da lo que quiero?"_

</div>

<div v-click class="mt-4 text-3xl italic text-primary py-3">

_"Pero si centrar un div es lo más fácil del mundo..."_

</div>

<div v-click class="mt-4 text-3xl italic text-primary py-3">

_"Si lo hubiera hecho yo, ya estaría listo"_

</div>



---
transition: slide-up
---

<!-- Timing: 3:30-4:30 (60 seconds) - Core analogy introduction -->

# Y es que la IA generativa puede ser dos cosas... 🎯

<div class="grid grid-cols-2 gap-8 mt-8">

<div v-click>
  <div class="text-center p-8 bg-red-500/20 rounded-lg">
    <div class="text-6xl mb-4">🎰</div>
    <h3 class="text-xl font-bold">Juego de Azar</h3>
    <p class="text-sm mt-2 opacity-80">Iteración sin intención</p>
  </div>
</div>

<div v-click>
  <div class="text-center p-8 bg-blue-500/20 rounded-lg">
    <div class="text-6xl mb-4">🃏</div>
    <h3 class="text-xl font-bold">Partida de Póker</h3>
    <p class="text-sm mt-2 opacity-80">Estrategia bajo incertidumbre</p>
  </div>
</div>

</div>

<div v-click class="mt-8 text-center">

**La IA puede ser ambas cosas. Tú decides cuál.**

</div>


---
layout: section
---

# 🤖 IA Generativa: Azar + Estrategia


---

# La realidad técnica 📊

<v-clicks class="space-y-4">

- **Predicción estadística**: Cada prompt es una tirada
- **Hay ruido, probabilidad, variabilidad**
- **Eso no es malo** ❌ si sabemos qué juego estamos jugando
- **Lo peligroso**: Iterar sin intención como apostadores buscando el jackpot 🎰

</v-clicks>

<div v-click class="mt-12 p-4 bg-yellow-500/20 rounded-lg">
  <div class="flex items-center gap-2">
    <div class="text-2xl">⚠️</div>
    <div>
      <strong>El problema no es el azar.</strong><br>
      <span class="text-sm opacity-80">El problema es no tener estrategia.</span>
    </div>
  </div>
</div>

---
layout: image-right
image: https://www.reviewjournal.com/wp-content/uploads/2024/06/19289092_web1_WSOP-061324-es_004.jpg?w=700
---

<!-- Timing: 5:00-6:00 (60 seconds) - Poker analogy deepening -->

# El póker también tiene azar 🎲

<v-clicks>

- **Los mejores jugadores del mundo son siempre los mismos** 🏆
- **¿Por qué?** 🤔
- **Porque juegan con estrategia** 🧠

</v-clicks>

<div v-click class="mt-8 space-y-2">

## Igual que nosotros como devs:


- ✅ Decisiones bajo incertidumbre
- ✅ Recursos limitados
- ✅ Ajuste en tiempo real

</div>

---
layout: section
---

# 🔧 Leyendo la mesa


---

# Lo que hace un buen jugador de póker... 🎯

<div v-click class="mt-4">

## Se parece mucho a sistemas que usamos para trabajar con IA:

</div>

<div class="grid grid-cols-2 gap-6 mt-8">

<div v-click class="p-4 bg-blue-500/10 rounded-lg">
  <h3 class="font-bold text-lg mb-2">🔌 Model Context Protocol (MCP)</h3>
  <ul class="text-sm space-y-1">
    <li>Conecta IA con fuentes de datos específicas</li>
    <li>Protocolo estándar para dar contexto</li>
    <li>Como "USB-C para aplicaciones de IA"</li>
    <li><strong>Estratégico: sabe qué datos necesita</strong></li>
  </ul>
</div>

<div v-click class="p-4 bg-green-500/10 rounded-lg">
  <h3 class="font-bold text-lg mb-2">⚙️ Project Managers y PRDs</h3>
  <ul class="text-sm space-y-1">
    <li>Decisiones iterativas</li>
    <li>Control bajo feedback</li>
    <li>Adaptación continua</li>
    <li><strong>Intencional, no aleatorio</strong></li>
  </ul>
</div>

</div>


---
layout: quote
---

# La IA es el sueño de cualquier Project Manager:
# Un programador que hace lo que le piden.

---
layout: center
---

<!-- Timing: 7:30-8:30 (60 seconds) - Decision framework -->

# 🧠 Framework de decisión: ¿Cuándo usar IA estratégicamente?

<div class="grid grid-cols-2 gap-12 mt-8">

<div class="p-6 bg-blue-500/10 rounded-lg">
  <h3 class="text-xl font-bold mb-4 text-center">Hazlo CON IA 🤖</h3>
  <ul class="space-y-2 text-sm">
    <li>✅ Patrones conocidos (login, CRUD)</li>
    <li>✅ Tienes specs claras</li>
    <li>✅ Framework/libs definidos</li>
    <li>✅ Iteración rápida (prototipo)</li>
    <li>✅ Código boilerplate</li>
    <li>✅ Traducción entre formatos</li>
  </ul>
</div>

<div class="p-6 bg-orange-500/10 rounded-lg">
  <h3 class="text-xl font-bold mb-4 text-center">Hazlo TÚ 🧑‍💻</h3>
  <ul class="space-y-2 text-sm">
    <li>⚠️ Lógica de negocio compleja</li>
    <li>⚠️ Arquitectura nueva</li>
    <li>⚠️ Rendimiento crítico</li>
    <li>⚠️ Código seguridad-sensible</li>
    <li>⚠️ Debugging profundo</li>
    <li>⚠️ Sin patrones claros</li>
  </ul>
</div>

</div>

<div class="mt-8 text-center">
<div class="text-lg font-bold">La clave: **Saber cuándo delegar y cuándo liderar**</div>
</div>

---
layout: section
---

# 🎵 Vibecoding con intención


---

# ¿Qué es vibecoding? 🌊

<div class="mt-6">

<div class="p-6 bg-purple-500/10 rounded-lg">
  <div class="text-2xl mb-4">
  
  💫 **"Construir software con IA sin revisar el código que escribe"**

  </div>
  <div class="text-lg opacity-80 text-right">— Andrej Karpathy & Simon Willison</div>
</div>

</div>

<div class="mt-8">

<v-clicks class="space-y-4 mt-8 text-xl">

- Iterar rápido, fallar rápido y aprender rápido 🚀
- Perfecto para prototipos 🗑️
- Con las reglas adecuadas, no es azar 🎯

</v-clicks>

</div>

---

## Pero cuando se convierte en... 😰

<div>

- Promptear sin reglas ni specs → **Vibe-gambling** 🎰

![Local image](/give-me-money.png)

</div>

---

## Pero cuando se convierte en... 😰

- Código de producción → **Si no la controlas, te controla** 🍃

![External image](https://nmn.gl/blog/assets/vibe-coding-security.webp)

---

## Pero cuando se convierte en... 😰

- Sin intención ni estrategia → **Frustración garantizada** 😤

<img src="https://pbs.twimg.com/media/GtlBJYPXUAQgwO5?format=jpg&name=4096x4096" alt="Frustración con IA" class="w-full max-w-md mx-auto mt-4 rounded-lg">


---
layout: section
---

# Pero no todo está perdido... 🙌

---

# Back to the basics 🎓

## Ingeniería de Software 101: PRDs y User Stories

<div class="grid grid-cols-2 gap-8 mt-8">

<div class="p-4 bg-blue-500/10 rounded-lg">
  <h3 class="font-bold text-lg mb-2">📋 Product Requirements Document</h3>
  <ul class="text-sm space-y-1">
    <li><strong>Visión general:</strong> "Usar Better Auth para autenticación"</li>
    <li><strong>Contexto:</strong> Por qué necesitamos esta solución</li>
    <li><strong>Objetivos:</strong> Seguridad, UX, mantenimiento</li>
  </ul>
</div>

<div class="p-4 bg-green-500/10 rounded-lg">
  <h3 class="font-bold text-lg mb-2">📝 User Stories</h3>
  <ul class="text-sm space-y-1">
    <li><strong>As a [user type], I want [goal] so that [benefit]</strong></li>
    <li>Contexto específico por tarea</li>
    <li>Corresponde a una parte del PRD</li>
    <li>Tareas específicas para la IA</li>
    <li>Fácil de probar y validar funcionamiento</li>
  </ul>
</div>

</div>

---

# Product Requirement Documents

<img src="https://substack-post-media.s3.amazonaws.com/public/images/756acf42-20c1-4631-841a-a48378f81310_2000x1414.png" class="w-full max-w-2xl mx-auto mt-[-4px] rounded-lg" alt="Oldies but goodies">

---

# User Stories

<div class="text-center mt-8">
  <img src="https://www.agile-academy.com/media/pages/agiles-lexikon/user-story/53ec3cb669-1749126240/04_user_story_card-eng-min.png" class="w-full max-w-2xl mx-auto rounded-lg" alt="User Stories">
</div>

---
layout: section
---

# Design Systems


<video src="/atomic-design-tokens.mp4"  autoplay loop muted playsinline class="w-full max-w-2xl mx-auto rounded-lg" />


---
layout: center
---

# El puente perfecto 🌉

<div class="space-y-6 mt-8">

<div v-click class="p-6 bg-purple-500/10 rounded-lg">
  <div class="text-xl font-bold mb-2">🔗 Metodologías clásicas + IA moderna</div>
  <div class="opacity-80">Las herramientas que ya conocemos se vuelven perfectas para estructurar el trabajo con LLMs</div>
</div>

<div v-click class="p-6 bg-blue-500/10 rounded-lg">
  <div class="text-xl font-bold mb-2">📋 PRD → Contexto para la IA</div>
  <div class="opacity-80">"Vamos a usar Better Auth porque necesitamos autenticación segura y fácil de mantener"</div>
</div>

<div v-click class="p-6 bg-green-500/10 rounded-lg">
  <div class="text-xl font-bold mb-2">📝 User Stories → Prompts específicos</div>
  <div class="opacity-80">"Instala Better Auth en Next.js, configura las variables de entorno, crea el middleware..."</div>
</div>

</div>

<div v-click class="mt-8 text-center text-xl font-bold">
Define antes de promptear - Dale a la IA las reglas del juego 🎯
</div>

---
layout: default
---

# Cursor rules

## El último eslabón: Configuración contextual

Una vez que tienes tus PRDs y User Stories, Cursor rules asegura que la IA mantenga consistencia con tu proyecto específico: patrones, estilo y arquitectura.

<img src="/cursor-rules.png" class="w-full max-w-2xl mx-auto mt-[4px] rounded-lg shadow-lg" alt="Ejemplo de configuración de Cursor rules">

---
layout: center
---

<!-- Timing: 8:30-9:30 (60 seconds) - Key takeaways -->

# 📚 Takeaways clave

<div class="space-y-4 max-w-4xl mx-auto">

<div v-click class="p-4 bg-blue-500/10 rounded-lg">
  <div class="text-xl font-bold mb-2">🎯 La IA no es magia, es probabilidad</div>
  <div class="opacity-80">Acepta el azar, pero juega con estrategia como en el póker</div>
</div>

<div v-click class="p-4 bg-green-500/10 rounded-lg">
  <div class="text-xl font-bold mb-2">📋 Define antes de promptear</div>
  <div class="opacity-80">PRDs, User Stories, specs - dale a la IA las reglas del juego</div>
</div>

<div v-click class="p-4 bg-orange-500/10 rounded-lg">
  <div class="text-xl font-bold mb-2">🤖 Usa AI para patrones, TÚ para la arquitectura</div>
  <div class="opacity-80">Delega lo repetitivo, mantén control sobre lo complejo</div>
</div>

<div v-click class="p-4 bg-purple-500/10 rounded-lg">
  <div class="text-xl font-bold mb-2">🎵 Vibecoding > Vibe-gambling</div>
  <div class="opacity-80">Con intención y framework, no iteración ciega</div>
</div>

</div>

---
layout: section
---

# 💭 Reflexión final


---
layout: center
---

# La IA puede ser una herramienta poderosa... 🔧

<div v-click class="mt-8 text-3xl">

**...o una máquina de apuestas** 🎰

</div>

<div v-click class="mt-8 text-2xl text-center">

**Si jugamos sin plan,** 
**estamos planeando perder.** 🎲

</div>


---
layout: center
---

<!-- Timing: 9:30-10:00 (30 seconds) - Final call to action -->

<div class="text-left max-w-2xl mx-auto">


# La próxima vez que trabajes con IA, no preguntes:

<div v-click class="text-2xl mb-6 text-red-600 line-through">
"¿Qué me va a dar?"
</div>

<div v-click class="text-2xl mb-6 text-green-600">
Pregúntate: 

**"¿Qué estoy decidiendo?"**

</div>

</div>

<div v-click class="mt-12 text-center">

## 🙏 Gracias

<div class="text-lg mt-4 opacity-80">
Si les resonó algo de esto,<br>
me encantará seguir la charla después.
</div>

</div>
