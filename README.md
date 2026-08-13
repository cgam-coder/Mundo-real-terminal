# Mundo Real // Macro Terminal

PWA móvil, gratuita y sin claves API, basada en widgets oficiales de TradingView. Está diseñada para seguir los 18 indicadores del panel “Mundo Real” y ver sus relaciones en gráficos tipo terminal.

## Qué incluye

- Ticker superior con los activos principales.
- Watchlist agrupada: tipos, divisas, energía, metales, riesgo y bolsas.
- Gráfico avanzado con los 18 símbolos en la watchlist.
- Sección “Relaciones” con seis paneles macro.
- Calendario económico.
- PWA instalable en Android.
- Sin backend, sin suscripción y sin claves API.

## Fuentes / frecuencia

Los gráficos usan widgets oficiales de TradingView. La frecuencia del dato depende del instrumento y de las licencias de cada mercado. Los símbolos `TVC:` son series calculadas por TradingView; TradingView indica que las muestra gratuitamente en tiempo real. Las series FRED son diarias. Los futuros e índices de bolsas concretas pueden mostrarse retrasados según el mercado.

Símbolos principales:

- TVC:US02Y — EE.UU. 2 años
- TVC:US10Y — EE.UU. 10 años
- FRED:T10Y2Y — spread 10Y-2Y
- FRED:T10YIE — breakeven 10 años
- TVC:DE02Y — Alemania 2 años
- TVC:DXY — índice dólar
- OANDA:EURUSD — EUR/USD
- TVC:UKOIL — Brent
- ICEEUR:TFN1! — Dutch TTF Natural Gas
- COMEX:HG1! — cobre
- COMEX:GC1! — oro
- COMEX:SI1! — plata
- CBOE:VIX — VIX
- COINBASE:BTCUSD — BTC/USD
- SP:SPX — S&P 500
- NASDAQ:IXIC — Nasdaq Composite
- TVC:SX5E — Euro Stoxx 50
- BME:IBC — IBEX 35

## Cómo ponerla en el móvil gratis

### Opción recomendada: GitHub Pages
1. Crea una cuenta gratuita en GitHub.
2. Crea un repositorio nuevo, por ejemplo `mundo-real-terminal`.
3. Sube todos los archivos de esta carpeta a la raíz del repositorio.
4. En el repositorio: **Settings → Pages**.
5. En **Build and deployment**, elige **Deploy from a branch**.
6. Selecciona `main` y `/ (root)` y guarda.
7. GitHub te dará una URL HTTPS.
8. Ábrela en Chrome de Android → menú ⋮ → **Instalar aplicación** o **Añadir a pantalla de inicio**.

La app seguirá siendo gratuita. TradingView puede cambiar en el futuro la disponibilidad o latencia de determinados mercados; si un símbolo deja de funcionar, basta con cambiar su código en `index.html`.

## Uso

- Toca un indicador en la barra horizontal para cargarlo en el gráfico principal.
- El gráfico avanzado también incluye la watchlist completa.
- Para comparar series, usa la función **Compare or Add Symbol** del gráfico de TradingView y cambia la escala a porcentaje cuando mezcles unidades muy distintas.

## Nota

No es una fuente oficial de ejecución ni una terminal profesional de mercado. Está pensada como panel personal de seguimiento macro. No debe asumirse que todos los instrumentos tienen la misma frecuencia de actualización.
