# 🛡️ Framework de Auditoría Técnica de Prompts (v1.5.2)

Sistema de nivel empresarial para la validación de agentes en el ecosistema A.M.O. Este repositorio contiene la infraestructura de testing para asegurar que cada módulo cumpla con los estándares de calidad antes del despliegue.

## 🤖 M12 - Motor de Scoring y Métricas (El Evaluador)

El M12 es el corazón de la calidad del sistema. Actúa bajo una arquitectura de **"IA auditando IA"** para eliminar la subjetividad en la validación de prompts.

### 🔗 Interconectividad de Módulos
* **M12 ➡️ M14:** Si el **scoring es < 7/9**, se emite un `error_flag: true` que activa automáticamente el protocolo de re-intento (Tenacity) en el motor de orquestación.
* **M12 ➡️ M13:** Envía métricas de **precisión (⭐)** y robustez para el Dashboard de supervisión y control de seguridad.

### 📈 Metodología de Evaluación
1. **Scoring Estructural:** Escala 1-9 (Aprobación en 7/9).
2. **Métricas Cualitativas:** Escala de estrellas (⭐) para el campo de precisión.
3. **Identificación de Modelo:** Registro obligatorio del `modelo_ejecutor` (ej. GPT-4o-mini).

### 🛠️ Evidencia Técnica
El sistema es validado automáticamente mediante **Promptfoo**, asegurando que la salida JSON sea siempre compatible con la base de datos de Notion.

```bash
# Comando de validación
npx promptfoo eval