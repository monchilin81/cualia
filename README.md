# cualia — ¿Qué IA necesito?

Directorio de IAs con recomendaciones potenciadas por IA real (Groq/Llama 3.3 70b).
**Completamente gratis** — Groq tiene 6.000 peticiones/día sin tarjeta de crédito.

---

## Despliegue en Vercel (5 minutos, 0€)

### 1. Consigue tu API key de Groq (gratis, sin tarjeta)
- Ve a https://console.groq.com
- Regístrate con Google → **API Keys → Create API Key**
- Copia la key (empieza por `gsk_...`)

### 2. Sube el proyecto a GitHub
```bash
git init
git add .
git commit -m "first commit"
gh repo create cualia --public --push
# O súbelo manualmente desde github.com/new
```

### 3. Despliega en Vercel
- Ve a https://vercel.com/new
- Selecciona tu repositorio `cualia`
- Click en **Deploy**

### 4. Añade tu API Key de Groq
- En tu proyecto de Vercel → **Settings → Environment Variables**
- Nombre: `GROQ_API_KEY`
- Valor: tu clave `gsk_...`
- Click **Save** → **Redeploy**

¡Listo! La app funciona con IA real, gratis, sin límites prácticos.

---

## Límites de Groq (plan gratuito)
- **6.000 peticiones/día** — más que suficiente
- **500 req/min** — respuestas en ~1 segundo
- Modelo: **llama-3.3-70b-versatile** — excelente calidad

---

## Offline (sin Vercel)
Abre `index.html` directamente en el navegador.
Funciona con el motor de reglas local — sin IA, pero útil.

---

## Estructura
```
cualia/
├── index.html        ← App completa (frontend)
├── api/
│   └── chat.js       ← Proxy serverless → Groq API
├── vercel.json       ← Routing
└── README.md
```


Directorio de IAs con recomendaciones personalizadas.

---

## Despliegue en Vercel (5 minutos)

### 1. Sube el proyecto a GitHub
```bash
git init
git add .
git commit -m "first commit"
gh repo create cualia --public --push
```

### 2. Conecta con Vercel
- Ve a https://vercel.com/new
- Selecciona tu repositorio `cualia`
- Click en **Deploy** (la config ya está en `vercel.json`)

### 3. Añade tu API Key de Anthropic
- En tu proyecto de Vercel → **Settings → Environment Variables**
- Nombre: `ANTHROPIC_API_KEY`
- Valor: tu clave de https://console.anthropic.com
- Click **Save** → **Redeploy**

---

## Desarrollo local

No funciona abriendo `index.html` directamente (CORS).

Opciones para probar en local:

```bash
# Opción A — Vercel dev (recomendado, usa el proxy real)
npm i -g vercel
vercel dev

# Opción B — servidor estático básico
npx serve .
# O con Python:
python -m http.server 3000
# ⚠️ Con servidor estático la API no funciona, solo el directorio
```

---

## Estructura
```
cualia/
├── index.html        # App completa (frontend)
├── api/
│   └── chat.js       # Proxy serverless → Anthropic API
├── vercel.json       # Config de routing
└── README.md
```
