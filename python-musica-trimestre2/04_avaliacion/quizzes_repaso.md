# 🧠 Quizzes de repaso — Inicio de sesión

**Obxectivo:** Activar coñecementos previos antes de cada sesión (5 min).

---

## 📌 Instrucións para o profesorado

- Proxectar ou repartir ao comezo de cada sesión
- Os alumnos responden **sen mirar apuntes** (1–2 min)
- Correxir en grupo (3 min)
- Non puntúa, é para **activar a memoria**

---

# 🟦 BLOQUE I — Python aplicado á música

## Quiz S02 (repaso de S01)

1. **Que tipo de dato usamos para representar unha nota como "C4"?**
   - a) int
   - b) float
   - c) str ✅
   - d) list

2. **Se `melodia = [60, 62, 64]` (MIDI), como a transpoñemos +5 semitonos?**
   - a) `melodia + 5`
   - b) `[n + 5 for n in melodia]` ✅
   - c) `melodia.append(5)`
   - d) `sum(melodia, 5)`

3. **Que significa transpoñer -12 semitonos?**
   - Resposta: Baixar unha oitava ✅

---

# 🟦 BLOQUE II — music21

## Quiz S03 (repaso de S02)

1. **Que é unha función en Python?**
   - Resposta: Un bloque de código reutilizable que se executa ao chamalo ✅

2. **Que é unha clase?**
   - Resposta: Un molde para crear obxectos con atributos e métodos ✅

3. **Se temos `def transpoñer(notas, n):`, que son `notas` e `n`?**
   - Resposta: Parámetros (ou argumentos) da función ✅

---

## Quiz S04 (repaso de S03)

1. **Que biblioteca usamos para música simbólica?**
   - Resposta: music21 ✅

2. **Como creamos unha nota Do4 en music21?**
   - a) `Note("C4")` ✅
   - b) `note.C4`
   - c) `music21.do(4)`

3. **Que é un Stream en music21?**
   - Resposta: Un contedor de obxectos musicais (notas, silencios, acordes) ✅

4. **Como exportamos unha partitura a MIDI?**
   - a) `stream.save("midi")`
   - b) `stream.write("midi")` ✅
   - c) `stream.export("midi")`

---

## Quiz S05 (repaso de S04)

1. **Que propiedade dunha nota indica a súa duración?**
   - Resposta: `quarterLength` (ou `duration`) ✅

2. **Se `quarterLength = 0.5`, que figura é?**
   - Resposta: Corchea ✅

3. **Que é unha frase musical?**
   - Resposta: Unha idea musical completa, como unha frase verbal ✅

4. **Na forma A–B–A, que significa a última A?**
   - Resposta: Reexposición/repetición da sección inicial ✅

---

## Quiz S06 (repaso de S05)

1. **Que fai `score.analyze('key')`?**
   - Resposta: Estima a tonalidade da obra ✅

2. **Que fai `chordify()`?**
   - Resposta: Reduce as voces a acordes (verticais) ✅

3. **Que é un cifrado romano (ex. V7)?**
   - Resposta: Un acorde identificado polo seu grao na escala e calidade ✅

4. **En Do maior, que acorde é o grao V?**
   - Resposta: Sol maior (G) ✅

---

# 🟦 BLOQUE III — librosa

## Quiz S07 (repaso de S06)

1. **Que diferenza hai entre música simbólica e audio?**
   - Resposta: Simbólica = notas/partitura; Audio = onda sonora dixital ✅

2. **Que mide o eixo Y nunha forma de onda?**
   - a) Frecuencia
   - b) Amplitude ✅
   - c) Tempo

3. **Se un audio ten sr=44100, que significa?**
   - Resposta: 44.100 mostras por segundo (sample rate) ✅

---

## Quiz S08 (repaso de S07)

1. **Que biblioteca usamos para audio?**
   - Resposta: librosa ✅

2. **Como cargamos un audio de exemplo?**
   - a) `librosa.load("exemplo")`
   - b) `librosa.ex('trumpet')` ✅
   - c) `audio.open("file")`

3. **Como calculamos a duración dun audio?**
   - Resposta: `len(y) / sr` ou `librosa.get_duration()` ✅

---

## Quiz S09 (repaso de S08)

1. **Que amosa un espectrograma?**
   - Resposta: Frecuencias ao longo do tempo ✅

2. **Que significa BPM?**
   - Resposta: Beats Per Minute (pulsacións por minuto) ✅

3. **Que son os onsets?**
   - Resposta: Os inicios/ataques das notas ou golpes ✅

4. **Que instrumento tería harmónicos máis visibles: piano ou bombo?**
   - Resposta: Piano (sons tonais teñen harmónicos claros) ✅

---

# 🟦 BLOQUE IV — Proxecto final

## Quiz S10 (repaso de S09)

1. **Que é o timbre?**
   - Resposta: A "cor" do son que distingue instrumentos/voces ✅

2. **Que mide o centroide espectral?**
   - Resposta: O "brillo" ou centro de gravidade do espectro ✅

3. **Que son os MFCCs?**
   - Resposta: Coeficientes que representan o timbre (usados en recoñecemento) ✅

---

## Quiz S11 (repaso de S10)

1. **Que é un MVP (Minimum Viable Product)?**
   - Resposta: A versión mínima funcional do proxecto ✅

2. **Por que é importante modularizar o código?**
   - Resposta: Para reutilizar, organizar e depurar máis facilmente ✅

3. **Cal é a diferenza entre as opcións A, B e C do proxecto?**
   - A = simbólico/music21
   - B = audio/librosa
   - C = exploración avanzada ✅

---

## Quiz S12 (repaso xeral)

1. **Nomea unha operación musical que se pode facer con código:**
   - Respostas válidas: transpoñer, inverter, xerar escala, analizar harmonía... ✅

2. **Que significa "ler código como partitura"?**
   - Resposta: Ver a estrutura, orde e lóxica do código como se fose música ✅

3. **Que aprendiches neste trimestre?** (resposta libre)

---

> 🎶 *Os quizzes son para activar, non para penalizar.*
