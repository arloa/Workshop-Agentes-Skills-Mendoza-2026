# Bioquímica con agentes y skills

Material de una actividad de 45 minutos: montar y probar un agente con tres
skills para hacer tareas de bioinformática **reproducibles y documentadas**.

## Qué hay

```
ACTIVIDAD.md          → el enunciado, con el guion de los 45 minutos
.opencode/agents/     → el agente
.opencode/skills/     → fuentes (UniProt + PubMed), blast-ncbi, informe
.opencode/commands/   → atajo /blast-pdb
plantillas/           → esqueletos para escribir un agente o un skill
```

Las piezas traen cuatro huecos marcados `HUECO`. Sin rellenarlos el agente
resuelve igual, pero no deja un método que otra persona pueda repetir.

## Requisitos

- [OpenCode](https://opencode.ai)
- `git` y `curl`

## Empezar

Abre `opencode` en una carpeta vacía y pídele que baje el repositorio:

```
clona https://github.com/arloa/Workshop-Agentes-Skills-Mendoza-2026
```

Cuando termine, cierra esa sesión y arranca `opencode` dentro de la carpeta
clonada: las piezas están en `.opencode/`, así que se cargan solas.

## Por dónde seguir

Lee `ACTIVIDAD.md`.
