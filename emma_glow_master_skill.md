# Guía Maestra de Desarrollo: EMMA Glow Enterprise Omnicanal 🧬
**Código de Habilidad:** `SKILL-EMMA-GLOW-OMNICANAL-V1`

## 1. Visión del Ecosistema
EMMA Glow no es un juego, es una **Plataforma SaaS B2B2C** para la industria cosmética y dermatológica. Consta de 4 pilares interactuando en tiempo real:
1.  **AI Scanner (B2C):** Diagnóstico biométrico facial y capilar (Sebo, Acné, Frizz, Porosidad) vía MediaPipe.
2.  **Smart Lab (B2C/B2B):** Simulador de manufactura reológica y química donde se cocrea la fórmula prescrita.
3.  **Regulatory Copilot (B2B):** Asistente IA que audita límites de toxicidad (FDA/INVIMA) leyendo fichas de seguridad (PDF).
4.  **Data Dashboard (B2B):** Panel analítico para empresas (ej. L'Oréal) mostrando tendencias de formulación y ROI del gemelo digital.

## 2. Directrices Arquitectónicas
*   **Modularidad:** Cada pilar debe poder funcionar de manera independiente, pero comunicarse a través de un "State Manager" central (o variables de URL/LocalStorage en prototipos) para mantener la historia del lote.
*   **Diseño Premium (UI/UX):** 
    *   Mantener estética "Glassmorphism" (paneles translúcidos, desenfoque de fondo).
    *   Esquema de colores: Rosa Emma (`#FDF4F2`, `#E7AC9A`, `#F472B6`) y Modo Oscuro Enterprise (`#0F0F13`).
    *   Fuentes: *Cormorant Garamond* (Títulos/Elegancia) y *Plus Jakarta Sans* (Datos/UI).
*   **Rendimiento:** Las animaciones complejas (como la física de fluidos) deben renderizarse nativamente en HTML5 Canvas (`requestAnimationFrame`), sin depender de librerías externas pesadas.

## 3. Integración Técnica (Simulación)
Para demostrar el flujo completo a los inversores, se debe usar un **"Master Wrapper"** (Contenedor Principal) que guíe al usuario por el embudo exacto:
*   *Flujo de Demostración:* Cliente se escanea ➔ IA receta Niacinamida ➔ Cliente fabrica en el lab ➔ La marca revisa el copilot para ver si la niacinamida está en regla ➔ La marca ve la estadística de esa venta en el Dashboard.

## 4. Reglas Críticas para la IA Agente
*   **Nunca perder el contexto de negocio:** Cualquier cambio en el código debe justificar cómo mejora la conversión (B2C) o ahorra costos (B2B).
*   **Respetar la Química Real:** Si se agregan ingredientes, deben tener sentido termodinámico y reológico (ej. no mezclar agua y aceite sin un emulsionante como SAMIX a RPMs altas).
