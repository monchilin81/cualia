# cualia
 
**¿Qué IA necesito para esto?**
 
El problema con las IAs no es que haya pocas. Es que hay demasiadas y nadie sabe cuál usar para cada cosa. La gente acaba usando ChatGPT para todo, perdiendo horas con la herramienta equivocada, o directamente sin aprovechar lo que existe.
 
cualia resuelve eso. Describes lo que quieres hacer y el sistema razona sobre tu caso concreto para recomendarte la IA correcta, explicarte por qué, y decirte exactamente cómo empezar.
 
---
 
## Qué hace
 
- **Recomendaciones por tarea** — no listas genéricas. El motor entiende si quieres crear un Excel desde cero o analizar datos existentes, si sabes programar o no, si necesitas algo gratis o puedes invertir. La respuesta cambia según el contexto.
 
- **Preguntas cuando hace falta** — si la consulta es ambigua, pide un dato concreto antes de recomendar. Una pregunta, no un formulario.
 
- **Directorio de 85+ herramientas** — organizadas por categoría, con precio real, plan gratuito y si tienen descuento para estudiantes. Filtrable y con comparativa entre dos herramientas.
 
- **Stack del día a día** — un wizard de 4 preguntas que arma tu combinación personal de IAs según tu perfil, tus usos y tu presupuesto.
 
---
 
## Stack
 
Frontend estático en HTML/CSS/JS vanilla — sin frameworks, sin dependencias, sin build step. Un fichero.
 
Backend mínimo: una serverless function en Vercel que proxea las peticiones a [Groq](https://groq.com) (Llama 3.3 70b). Gratis, ~1 segundo de respuesta. La API key vive en el servidor, nunca en el cliente.
 
Si no hay conexión, el motor de reglas local cubre los casos más comunes sin llamada a ninguna API.
 
---
 
## Por qué Groq y no OpenAI
 
Groq es gratuito sin tarjeta de crédito, tiene 6.000 peticiones/día en el plan free y su latencia es sub-segundo. Llama 3.3 70b razona bien sobre comparativas y casos de uso. Para lo que hace esta app, es más que suficiente y evita cualquier fricción de pago.
 
---
 
Hecho por [monchilin](https://buymeacoffee.com/monchilin).
 
 
Directorio de IAs con recomendaciones potenciadas por IA real (Groq/Llama 3.3 70b).
**Completamente gratis** — Groq tiene 6.000 peticiones/día sin tarjeta de crédito.
