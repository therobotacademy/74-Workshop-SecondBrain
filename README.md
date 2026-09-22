# Corpus `raw/` para el taller Second Brain

Paquete preparado para trabajar con la rama `master` de
[`therobotacademy/obsidian-llm-wiki`](https://github.com/therobotacademy/obsidian-llm-wiki).

Incluye cuatro corpus alternativos. Cada uno contiene una carpeta `raw/` ya organizada por topics,
con una fuente Markdown por archivo y metadatos de procedencia. Los originales no se han resumido ni
reescrito.

## Corpus incluidos

| Carpeta | Fuentes | Nivel | Uso sugerido |
|---|---:|---|---|
| `01-genai-es` | 6 | Inicial | Taller común recomendado |
| `02-google-adk` | 7 | Intermedio | IA Agents y Google ADK |
| `03-mlops` | 8 | Inicial/intermedio | Pipeline de ML de extremo a extremo |
| `04-system-design` | 7 | Avanzado | Relaciones cruzadas entre casos de arquitectura |

## Uso

1. Clona la rama `master` de `obsidian-llm-wiki`.
2. Elige **un solo corpus** para la primera ejecución.
3. Copia su carpeta `raw/` a la raíz del repositorio clonado.
4. Ejecuta `bootstrap vault` si aún no existe `wiki/`.
5. Pide al agente que compile las fuentes de `raw/` una a una y actualice `wiki/index.md` y
   `wiki/log.md`.
6. Abre el vault en Obsidian y revisa artículos, enlaces y grafo.

Ejemplo:

```bash
cp -R 01-genai-es/raw /ruta/a/obsidian-llm-wiki/
```

## Nota metodológica

La receta original genera `raw/` durante Fetch. En este paquete se entrega `raw/` ya preparado para
ahorrar tiempo de descarga en el taller y concentrar la sesión en Compile, Cascade, Query y Graph.
Para enseñar el ciclo completo, puede reservarse una fuente adicional e ingerirla desde `sources/`.

## Procedencia y licencias

Cada archivo conserva su URL, commit de origen, fecha de recogida y licencia en una cabecera YAML.
Las licencias completas están en `LICENSES/`. No se incluye una copia de Obsidian Help porque no se
encontró una licencia de redistribución explícita en la raíz de ese repositorio.

