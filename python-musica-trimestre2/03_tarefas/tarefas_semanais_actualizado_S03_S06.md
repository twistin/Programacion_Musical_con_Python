# 📘 Tarefas semanais — Programación Musical con Python (Actualizado Bloque II: Análise con corpus)

Estas tarefas acompañan cada sesión (S01–S09).
O obxectivo é **practicar**, non “facelo perfecto”.

📌 Entrega habitual:
- Ligazón ao notebook de Colab
- Código executa sen erros
- Pequena reflexión escrita (3–8 liñas)

---

## 🟦 S01 — Python musical básico
**Tarefa**
- Crea unha melodía de 8–12 notas como lista.
- Transpóñea a +7 e -12 semitonos.
- Mostra as tres versións (orixinal + 2 transposicións).

**Reflexión**
- Que cambia e que se mantén?
- Por que dicimos que a melodía “segue sendo a mesma”?

---

## 🟦 S02 — Funcións, clases e canon
**Tarefa**
- Crea unha clase `Nota` con `pitch` e `dur`.
- Define unha frase de 4–6 notas.
- Xera un **canon** cun desfase de 4 pulsos.

**Reflexión**
- Onde aparece a repetición no código?
- Como representa o canon musicalmente?

---

# ✅ BLOQUE II (music21) — Agora é ANÁLISE sobre obras reais

---

## 🟦 S03 — Ler unha obra do corpus (music21 lector)
**Tarefa**
1) Carga **unha obra do corpus de music21** (non a mesma que no exemplo):
   - recomendación: outra coral de Bach (BWV diferente)
2) Extrae e escribe:
   - nº de partes (voces/instrumentos)
   - compás (TimeSignature)
   - tonalidade estimada (`analyze('key')`)
3) Exporta a **MusicXML** co nome:
   - `S03_obra_corpus.musicxml`

**Reflexión (4–6 liñas)**
- Coincide a tonalidade estimada coa túa percepción/análise?
- Que che parece ver a obra “por dentro” (parts/measures) desde código?

---

## 🟦 S04 — Análise de melodía e ritmo sobre repertorio
**Tarefa**
1) Na mesma obra (ou noutra do corpus), escolle **2 voces** (por ex. Soprano e Baixo).
2) Para cada voz:
   - debuxa o **perfil melódico** (gráfico MIDI)
   - calcula o **rango** (máx–mín en MIDI)
   - calcula a **duración máis frecuente** (contador)
3) Compara as voces nunha conclusión curta.

**Reflexión (6–8 liñas)**
- Que diferenzas musicais ves entre soprano e baixo a partir dos datos?
- Coincide coa túa intuición harmónica/textural?

---

## 🟦 S05 — Harmonía funcional: acordes reais + cifrado romano
**Tarefa**
1) Escolle **un fragmento curto** (ex. 8–12 eventos/chords) dunha obra do corpus.
2) Fai:
   - `chordify()`
   - tonalidade estimada
   - **cifrado romano** para ese fragmento
3) Marca polo menos:
   - 1 posible **cadencia** (V–I, V7–I, IV–V–I…)  
   - 1 lugar onde sospeites **notas non harmónicas** (paso, retardos, bordaduras)

**Reflexión (6–8 liñas)**
- En que momentos `music21` che axuda máis?
- En que momentos hai que desconfiar do automático?

---

## 🟦 S06 — Comparación computacional entre dúas obras (estilo)
**Tarefa**
1) Escolle **2 obras do corpus** (poden ser:
   - dúas corais de Bach, ou
   - Bach vs outra obra)
2) Para unha voz (por defecto a 1ª), calcula:
   - rango (MIDI)
   - intervalo medio absoluto
   - nota máis frecuente
3) Engade 1 elemento harmónico aproximado:
   - top-5 tipos de acordes (`commonName`) en `chordify()`
4) Escribe unha interpretación.

**Reflexión (8–10 liñas)**
- Que che din os datos do estilo?
- Coincide co que escoitarías/analizarías a man?
- Que limitacións ten este enfoque?

---

## 🟦 S07 — Audio básico
**Tarefa**
- Carga un audio.
- Debuxa a forma de onda.
- Corta 2 fragmentos (≥2s).
- Garda os fragmentos en WAV.

**Reflexión**
- Que información che dá a onda?
- Que diferenzas ves entre fragmentos?

---

## 🟦 S08 — Espectrograma, BPM e onsets
**Tarefa**
- Debuxa un espectrograma.
- Calcula BPM.
- Detecta onsets.
- Compara 2 fragmentos.

**Reflexión**
- O BPM coincide coa túa percepción?
- Que fragmento é máis “denso”?

---

## 🟦 S09 — Timbre e features
**Tarefa**
- Calcula RMS, centroide e ZCR.
- Constrúe unha “pegada sonora”.
- Compara dous audios ou fragmentos.

**Reflexión**
- Que feature distingue mellor os sons?
- Que limitacións ves nesta análise?
