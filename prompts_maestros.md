# 🛠️ KIT DE AUDITORÍA DE PROMPTS - PROYECTO 04

Este archivo contiene los dos prompts maestros utilizados para el control de calidad en el sistema de Ingeniería de Prompts.

---

## 1. JUEZ DE SCORING (Puntuación Estructural)
**Objetivo:** Evaluar si el prompt cumple con los 7 pilares fundamentales.

**Prompt:**
Actúa como un Auditor Senior de IA. Analiza la estructura del prompt adjunto y asígnale los puntos exactos según mi baremo de Notion.

Prompt a evaluar: {{prompt}}

Baremo de Puntuación:
- Contexto: (0 o 2 puntos).
- Instrucción: (0 o 2 puntos).
- Formato: (0 o 1 punto).
- Restricciones: (0 o 1 punto).
- Ejemplos: (0 o 1 punto).
- Rol: (0 o 1 punto).
- Verificable: (0 o 1 punto).

Resultado: Devuelve una tabla Markdown con la columna "Puntos" y una "Justificación".

---

## 2. JUEZ DE MÉTRICAS (Metadatos Técnicos)
**Objetivo:** Extraer información técnica para la base de datos de Notion.

**Prompt:**
Actúa como un Analista de Arquitectura de Prompts. Extrae los metadatos técnicos del prompt adjunto para mi tabla de métricas de Notion.

Prompt a evaluar: {{prompt}}

Extrae los valores para estas columnas:
1. Modelo sugerido.
2. Nivel de complejidad (Principiante/Intermedio/Avanzado).
3. Token-Efficient (SÍ/NO).
4. JSON-Ready (SÍ/NO).
5. Versión recomendada.

Resultado: Devuelve una tabla Markdown lista para copiar en Notion.