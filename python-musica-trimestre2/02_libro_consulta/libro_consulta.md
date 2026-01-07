🎶 Curso: Programación Musical con Python
Duración: 1 trimestre (≈ 12 semanas)
Nivel: Iniciación–intermedio
Requisitos previos: Coñecementos básicos de Python
Enfoque: entender a música pensando de forma algorítmica
🎯 Obxectivos do trimestre
Ao finalizar este tramo do curso, o alumnado será capaz de:
Usar Python para representar, analizar e transformar música.
Comprender a diferenza entre música simbólica e audio (son dixital).
Empregar bibliotecas musicais de Python na práctica (p.ex. music21, librosa).
Desenvolver un proxecto musical computacional propio.
Ler o código como se fose unha partitura (interpretar a lóxica do programa en termos musicais).
🧭 Estrutura xeral do trimestre
Bloque Semanas Enfoque
I 1–2 Repaso + pensamento musical algorítmico
II 3–6 Música simbólica con music21
III 7–9 Audio e son con librosa
IV 10–12 Proxecto final
🟦 BLOQUE I — Python aplicado á música (Semanas 1–2)
🎯 Obxectivo
Reactivar os coñecementos de Python básico e cambiar o chip: pasar de resolver problemas abstractos a aplicar a programación na música. Trátase de conectar conceptos de código coas súas contrapartes musicais, para que o alumnado vexa a linguaxe Python como unha ferramenta creativa máis.
Contidos
Repaso rápido de Python e contorna: Inclúe un recordatorio do uso básico da terminal (comandos como cd, ls, etc. para navegar polos cartafoles e executar scripts). Repásanse os tipos de datos fundamentais de Python (números enteiros, números decimais, cadeas de texto, booleanos
recursos.edu.xunta.gal
), a creación e uso de variables (espazos en memoria para gardar datos
recursos.edu.xunta.gal
), así como estruturas de datos como listas, tuplas, diccionarios e conxuntos
recursos.edu.xunta.gal
recursos.edu.xunta.gal
. Tamén se revisan as estruturas de control de fluxo: bucles (for, while) e condicións (if/elif/else), a definición de funcións e o concepto básico de clases e obxectos. En Python, unha clase funciona como un molde para crear obxectos, definindo atributos e métodos que describen o seu comportamento
recursos.edu.xunta.gal
. As clases permiten organizar e reutilizar código de forma clara, sendo moi útiles en proxectos complexos
recursos.edu.xunta.gal
.
Representación da música con Python: Preséntanse formas sinxelas de modelar elementos musicais empregando tipos de datos básicos. Por exemplo, podemos representar as notas mediante cadeas de texto ("Do4" para a nota do na cuarta oitava, "Re#3" para un re sostenido na terceira oitava, etc.), as duracións rítmicas mediante números (p. ex. 1.0 para unha negra, 0.5 para unha corchea, etc.) e as melodías completas mediante listas que combinan estes elementos (lista de parellas nota-duración ou dúas listas paralelas). Desta forma, un fragmento musical sinxelo pódese codificar como unha estrutura de datos que Python pode manipular. Exemplo: melodia = [("Do4", 1.0), ("Re4", 1.0), ("Sol3", 2.0)] podería representar unha melodía de tres notas cunha duración total de 4 tempos. Esta representación senta as bases para aplicar operacións algorítmicas sobre a música.
Pensamento algorítmico musical: Introdúcese a idea de que moitos procesos musicais teñen paralelismos na programación. Destácanse tres ideas clave: a repetición, a variación e a transformación. En música é frecuente repetir motivos ou seccións (refráns, compases repetidos, etc.); de forma análoga, en código usamos bucles para repetir instrucións. Tamén é habitual tomar un tema musical e aplicarlle variacións (cambios de ritmo, tonalidade, etc.); en programación podemos modificar datos ou parámetros para xerar variacións automaticamente. Por último, moitas técnicas compositivas son transformacións sistemáticas (transposición a outra tonalidade, investimento de intervalos, retrogradación, etc.), todas estas operacións que podemos implementar con código. O alumnado aprenderá a ver un fragmento de código do mesmo xeito que ve unha partitura, identificando patróns repetitivos e estruturas anidadas, e comprenderá que a lóxica dun programa pode imitar procesos creativos musicais.
Exercicios tipo
Transpoñer unha melodía: dada unha melodía representada como lista de notas, escribir unha función que a transpoña a outra tonalidade automaticamente (por exemplo, subir todos os tons un intervalo determinado). Este exercicio reforza o manexo de listas e operacións aritméticas con pitches musicais (pódense representar as notas como números MIDI ou graos e sumarlles unha constante para transpoñer).
Inverter intervalos dun tema: tomar unha serie de notas e xerar a inversión (intervalos ao revés, convertendo ascensos en descensos e viceversa). Isto implica restar en lugar de sumar ao calcular os saltos entre notas e axústase ben para practicar operacións con listas e matemáticas simples.
Xeración automática de escalas: a partir dun nome de escala (p. ex. maior, menor natural, modo Xónico, Dórico, etc.), construír a escala completa mediante código. Por exemplo, xerando a escala maior de Do calculando os intervalos correctos (T-T-S-T-T-T-S). Isto combina coñecemento musical teórico con lógica condicional e loops en Python.
Crear un canon simple con desfase: dada unha melodía de entrada, producir un canon a certa distancia temporal (p. ex. a dous compases de desfase). Basicamente consiste en repetir a lista de notas orixinal engadindo pausas (silencios) ao comezo para desprazala no tempo. Así, practícase a manipulación de listas (concatenación de silencios e notas) e introdúcese a idea de streams temporais.
💡 Consello: Ao longo destes exercicios énfase en debuxar paralelismos entre o código e a música: por exemplo, un bucle que repite catro veces un motivo é similar a unhas barras de repetición nunha partitura; unha función que encapsula unha operación musical (como transpoñer) é análoga a reutilizar un recurso temático nunha composición. Entender estas conexións axudará a cambiar o chip do alumnado cara a pensar a música de forma computacional.
🟦 BLOQUE II — Música simbólica con music21 (Semanas 3–6)
Nota: Este bloque é o cerne pedagóxico do curso – aquí é onde realmente se combinan Python e teoría musical para crear e analizar partituras de forma dinámica.
Semana 3 — Introdución a music21
Que é unha biblioteca? Explícase o concepto de biblioteca de código (ou libraría). Do mesmo xeito que usamos módulos estándar de Python, podemos instalar bibliotecas creadas por terceiros para tarefas específicas. Neste caso, music21 será a nosa biblioteca clave: music21 é unha biblioteca de Python que proporciona funcións e obxectos específicos para o manexo e manipulación de información musical (notas, partituras, acordes, intervalos, escalas, etc.)
2023.nodos.org
. Permitiranos crear e analizar música de forma programada.
Instalación de music21: Indícanse os pasos para instalar music21 (por exemplo, usando pip install music21). Tamén se comenta como verificar se a instalación foi correcta importando o módulo en Python (from music21 import \*). Se a instalación é exitosa, obteremos acceso a centos de clases e ferramentas musicais dentro de Python.
Conceptos clave de music21: Preséntanse as clases básicas que ofrece a libraría: note.Note (para representar unha nota musical individual, coa súa altura e duración), note.Rest (para representar un silencio ou pausa), chord.Chord (para representar un acorde, é dicir, varias notas simultáneas) e stream.Stream (un contedor secuencial de obxectos musicais, equivalente a un pentagrama ou secuencia de compases). Por exemplo, unha Note("C4") representa a nota de Do4, e pódese asignar unha duración como Note("C4", quarterLength=1.0) para facer que sexa unha negra
music21.org
. Un Stream pódese imaxinar como unha “partitura virtual” onde imos engadindo notas, silencios ou acordes de forma ordenada no tempo.
Creación dunha partitura por código: Unha vez coñecidos os obxectos básicos, demóstrase como construir unha pequena partitura usando Python. Por exemplo, crear un stream.Stream, engadir varias notas e silencios, e especificar atributos como o compás ou a armadura. music21 permite definir un compás (usando obxectos meter.TimeSignature), un tempo (obxecto tempo.MetronomeMark) e incluso tonalidade (obxecto key.Key) se é necesario. A partitura construída pode conter múltiples voces ou partes usando diferentes Streams anidados (por exemplo, un stream.Part para cada instrumento).
Exportación a formatos musicais (MusicXML, MIDI, PDF): Un dos momentos máis emocionantes desta semana é mostrar que o código que escribimos pode xerar música real fóra de Python. music21 permite gardar ou amosar as nosas composicións en varios formatos estándar. Usando stream.write(), podemos gardar unha partitura en formato MusicXML (formato intercambiable que poden ler programas de notación). Tamén podemos crear arquivos MIDI para escoitar o resultado. Ademais, se no ordenador temos instalado un programa de notación como MuseScore ou LilyPond, o comando stream.show() poderá lanzar ese programa e amosar a partitura en partitura tradicional. Incluso é posible obter un PDF coa notación. music21 actúa de ponte entre o noso código e a partitura impresa ou audible, o que causa un grande efecto “wow” ao ver unha melodía escrita en Python convertida en notas sobre un pentagrama na pantalla 🎼.
Semana 4 — Melodía, ritmo e estrutura
Duracións e ritmo: Apréndese a manexar as propiedades de duración das notas en music21. Cada note.Note ten un atributo duration (ou atallos como quarterLength) que indica o seu valor rítmico. Por exemplo, quarterLength=1.0 equivale a unha negra, 0.5 unha corchea, 2.0 unha mínima, etc. Explícase como se representan as figuras musicais e como combinando notas e silencios de distintas duracións formamos o ritmo dunha melodía. Tamén se introduce o concepto de compás: mediante obxectos de tipo meter.TimeSignature podemos definir, por exemplo, que a peza está en 4/4 ou 3/4, e music21 axudará a manter as duracións correctas en cada compás dun Stream.
Tempo (pulso) e velocidade: Destácase que, ademais das duracións relativas, unha peza musical necesita un tempo absoluto para saber canto dura cada figura. En music21, podemos especificar un tempo ou pulso usando tempo.MetronomeMark. Por exemplo, definir un tempo = 120 BPM (negra = 120) fará que o MIDI resultante soe a esa velocidade. Nos notebooks, tamén podemos escoitar os fragmentos usando Stream.show('midi') e apreciar os efectos de cambiar o tempo.
Frases musicais e estrutura: Explícase o concepto de frase musical (unha idea musical completa, equivalente a unha frase verbal). No código, aínda que non existe un obxecto “Frase”, podemos organizarnos agrupando as notas de cada frase en sub-listas ou en Streams separados, para logo xuntalos. Discútese a forma básica de estruturas musicais como A–B–A (forma ternaria simple): A sección inicial, B unha sección contrastante, e volta a A. A nivel de código, podemos compoñer unha sección A, compoñer unha sección B distinta, e despois reutilizar A (por exemplo, volver reproducir ou copiar ese Stream). Este enfoque enfatiza a reutilización de código (evitar duplicación) do mesmo xeito que en música reutilizamos seccións.
Exercicios prácticos desta semana:
Xeración de melodías con regras: Por exemplo, programar a creación aleatoria dunha melodía que siga unha escala dada (major, menor, modo exótico, etc.) aplicando regras (non saltar máis dunha 5ª, regresar á tónica periodicamente, etc.). Isto fai que o alumnado escriba código que decide notas en base a condicións, semellante a compor con algoritmos.
Variación rítmica: Tomar unha mesma secuencia de alturas (notas) e xerar versións con ritmos distintos. Por exemplo, unha melodía dada en corcheas convertela a tresillos ou a síncopas distintas. En código, reutilízanse as mesmas notas pero asígnanselles novos valores de duration. Este exercicio conecta coa idea de separar altura e ritmo na música, e permite practicar modificación de propiedades de obxectos en music21.
Preguntas e respostas musicales: Compoñer dúas frases onde a segunda “responda” á primeira. Por exemplo, a frase pregunta remata nunha semicadencia (suspensa) e a frase resposta conclúe na tónica. En código, poden xerarse dúas listas/Streams: a pregunta quizais ascende e deixa sensación de incompletude (termina nun acorde dominante), mentres que a resposta pode comezar máis alto e logo caer a reposo (termina en tónica). É un exercicio creativo que invita a pensar en forma musical e estrutura, mentres se programan dúas partes relacionadas. O importante é que o código poida reutilizar motivos da pregunta na resposta (variándoos lixeiramente), fomentando a idea de patróns repetidos con variacións (tal como bucles con modificacións).
Semana 5 — Harmonía funcional con music21

