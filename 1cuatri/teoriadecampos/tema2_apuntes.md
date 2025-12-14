# Tema 2: Las Leyes de Newton - Apuntes Completos

## 📚 Resumen de la Teoría

### 1. Concepto de Inercia

La **inercia** es la tendencia de un cuerpo a mantener su estado de movimiento (reposo o movimiento rectilíneo uniforme) en ausencia de fuerzas externas.

**Definición:** La inercia es la propiedad de un cuerpo que determina su resistencia a cambiar su estado de movimiento.

### 2. Sistemas de Referencia

#### Sistemas de Referencia Inerciales
Un **sistema de referencia inercial** es aquel en el que un cuerpo libre de fuerzas permanece en reposo o en movimiento rectilíneo uniforme.

**Características:**
- Las leyes de Newton solo se cumplen en sistemas inerciales
- A distancias suficientemente grandes de otros cuerpos, tenemos un sistema inercial
- Un cuerpo en caída libre también está (localmente) en un sistema inercial

### 3. El Concepto de Fuerza

Una **fuerza** es toda acción capaz de modificar el estado de movimiento de un cuerpo o deformarlo.

#### Ley de Hooke
Para un muelle, la fuerza es proporcional a la elongación:

```
F = -kx
```

Donde:
- `F` = fuerza (N)
- `k` = constante elástica (N/m)
- `x` = elongación (m)

### 4. Las Tres Leyes de Newton

#### Primera Ley (Ley de Inercia)
**Si sobre un cuerpo no actúan fuerzas o la suma de todas las fuerzas es cero, el cuerpo permanecerá en reposo o en movimiento rectilíneo uniforme.**

```
ΣF = 0  ⟹  v = constante
```

#### Segunda Ley (Ley Fundamental de la Dinámica)
**La fuerza o suma de fuerzas que actúan sobre un cuerpo es proporcional a la aceleración, siendo la constante de proporcionalidad la masa:**

```
ΣF = m·a = m·(d²r/dt²)
```

**Aspectos importantes:**
- La fuerza solo depende de la segunda derivada de la posición
- Es una ecuación diferencial de segundo orden
- Necesita dos condiciones iniciales: posición y velocidad

#### Tercera Ley (Acción y Reacción)
**Si un cuerpo A ejerce una fuerza sobre un cuerpo B, entonces B ejerce sobre A una fuerza de igual magnitud y dirección pero sentido contrario:**

```
F_AB = -F_BA
```

**Características:**
- Las fuerzas actúan sobre cuerpos diferentes
- Son simultáneas
- Tienen la misma naturaleza

### 5. Momento Lineal o Cantidad de Movimiento

**Definición:** El momento lineal es el producto de la masa por la velocidad:

```
p = m·v
```

**Unidades:** kg·m/s

**Conservación:** En ausencia de fuerzas externas, el momento lineal se conserve:

```
Si ΣF_ext = 0  ⟹  p = constante
```

La segunda ley de Newton se puede expresar como:

```
F = dp/dt
```

### 6. Impulso y Trabajo

#### Impulso
El **impulso** es la integral temporal de la fuerza:

```
I = ∫F dt = Δp
```

Para fuerza constante:
```
I = F·Δt = Δp
```

#### Trabajo
El **trabajo** es el producto escalar de la fuerza por el desplazamiento:

```
dW = F·dr

W = ∫(1→2) F·dr
```

**Unidades:** Joule (J) = N·m

### 7. La Energía

#### Energía Cinética
**Definición:** Energía asociada al movimiento:

```
T = (1/2)·m·v²
```

**Teorema del Trabajo y la Energía:**
```
W = ΔT = (1/2)·m·v₂² - (1/2)·m·v₁²
```

#### Energía Potencial
Energía que está "almacenada" en función de la posición.

Para un campo gravitatorio uniforme:
```
V = m·g·h
```

#### Energía Mecánica
La suma de energía cinética y potencial se conserva:

```
E = T + V = constante

(1/2)·m·v₁² + m·g·h₁ = (1/2)·m·v₂² + m·g·h₂
```

### 8. Momento Angular

**Definición:** Producto vectorial del vector posición por el momento lineal:

