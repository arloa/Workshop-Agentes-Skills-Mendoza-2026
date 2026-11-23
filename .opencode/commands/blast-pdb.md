---
description: BLAST contra PDB desde un código UniProt o el nombre de una proteína
---

Haz un BLAST contra PDB de: $ARGUMENTS

1. Resuelve el nombre a código con el método del skill `blast-ncbi`. Si hay
   varias candidatas, lístalas y para.
2. Ejecuta el resto del skill y devuelve el código usado, el enlace
   `Blast.cgi?CMD=Get&RID=...` y la fecha de envío.

Si no hay `RID`, dilo. No inventes un enlace.
