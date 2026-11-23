# Clave de los cuatro huecos

Mírala solo si te trabas.

## 1 · `agents/bioquimica.md`

**¿Dónde puede escribir el agente?**

```markdown
5. Escribe solo dentro del proyecto y con rutas relativas.
```

**Comprueba:** `informe.md` aparece en la raíz del proyecto, no en `~/`.

## 2 · `skills/fuentes/SKILL.md`

**Si salen varias y la pregunta no dice la especie, ¿qué haces?**

```markdown
2. Si salen varias filas y la pregunta no dice la especie, no sigas: lista las
   candidatas y para. No elijas aunque una parezca la más común.
```

**Comprueba:** `¿qué es la mioglobina?` → lista y para. `¿de rata?` → sigue sola.

## 3 · `skills/blast-ncbi/SKILL.md`

**Escribe la descripción leyendo el método.**

```yaml
description: Envía un blastp contra PDB a NCBI y devuelve el RID y el enlace a los resultados.
```

**Comprueba:** al pedir un BLAST aparece `Loaded blast-ncbi skill` y un `RID`.

## 4 · `skills/informe/SKILL.md`

**¿Qué convierte el informe en prueba?**

```markdown
3. **Fuentes:** todas las URLs usadas, una por dato.
```

**Comprueba:** cada enlace de `informe.md` abre y contiene el dato citado.
