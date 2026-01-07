# ✅ Auto-tests para notebooks

**Obxectivo:** Permitir ao alumnado verificar automaticamente se o seu código é correcto.

---

## 📌 Que é un auto-test?

Un **auto-test** usa `assert` de Python para comprobar que o código fai o esperado.

```python
# Se a condición é True, non pasa nada (correcto!)
# Se é False, lanza un AssertionError (incorrecto!)

assert 2 + 2 == 4  # ✅ Pasa
assert 2 + 2 == 5  # ❌ Falla: AssertionError
```

---

## 🧪 Exemplo básico para o alumnado

```python
# A túa melodía
melodia = ["C4", "D4", "E4", "G4"]

# ═══════════════════════════════════════════════════════
# 🧪 AUTO-TEST (executa para verificar)
# ═══════════════════════════════════════════════════════
assert isinstance(melodia, list), "❌ 'melodia' debe ser unha lista"
assert len(melodia) >= 4, "❌ A melodía debe ter polo menos 4 notas"
assert all(isinstance(n, str) for n in melodia), "❌ Todas as notas deben ser strings"
print("✅ Todos os tests pasaron!")
```

---

# 📋 Auto-tests por sesión

## S01 — Python musical básico

```python
# ═══════════════════════════════════════════════════════
# 🧪 AUTO-TESTS S01
# ═══════════════════════════════════════════════════════

# Test 1: Melodía creada
assert 'melodia' in dir(), "❌ Debes crear unha variable 'melodia'"
assert isinstance(melodia, list), "❌ 'melodia' debe ser unha lista"
assert len(melodia) >= 4, "❌ A melodía debe ter polo menos 4 notas"

# Test 2: Función de transposición
assert 'transpoñer' in dir(), "❌ Debes crear a función 'transpoñer'"
test_mel = [60, 62, 64]
assert transpoñer(test_mel, 0) == test_mel, "❌ Transpoñer +0 debe dar o mesmo"
assert transpoñer(test_mel, 12) == [72, 74, 76], "❌ Transpoñer +12 non funciona"

print("✅ S01: Todos os tests pasaron!")
```

---

## S02 — Funcións e clases

```python
# ═══════════════════════════════════════════════════════
# 🧪 AUTO-TESTS S02
# ═══════════════════════════════════════════════════════

# Test 1: Clase Nota creada
assert 'Nota' in dir(), "❌ Debes crear a clase 'Nota'"

# Test 2: Atributos correctos
n = Nota("C4", 1.0)
assert hasattr(n, 'pitch'), "❌ A clase Nota debe ter atributo 'pitch'"
assert hasattr(n, 'dur'), "❌ A clase Nota debe ter atributo 'dur'"

# Test 3: Canon creado
assert 'canon' in dir() or 'crear_canon' in dir(), "❌ Debes crear o canon"

print("✅ S02: Todos os tests pasaron!")
```

---

## S03 — music21 corpus

```python
# ═══════════════════════════════════════════════════════
# 🧪 AUTO-TESTS S03
# ═══════════════════════════════════════════════════════
from music21 import stream

# Test 1: Obra cargada
assert 'score' in dir() or 'obra' in dir(), "❌ Debes cargar unha obra do corpus"

# Test 2: É un Stream válido
obra_test = score if 'score' in dir() else obra
assert isinstance(obra_test, stream.Score) or isinstance(obra_test, stream.Stream), \
    "❌ A obra debe ser un Stream de music21"

# Test 3: Ten partes
assert len(obra_test.parts) > 0, "❌ A obra debe ter polo menos unha parte"

print("✅ S03: Todos os tests pasaron!")
```

---

## S04 — Análise melódica

