# Second Brain — Práctica de Taller (Demostración Alumno Modelo)

* **Participante:** Alumno Modelo (Demostración para la clase)
* **Corpus seleccionado:** `01-genai-es` (Microsoft Generative AI for Beginners)
* **Concepto transversal analizado:** **Contexto**
* **Fecha:** Septiembre 2026

---

## 1. Estructura del Repositorio de la Práctica

```text
demo-alumno/
├── README-taller.md          # Este documento de resumen del taller
├── revision-humana.md        # Registro canónico de la intervención y curación humana
├── wiki/                     # Notas conceptuales compiladas y curadas
│   └── contexto.md           # Nota hub curada con enlaces bidireccionales y fuentes
└── raw/ -> ../01-genai-es/raw # Fuentes originales conservadas intactas
```

---

## 2. Metodología Ejecutada

1. **Conservación de fuentes (`raw/`):** Se mantuvieron inmutables las 6 lecciones en español distribuidas en sus 5 topics (`fundamentos-llm`, `gobernanza`, `prompting`, `rag`, `agentes`).
2. **Ingesta en dos lotes:**
   - **Lote A (Fundamentos):** Creación del primer núcleo conceptual (atención, ventana de contexto estática, codificador vs decodificador).
   - **Lote B (Aplicaciones):** Ingesta incremental de prompting, RAG y agentes, observando la densificación de enlaces y la aparición de nuevas dependencias.
3. **Auditoría crítica:** Detección de aplanamiento conceptual en la síntesis automática del término *contexto*.
4. **Curación manual:** Edición directa en Markdown para desglosar el concepto en 3 dimensiones (Cómputo, Grounding y Estado) y conectar notas huérfanas mediante `[[...]]`.
5. **Validación en Obsidian:** Comprobación del grafo resultante, enlaces de retorno (*backlinks*) y respuesta a consultas de síntesis trazables.

---

## 3. Navegación en Obsidian

Para revisar esta práctica en Obsidian:
1. Abre la carpeta `demo-alumno/` como un nuevo Vault o añade `demo-alumno/wiki/` a tu vault existente.
2. Abre la nota `wiki/contexto.md`.
3. Activa la vista de **Grafo local** (`Ctrl+G` / `Cmd+G` con el panel local abierto) para observar las relaciones hacia `ventana-de-contexto`, `rag-bases-vectoriales` y `agentes-ia-arquitectura`.
4. Revisa los metadatos YAML superiores para comprobar la trazabilidad hacia las rutas originales en `raw/`.
