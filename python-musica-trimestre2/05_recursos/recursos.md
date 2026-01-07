# 📚 Recursos — Programación Musical con Python

**Curso:** Novas Tecnoloxías aplicadas á Música — 2º Trimestre

---

## 🔗 Documentación oficial

### music21
- [Documentación principal](https://web.mit.edu/music21/doc/)
- [Tutorial rápido](https://web.mit.edu/music21/doc/usersGuide/index.html)
- [Referencia de API](https://web.mit.edu/music21/doc/moduleReference/index.html)
- [Corpus incluído](https://web.mit.edu/music21/doc/about/referenceCorpus.html)

### librosa
- [Documentación principal](https://librosa.org/doc/latest/)
- [Tutorial de introdución](https://librosa.org/doc/latest/tutorial.html)
- [Exemplos de código](https://librosa.org/doc/latest/auto_examples/index.html)
- [Referencia de API](https://librosa.org/doc/latest/core.html)

### Outras ferramentas útiles
- [NumPy para principiantes](https://numpy.org/doc/stable/user/absolute_beginners.html)
- [Matplotlib — galería](https://matplotlib.org/stable/gallery/index.html)
- [Google Colab — FAQ](https://research.google.com/colaboratory/faq.html)

---

## 🎵 Audios CC0 para análise

Fontes de audio con licenza libre (dominio público ou CC0):

### Coleccións xerais
- [Freesound.org](https://freesound.org/) — buscar con filtro "Creative Commons 0"
- [Internet Archive Audio](https://archive.org/details/audio) — gravacións históricas
- [Musopen](https://musopen.org/) — música clásica libre de dereitos

### Audios incluídos en librosa
```python
import librosa

# Exemplos xa incluídos (non necesitan descarga)
librosa.ex('trumpet')      # trompeta
librosa.ex('nutcracker')   # O Cascanueces (orquestra)
librosa.ex('brahms')       # Brahms (orquestra)
librosa.ex('choice')       # voz cantada
librosa.ex('fishin')       # música folk
librosa.ex('pistachio')    # percusión
```

### Corpus MIDI/MusicXML en music21
```python
from music21 import corpus

# Obras dispoñibles (exemplos)
corpus.parse('bach/bwv66.6')         # coral de Bach
corpus.parse('mozart/k545')          # sonata de Mozart (parcial)
corpus.parse('beethoven/opus18no1')  # cuarteto de Beethoven
corpus.search('bach')                # buscar obras de Bach
```

---

## 📖 Bibliografía recomendada

### Libros fundamentais

| Título | Autor(es) | Tema |
|--------|-----------|------|
| *Music and Computers: A Theoretical and Historical Approach* | Burk et al. | Fundamentos audio/MIDI |
| *Fundamentals of Music Processing* | Meinard Müller | MIR, análise de audio |
| *The Oxford Handbook of Computer Music* | Dean (ed.) | Computación musical |

### Artigos e recursos en liña

- [ISMIR Papers](https://ismir.net/resources/papers/) — conferencia de referencia en MIR
- [Music Information Retrieval (tutorial)](https://musicinformationretrieval.com/) — Steve Tjoa
- [FMP Notebooks](https://www.audiolabs-erlangen.de/resources/MIR/FMP/C0/C0.html) — Meinard Müller (gratuíto)

### En galego/español

- Blog [Python para músicos](https://pythonparamusicos.com/) (se existe)
- Documentación en español de [Real Python](https://realpython.com/) (parcial)

---

## 🎓 Para profundar

### Cursos en liña (gratuítos)
- [Audio Signal Processing for Music Applications](https://www.coursera.org/learn/audio-signal-processing) — Coursera/Stanford
- [Music Information Retrieval](https://www.kadenze.com/courses/machine-learning-for-music-information-retrieval) — Kadenze

### Ferramentas avanzadas
- [Essentia](https://essentia.upf.edu/) — análise de audio (UPF Barcelona)
- [Sonic Visualiser](https://www.sonicvisualiser.org/) — visualización de audio
- [MuseScore](https://musescore.org/) — edición de partituras (gratuíto)

### Live coding (para exploración avanzada)
- [Sonic Pi](https://sonic-pi.net/) — música en tempo real con código
- [FoxDot](https://foxdot.org/) — live coding con Python
- [SuperCollider](https://supercollider.github.io/) — síntese e composición

---

## 💡 Consellos de uso

1. **Empeza polos exemplos integrados** — `librosa.ex()` e `corpus.parse()` non requiren descargas
2. **Verifica licenzas** — se usas audio externo, comproba que sexa CC0 ou dominio público
3. **Cita sempre** — en proxectos, indica a fonte do audio ou partitura

> 🎶 *"Os recursos son infinitos; o importante é saber onde buscar."*
