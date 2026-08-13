# Mundo Real // Macro Terminal — v1.1

PWA móvil gratuita para seguir los 18 indicadores del panel “Mundo Real”. Esta versión corrige el problema **“This symbol is only available on TradingView”**.

## Qué cambia en v1.1

TradingView no permite incrustar en widgets todos los símbolos que sí pueden verse dentro de tradingview.com. Por eso esta versión evita los feeds restringidos y usa tres estrategias:

1. **Símbolos TVC/spot embebibles** cuando existe el mismo indicador.
2. **Proxy CFD muy correlacionado** cuando el futuro exacto de la bolsa está restringido en widgets.
3. **Gráfico oficial FRED** para el spread 10Y–2Y y el breakeven 10Y, que son series diarias.

Esto mantiene la app a **0 €**, a cambio de aceptar retrasos y pequeñas diferencias entre un proxy y el contrato exacto que ves en Investing.

## Mapeo de datos

- EE.UU. 2A → `TVC:US02Y`
- EE.UU. 10A → `TVC:US10Y`
- 10Y–2Y → FRED `T10Y2Y` (gráfico oficial, diario)
- Breakeven 10Y → FRED `T10YIE` (gráfico oficial, diario)
- Alemania 2A → `TVC:DE02Y`
- DXY → `TVC:DXY`
- EUR/USD → `OANDA:EURUSD`
- Brent → `TVC:UKOIL` (proxy CFD)
- TTF → `CMCMARKETS:DUTCHNATGAS1!` (proxy TTF)
- Cobre → `CAPITALCOM:XCUUSD` (proxy spot/CFD)
- Oro → `TVC:GOLD` (proxy spot/CFD)
- Plata → `TVC:SILVER` (proxy spot/CFD)
- VIX → `TVC:VIX`
- BTC/USD → `COINBASE:BTCUSD`
- S&P 500 → `TVC:SPX`
- Nasdaq Composite → `TVC:IXIC`
- Euro Stoxx 50 → `TVC:SX5E`
- IBEX 35 → `TVC:IBEX35`

## Cómo actualizar tu GitHub Pages

Sustituye en la raíz del repositorio estos archivos por los de esta versión:

- `index.html`
- `sw.js`
- `README.md`

Puedes dejar `manifest.webmanifest`, `icon-192.png` e `icon-512.png` como están, aunque el ZIP incluye todo el proyecto por comodidad.

Después de hacer commit, GitHub Pages se vuelve a desplegar automáticamente. La v1.1 cambia la versión de la caché del Service Worker para que el móvil no se quede atrapado en la versión anterior.

## Limitación importante

Un proxy sirve muy bien para leer dirección, tendencia y relaciones macro, pero no debe esperarse que su cotización coincida al céntimo con el futuro exacto de COMEX/ICE o con el derivado mostrado por Investing.