```
L = r × p = r × (m·v)
```

**Momento de una fuerza (par motor):**
```
N = r × F
```

**Ecuación del movimiento angular:**
```
dL/dt = N
```

**Conservación:** Si el momento de las fuerzas es cero, el momento angular se conserva.

### 9. Principio de Relatividad de Galileo

**Enunciado:** Las leyes de Newton son las mismas en todos los sistemas de referencia inerciales.

**Transformaciones de Galileo:**
```
r' = r - V·t
v' = v - V
a' = a
```

Donde `V` es la velocidad relativa entre los sistemas.

### 10. El Peso

El **peso** es la fuerza con que la Tierra atrae a un cuerpo:

```
P = m·g
```

Donde:
- `g` ≈ 9.8 m/s² (aceleración de la gravedad)

**Importante:** La masa pesante y la masa inercial son iguales (Principio de Equivalencia).

### 11. Sistemas de Referencia No Inerciales

En sistemas no inerciales aparecen **fuerzas ficticias**:

#### Fuerza Centrífuga
```
F_centrífuga = m·ω²·r
```

Donde:
- `ω` = velocidad angular
- `r` = distancia al eje de rotación

#### Fuerza de Coriolis
```
F_Coriolis = -2m·(ω × v)
```

**Ejemplos:**
- Desviación de proyectiles en la Tierra
- Formación de ciclones y anticiclones
- Péndulo de Foucault

---

## 💡 Aplicaciones Importantes de las Leyes de Newton

### 1. Caída Libre

En ausencia de resistencia del aire y con campo gravitatorio uniforme:

**Ecuaciones del movimiento:**
```
v(t) = v₀ - g·t
z(t) = h + v₀·t - (1/2)·g·t²
v²(z) = v₀² - 2g(z - h)
```

### 2. Tiro Parabólico

**Componentes del movimiento:**
- Horizontal: MRU (movimiento rectilíneo uniforme)
- Vertical: MRUA (movimiento rectilíneo uniformemente acelerado)

**Ecuaciones:**
```
x(t) = v₀·cos(α)·t
y(t) = v₀·sin(α)·t - (1/2)·g·t²
```

**Alcance máximo:**
```
R = (v₀²·sin(2α))/g
```

El alcance es máximo cuando α = 45°.

### 3. Movimiento con Resistencia del Aire

#### Resistencia proporcional a la velocidad
```
F_resistencia = -k·v
```

**Velocidad límite:**
```
v_L = m·g/k
```

**Ecuaciones:**
```
v(t) = (v₀ + g/k)·e^(-kt) - g/k
```

#### Resistencia proporcional al cuadrado de la velocidad
```
F_resistencia = -k·v²
```

**Velocidad límite:**
```
v_L = √(m·g/k)
```

---

## 📝 Ejercicios Resueltos Paso a Paso

### Ejercicio 1: Momento Lineal y Fuerza de Frenado

**Enunciado:** Calcular la cantidad de movimiento o momento lineal de un automóvil de 1 t de peso que circula a una velocidad de 144 km/h. Si frena bruscamente, deteniéndose en 100 m, calcular la fuerza de frenado.

**Solución paso a paso:**

#### Paso 1: Identificar los datos
- Masa: m = 1 t = 1000 kg
- Velocidad: v = 144 km/h
- Distancia de frenado: d = 100 m

#### Paso 2: Convertir unidades
```
v = 144 km/h × (1000 m/1 km) × (1 h/3600 s) = 40 m/s
```

#### Paso 3: Calcular el momento lineal
```
p = m·v = 1000 kg × 40 m/s = 40000 kg·m/s = 4×10⁴ kg·m/s
```

#### Paso 4: Calcular la aceleración de frenado
Usamos la ecuación cinemática: v² = v₀² + 2a·d

En el frenado final: v = 0
```
0 = (40)² + 2·a·100
0 = 1600 + 200a
a = -1600/200 = -8 m/s²
```

#### Paso 5: Calcular la fuerza de frenado
```
F = m·a = 1000 kg × (-8 m/s²) = -8000 N
```

El módulo de la fuerza es **8000 N** (en sentido contrario al movimiento).

**Respuesta:** p = 4×10⁴ kg·m/s; F = 8000 N