⚠️ Semana clave para o perfil do alumnado

**Contidos**

- Tonalidade automática
- Acordes reais da obra
- Cifrado romano (romanNumeral)
- Graos e funcións harmónicas

```python
from music21 import analysis

score.analyze('key')
score.chordify().show()

from music21 import roman
rn = roman.romanNumeralFromChord(chord, key)
```

**Exercicios tipo**

- Analizar unha coral de Bach
- Comparar análise manual vs automática
- Detectar cadencias
- Contar aparicións de cada grao

📌 **Moi importante:**
Non se avalía se music21 "acerta", senón se o alumno interpreta críticamente o resultado.

---

Semana 6 — Análise musical computacional (nivel conservatorio)

Aquí music21 convértese en ferramenta de investigación musical.

**Contidos**

- Intervalos reais nunha obra
- Distribución de alturas
- Estatísticas musicais
- Comparación entre obras / estilos

```python
intervals = []
for n1, n2 in zip(notes, notes[1:]):
    intervals.append(interval.Interval(n1, n2).semitones)
```

"Estilo" visto como patrón de datos.

**Exercicios tipo**

- Perfil melódico de Bach vs Mozart
- Comparación de rango, densidade, intervalos
- Que nos di o dato que non vemos na partitura?

🎯 Aquí péchase a ponte:
Harmonía → Análise → MIR

