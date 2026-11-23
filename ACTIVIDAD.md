# Actividad

Montamos y probamos un agente y tres skills para hacer tareas de bioinformática
de forma **reproducible y documentada**.

El agente hace cuatro cosas: busca una proteína por nombre, describe su ficha de
UniProt, lanza un BLAST contra PDB y redacta un informe. Los skills fijan *cómo*
se hace cada paso — qué URL, qué comando, qué se anota — para que otra persona
pueda repetirlo y comprobarlo.

Las piezas vienen incompletas: hay cuatro huecos que se rellenan durante la
sesión.

## Preparación

Abre `opencode` en una carpeta vacía y pídele que baje el repositorio:

```
clona https://github.com/arloa/Workshop-Agentes-Skills-Mendoza-2026
```

Cuando termine, cierra esa sesión, entra en la carpeta clonada y arranca
`opencode` otra vez desde ahí: así carga el agente y los skills de `.opencode/`.

## La actividad

Las piezas tienen cuatro huecos marcados `HUECO` en los skills y el agente. 

**No se ejecuta nada hasta haberlo leído y completado.** Primero se lee qué haría cada pieza y se rellena el hueco; después se lanza y se comprueba. Un agente del que no sabes qué hace no se pone en marcha.

| min | bloque | qué haces |
|---|---|---|
| 0–5 | Arranque | clona, abre `opencode` |
| 5–12 | Lectura | lee el agente y los tres skills: qué haría cada uno |
| 12–19 | HUECO 1 | ¿dónde puede escribir? y lo compruebas con el primer prompt |
| 19–26 | HUECO 2 | ¿qué hace si el nombre devuelve varias? y lo compruebas |
| 26–33 | HUECO 3 | la descripción del skill de BLAST, y lo lanzas |
| 33–39 | HUECO 4 | qué convierte el informe en prueba |
| 39–45 | Intercambio | otra pareja ejecuta tu skill solo con lo que escribiste |

Los prompts, con el nombre que te den. Cada uno se lanza en el bloque que le toca:

```
@bioquimica ¿Qué es la mioglobina de rata?
@bioquimica Haz un BLAST de la mioglobina de rata contra PDB y dame el enlace
@bioquimica Redacta el informe
```

Si sobra tiempo: `/blast-pdb mioglobina de rata` hace lo mismo desde un atajo.

## Los cuatro huecos

| Hueco | Pieza | Qué tiene que conseguir |
|---|---|---|
| 1 | `agents/bioquimica.md` | que el resultado quede donde se pueda encontrar |
| 2 | `skills/fuentes/SKILL.md` | que no elija por ti cuando hay varias |
| 3 | `skills/blast-ncbi/SKILL.md` | que el skill se active cuando toca |
| 4 | `skills/informe/SKILL.md` | que el informe sirva de prueba |

La pregunta está dentro de cada archivo: no hay clave. Si el agente la contesta
antes que tú, borra su respuesta y escribe la tuya.

## Las tres facetas

| Faceta | Pieza | Qué hace |
|---|---|---|
| Control | `agents/bioquimica.md` | decide y firma |
| Lectura | `skills/fuentes/SKILL.md` | consulta UniProt y PubMed |
| Envío | `skills/blast-ncbi/SKILL.md` | manda un trabajo a un servidor |
| Escritura | `skills/informe/SKILL.md` | escribe `informe.md` |

El agente decide qué hacer, el skill decide cómo. El shell queda abierto a
propósito: en producción se acota con reglas `shell`.