---

### Ejercicio 2: Tiempo de Parada con Fuerza Constante

**Enunciado:** El momento lineal de una partícula cuya masa es de 30 kg es de 150 N·s. Si se le aplica una fuerza de 60 N en sentido contrario a su movimiento, calcular el tiempo que tardará en pararse.

**Solución paso a paso:**

#### Paso 1: Identificar los datos
- Masa: m = 30 kg
- Momento lineal inicial: p₀ = 150 kg·m/s (N·s = kg·m/s)
- Fuerza: F = -60 N (negativa por ser contraria al movimiento)
- Momento lineal final: p_f = 0 (se para)

#### Paso 2: Calcular la velocidad inicial
```
p₀ = m·v₀
v₀ = p₀/m = 150/30 = 5 m/s
```

#### Paso 3: Aplicar el teorema del impulso
El impulso es igual a la variación del momento lineal:
```
F·Δt = Δp = p_f - p₀
-60·Δt = 0 - 150
-60·Δt = -150
Δt = 150/60 = 2.5 s
```

**Respuesta:** t = 2.5 s

---

### Ejercicio 3: Bombardero - Tiro Parabólico

**Enunciado:** Un bombardero vuela a una velocidad de 972 km/h a una altura de 1 km. Calcular desde qué distancia ha de soltar una carga explosiva para que alcance un objetivo en tierra.

**Solución paso a paso:**

#### Paso 1: Identificar los datos y convertir unidades
- Altura: h = 1 km = 1000 m
- Velocidad horizontal: v₀ = 972 km/h = 972/3.6 = 270 m/s
- Velocidad vertical inicial: v_y0 = 0 (vuelo horizontal)

#### Paso 2: Calcular el tiempo de caída
La carga cae con movimiento de caída libre vertical:
```
y = h - (1/2)·g·t²

Cuando llega al suelo: y = 0
0 = 1000 - (1/2)·9.8·t²
(1/2)·9.8·t² = 1000
t² = 2000/9.8 = 204.08
t = √204.08 = 14.29 s
```

#### Paso 3: Calcular la distancia horizontal
Durante la caída, la componente horizontal de la velocidad se mantiene constante:
```
x = v₀·t = 270 m/s × 14.29 s = 3858.3 m ≈ 3857 m
```

**Respuesta:** Distancia = 3857 m (o 3.857 km)

**Explicación física:** La bomba debe soltarse 3.857 km antes del objetivo porque mientras cae verticalmente durante 14.29 segundos, sigue avanzando horizontalmente a la velocidad del avión.

---

### Ejercicio 4: Máquina de Atwood

**Enunciado:** Las masas que penden de la cuerda de una máquina de Atwood (supuesta inextensible y sin peso) son 505 g y 495 g. Se supone que la polea tiene masa despreciable. Calcular la velocidad de la masa mayor al haber efectuado un recorrido de 1 m.

**Solución paso a paso:**

#### Paso 1: Identificar los datos
- Masa mayor: m₁ = 505 g = 0.505 kg
- Masa menor: m₂ = 495 g = 0.495 kg
- Distancia recorrida: d = 1 m
- Velocidad inicial: v₀ = 0

#### Paso 2: Diagrama de fuerzas y ecuaciones de movimiento
Para m₁ (desciende): m₁·a = m₁·g - T
Para m₂ (asciende): m₂·a = T - m₂·g

Donde T es la tensión de la cuerda y a es la aceleración (igual para ambas masas).

#### Paso 3: Calcular la aceleración
Sumando ambas ecuaciones:
```
m₁·a + m₂·a = m₁·g - m₂·g
a(m₁ + m₂) = g(m₁ - m₂)
a = g·(m₁ - m₂)/(m₁ + m₂)
a = 9.8 × (0.505 - 0.495)/(0.505 + 0.495)
a = 9.8 × 0.010/1.000 = 0.098 m/s²
```

#### Paso 4: Calcular la velocidad final
Usamos la ecuación cinemática: v² = v₀² + 2·a·d
```
v² = 0 + 2 × 0.098 × 1
v² = 0.196
v = √0.196 = 0.4427 m/s ≈ 0.44 m/s
```