---

🔄 **Cambio metodolóxico clave (moi importante)**

❌ Antes:

- Crear melodías artificiais
- Usar music21 como xerador

✅ Agora:

- En Bloque II: analizar música real
- Corpus clásico
- Pensamento musicolóxico

A creación queda:

- para Bloque I (conceptual)
- para Proxecto final (opcional)
  ☑️ Ao rematar o Bloque II, o alumnado debería notar que Python “pensa música”: serán capaces de escribir código que compón, transforma e analiza música seguindo regras, do mesmo xeito que faría un músico pero con axuda da automatización. Isto prepara o terreo para, no seguinte bloque, cambiar de perspectiva e abordar o son dixital.
  🟦 BLOQUE III — Audio e son con librosa (Semanas 7–9)
  (Neste bloque mudamos de paradigma: pasamos de tratar co simbólico —notas e partituras— a traballar co son bruto —ondasaúde e audio dixital—.)
  Semana 7 — Audio dixital básico
  Que é un arquivo de audio?: Explícase de forma introductoria que un audio dixital non é máis ca unha serie de mostras (números) que representan unha onda sonora ao longo do tempo. Pódese lembrar brevemente teoría: o son é unha onda de presión no aire, e un arquivo de audio garda esa información convertida a dixital (0 e 1). Distínguese entre formatos sen compresión (WAV, AIFF) e comprimidos (MP3, OGG), e coméntase que para análise e procesamento normalmente usaremos formatos sen perda de calidade.
  Taxa de mostraxe (sampling rate): Introdúcese este concepto clave do audio dixital. A taxa de mostraxe é o número de mostras por segundo que se toman da onda continua para representala en dixital. Por exemplo, 44.100 Hz significa 44.100 mostras cada segundo. Canto maior é a taxa, máis fiel é a reprodución do son (maior rango de frecuencias representables, segundo o Teorema de Nyquist). Para experimentación, usarase normalmente 22050 Hz ou 44100 Hz. Os alumnos deben entender que un audio é basicamente unha lista (ou array) de valores numéricos moi longa.
  Forma de onda: Unha vez cargado un audio, podemos representalo graficamente como unha onda (amplitude no eixo vertical, tempo no eixo horizontal). Empregaremos bibliotecas como NumPy para manexar os datos numéricos e Matplotlib para trazar gráficos. Por exemplo, tras cargar un ficheiro WAV cunha función de librosa (y, sr = librosa.load("ficheiro.wav")), podemos debuxar a forma de onda dese audio. Visualizar a forma de onda axuda a identificar características básicas: zonas de silencio, zonas máis intensas, etc., pero non nos dá información de frecuencia (eso virá co espectrograma).
  Escoitar audio con Python: Amosamos maneiras de reproducir audio directamente dende Python (por exemplo, usando librosa ou outras librarías, ou exportando a WAV e escoitando). Nun contorno como Jupyter Notebook pódese integrar un widget de audio. O importante é que os alumnos poidan escoitar os clips que van cargando ou xerando, para relacionar a percepción auditiva co que ven nos datos.
  Bibliotecas utilizadas: Presentamos as ferramentas principais para este bloque:
  librosa: unha biblioteca de Python para análise de música e audio. Librosa proporciona bloques básicos para crear sistemas de Music Information Retrieval (MIR)
  librosa.org
  , incluíndo funcións para cargar audio, calcular espectrogramas, extraer características como pitch (altura) e ritmo, etc.
  NumPy: para manipulación eficiente de arrays numéricos (onde estarán as mostras do audio).
  Matplotlib: para xeración de gráficos e visualizacións (formas de onda, espectrogramas, etc.).
  Exercicios prácticos desta semana:
  Cargar e visualizar un audio: Usando librosa, cargar un arquivo WAV curto e obter a súa onda de audio. Logo, empregar matplotlib.pyplot para debuxar esa onda. Identificar visualmente partes de maior amplitude (quizais correspondan a partes máis altas en volume) e de menor. Este exercicio ensina a usar a biblioteca e interpreta unha representación básica.
  Comparar duracións de audios: Cargar dous clips de audio distintos e, a partir do tamaño do array ou de parámetros de librosa, obter a duración en segundos de cada un (len(y)/sr). Comparar cal é máis longo e por canto. Isto reforza comprensión de sampling rate e permite practicar operacións numéricas simples.
  Cortar fragmentos dun audio: Tomar un audio e extraer un sub-treito, por exemplo os primeiros 5 segundos ou do segundo 10 ao 15. En Python isto faise troceando o array de mostras (y_sub = y[inicio:fin]). Gardar ese fragmento nun novo arquivo ou reproducilo. Este exercicio afianza o manexo de índices e slicing en arrays, aplicándoo a un contexto real (editar audio). Tamén permite ver que, se cortamos polo medio dunha onda, ao reproducila podemos escoitar un corte brusco (pop/click), o cal serve para discutir brevemente a continuidade da onda.
  Semana 8 — Análise musical do son
  Espectrograma: Introdúcese esta importante ferramenta de análise de audio. Un espectrograma é unha representación visual que amosa como o espectro de frecuencias dun sinal evoluciona co tempo
  en.wikipedia.org
  . En termos sinxelos, é como debuxar moitos espectros (FFT) consecutivos un tras outro: no eixo horizontal está o tempo, no vertical a frecuencia, e mediante cores ou intensidade represéntase a amplitude (potencia) de cada frecuencia nese instante
  en.wikipedia.org
  . Aprenderemos a xerar espectrogramas en Python con librosa (por exemplo empregando librosa.stft para a transformada de Fourier de curto tempo e logo librosa.display.specshow para debuxalo). Tamén se explica a diferenza entre un espectrograma lineal e un mel-spectrogram (aplicando a escala mel para parecerse máis a como escoitamos, comprimindo as frecuencias altas)
  khareanu1612.medium.com
  khareanu1612.medium.com
  . O espectrograma é fundamental porque revela características invisibles na forma de onda: por exemplo, que frecuencias están presentes (timbre, notas, etc.) e cando.

