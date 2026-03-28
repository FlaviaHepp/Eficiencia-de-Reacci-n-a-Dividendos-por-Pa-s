# 🌏Eficiencia de Reacción a Dividendos por País

Front-Running Pre-Evento

Este proyecto implementa una consulta SQL que analiza el comportamiento de los precios antes de eventos de dividendos, comparando el rendimiento previo al evento entre distintos países o mercados.

La señal busca detectar ineficiencias informativas, donde el mercado parece anticipar el evento antes de su fecha oficial.

## 🧠Idea central

En mercados perfectamente eficientes:
- el precio no debería reaccionar antes del evento
- la información relevante se descuenta solo cuando es pública

En la práctica:
- hay filtraciones
- hay trading algorítmico predictivo
- hay diferencias regulatorias

Si el precio sube sistemáticamente antes del dividendo, alguien está llegando antes.

🎯 Valor de negocio

Mide eficiencia informativa por país

Útil para:
- diseño de estrategias pre-evento
- análisis regulatorio
- comparación entre mercados desarrollados y emergentes
- Revela posibles patrones de front-running

## 🗄️Estructura de datos esperada

- eventos_corporativos
- campo	descripción
- ticker_id	Identificador
- fecha	Fecha del evento
- tipo_evento	Tipo (Dividendo)
- tickers
- campo	descripción
- ticker_id	Identificador
- bolsa_mercado	País / mercado de cotización
- precios_diarios
- campo	descripción
- ticker_id	Identificador
- fecha	Fecha
- close	Precio de cierre

## ⚙️Lógica de la consulta

- Identifica eventos de dividendo

Calcula el rendimiento:
- desde 3 días antes del evento
- hasta el día del evento
- Agrega resultados por país / mercado
- Ordena por mayor rendimiento pre-evento

## 🔎Interpretación de resultados

Rendimiento positivo alto:
- anticipación del evento
- posible filtración o modelos predictivos

Rendimiento cercano a cero:
- mercado más eficiente
- Rendimiento negativo:
- aversión o fricciones locales

## 🚀Posibles extensiones

- Analizar ventanas múltiples (1, 5, 10 días)
- Comparar dividend yield vs reacción
- Ajustar por volatilidad país
- Separar por tamaño de empresa

## 📝Notas finales

- No implica ilegalidad per se
- Señala asimetrías informativas
- Muy útil para análisis comparativo internacional

## 👤Autora
Flavia Hepp Proyecto de SQL aplicó un análisis de riesgo basado en eventos.

***
🌍 **¿El mercado realmente espera… o se adelanta?**

En teoría, los dividendos son eventos públicos y conocidos.
Pero en la práctica, el comportamiento del precio puede contar otra historia.

---

📊 En este análisis evalué algo simple:

👉 ¿Qué pasa con el precio **3 días antes** de la fecha de dividendo?
👉 ¿Y cómo varía esto según el país / mercado?

---

⚠️ Resultado interesante:

En algunos mercados, las acciones muestran un
📈 **rendimiento positivo antes del dividendo**

💡 Lo que podría indicar:

* Anticipación sistemática del evento
* Estrategias de trading algorítmico
* O incluso… **posible filtración de información**

---

🧠 ¿Por qué importa?

Porque no todos los mercados son igual de eficientes.

👉 En algunos:

* El precio ajusta de forma “limpia”
  👉 En otros:
* El movimiento empieza antes de que el evento ocurra

---

🚨 Insight clave:
**El edge no siempre está en el evento…
sino en quién se adelanta a él.**

---

🔍 Este tipo de análisis permite:
✔️ Detectar mercados más predecibles
✔️ Identificar oportunidades de front-running
✔️ Ajustar estrategias según la eficiencia del mercado

---

📉 En finanzas globales, entender *dónde* operás
puede ser tan importante como *qué* operás.

#Quant #Trading #DataScience #Dividendos #MarketEfficiency #Finanzas #AlgoTrading
