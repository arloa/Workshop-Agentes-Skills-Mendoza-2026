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

```bash
git clone https://github.com/arloa/bioquimica-agentes.git
cd bioquimica-agentes
opencode
```

Las piezas ya están en `.opencode/`: se arranca desde la raíz del repositorio,
sin copiar nada.

## Por dónde seguir

Lee `ACTIVIDAD.md`.
