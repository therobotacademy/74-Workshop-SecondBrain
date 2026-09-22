# Registro de Revisión Humana — Taller Second Brain

Documento canónico de entrega de la práctica central del taller. Registra la auditoría crítica y la intervención humana realizada sobre el concepto transversal **"Contexto"**.

---

### 1. Concepto revisado
**Contexto en Sistemas de Inteligencia Artificial Generativa**

---

### 2. Resultado inicial (salida automática del compilador)
El pipeline automático de compilación generó una nota única bajo el término `contexto.md` que resumía superficialmente las menciones de la palabra en los seis documentos ingeridos. El texto presentaba una descripción homogénea donde se mezclaban indistintamente:
* La capacidad de memoria en tokens del modelo.
* Los ejemplos de un prompt *few-shot*.
* La base de datos documental de RAG.
* El historial de conversación de un agente.

El grafo resultante mostraba a `contexto` como un nodo secundario vinculado únicamente a la nota de *prompt engineering*, sin conexiones directas con *fundamentos*, *RAG* ni *agentes*.

---

### 3. Problema detectado
1. **Aplanamiento terminológico y pérdida de matiz conceptual:** Se trataba como un mismo fenómeno la limitación física computacional (la ventana de contexto) y la estrategia de software para anclar conocimiento externo (RAG) o persistir estados multi-turno (agentes).
2. **Ruptura de la causalidad técnica:** En `explorar-y-comparar-llm.md` se establece con claridad que las bases de datos vectoriales y RAG surgen para solventar las restricciones de tamaño, coste y latencia de la ventana de contexto del prompt. La nota automática omitió completamente este vínculo causa-efecto.
3. **Omisión de estándares agénticos:** Se ignoró el papel del *Model Context Protocol* (MCP) y de los archivos YAML de experiencia mencionados en la lección de agentes, fundamentales para entender el contexto moderno en sistemas autónomos.

---

### 4. Modificación realizada
Se realizó una reestructuración manual y quirúrgica del archivo `wiki/contexto.md`:
* **Taxonomía en 3 dimensiones:** Se dividió el concepto en:
  1. *Contexto de Cómputo* (Ventana de tokens, atención Transformer, diferencias codificador/decodificador).
  2. *Contexto de Grounding* (RAG, vector search, anclaje documental para mitigar la fabricación).
  3. *Contexto de Estado* (Hilos de conversación, persistencia YAML, paso de contexto secuencial y MCP).
* **Adición de diagrama Mermaid:** Representación visual del flujo entre saturación de ventana, recuperación en vector DB y orquestación agéntica.
* **Enlaces wiki bidireccionales (`[[...]]`):** Inserción deliberada de enlaces hacia `[[ventana-de-contexto]]`, `[[rag-bases-vectoriales]]`, `[[agentes-ia-arquitectura]]` y `[[fabricacion-alucinacion]]`.
* **Citas de procedencia explícitas:** Vinculación exacta de cada afirmación con su archivo de origen en `raw/`.

---

### 5. Fuentes utilizadas
* `01-genai-es/raw/fundamentos-llm/introduccion-a-la-ia-generativa.md` (origen histórico en RNNs y contexto secuencial).
* `01-genai-es/raw/fundamentos-llm/explorar-y-comparar-llm.md` (límites de ventana de contexto y causalidad de RAG).
* `01-genai-es/raw/prompting/fundamentos-de-prompt-engineering.md` (delimitadores, contexto de sistema y plantillas de dominio).
* `01-genai-es/raw/rag/rag-y-bases-de-datos-vectoriales.md` (aumento de generación con contexto recuperado y mitigación de fabricación).
* `01-genai-es/raw/agentes/agentes-de-ia.md` (estado conversacional, ejecutor del agente, memoria YAML y MCP).
* `01-genai-es/raw/gobernanza/uso-responsable-de-ia-generativa.md` (contexto de uso ético y no discriminatorio).

---

### 6. Efecto sobre la wiki
* **Transformación topológica del grafo:** `[[contexto]]` pasó de ser un nodo periférico aislado a un **nodo central conector (hub)** que une de manera natural el cluster de *Fundamentos* (Lote A) con el cluster de *Aplicaciones y Agentes* (Lote B).
* **Eliminación de notas huérfanas:** Se resolvieron los enlaces bidireccionales de retorno (*backlinks*) en las notas de `rag-bases-vectoriales.md` y `agentes-ia-arquitectura.md`.
* **Mejora en la capacidad de consulta:** El Second Brain ahora permite responder con solvencia arquitectónica a preguntas cruzadas como *"¿Por qué una ventana de contexto de 1M de tokens no elimina la necesidad de RAG?"*, sustentando la respuesta directamente en citas comprobables de las fuentes originales.
