CHEATSHEET — Programación Musical con Python

Novas Tecnoloxías aplicadas á Música · 2º Trimestre

Idea clave: pensa no código como nunha partitura
→ listas = melodías
→ bucles = repetición
→ funcións = motivos reutilizables
→ clases = instrumentos / obxectos musicais

1️⃣ Python básico (o imprescindible)
Tipos de datos
int # 4, 8, -2
float # 0.5, 1.0
str # "C4", "La menor"
bool # True / False

Variables
nota = "C4"
duracion = 1.0
tempo = 120

Listas (melodías)
melodia = ["C4", "D4", "E4", "G4"]
duracions = [1, 1, 1, 2]

Acceso:

melodia[0] # primeira nota
melodia[-1] # última
melodia[1:3] # submelodía

Percorrer:

for nota in melodia:
print(nota)

Diccionarios (relacións)
nota_a_midi = {
"C": 0,
"D": 2,
"E": 4,
"F": 5,
"G": 7,
"A": 9,
"B": 11
}

Funcións (xestos musicais)
def transpoñer(melodia, semitonos):
return nova_melodia

Clases (obxectos musicais)
class Nota:
def **init**(self, pitch, dur):
self.pitch = pitch
self.dur = dur

2️⃣ Representar música con Python
Nota como string
"C4", "D#4", "Bb3"

Melodía como lista
melodia = ["C4", "D4", "E4", "G4"]

Melodía con ritmo
melodia = [
("C4", 1),
("D4", 1),
("E4", 2)
]

Transposición simple (idea)
nota → número → sumar → volver a nota

3️⃣ music21 — Música simbólica
Importar
from music21 import stream, note, chord, meter, tempo, key

Crear unha partitura
s = stream.Stream()
s.append(meter.TimeSignature("4/4"))
s.append(tempo.MetronomeMark(number=100))

Engadir notas
n = note.Note("C4", quarterLength=1)
s.append(n)

Silencio:

r = note.Rest(quarterLength=1)
s.append(r)

Acordes
c = chord.Chord(["C4", "E4", "G4"])
s.append(c)

Tonalidade
k = key.Key("C") # Do maior
k = key.Key("A", "minor")

Mostrar / exportar
s.show("text") # ver contido
s.show() # partitura (se hai MuseScore)
s.write("midi") # exportar MIDI

4️⃣ Estruturas musicais en código
Repetición (canon, refrán)
for i in range(4):
s.append(nota)

Forma A–B–A
forma = A + B + A

Variación
A_transposta = transpoñer(A, 5)

5️⃣ Audio con librosa
Importar
import librosa
import librosa.display
import numpy as np
import matplotlib.pyplot as plt

Cargar audio
y, sr = librosa.load("audio.wav")

y → array de mostras

sr → sampling rate (Hz)

Forma de onda
librosa.display.waveshow(y, sr=sr)
plt.show()

Cortar audio
y_corte = y[sr*5 : sr*10] # de 5s a 10s

Gardar audio
import soundfile as sf
sf.write("corte.wav", y_corte, sr)

6️⃣ Espectrograma
S = np.abs(librosa.stft(y))
S_db = librosa.amplitude_to_db(S, ref=np.max)

librosa.display.specshow(
S_db,
sr=sr,
x_axis="time",
y_axis="hz"
)
plt.colorbar()
plt.show()

7️⃣ Tempo, ritmo e eventos
BPM
tempo, \_ = librosa.beat.beat_track(y=y, sr=sr)
tempo

Onsets (ataques)
onsets = librosa.onset.onset_detect(y=y, sr=sr)

8️⃣ Timbre e features básicas
Enerxía (RMS)
rms = librosa.feature.rms(y=y)

Centroide espectral (brillo)
centroid = librosa.feature.spectral_centroid(y=y, sr=sr)

Zero Crossing Rate
zcr = librosa.feature.zero_crossing_rate(y)

9️⃣ Boas prácticas (importantísimo)

✅ Código curto
✅ Funcións pequenas
✅ Nomes claros (melodia_A, bpm_audio1)
✅ Comentarios como indicacións musicais
✅ Escoitar TODO o que se xera
❌ Copiar/pegar sen entender

🔁 Ler código como partitura
Música Código
Motivo función
Repetición bucle
Variación parámetro
Forma estrutura do script
Instrumento clase
Partitura notebook
