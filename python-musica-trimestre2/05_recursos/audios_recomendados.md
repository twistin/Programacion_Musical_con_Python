# 🎧 Audios recomendados para o curso

Lista de audios CC0/dominio público para usar nos exercicios.

---

## Exemplos integrados en librosa

Non necesitan descarga — úsanse directamente:

```python
import librosa

# Lista completa de exemplos
y, sr = librosa.load(librosa.ex('trumpet'))     # 🎺 Trompeta (solo)
y, sr = librosa.load(librosa.ex('nutcracker'))  # 🩰 O Cascanueces
y, sr = librosa.load(librosa.ex('brahms'))      # 🎻 Brahms (orquestra)
y, sr = librosa.load(librosa.ex('choice'))      # 🎤 Voz cantada
y, sr = librosa.load(librosa.ex('fishin'))      # 🎸 Folk/guitarra
y, sr = librosa.load(librosa.ex('pistachio'))   # 🥁 Percusión
```

---

## Obras do corpus de music21

```python
from music21 import corpus

# Corais de Bach (moi recomendadas para análise harmónica)
corpus.parse('bach/bwv66.6')
corpus.parse('bach/bwv269')
corpus.parse('bach/bwv347')

# Outras obras
corpus.parse('monteverdi/madrigal.5.1')
corpus.parse('handel/hwv56/movement1-01')

# Buscar obras
corpus.search('bach', 'composer')
corpus.search('sonata', 'title')
```

---

## Fontes externas CC0

| Fonte | URL | Tipo |
|-------|-----|------|
| Freesound | freesound.org | Sons e efectos |
| Musopen | musopen.org | Clásica libre |
| IMSLP | imslp.org | Partituras dominio público |
| Internet Archive | archive.org/details/audio | Gravacións históricas |

### Recomendacións específicas para o curso

**Para S07-S09 (librosa):**
- Buscar en Freesound: "classical guitar CC0"
- Buscar en Musopen: gravacións de Bach, Mozart

**Para análise de interpretacións:**
- Internet Archive ten gravacións antigas de dominio público
- Comparar dúas versións da mesma obra

---

## ⚠️ Nota sobre licenzas

- **CC0** = dominio público, úsase libremente
- **CC-BY** = libre pero citar autor
- **Non usar** audios con © sen permiso

> 💡 Sempre verifica a licenza antes de usar un audio no proxecto final.
