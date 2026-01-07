# 🧪 Solucionario docente — Mini-proxectos

**Programación Musical con Python · 2º Trimestre · Conservatorio**

⚠️ Documento interno do profesorado  
Non proporciona “respostas correctas”, senón **vías razoables de resolución**  
e **criterios para interpretar o traballo do alumnado**.

---

# 🟦 Mini-proxecto 1

## Análise melódica e rítmica dunha obra real (S03–S04)

### Enfoque musical esperado

- Comprensión de que **cada voz ten un papel distinto**
- Relación entre:
  - rexistro
  - densidade rítmica
  - función harmónica/textural

Non se espera linguaxe estatística avanzada, senón **lectura musical dos datos**.

---

### Solución orientativa (exemplo)

```python
from music21 import corpus
import matplotlib.pyplot as plt
from collections import Counter

score = corpus.parse("bach/bwv66.6")
parts = score.parts

soprano = parts[0]
bass = parts[-1]

def analise_voz(part):
    notes = list(part.recurse().notes)
    midi = [n.pitch.midi for n in notes]
    durs = [float(n.quarterLength) for n in notes]
    return {
        "rango": max(midi) - min(midi),
        "dur_mais_freq": Counter(durs).most_common(1),
        "midi": midi
    }

s = analise_voz(soprano)
b = analise_voz(bass)
```
