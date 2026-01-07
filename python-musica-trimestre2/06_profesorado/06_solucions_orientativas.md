# 🧪 SOLUCIÓNS ORIENTATIVAS — DOCUMENTO DOCENTE  

## Programación Musical con Python · 2º Trimestre · Conservatorio

⚠️ DOCUMENTO INTERNO DO PROFESORADO  
⚠️ NON COMPARTIR CO ALUMNADO  
⚠️ As solucións son ORIENTATIVAS, non únicas

Este documento serve para:

- orientar a corrección das tarefas e mini-proxectos
- garantir mínimos comúns entre grupos
- detectar erros habituais
- manter coherencia pedagóxica coa materia de Harmonía

O criterio central de avaliación é sempre:

> **comprensión musical + lectura crítica**,  
> non complexidade técnica nin “acertar” automaticamente.

---

# 🟦 S01 — Python musical básico

### Tarefa

Crear melodía + transposicións.

### Solución orientativa

```python
melodia = ["C4","D4","E4","G4","E4","D4","C4"]

from music21 import note

def transpoñer(mel, n):
    out = []
    for p in mel:
        nn = note.Note(p)
        nn.transpose(n, inPlace=True)
        out.append(nn.nameWithOctave)
    return out

mel_up = transpoñer(melodia, 7)
mel_down = transpoñer(melodia, -12)
Indicadores positivos
✔ Mantén identidade melódica
✔ Usa función reutilizable
✔ Entende transposición como relación interválica

Erros habituais
❌ Cambiar orde das notas
❌ Confundir transposición con inversión

🟦 S02 — Funcións, clases e canon
Tarefa
Definir clase + canon con desfase temporal.

Solución orientativa
python
Copiar código
class Nota:
    def __init__(self, pitch, dur):
        self.pitch = pitch
        self.dur = dur

frase = [
    Nota("C4",1),
    Nota("D4",1),
    Nota("E4",2)
]

def canon(frase, desfase):
    return frase + [Nota("REST", desfase)] + frase
Clave de avaliación
✔ O canon é temporal, non só repetición
✔ Relación clara código ↔ música

🟦 BLOQUE II — music21 como ferramenta de ANÁLISE
🟦 S03 — Lectura dunha obra real (corpus music21)
Tarefa
Cargar obra, identificar estrutura, exportar MusicXML.

Solución orientativa
python
Copiar código
from music21 import corpus
score = corpus.parse("bach/bwv66.6")

score.show("text")
print("Tonalidade estimada:", score.analyze("key"))
Avaliación
✔ Identifica número de partes
✔ Localiza compás
✔ Reflexiona criticamente sobre a tonalidade

❌ Penalizar aceptación acrítica de analyze('key')

🟦 S04 — Análise melódica e rítmica sobre repertorio
Tarefa
Comparar dúas voces da mesma obra.

Solución orientativa
python
Copiar código
from collections import Counter

def analise_voz(part):
    notes = list(part.recurse().notes)
    midi = [n.pitch.midi for n in notes]
    durs = [float(n.quarterLength) for n in notes]
    return {
        "rango": max(midi) - min(midi),
        "dur_mais_frecuente": Counter(durs).most_common(1)
    }
Interpretación esperable
soprano → maior mobilidade melódica

baixo → estabilidade estrutural

Erros habituais
❌ Comparación sen interpretación musical
❌ Gráficas sen explicación

🟦 S05 — Harmonía funcional con music21
Tarefa
Cifrado romano + identificación de cadencia.

Solución orientativa
python
Copiar código
from music21 import corpus, roman

score = corpus.parse("bach/bwv66.6")
k = score.analyze("key")
ch = score.chordify()

from music21 import chord as m21chord

for c in ch.recurse().getElementsByClass(m21chord.Chord)[:10]:
    print(roman.romanNumeralFromChord(c, k))
Avaliación
✔ Detecta funcións principais
✔ Identifica V–I / V7–I
✔ Recoñece notas non harmónicas

❌ Penalizar:

aceptar cifrado automático como definitivo

non relacionar coa Harmonía tradicional

🟦 S06 — Comparación computacional de dúas obras
Tarefa
Comparar dúas obras do corpus con métricas simples.

Solución orientativa
python
Copiar código
from music21 import interval
import numpy as np

def metricas(score):
    part = score.parts[0]
    notes = list(part.recurse().notes)
    midi = [n.pitch.midi for n in notes]
    semis = [
        interval.Interval(a,b).semitones
        for a,b in zip(notes, notes[1:])
    ]
    return {
        "rango": max(midi)-min(midi),
        "intervalo_med": np.mean([abs(x) for x in semis])
    }
Avaliación
✔ Usa datos para apoiar ideas musicais
✔ Recoñece límites do enfoque

🟦 S07 — Audio básico
python
Copiar código
import librosa
y, sr = librosa.load("audio.wav", sr=None)
frag = y[int(2*sr):int(5*sr)]
✔ Entende que audio = mostras no tempo

🟦 S08 — Espectrograma, BPM e onsets
python
Copiar código
tempo, beats = librosa.beat.beat_track(y=y, sr=sr)
onsets = librosa.onset.onset_detect(y=y, sr=sr)
✔ Interpreta resultados
❌ Non se penaliza BPM inexacto

🟦 S09 — Timbre e features
python
Copiar código
rms = librosa.feature.rms(y=y)
cent = librosa.feature.spectral_centroid(y=y, sr=sr)
zcr = librosa.feature.zero_crossing_rate(y)
✔ Usa features como descrición, non como etiqueta absoluta

🧩 MINI-PROXECTOS — SOLUCIÓNS ORIENTATIVAS
Mini-proxecto 1 — Análise melódica e rítmica
✔ Dúas voces reais
✔ Gráficas claras
✔ Conclusión musical razoada

Mini-proxecto 2 — Harmonía funcional
✔ Fragmento delimitado
✔ Cifrado explicado
✔ Cadencia xustificada
✔ Lectura crítica do automático

Mini-proxecto 3 — Comparación de estilo
✔ Métricas coherentes
✔ Interpretación musical
✔ Relación con audición/análise tradicional

🎯 CRITERIOS XERAIS DE CORRECCIÓN
✔ Comprensión musical
✔ Código claro e funcional
✔ Capacidade de explicar resultados

❌ Penalizar:

copiar sen entender

aceptar resultados automáticos sen crítica

ausencia de reflexión escrita

🧠 NOTA FINAL PARA O PROFESORADO
Un traballo ben avaliado é aquel no que o alumnado pode dicir:

“Isto xa o sabía como estudante de Harmonía,
pero agora vexo como Python pode axudarme a analizalo.”

Ese é o obxectivo real da materia.

yaml
Copiar código

---

Si quieres, el **último paso “premium”** sería:
- un **README docente final** que explique todo o repositorio  
- o un **documento de xustificación metodolóxica** listo para inspección

Pero a nivel de **material**, isto xa está **redondo e profesional**.