```python
# ═══════════════════════════════════════════════════════
# 🧪 AUTO-TESTS S04
# ═══════════════════════════════════════════════════════

# Test 1: Rango calculado
assert 'rango' in dir() or 'rango_melodico' in dir(), \
    "❌ Debes calcular o rango melódico"

# Test 2: Rango é un número
rango_test = rango if 'rango' in dir() else rango_melodico
assert isinstance(rango_test, (int, float)), "❌ O rango debe ser un número"
assert rango_test > 0, "❌ O rango debe ser positivo"

# Test 3: Duracións analizadas
assert 'duracions' in dir() or 'contador_dur' in dir(), \
    "❌ Debes analizar as duracións"

print("✅ S04: Todos os tests pasaron!")
```

---

## S05 — Análise harmónica

```python
# ═══════════════════════════════════════════════════════
# 🧪 AUTO-TESTS S05
# ═══════════════════════════════════════════════════════
from music21 import key

# Test 1: Tonalidade estimada
assert 'tonalidade' in dir() or 'key_estimated' in dir(), \
    "❌ Debes estimar a tonalidade"

# Test 2: Chordify aplicado
assert 'acordes' in dir() or 'chords' in dir(), \
    "❌ Debes aplicar chordify()"

# Test 3: Cifrado romano
assert 'cifrado' in dir() or 'roman' in dir(), \
    "❌ Debes calcular o cifrado romano"

print("✅ S05: Todos os tests pasaron!")
```

---

## S07 — Audio básico

```python
# ═══════════════════════════════════════════════════════
# 🧪 AUTO-TESTS S07
# ═══════════════════════════════════════════════════════
import numpy as np

# Test 1: Audio cargado
assert 'y' in dir(), "❌ Debes cargar un audio en 'y'"
assert 'sr' in dir(), "❌ Debes gardar o sample rate en 'sr'"

# Test 2: Formato correcto
assert isinstance(y, np.ndarray), "❌ 'y' debe ser un array de numpy"
assert isinstance(sr, int), "❌ 'sr' debe ser un enteiro"

# Test 3: Fragmentos cortados
assert 'frag_A' in dir() or 'fragmento' in dir(), \
    "❌ Debes cortar polo menos un fragmento"

print("✅ S07: Todos os tests pasaron!")
```

---

## S08 — Espectrograma

```python
# ═══════════════════════════════════════════════════════
# 🧪 AUTO-TESTS S08
# ═══════════════════════════════════════════════════════

# Test 1: BPM calculado
assert 'tempo' in dir() or 'bpm' in dir(), "❌ Debes calcular o BPM"

# Test 2: BPM é razoable
bpm_test = tempo if 'tempo' in dir() else bpm
if isinstance(bpm_test, np.ndarray):
    bpm_test = bpm_test[0]
assert 30 < bpm_test < 300, f"❌ BPM={bpm_test} parece incorrecto"

# Test 3: Onsets detectados
assert 'onsets' in dir() or 'onset_frames' in dir(), \
    "❌ Debes detectar os onsets"

print("✅ S08: Todos os tests pasaron!")
```

---

## S09 — Timbre e features

```python
# ═══════════════════════════════════════════════════════
# 🧪 AUTO-TESTS S09
# ═══════════════════════════════════════════════════════
import numpy as np

# Test 1: Features calculados
assert 'rms' in dir(), "❌ Debes calcular RMS"
assert 'centroide' in dir() or 'centroid' in dir(), \
    "❌ Debes calcular o centroide"

# Test 2: Pegada construída
assert 'fingerprint' in dir() or 'pegada' in dir(), \
    "❌ Debes construír a pegada sonora"

print("✅ S09: Todos os tests pasaron!")
```

---

## 💡 Como integrar nos notebooks

Engade unha cela ao final de cada sección co auto-test:

```python
# Ao final de cada sección importante:

# ═══════════════════════════════════════════════════════
# 🧪 VERIFICA O TEU CÓDIGO
# ═══════════════════════════════════════════════════════
# Executa esta cela para comprobar que todo está correcto

assert ...  # tests aquí
print("✅ Sección completada correctamente!")
```

---

> 🎯 *Os auto-tests axudan a detectar erros antes de entregar.*
