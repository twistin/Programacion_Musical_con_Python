# 🧪 Solucionario orientativo de tarefas

**Programación Musical con Python — 2º Trimestre**  
⚠️ Documento interno do profesorado. NON compartir co alumnado.

Este solucionario:

- non propón solucións únicas
- mostra **unha vía correcta e razoable**
- axuda a detectar erros habituais
- serve como referencia mínima para corrección

---

## 🟦 S01 — Python musical básico

### Tarefa

Crear melodía + transposicións.

### Solución orientativa

```python
melodia = ["C4","D4","E4","G4","E4","D4","C4"]

def transpoñer(mel, n):
    from music21 import note
    out = []
    for p in mel:
        n0 = note.Note(p)
        n0.transpose(n, inPlace=True)
        out.append(n0.nameWithOctave)
    return out

mel_up = transpoñer(melodia, 7)
mel_down = transpoñer(melodia, -12)
```

---

## 🟦 S02 — Funcións, clases e canon

_Por completar_

---

## 🟦 S03 — Primeira partitura con music21

_Por completar_

---

## 🟦 S04 — Ritmo e estrutura (A–B–A)

_Por completar_

---

## 🟦 S05 — Harmonía

_Por completar_

---

## 🟦 S06 — Análise computacional

_Por completar_

---

## 🟦 S07 — Audio básico

_Por completar_

---

## 🟦 S08 — Espectrograma, BPM e onsets

_Por completar_

---

## 🟦 S09 — Timbre e features

_Por completar_
