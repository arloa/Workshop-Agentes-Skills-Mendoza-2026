---
name: blast-ncbi
# HUECO 3 · Escribe la descripción del skill leyendo el método.
# Pistas: ¿envía un trabajo o solo consulta? ¿contra qué base? ¿devuelve los
# resultados o un ticket para abrirlos?
description: BLAST
---

# BLAST en NCBI

## Cuándo

La pregunta pide buscar secuencias similares de una proteína contra PDB.

## Método

1. Toma el nombre de la proteína de la pregunta y búscalo en UniProt. Si no devuelve filas, tradúcelo al inglés. Si salen varias, lístalas y para:

   ```bash
   curl -s "https://rest.uniprot.org/uniprotkb/search?query=<nombre>&format=tsv&fields=accession,protein_name,organism_name,length&size=5"
   ```

2. Descarga la secuencia del código (BLAST no acepta códigos):

   ```bash
   seq=$(curl -s "https://rest.uniprot.org/uniprotkb/<ACC>.fasta" | tail -n +2 | tr -d '\n\r ')
   ```

3. Envía el trabajo. Devuelve un `RID`, no resultados: extrae el `RID` de la
   respuesta y arma `https://blast.ncbi.nlm.nih.gov/Blast.cgi?CMD=Get&RID=<RID>`.

   ```bash
   curl -s --data-urlencode "QUERY=$seq" \
     "https://blast.ncbi.nlm.nih.gov/Blast.cgi?CMD=Put&PROGRAM=blastp&DATABASE=pdb&HITLIST_SIZE=10"
   ```

## Verifica y cita

Cita el código, el programa, la base, el enlace con `RID` y la fecha de envío.
Si no hay `RID`, avisa que falló el envío.
