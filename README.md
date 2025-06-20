
# 💼 Quantitative Trading Challenge

## 🎯 **Objetivo**

Diseñar, implementar y evaluar una estrategia de trading cuantitativo sobre BTC/USDT usando datos históricos de Binance, indicadores técnicos y modelos de decisión.

## 🧪 Descripción del Challenge

Tu tarea es construir un sistema de trading cuantitativo completo sobre el par BTC/USDT. El proceso deberá incluir: **extracción de datos**, **cálculo de indicadores/features**, **formulación de una estrategia** y **evaluación mediante backtesting**.

---

### 1️⃣ Extracción de Datos Históricos

* Obtener datos históricos OHLCV de BTC/USDT desde la API de Binance.
* El rango mínimo debe abarcar los últimos 6 meses.

Este módulo debe ser **reutilizable** y apto para actualizar o cambiar pares/timeframes fácilmente.

---

### 2️⃣ Cálculo de Indicadores y Features

Diseñar un módulo para construir features técnicos derivados del precio.

📌 Se espera que el sistema pueda escalar en el futuro para incluir nuevos indicadores. La forma en que estructures este componente es clave.

**Ejemplos de indicadores a incluir (no limitativos):**

* Medias móviles (SMA/EMA)
* RSI
* Bandas de Bollinger
* Distancia entre el precio y cada indicador
* Volatilidad, momentum, etc.

**Ejemplos de features a incluir (no limitativos):**
* Distancia entre el precio y los indicadores (donde se pueda aplicar y tenga sentido, ej. No tiene sentido medir la distancia entre el RSI y el precio ya que son en escalas diferentes).
  
Tu sistema debe permitir incorporar fácilmente nuevos indicadores y features en el futuro.

---

### 3️⃣ Implementación de Estrategia

Formular una estrategia de trading basada en los indicadores y features calculados.

Puedes optar por una de las siguientes aproximaciones:

* **Estrategia basada en reglas** (ej. cruces de medias, RSI sobrevendido/sobrecomprado, etc.)
* **Modelo predictivo / caja negra** (ML simple, red neuronal, árbol de decisión, NLP, etc.)

En ambos casos, deberás explicar detalladamente:

* Qué variables estás usando y por qué.
* Cómo funciona la lógica de entrada/salida.

---

### 4️⃣ Backtesting y Evaluación

Implementar un módulo de backtesting que evalúe la estrategia sobre datos históricos, calculando al menos las siguientes métricas:

* **Total Return / CAGR**:
  - Total Return: Es la ganancia total que obtuvo tu estrategia durante el período del backtest, expresada como un porcentaje. Por ejemplo, si empezaste con $1,000 y terminaste con $1,300, tu retorno total es 30%.

  - CAGR (Compound Annual Growth Rate): Es el crecimiento promedio anual compuesto. Sirve para normalizar el rendimiento en el tiempo, especialmente si tu backtest cubre varios años. Muestra cuánto habrías crecido en promedio cada año si todo fuera compuesto de forma estable.

* **Sharpe y Sortino Ratio**:
  - Sharpe Ratio: Mide el rendimiento ajustado al riesgo. Compara la rentabilidad obtenida con la volatilidad de los retornos. Cuanto más alto, mejor: más estás ganando por cada unidad de riesgo.

  - Sortino Ratio: Similar al Sharpe, pero más exigente. Solo penaliza la volatilidad negativa (las pérdidas), lo que lo hace más útil cuando te interesa saber cómo se comporta la estrategia ante caídas.

* **Máximo Drawdown**:
  - Es la mayor caída de capital desde un pico hasta un valle durante todo el backtest. Indica el peor golpe que hubieras recibido antes de que la estrategia se recuperara. Muy útil para medir el “dolor psicológico” que podrías haber experimentado.
    
* **Número de trades / win rate**:
  - Número de trades: Simplemente cuántas operaciones ejecutó la estrategia.

  - Win rate: Porcentaje de operaciones que fueron ganadoras. Ojo: no siempre un win rate alto significa una mejor estrategia, si las pérdidas son mayores que las ganancias.
    
* **Equity curve y drawdown**
  - Equity curve: Es la curva que muestra cómo va creciendo (o decreciendo) tu capital con el tiempo. Ayuda a visualizar si tu estrategia tiene una tendencia sana o errática.

  - Drawdown (curva): Muchas veces se grafica debajo de la equity curve y muestra visualmente cuándo y cuánto cayó tu capital en cada momento del tiempo.
---

## 💡 Consideración Importante

Este challenge **NO busca obtener una estrategia rentable**, sino observar **cómo estructuras y escalas tu código**. Esperamos ver un enfoque organizado, extensible, y que refleje pensamiento profesional.

---

## 📬 Entrega

Una vez finalices el challenge, **sube tu solución a un repositorio privado en GitHub**  y envíame el enlace para su revisión.

### 📦 **Entregables**

* Código en Python (módulos y notebooks organizados).
* README explicando el enfoque, supuestos y cómo ejecutar.
* Visualizaciones y métricas del backtest.

### ⏱️ Fecha de Entrega

No existe una fecha límite estricta para la entrega de este challenge. Lo que evaluamos es principalmente:

- **Calidad del trabajo entregado.**
- **Capacidad para estructurar soluciones de forma profesional.**
- **Rapidez y criterio para resolver problemas técnicos.**

Puedes tomarte el tiempo necesario para presentar un resultado sólido, pero también valoramos eficiencia en la ejecución.
