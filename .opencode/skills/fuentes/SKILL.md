---
name: fuentes
description: Responde qué es una proteína o un gen (longitud, organismo, función) y busca referencias bibliográficas. Devuelve los campos con su URL.
---

# Fuentes

## Cuándo

La pregunta da el nombre de una proteína o de un gen, o pide una referencia bibliográfica.

## Método A — la ficha de la proteína (UniProt)

1. Busca el nombre de la proteína o del gen. La columna `Entry` es el código (`<ACC>`). Si no devuelve filas, tradúcelo al inglés y repite:

   ```bash
   curl -s "https://rest.uniprot.org/uniprotkb/search?query=<nombre>&format=tsv&fields=accession,protein_name,organism_name,length&size=5"
   ```

2. <!-- HUECO 2 · El nombre puede devolver varias entradas. ¿Qué haces: elegir la que parezca mejor o parar? -->
3. Abre la ficha en `https://www.uniprot.org/uniprotkb/<ACC>/entry`.
4. Extrae longitud, organismo, función y el nombre del gen.
5. Anota la versión de la base (viene en la cabecera `X-UniProt-Release`) y la fecha de consulta.

## Método B — la literatura (PubMed)

1. PubMed no indexa códigos de UniProt: busca por el nombre del gen.
2. Si piden revisión, filtra por tipo de publicación.
3. Extrae revista, año y DOI y comprueba que el DOI abre.

## Verifica y cita

Método A: la URL de la entrada, la versión de la base y la fecha.
Método B: la URL del artículo y el DOI.

## Si no aparece

Responde "sin datos" y di qué búsqueda hiciste.
