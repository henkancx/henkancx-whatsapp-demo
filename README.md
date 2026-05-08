# HenkanCX Agent for WhatsApp — Live Demo

> Demo interactivo del agente conversacional de HenkanCX sobre WhatsApp Business API. Reproduce un flujo completo de soporte técnico con NLP, IA generativa, consulta de datos en CRM/ERP, troubleshooting guiado y creación de orden de servicio en autogestión total.

🌐 **Demo en vivo:** https://henkancx.github.io/henkancx-whatsapp-demo/

---

## ¿Qué muestra este demo?

Un caso real de soporte técnico para reparación de refrigeradora, donde la clienta **María** interactúa con **Henky**, el agente conversacional de HenkanCX, completamente sobre WhatsApp Business — sin transferencia a humanos, sin formularios, sin esperas.

### Capacidades demostradas

| Capacidad | Implementación en el flujo |
|---|---|
| 🧠 **NLP + IA generativa** | María escribe en lenguaje natural ("mi refri no enfría desde anoche 😩"), no menús ni opciones numeradas |
| 🔍 **Consulta de datos** | El agente consulta CRM + ERP en tiempo real y devuelve nombre, dirección, modelo, S/N y vigencia de garantía |
| 🛠️ **Troubleshooting guiado** | Mini-diagnóstico de 3 preguntas estructuradas que evita visitas innecesarias |
| 🎯 **Diagnóstico con IA** | Análisis de síntomas + historial → diagnóstico preliminar razonado |
| ⚡ **Quick replies nativos** | Selección de ventana horaria con botones de WhatsApp |
| 📋 **Creación de orden de servicio** | Asignación automática de técnico, fecha, repuestos y costo final |
| 🔁 **Autogestión completa** | El cliente nunca habla con un humano y resuelve en menos de 5 minutos |

---

## Stack visual

- HTML/CSS/JS vanilla — single-file, sin dependencias
- Mockup de iPhone con Dynamic Island, bezel realista y tilt 3D
- WhatsApp Business UI fiel: header verificado, banner E2E, burbujas con cola, checks azules
- Animaciones: typing indicators, bubble entrance, status dinámico ("escribiendo…" / "en línea")
- Paleta de marca HenkanCX: Magenta Pulse `#CB6CE6`, Royal Purple `#833AE0`, Midnight Navy `#0D1B2A`
- Tipografía: Bricolage Grotesque (display) + Inter (UI)

---

## Despliegue en GitHub Pages

1. **Settings** → **Pages**
2. **Source:** Deploy from a branch
3. **Branch:** `main` / root (`/`)
4. Guarda y espera ~1 minuto. La URL será:
   `https://henkancx.github.io/henkancx-whatsapp-demo/`

---

## Personalización

Toda la conversación está definida en el array `conversation` dentro del `<script>` al final de `index.html`. Cada paso es un objeto:

```js
{ type: 'in' | 'out' | 'system' | 'typing' | 'enc',
  content: 'HTML del mensaje',
  meta: '9:42 AM',
  delay: 800,        // ms antes de mostrar
  duration: 1200,    // solo para typing
  quickReplies: [],  // botones opcionales
  receipt: { ... }   // tarjeta de orden de servicio opcional
}
```

Para adaptar el demo a otro caso de uso (cobranza, ventas, reservas, reclamos), basta con reescribir el array.

---

## Sobre HenkanCX

HenkanCX automatiza el CX de punta a punta sobre WhatsApp Business API oficial, contact center con IA, inspecciones inteligentes (Snnapi), gestión de telecom (TeleInspect Suite) y soluciones por industria.

**Transformamos la experiencia del cliente desde el día 1.**

🌐 [henkancx.com](https://henkancx.com) · 📧 info@henkancx.com · 📍 Ciudad de Panamá

---

© 2026 HenkanCX. Todos los derechos reservados.
