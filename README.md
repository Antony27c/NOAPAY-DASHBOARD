# NOAPAY-DASHBOARD

**NOAPAY (NoaInnova)** es una plataforma fintech de orquestación de pagos que ofrece un cliente API unificado (`NoaClient`) para onramp y offramp de dinero fiat en Latinoamérica, con liquidación en cripto.

## ¿Qué hace?

Un solo cliente para todos los rieles de pago de la región. En lugar de integrar múltiples SDKs (Mercado Pago, PIX, SPEI, anchors Stellar, wallets cripto), se usa una sola API REST que abstrae todo.

```
import { NoaClient, FiatCurrency } from "noa-pay";
```

### Rieles soportados

- **Fiat:** Mercado Pago, PIX, SPEI, transferencias bancarias
- **Cripto:** Liquidación automática con stablecoins, anchors SEP en Stellar, pricing vía CoinGecko con spread personalizado
- **Sin dependencias de SDK:** Todo funciona con REST y `fetch`

## Estructura del proyecto

| Pantalla | Propósito |
|----------|-----------|
| **Landing** | Página de producto — explica la plataforma, muestra ejemplos de código, lista los rieles soportados |
| **Dashboard** | Vista de transacciones — balance, historial con búsqueda y filtros por método (SPEI, tarjeta, débito directo, efectivo), rango de fechas, exportación |
| **Console** | Panel de administración/desarrollo — catálogo de servicios, toggle Sandbox/Producción, API keys, webhooks, documentación, monitoreo por riel |

## Diseño

Todas las pantallas siguen el sistema de diseño **Nocturne**: interfaz oscura, tipografía Inter, acento blurple (`#9184d9`), iconos Phosphor. UI completamente en español.

## Paquete npm

- **Nombre:** `noa-pay`
- **Formato:** ESM + CJS, tipos TypeScript incluidos
- **Licencia:** MIT
- **Runtime:** Node >= 18
