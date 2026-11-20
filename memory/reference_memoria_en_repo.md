---
name: reference-memoria-en-repo
description: "La memoria de Claude vive en la carpeta memory/ del repo privado CamiCruiser/riot; Claude la lee, la alimenta y sube los cambios solo"
metadata:
  node_type: memory
  type: reference
  originSessionId: 46f44d84-6506-4e1d-923c-b58292c12629
  modified: 2026-11-20T17:09:19.341Z
---

La carpeta `memory/` del proyecto (repo privado https://github.com/CamiCruiser/riot, branch main) es la memoria viva y única de Claude. En el computador de Camila, la carpeta interna de Claude (`~/.claude/projects/C--Users-Camila-Desktop-claude-riot/memory`) es un acceso directo (junction) a `C:\Users\Camila\Desktop\claude riot\memory`, así que hay una sola copia. El respaldo original quedó en `memory_respaldo` junto a ese acceso directo.

**Why:** Camila quiere acceder al proyecto desde el repo y no solo desde su PC (2026-11-20), y quiere que Claude lea, alimente y modifique la memoria con el tiempo siempre de forma automática.

**How to apply:** al empezar leer `memory/MEMORY.md`; al aprender algo nuevo, actualizar o crear el archivo en `memory/` y su línea en el índice, sin esperar que lo pida; después de cambiar `memory/` o `CLAUDE.md`, `git add memory CLAUDE.md`, commit "Memoria: ..." y `git push` (solo esos archivos). Si trabaja desde otro computador sin el acceso directo, hacer `git pull` antes y escribir directo en `memory/` del repo. Relacionado: [[project_class_building_system]].
