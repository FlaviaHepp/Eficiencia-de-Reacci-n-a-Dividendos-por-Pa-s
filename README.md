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