**Respuesta:** v = 0.44 m/s

**Nota:** La diferencia de masas es muy pequeña (solo 10 g), por eso la aceleración es muy pequeña comparada con g.

---

### Ejercicio 5: Velocidad Orbital

**Enunciado:** Suponiendo la Tierra esférica y sin relieve, calcular la velocidad a la que debe ser lanzado un proyectil, horizontalmente y desde la cercanía de la superficie, para ponerlo en órbita, es decir, para que dé vueltas en torno a la Tierra. Dato: radio terrestre R₀ = 6370 km.

**Solución paso a paso:**

#### Paso 1: Identificar el concepto
Para que un objeto esté en órbita circular, la fuerza centrípeta debe ser igual a la fuerza gravitatoria:

```
F_centrípeta = F_gravitatoria
m·v²/R = m·g
```

#### Paso 2: Simplificar y despejar v
La masa se cancela:
```
v²/R = g
v² = g·R
v = √(g·R)
```

#### Paso 3: Sustituir valores
```
R = 6370 km = 6.37 × 10⁶ m
g = 9.8 m/s²

v = √(9.8 × 6.37 × 10⁶)
v = √(6.2426 × 10⁷)
v = 7901.3 m/s
```

#### Paso 4: Convertir a km/h
```
v = 7901.3 m/s × (3600 s/h) / (1000 m/km)
v = 7901.3 × 3.6 = 28444.7 km/h ≈ 28444 km/h
```

**Respuesta:** v = 28444 km/h (aproximadamente 7.9 km/s)

**Nota:** Esta es la velocidad orbital mínima, también conocida como "primera velocidad cósmica".

---

### Ejercicio 6: Aceleraciones Centrífugas

**Enunciado:** Calcular:
a) La aceleración centrífuga debido a la rotación de la Tierra en torno a su eje en un punto del ecuador (R_T = 6370 km)
b) La aceleración centrífuga debido al movimiento de rotación de la Tierra en torno al Sol (R = 1.5 × 10⁸ km)

**Solución paso a paso:**

#### Parte a) Rotación de la Tierra sobre su eje

**Paso 1: Calcular la velocidad angular**
La Tierra da una vuelta completa en 24 horas:
```
ω = 2π/T = 2π/(24 × 3600) = 2π/86400
ω = 7.272 × 10⁻⁵ rad/s
```

**Paso 2: Calcular la aceleración centrífuga**
```
a_c = ω²·R

R = 6370 km = 6.37 × 10⁶ m

a_c = (7.272 × 10⁻⁵)² × 6.37 × 10⁶
a_c = 5.288 × 10⁻⁹ × 6.37 × 10⁶
a_c = 0.0337 m/s²
```

#### Parte b) Traslación de la Tierra alrededor del Sol

**Paso 1: Calcular la velocidad angular**
La Tierra da una vuelta alrededor del Sol en 365.25 días:
```
T = 365.25 × 24 × 3600 = 31557600 s

ω = 2π/T = 2π/31557600
ω = 1.991 × 10⁻⁷ rad/s
```

**Paso 2: Calcular la aceleración centrífuga**
```
R = 1.5 × 10⁸ km = 1.5 × 10¹¹ m

a_c = ω²·R
a_c = (1.991 × 10⁻⁷)² × 1.5 × 10¹¹
a_c = 3.964 × 10⁻¹⁴ × 1.5 × 10¹¹
a_c = 0.00595 m/s² ≈ 0.0060 m/s²
```

**Respuestas:** 
- a) 0.0337 m/s² (rotación terrestre)
- b) 0.0060 m/s² (traslación alrededor del Sol)

**Observación:** Estas aceleraciones son muy pequeñas comparadas con g = 9.8 m/s². La primera representa aproximadamente 0.34% de g, por eso el peso es ligeramente menor en el ecuador que en los polos.

---

### Ejercicio 7: Fuerza de Coriolis en un Avión

**Enunciado:** Sea un avión que vuela a 800 km/h en dirección este, a lo largo de un paralelo, a 45° de latitud. Calcular, en módulo, la aceleración lateral que experimentará.

**Solución paso a paso:**