https://commons.wikimedia.org/wiki/File:Spectrogram_of_violin.png
Figura: Espectrograma do son dun violín. As liñas horizontais brillantes corresponden aos harmónicos producidos por este instrumento (frecuencias múltiples da fundamental que definen o seu timbre)
commons.wikimedia.org
. Un espectrograma en xeral represéntase con frecuencia no eixo vertical e tempo no horizontal; a intensidade de cada frecuencia codifícase con distinto brillo ou cor
en.wikipedia.org
. Esta visualización permítenos “ver” a música: por exemplo, nun violín obsérvanse moitas franxas estacionarias (cada nota xera unha fundamental e varios harmónicos constantes), mentres que noutros instrumentos ou sons, os patróns no espectrograma serán diferentes. Analizando espectrogramas podemos distinguir un piano dun violín, ou identificar partes rítmicas (sons curtos e percusivos producen trazos verticais breves, etc.).
Extracción de pitch (altura musical): Discutimos métodos básicos para atopar a altura ou frecuencia predominante nun son a cada instante (é dicir, “que nota está soando”). librosa ofrece funcións como librosa.yin ou librosa.piptrack que implementan algoritmos de detección de pitch. Explicamos que non é trivial: cando hai acordes ou sons complexos, a detección de pitch pode dar varios resultados ou un promedio. Aínda así, pódese probar cun son monofónico (por exemplo gravar un amigo cantando unha nota) e ver se o algoritmo atopa correctamente a frecuencia fundamental (que se convertería en Hz e incluso se podería mapear a unha nota MIDI). Este apartado conecta coa teoría de física do son (frecuencia fundamental vs. harmónicos) e coa percepción (altura percibida).
Detección de tempo e ritmo: Mostramos como un algoritmo pode estimar o tempo (BPM) dunha grabación de audio. librosa ten librosa.beat.beat_track ou librosa.tempo que poden devolver unha estimación de pulsacións por minuto analizando o patrón de enerxía no tempo. Tamén se introduce o concepto de detección de onsets (ataques): identificar automaticamente cando comeza unha nota ou golpe de percusión nunha sinal (p. ex. librosa.onset.onset_detect). Para facelo, a técnica común é calcular unha función de enerxía ou novidade spectral e atopar picos. Os alumnos poden experimentar con algunha percusión simple (unha palmada, un ritmo de batería) e ver se o código marca correctamente os comezos de cada golpe. Estes procedementos son cruciais en áreas como a sincronización audio-partitura ou transcrición automática.
Exercicios prácticos desta semana:
Detectar o BPM dunha canción: Tomar un arquivo de audio musical (idealmente música con compás marcado, como pop ou electrónica) e usar librosa para estimar os seus BPM. Logo comparar ese valor co que o alumno poida contar manualmente escoitando. Por exemplo, o programa podería devolver ~128 BPM para un tema de dance. Se hai discrepancias, discutir por que (ritmo complexo, half-time feeling, etc.).
Comparar espectros de distintos instrumentos: Coller breves mostras sonoras de distintos instrumentos tocando a mesma nota (p.ex. un La440 de violín, piano, frauta) e xerar os espectrogramas ou simplemente os espectros medios. Observar como un piano ten moita enerxía inicial que decae rápido, un violín sustén máis o son e mostra harmónicos máis definidos, etc. Este exercicio visualiza claramente a noción de timbre e fai entender por que soan distinto dous instrumentos aun que fagan a mesma nota.
Comparar dúas interpretacións: Se se dispón de dúas gravacións diferentes dunha mesma peza (p.ex. dous pianistas tocando unha obra breve), propoñemos cargalas e medir diferenzas. Poden compararse os tempos (unha versión máis rápida ca outra, facilmente medible en duración total ou mediante a detección de pulsos e onsets para ver variacións de tempo). Tamén se poden comparar dinámicas: por exemplo calculando a enerxía RMS ao longo do tempo e vendo cal ten contrastes máis fortes. A idea é que o alumnado vexa cuantificado o que doutro xeito percibiría de oído: “esta interpretación é máis expresiva que esta outra” pode reflectirse en datos obxectivos.
Semana 9 — Música, percepción e datos
Timbre e características de audio: Profúndase no concepto de timbre, que é o conxunto de características que fan que unha fonte de son teña unha cor determinada (é o que nos permite distinguir a voz dunha persoa ou un instrumento doutro, máis aló da altura ou volume). Explicamos que o timbre está ligado á presenza de determinados harmónicos e ás envolventes de son (ataque, decaemento, etc.). A nivel de computación, introduce-se a idea de características de audio (audio features): por exemplo, o espectro ou centroide espectral (que indica se o son é brillante ou oscuro en promedio
khareanu1612.medium.com
), o RMS ou potencia media (relacionado coa intensidade/volume), ou os MFCCs (coeficientes cepstrais, que son unha representación estándar do timbre usada en recoñecemento de voz e música). Sen entrar no detalle matemático, pódese ensinar a calcular algunhas destas características coas funcións de librosa e interpretar os resultados. Por exemplo, calcular o centroide espectral ao longo do tempo e superpoñelo sobre un espectrograma para ver como unha sección con violíns ten centroides máis altos (máis agudos) ca unha sección con contrabaixos.
Enerxía e dinámica: Relacionado co anterior, examínase como representar a enerxía dun audio. Unha medida simple é a enerxía RMS (raíz cadrada da media dos cadrados das amplitudes) ao longo do tempo. Isto básicamente dá un contorno de volume. Podemos extraer a curva de volume dunha canción e ver, por exemplo, a forma global (intro suave, crecendo ata o refrán, etc.). Os alumnos poden practicar normalizar audios (facer que o volume máximo sexa un certo nivel) modificando esa enerxía, ou detectar cando hai silencios (enerxía por debaixo dun umbral). Todo isto son operacións comúns no procesado de audio.
Comparación de audios e “fingerprinting”: Como colofón, preséntase o concepto de identificación de audio e comparación automática. Por exemplo, Shazam e apps similares crean un “fingerprint” (pegada) única de cada canción baseada en características do seu espectro e tempo. Sen implementar nada tan avanzado, podemos facernos unha idea creando vectores de características sinxelas para distintos audios e medindo distancias. Un exercicio divertido é intentar que o programa distingua entre dous estilos ou intérpretes: por exemplo, cargar 5 seg. dun tema rock e 5 seg. dun tema clásico, extraer 2-3 atributos (BPM, brillo, presenza de frecuencias graves) e ver se realmente son moi diferentes numéricamente. Isto introduce moi superficialmente a noción de clasificación mediante características, tópico central do MIR (Music Information Retrieval). De feito, MIR é o campo que combina música, informática e procesamento de sinal para extraer información útil de sinais musicais
proceedings.scipy.org
– vai dende recoñecer xéneros musicais ata converter tarareos en partituras.
Exercicios propostos:
Clasificar sons: O alumnado recibe unha colección pequena de sons (por exemplo, catro mostras: unha de piano, unha de percusión, unha de sintetizador, unha de voz). Teñen que idear algún criterio cuantitativo para distinguilos. Por exemplo, sons de percusión terán centroides espectrais altos pero duracións curtas; a voz humana terá un espectro con formantes definidos; un sintetizador de baixo terá moita enerxía en frecuencias graves, etc. Usando librosa, que calculen eses parámetros e fagan unha predición de cal é cal antes de escoitalos, logo comproben escoitando. Isto simula un sistema de clasificación automático a pequenísima escala.
Huellas sonoras de obras: Escoller dúas cancións moi diferentes (por ex., unha nana e un tema de rock) e representar unha “huella” simple de cada unha: por exemplo, unha gráfica do espectro medio e da evolución de volume. Comparalas e describir en termos de data science as diferencias. A “pegada sonora” refírese a captar aqueles atributos cuantificables que individualizan unha peza. Os alumnos poden tentar visualizar dúas pegadas e mesmo mesturar audios (que pasa se collemos o ritmo dunha e o espectro doutra?). Este exercicio reforza creatividade e aplicación práctica de todos os conceptos de audio vistos.
🎧 Reflexión: Tras estes tres meses de curso (bloques I–III), o alumnado terá tocado tanto a partitura como o audio. Unha hora á semana é pouco tempo, pero combinando teoría e práctica logramos unha panorámica da Computación Musical: dende escribir un canon ata ler espectros. O seguinte paso será aplicar e profundar nestes coñecementos nun proxecto propio.
🟦 BLOQUE IV — Proxecto final (Semanas 10–12)
🎯 Obxectivo
Integrar todo o aprendido nun proxecto creativo ou analítico desenvolvido polo propio estudante. Este proxecto servirá para que cada alumno/a explore o aspecto da programación musical que máis lle interese (composición, análise, procesamento de son, etc.) e para consolidar as súas habilidades resolvendo un problema máis aberto de principio a fin.
Tipos de proxecto (a elixir)
🎼 Opción A — Proxecto de música simbólica: Enfocado a composición e teoría musical usando music21. Por exemplo: desenvolver un xenerador musical que cree melodías ou pequenas pezas seguindo certas pautas (aleatorias ou baseadas nun estilo); realizar o análise dunha obra existente empregando código (obter estatísticas, identificar motivos, etc. dunha partitura famosa); implementar un sistema de variacións onde, dada unha melodía de entrada, o programa xera variacións automáticamente (cambiando ritmo, ton, invertendo, etc.); ou incluso experimentar con composición algorítmica completa (usar regras matemáticas ou algorítmicas – como L-systems, turinas, etc. – para compoñer música). A creatividade é o límite, sempre traballando sobre representacións simbólicas (notas, partituras). 🎧 Opción B — Proxecto de audio e son: Centrado en análise de gravacións ou sons co aprendido de librosa. Pódese abordar, por exemplo, a análise de gravacións musicais: estudar en profundidade un par de audios (quizais do mesmo tema) e extraer conclusións sobre interpretación, calidade de son, etc.; ou facer unha comparación de intérpretes: escribir código que, dado dúas interpretacións distintas dunha peza, compare o tempo, a afinación ou incluso detecte que diferencias de dinámica existen; tamén cabe un estudo de tempo ou afinación ao longo dunha interpretación (por exemplo, ver como un cantante pode desafinar nalgunhas notas comparando a frecuencia real coa teórica, ou como un baterista acelera/ralentiza respecto ao BPM ideal). Estes proxectos permiten aplicar o análise de sinal a casos do mundo real que resulten interesantes para o alumnado músico. 🤖 Opción C — Exploración avanzada (mistura ou novos métodos): Para alumnos con maior curiosidade técnica, proponse proxectos máis experimentais. Por exemplo, un sistema de clasificación simple de xéneros ou de instrumentos: adestrar (a moi pequena escala) un clasificador que dada unha audio adiviñe se é rock ou clásica, ou que instrumento soa, empregando algúns features básicos e un algoritmo de machine learning sinxelo. Outro posible é preparar datos para intelixencia artificial musical: por exemplo, escribir un script que extraia loops de batería dun conxunto de cancións, ou converter un corpus de MIDI en formato entrenable (JSON, CSV de características, etc.). Tamén se podería investigar a conexión con ferramentas de live coding (como FoxDot ou Sonic Pi), facendo que Python envíe información musical en tempo real. Estas opcións permiten albiscar temas de vangarda na tecnoloxía musical.
Avaliación suxerida
Para avaliar este trimestre mantemos un equilibrio entre o traballo continuo e o final:
30% dos exercicios semanais e tarefas curtas de cada bloque. (Valórase a constancia, a entrega puntual e a corrección dos resultados semana a semana).
30% por mini-proxectos ou traballos parciais (por exemplo, pequenos retos nas semanas 4, 6 e 9 que integran varias habilidades).
40% o proxecto final completo. Inclúe tanto o produto (código e resultado musical) coma a memoria ou presentación que o acompaña.
É importante aclarar que se valorará moito o proceso, non só o resultado final. É dicir, ter boas prácticas de código, facer probas intermedias, mostrar creatividade e aprendizaxe dos erros contará positivamente, incluso se o proxecto ten limitacións no seu resultado musical ou técnico.
🧠 Metodoloxía recomendada
Usar intensivamente contornas de notebook (como Jupyter): permiten combinar explicación, código e resultados (gráficos, música) no mesmo documento. Isto facilita que o alumnado experimente cambiando o código e vexa inmediatamente o efecto.
Escribir código curto e modular: fomentar funcións breves para cada tarefa musical (por exemplo, unha función que dada unha lista de notas as transpoña). Así evítanse longos scripts difíciles de depurar e enténdese mellor a estrutura musical do programa.
Escoitar sempre o que se xera: cada vez que se cree unha melodía ou se modifique un audio, recoméndase reproducilo (coa ferramenta que corresponda) para comprobar que efectivamente soa como se espera. A conexión oído-código é fundamental nesta materia artística.
Comparar co música real: animar a que, se se xera unha partitura, se abra en MuseScore e se mire como queda escrita; ou se se analiza unha canción, que tamén a teñan en partitura ou polo menos a escoiten orixinal. Isto reforza a ponte entre o abstracto (código/datos) e o real (execución musical).
Manter unha relación constante coa teoría musical: cada concepto de programación introdúcese apoiado nun concepto musical equivalente, e viceversa. Por exemplo, ao falar de bucles, lembrar a forma rondó con seus refráns; ao tratar arrays de audio, comentar a física do son. Deste xeito, a aprendizaxe de Python contextualízase e cobra sentido para o músico, e á vez a teoría musical enriquécese con novas ferramentas.
