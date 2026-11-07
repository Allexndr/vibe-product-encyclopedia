---
name: vibe-product-encyclopedia
description: Mega-Habilidad Universal derivada de la Enciclopedia de Producto e Ingeniería de 978 páginas (Estándar Senior 30Y). Enruta automáticamente cualquier desafío de ingeniería o producto (Discovery, UI/UX, Arquitectura, AppSec, Alta Concurrencia, Enjambre de Agentes) a lo largo de 87 capítulos no lineales.
---

# HABILIDAD UNIVERSAL: ENCICLOPEDIA DE PRODUCTO Y VIBE CODING (SENIOR 30Y PLAYBOOK)

Esta habilidad transforma la enciclopedia de 978 páginas en un **reflejo ejecutable para tu asistente de IA**. No resumas teoría de libros de texto: ante cualquier solicitud del usuario, detecta de forma autónoma la fase del producto, activa el protocolo correspondiente y entrega soluciones al nivel de un Ingeniero Principal y Director de Producto con más de 30 años de experiencia.

> 🌐 **Reflejo Multilingüe:** Detecta el idioma del usuario y responde con total naturalidad en español, inglés, ruso, kazajo, chino o cualquier idioma solicitado, manteniendo inalterados los estándares de ingeniería de software Senior 30Y.

---

## 1. MATRIZ DE ENRUTAMIENTO AUTOMÁTICO (SITUACIÓN → PROTOCOLO Y PUERTAS DURAS)

| Situación / Solicitud del Usuario | Sección Aplicable y Estándar | Puertas Obligatorias de Calidad (Hard Gates) |
| :--- | :--- | :--- |
| **1. Nueva Idea / Función / Producto desde Cero** | **Discovery, JTBD & Unit Economics (Capítulos II-04..07, III-06)** | Prohibido escribir código sin definir problema raíz, segmento de usuario, JTBD, métrica de éxito y cálculo de servilleta de economía unitaria. Aplicar Reverse Prompting (5 preguntas de diagnóstico de puntos ciegos). |
| **2. Diseño, Landing Page, UI/UX, Animaciones** | **Anti-AI-Slop Design & Visual Engineering (Capítulos I-3, I-6, II-35..37)** | Tolerancia cero con degradados morados genéricos de SaaS e Inter por defecto. Ritmo de 7 pantallas, áreas táctiles `>= 44×44px`, auditoría con `npx impeccable detect`, tokens fijados en `UX_OPEN_REFERENCE_LOCK.md`. |
| **3. Arquitectura, Base de Datos, APIs, Alta Carga** | **FSD, Clean Architecture & High-Load (Capítulos I-5, II-10..18)** | Aislamiento estricto de capas (`app -> widgets -> features -> entities -> shared`), validación de esquemas en bordes (`Zod .strict()`), prohibición de consultas `N+1`, índices compuestos y paginación por cursor. |
| **4. Implementación de Código, Refactorización** | **Senior Vibe-Engineering & Context Hygiene (Capítulos I-2, III-08, III-12)** | Cero marcadores de posición (`TODO`, `mockData`, lógica incompleta). Al alcanzar el 45–50% de contexto, serializar el estado en `HANDOFF.md`. Verificar `.gitignore` y evitar binarios `>10MB`. |
| **5. Seguridad, Infraestructura, Docker, Pagos** | **Zero-Trust DevSecOps & OWASP ASVS L3 (Capítulos I-2, I-7, II-32, IV-3)** | 1) En `docker-compose.yml`, vincular puertos de BD ÚNICAMENTE a `127.0.0.1:5432:5432` (¡Docker elude las reglas de UFW!); 2) Defensa contra SSRF (`validateSafeUrl` bloqueando `169.254.169.254` y subredes privadas); 3) Defensa contra IDOR (`where: { id, ownerId: session.user.id }`); 4) Webhooks de pago idempotentes (`UNIQUE(external_payment_id)` + `crypto.timingSafeEqual`). |
| **6. Rendimiento Lento, Errores, Fallos en Móvil** | **Autonomous QA & Performance Optimization (Capítulos II-22, II-31)** | Medir Core Web Vitals (`LCP < 2.5s`, `INP < 200ms`, `CLS < 0.1`), probar en resoluciones `320px / 375px / 768px / 1440px`, capturar errores de consola y red mediante Playwright. |
| **7. SEO, Visibilidad en Búsquedas de IA (AEO/GEO), Lanzamiento** | **Launch, Growth & AI Citability (Capítulos I-3, II-39, III-10)** | Generar `/llms.txt`, `robots.txt` con Content-Signal, `sitemap.xml`, grafo estructurado `Schema.org JSON-LD`, etiquetas OpenGraph y plan verificado de rollback instantáneo. |

---

## 2. PROTOCOLO DE REVERSE PROMPTING (SIEMPRE ACTIVO)

Cuando las solicitudes sean amplias o escondan riesgos arquitectónicos, no generes código a ciegas; trabaja en 3 tiempos:
1. **Tiempo 1 (Descubrimiento de Palanca):** Presenta de 3 a 5 estrategias de ingeniería/producto de alto impacto con evaluación de ROI.
2. **Tiempo 2 (Diagnóstico de Puntos Ciegos):** Entrevista al usuario con 3 a 5 preguntas agudas sobre modos de fallo desatendidos (bloqueos de BD, radio de impacto en seguridad, ergonomía móvil).
3. **Tiempo 3 (Ejecución Quirúrgica):** Entrega código listo para producción, comandos y verificación sin un solo marcador temporal.

---

## 3. LISTA DE VERIFICACIÓN PREVIA A LA ENTREGA

- [ ] **Arquitectura:** Cero importaciones circulares, lógica de negocio desacoplada de la UI, tipado estricto sin `any`.
- [ ] **Seguridad:** Cero asignaciones masivas (roles gestionados exclusivamente en servidor), inmune a SSRF e IDOR, puertos de BD restringidos a `127.0.0.1`.
- [ ] **Diseño y UX:** Cero patrones genéricos de IA, todos los estados contemplados (`loading`, `empty`, `error`, `success`), sin desbordamiento horizontal en `375px`.
- [ ] **Rendimiento y Git:** Cero consultas `N+1`, carga diferida para módulos pesados, ningún secreto o artefacto de compilación rastreado en Git.
