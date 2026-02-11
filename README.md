# Identificación de Acciones Ilíquidas con Riesgo de Evento

Cuando la falta de liquidez amplifica el shock

## 📌Descripción General

Este proyecto identifica acciones con bajo nivel de liquidez que, al mismo tiempo, están expuestas a eventos corporativos negativos, específicamente problemas regulatorios.

La combinación de:
- volumen estructuralmente bajo, y
- riesgo de evento adverso
- crea un escenario donde los movimientos de precio pueden ser desproporcionados, violentos y difíciles de gestionar.

## 📍Insight Clave

- ¿Qué acciones presentan riesgo extremo porque nadie puede salir cuando ocurre el evento?

Un activo ilíquido puede parecer estable… hasta que ocurre un evento.
En ese momento, la ausencia de compradores convierte una mala noticia en un colapso.

## 💼Valor de Negocio

Identifica activos altamente peligrosos para carteras grandes.

Útil para:
- gestión de riesgo,
- compliance,
- exclusión preventiva de universos invertibles.

Reduce riesgo de:
- gaps severos,
- imposibilidad de ejecutar stops,
- slippage extremo.

Fundamental para sectores regulados como minería, energía o finanzas.

Fuentes de Datos
- tickers
- ticker_id
- industria
- precios_diarios
- ticker_id
- fecha
- volume
- eventos_corporativos
- ticker_id
- fecha
- tipo_evento

## 🧠Lógica del Análisis

1. Liquidez de Referencia Industrial
- Se calcula el volumen promedio de negociación por industria en los últimos 6 meses.

2. Evaluación de Liquidez Individual
- Se calcula el volumen promedio de cada ticker en el mismo período.

3. Riesgo de Evento
- Se filtran acciones que tuvieron Problemas Regulatorios en los últimos 6 meses.

4. Filtro de Riesgo Crítico
- Se seleccionan tickers que cumplen:
  - volumen promedio < 50% del promedio de su industria,
  - presencia de evento regulatorio reciente.

## 📊Interpretación de Resultados

Ilíquido + Evento Negativo
→ Riesgo de cola extremo.
→ Salidas forzadas y gaps severos.

Ilíquido sin evento
→ Riesgo latente, pero no inmediato.

Evento en activo líquido
→ El mercado puede absorber el shock.

## 🧩Casos de Uso

- Exclusión automática de carteras institucionales.
- Alertas tempranas de riesgo operativo.
- Análisis de impacto regulatorio.
- Stress testing de portafolios.
- Due diligence cuantitativa.

## 🚀Posibles Extensiones

- Medir impacto post-evento en retornos.
- Analizar spreads bid-ask si están disponibles.
- Combinar con kurtosis post-evento.
- Evaluar persistencia de la iliquidez.
- Ampliar a otros tipos de eventos negativos.

## ✒️Nota Final

El riesgo no siempre está en el precio.
A veces está en no poder salir.

Este insight no busca oportunidades,
busca evitar escenarios donde el mercado se vuelve unidireccional 🚪📉

## 👤Autora
Flavia Hepp Proyecto de SQL aplicó un análisis de riesgo basado en eventos.