#### Paso 1: Identificar los datos
- Velocidad del avión: v = 800 km/h = 800/3.6 = 222.22 m/s
- Latitud: λ = 45°
- Dirección: Este (paralelo)
- Velocidad angular de la Tierra: ω = 7.272 × 10⁻⁵ rad/s (del ejercicio anterior)

#### Paso 2: Fórmula de la aceleración de Coriolis
La aceleración de Coriolis es:
```
a_Coriolis = 2·ω·v·sin(λ)
```

Para un movimiento hacia el este a lo largo de un paralelo a latitud λ, la componente vertical de ω que contribuye es ω·sin(λ).

#### Paso 3: Calcular la aceleración
```
a_c = 2 × ω × v × sin(45°)
a_c = 2 × 7.272 × 10⁻⁵ × 222.22 × sin(45°)
a_c = 2 × 7.272 × 10⁻⁵ × 222.22 × 0.7071
a_c = 0.0228 m/s² ≈ 0.023 m/s²
```

**Respuesta:** a = 0.023 m/s²

**Interpretación física:** Esta aceleración lateral hacia el sur (en el hemisferio norte) es la que siente el avión debido a la rotación de la Tierra. Aunque es pequeña (0.23% de g), debe ser tenida en cuenta en vuelos largos para correcciones de navegación.

---

## 🎯 Estrategias para el Examen

### Basado en el Análisis de Exámenes Anteriores

#### 1. Tipos de Preguntas de Teoría Frecuentes

**a) Campos Conservativos**
- Condiciones que deben cumplir
- Ejemplos (gravitatorio, eléctrico)
- Relación con energía potencial

**b) Momento Angular**
- Ecuación de movimiento para sistemas de partículas
- Tercera ley de Newton (versión fuerte)
- Conservación del momento angular

**c) Relatividad Especial**
- Postulados
- Consecuencias (dilatación temporal, contracción de longitud)
- Efectos relativistas

#### 2. Tipos de Problemas Frecuentes

**a) Tiro Parabólico / Balística**
- Altura máxima
- Tiempo de vuelo
- Alcance horizontal
- Estrategia: Descomponer en movimiento horizontal (MRU) y vertical (MRUA)

**b) Cohetes / Propulsión**
- Ecuación de Tsiolkovsky
- Velocidad máxima
- Efectos de fuerzas externas (gravedad)
- Estrategia: Conservación del momento lineal

**c) Sistemas de Referencia No Inerciales**
- Fuerzas ficticias (centrífuga, Coriolis)
- Desviaciones en la Tierra
- Estrategia: Identificar sistema de referencia y añadir fuerzas ficticias

#### 3. Consejos Prácticos para el Examen

##### ✅ Preparación
1. **Dominar las ecuaciones fundamentales:**
   - Tres leyes de Newton
   - Conservación de momento lineal
   - Conservación de energía
   - Trabajo y energía

2. **Practicar conversión de unidades:**
   - km/h ↔ m/s (dividir/multiplicar por 3.6)
   - Masas, fuerzas, energías

3. **Memorizar valores importantes:**
   - g = 9.8 m/s² ≈ 10 m/s²
   - Radio terrestre: R_T ≈ 6370 km
   - Velocidad angular Tierra: ω ≈ 7.27 × 10⁻⁵ rad/s

##### ✅ Durante el Examen

1. **Para problemas de dinámica:**
   - Dibuja un diagrama de cuerpo libre
   - Identifica todas las fuerzas
   - Escribe F = ma para cada dirección
   - Resuelve el sistema de ecuaciones

2. **Para tiro parabólico:**
   - Separa componentes horizontal y vertical
   - Horizontal: x = v₀·cos(α)·t
   - Vertical: y = v₀·sin(α)·t - ½gt²

3. **Para energía:**
   - Identifica estado inicial y final
   - Aplica conservación de energía: E₁ = E₂
   - T₁ + V₁ = T₂ + V₂

4. **Para sistemas no inerciales:**
   - Identifica el sistema de referencia
   - Añade fuerzas ficticias si es no inercial
   - Aplica F = ma en ese sistema

##### ✅ Errores Comunes a Evitar

1. **No convertir unidades** antes de calcular
2. **Olvidar el signo** en fuerzas de resistencia (son opuestas al movimiento)
3. **Confundir masa y peso** (P = m·g)
4. **No usar vectores** cuando es necesario
5. **Olvidar condiciones iniciales** en problemas de cinemática
6. **No verificar** si las respuestas tienen sentido físico

##### ✅ Gestión del Tiempo

1. Lee todo el examen primero (5 min)
2. Responde primero lo que sabes seguro (30 min)
3. Aborda los problemas complejos (40 min)
4. Revisa cálculos y unidades (15 min)

---

## 📖 Conceptos Clave para Recordar

### Fórmulas Esenciales

```
Segunda Ley de Newton:        F = m·a = dp/dt
Momento lineal:               p = m·v
Trabajo:                      W = ∫F·dr
Energía cinética:             T = ½·m·v²
Energía potencial (gravedad): V = m·g·h
Momento angular:              L = r × p
Fuerza centrípeta:            F_c = m·v²/r = m·ω²·r
Fuerza de Coriolis:           F_Cor = -2m·(ω × v)
```

### Principios de Conservación

1. **Momento lineal:** Se conserva si ΣF_ext = 0
2. **Energía mecánica:** Se conserva si solo actúan fuerzas conservativas
3. **Momento angular:** Se conserva si ΣN_ext = 0

### Relaciones Importantes

- Impulso = Variación del momento: I = Δp
- Trabajo = Variación de energía cinética: W = ΔT
- Para fuerzas conservativas: F = -∇V

---

## 🔍 Problemas Tipo Adicionales

### Problema Extra: Péndulo Simple

Un péndulo de longitud L = 2 m se suelta desde un ángulo de 30° con la vertical. Calcular la velocidad en el punto más bajo.

**Solución usando conservación de energía:**

```
Altura inicial: h = L - L·cos(30°) = L(1 - cos(30°))
h = 2(1 - 0.866) = 0.268 m

Energía inicial = Energía final:
m·g·h = ½·m·v²

v = √(2gh) = √(2 × 9.8 × 0.268)
v = √5.25 = 2.29 m/s
```

### Problema Extra: Plano Inclinado con Rozamiento

Un bloque de masa m = 5 kg se desliza por un plano inclinado 30° con coeficiente de rozamiento μ = 0.2. Calcular la aceleración.

**Solución:**

```
Fuerzas paralelas al plano:
F_paralela = m·g·sin(30°) - f_rozamiento
F_paralela = m·g·sin(30°) - μ·m·g·cos(30°)

a = g·(sin(30°) - μ·cos(30°))
a = 9.8·(0.5 - 0.2 × 0.866)
a = 9.8·(0.5 - 0.173)
a = 9.8 × 0.327 = 3.20 m/s²
```

---

## 📚 Bibliografía y Referencias

- Espinosa, P. C. (2015). Dispositivos y experiencias sencillas para explicar el principio de acción y reacción.
- Franco, J. E. C., et al. (2007). Principio de la conservación de la energía mecánica en caída libre.
- Garde, E. A. & López, V. S. (1992). La estructura de las leyes de Newton: un enfoque alternativo.
- Vila, J. & Sierra, C. (2008). Explicación con experimentos sencillos de la primera ley de Newton.

---

## 📝 Notas Finales

### Consejos del Profesor

1. **Practica, practica, practica:** La física se aprende resolviendo problemas
2. **Entiende, no memorices:** Comprende los conceptos físicos detrás de las ecuaciones
3. **Dibuja diagramas:** Un buen diagrama es la mitad de la solución
4. **Verifica dimensiones:** Las unidades deben ser consistentes
5. **Piensa en casos límite:** ¿Tiene sentido tu respuesta en situaciones extremas?

### Para Profundizar

- Estudia el oscilador armónico (Tema siguiente)
- Problema de los dos cuerpos (gravitación)
- Sistemas de muchas partículas
- Centro de masas y su movimiento
- Choques elásticos e inelásticos

---

**¡Mucho éxito en tu estudio del Tema 2!** 🚀

Recuerda: Las Leyes de Newton son la base de toda la mecánica clásica. Dominarlas bien te facilitará enormemente el resto de la física.
