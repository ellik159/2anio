# Tema 5: Teoría de la Relatividad Especial

## 📚 Índice

1. [Resumen de Teoría](#resumen-de-teoría)
   - [Experimento de Michelson-Morley](#experimento-de-michelson-morley)
   - [Postulados de la Relatividad Especial](#postulados-de-la-relatividad-especial)
   - [Transformaciones de Lorentz](#transformaciones-de-lorentz)
   - [Efectos Relativistas](#efectos-relativistas)
   - [Composición de Velocidades](#composición-de-velocidades)
   - [Efecto Doppler Relativista](#efecto-doppler-relativista)
2. [Ejercicios Resueltos](#ejercicios-resueltos)
3. [Estrategias para el Examen](#estrategias-para-el-examen)

---

## Resumen de Teoría

### 🔬 Experimento de Michelson-Morley

**Contexto histórico:**
Durante el siglo XIX, se creía en la existencia del **éter**, un medio hipotético a través del cual se propagaban las ondas electromagnéticas (incluida la luz).

**El experimento:**
- Michelson y Morley diseñaron un experimento para medir la velocidad de la luz en direcciones perpendiculares.
- Usaron un interferómetro con dos brazos perpendiculares de longitud `l`.
- La luz se propagaba por ambos brazos y se medía la diferencia de tiempos.

**Cálculos importantes:**

Para el brazo horizontal (paralelo al movimiento de la Tierra):
```
t₁ = l/(c-v) + l/(c+v) = 2cl/(c²-v²) = (2l/c) · 1/(1-v²/c²)
```

Para el brazo vertical (perpendicular):
```
t₂ = (2l/c) · 1/√(1-v²/c²)
```

Diferencia de tiempos (aproximación para v << c):
```
Δt ≈ lv²/c³
```

Esta aproximación se obtiene expandiendo en serie de Taylor las expresiones anteriores y despreciando potencias superiores a v²/c², dado que v/c ≈ 10⁻⁴ para la Tierra.

**Resultado sorprendente:**
- ¡La diferencia de tiempos fue **CERO**!
- La luz se propagaba con la **misma velocidad** en ambas direcciones.
- Esto descartó la hipótesis del éter.

**Consecuencias:**
- Abandono del concepto de éter
- La velocidad de la luz es independiente del movimiento de la fuente o del observador

---

### 📐 Postulados de la Relatividad Especial

Einstein formuló su teoría basándose en dos postulados fundamentales:

#### **Postulado 1: Principio de Relatividad**
> *Todas las leyes físicas (no solo las mecánicas) son las mismas en todos los sistemas de referencia inerciales y se expresan mediante leyes análogas.*

- Generaliza el principio de relatividad de Galileo
- No existe un espacio absoluto
- Solo importa el movimiento relativo

#### **Postulado 2: Constancia de la velocidad de la luz**
> *En cualquier sistema de referencia inercial, la velocidad de la luz en el vacío es una constante universal `c`, independiente del movimiento relativo entre la fuente y el observador.*

- `c ≈ 3 × 10⁸ m/s` (más precisamente: c = 299,792,458 m/s) es una constante universal
- La velocidad de la luz es la misma para todos los observadores inerciales
- Es la velocidad máxima a la que se puede propagar cualquier señal

---

### 🔄 Transformaciones de Lorentz

Las transformaciones de Lorentz relacionan las coordenadas espacio-temporales entre dos sistemas de referencia inerciales.

**Sistema S' se mueve con velocidad v respecto a S en la dirección x:**

```
x' = γ(x - vt)
y' = y
z' = z
t' = γ(t - vx/c²)
```

**Transformación inversa:**
```
x = γ(x' + vt')
y = y'
z = z'
t = γ(t' + vx'/c²)
```

**Factor de Lorentz:**
```
γ = 1/√(1 - v²/c²) = 1/√(1 - β²)
```

donde `β = v/c` (velocidad normalizada)

**Propiedades importantes:**
- Cuando `v << c`: γ ≈ 1 y recuperamos las transformaciones de Galileo
- Cuando `v → c`: γ → ∞
- El factor γ siempre es ≥ 1

---

### ⏱️ Efectos Relativistas

#### **1. Pérdida de la Simultaneidad**

Dos eventos simultáneos en un sistema de referencia NO son simultáneos en otro sistema en movimiento.

Si en S: `t₂ = t₁` (simultáneos), entonces en S':
```
t'₂ - t'₁ = -γv(x₂ - x₁)/c²
```

**Conclusión:** La simultaneidad es relativa, no absoluta.

---

#### **2. Dilatación Temporal**

El tiempo transcurre más lentamente en sistemas en movimiento.

**Tiempo propio (Δτ):** Intervalo de tiempo medido en el sistema donde los eventos ocurren en el mismo lugar.

**Tiempo medido por un observador en movimiento relativo:**
```
Δt = γΔτ = Δτ/√(1 - v²/c²)
```

**Consecuencia:** Como γ ≥ 1, entonces Δt ≥ Δτ

> 🕐 **"Los relojes en movimiento van más despacio"**

**Ejemplo práctico:** Un muón en reposo vive 2 μs, pero viajando a 0.99c vive 14.18 μs desde nuestro punto de vista.

---

#### **3. Contracción de Longitudes**

Los objetos en movimiento se contraen en la dirección del movimiento.

**Longitud propia (L₀):** Longitud medida en el sistema de reposo del objeto.

**Longitud medida por un observador en movimiento relativo:**
```
L = L₀/γ = L₀√(1 - v²/c²)
```

**Consecuencia:** Como γ ≥ 1, entonces L ≤ L₀

> 📏 **"Los objetos en movimiento se acortan"**

**Importante:** Solo se contrae en la dirección del movimiento. Las dimensiones perpendiculares no cambian.

---

### 🚀 Composición de Velocidades

En mecánica clásica: `v = v₁ + v₂` (simple suma)

En relatividad especial, las velocidades NO se suman aritméticamente:

**Fórmula de composición de velocidades relativista:**
```
v = (v₁ + v₂)/(1 + v₁v₂/c²)
```

**Casos especiales:**
- Si `v₁ << c` y `v₂ << c`: recuperamos `v ≈ v₁ + v₂`
- Si `v₁ = c`: entonces `v = c` (¡la velocidad de la luz es invariante!)
- Si `v₁ = v₂ = c/2`: entonces `v = c·(c/2 + c/2)/(1 + 1/4) = 4c/5 = 0.8c` (no es c)

**Para velocidades en sentido opuesto:**
```
v = (v₁ - v₂)/(1 - v₁v₂/c²)
```

---

### 🌈 Efecto Doppler Relativista

El efecto Doppler relativista describe el cambio de frecuencia de la luz debido al movimiento relativo.

**Fuente y observador acercándose:**
```
f_obs = f_fuente · √((c + v)/(c - v))
```

**Fuente y observador alejándose:**
```
f_obs = f_fuente · √((c - v)/(c + v))
```

**Desplazamiento al rojo (redshift):** La luz se desplaza hacia frecuencias más bajas cuando la fuente se aleja.

**Desplazamiento al azul (blueshift):** La luz se desplaza hacia frecuencias más altas cuando la fuente se acerca.

---

### 👥 La Paradoja de los Gemelos

**Planteamiento:** Un gemelo viaja al espacio a alta velocidad mientras el otro se queda en la Tierra.

**Pregunta:** ¿Quién envejece más?

**Respuesta:** El gemelo viajero envejece menos debido a la dilatación temporal.

**Resolución de la "paradoja":**
- NO es una verdadera paradoja
- La situación NO es simétrica: el gemelo viajero acelera y desacelera
- El gemelo viajero no está siempre en un sistema inercial
- El gemelo en la Tierra permanece (aproximadamente) en un sistema inercial

**Cálculo:**
Si el viaje dura `Δt` según la Tierra y el gemelo viaja a velocidad `v`:
```
Edad del gemelo viajero = Edad inicial + Δt/γ
Edad del gemelo en Tierra = Edad inicial + Δt
```

---

### 💡 Sobre la Velocidad de la Luz

**¿Por qué `c` es especial?**

- `c` es la velocidad máxima en el universo
- Cuando `v → c`, el factor γ → ∞
- `c` es una constante universal de la naturaleza
- Cualquier partícula sin masa se mueve a la velocidad `c`
- Los fotones (cuantos de luz) tienen masa nula, por eso viajan a `c`
- Las ondas gravitacionales también se propagan a velocidad `c`

**La luz no es especial por sí misma:**
Lo especial es la constante universal `c`, que representa:
- La velocidad máxima de propagación de información
- La conexión fundamental entre espacio y tiempo
- La estructura del espacio-tiempo

---

## Ejercicios Resueltos

### 📝 Ejercicio 1: Paradoja de los Gemelos

**Enunciado:** Un astronauta de 25 años realiza un viaje interestelar a una velocidad de 1.8 × 10⁸ m/s. Cuando regresa, en la Tierra han transcurrido 50 años. ¿Qué edad tiene el viajero?

**Solución paso a paso:**

**Paso 1:** Identificar los datos
- Edad inicial del astronauta: 25 años
- Velocidad del viaje: v = 1.8 × 10⁸ m/s
- Tiempo transcurrido en la Tierra: Δt = 50 años
- Velocidad de la luz: c = 3 × 10⁸ m/s

**Paso 2:** Calcular el factor β
```
β = v/c = (1.8 × 10⁸)/(3 × 10⁸) = 0.6
```

**Paso 3:** Calcular el factor de Lorentz γ
```
γ = 1/√(1 - β²) = 1/√(1 - 0.6²) = 1/√(1 - 0.36) = 1/√0.64 = 1/0.8 = 1.25
```

**Paso 4:** Calcular el tiempo propio (tiempo del astronauta)
Por la dilatación temporal:
```
Δτ = Δt/γ = 50/1.25 = 40 años
```

**Paso 5:** Calcular la edad final del astronauta
```
Edad final = Edad inicial + Δτ = 25 + 40 = 65 años
```

**Respuesta:** El astronauta tiene **65 años**.

**Interpretación física:** 
- En la Tierra pasaron 50 años
- Para el astronauta solo pasaron 40 años (envejeció 15 años menos que si hubiera permanecido en la Tierra)
- El astronauta vivió menos tiempo propio debido a que viajaba a alta velocidad

---

### 📝 Ejercicio 2: Contracción de Longitudes

**Enunciado:** ¿Qué velocidad ha de tener una varilla para que su longitud sea la tercera parte de la medida cuando está en reposo?

**Solución paso a paso:**

**Paso 1:** Identificar la condición
- Longitud en reposo: L₀
- Longitud medida: L = L₀/3
- Encontrar: v = ?

**Paso 2:** Aplicar la fórmula de contracción de longitudes
```
L = L₀√(1 - v²/c²)
```

**Paso 3:** Sustituir y despejar
```
L₀/3 = L₀√(1 - v²/c²)
1/3 = √(1 - v²/c²)
```

**Paso 4:** Elevar al cuadrado ambos lados
```
(1/3)² = 1 - v²/c²
1/9 = 1 - v²/c²
```

**Paso 5:** Despejar v²/c²
```
v²/c² = 1 - 1/9 = 8/9
```

**Paso 6:** Calcular v
```
v/c = √(8/9) = 2√2/3 ≈ 0.9428
v ≈ 0.94c
```

**Respuesta:** La varilla debe moverse a aproximadamente **0.94c** (94% de la velocidad de la luz).

**Verificación:**
```
γ = 1/√(1 - 0.9428²) ≈ 1/√(1 - 0.8889) ≈ 1/√0.1111 ≈ 3
L = L₀/γ = L₀/3 ✓
```

---

### 📝 Ejercicio 3: Área de un Rectángulo en Movimiento

**Enunciado:** Un rectángulo cuyos lados en reposo miden 0.50 m y 0.75 m se mueve paralelamente a su lado mayor a una velocidad de (1/2)c. 
a) Calcular el área que medirá un observador en reposo.
b) ¿A qué velocidad ha de moverse para que al observador en reposo le parezca un cuadrado?

**Solución paso a paso:**

**PARTE A:**

**Paso 1:** Identificar los datos
- Lado menor (perpendicular al movimiento): a = 0.50 m (no cambia)
- Lado mayor (paralelo al movimiento): b₀ = 0.75 m
- Velocidad: v = c/2
- β = v/c = 0.5

**Paso 2:** Calcular el factor γ
```
γ = 1/√(1 - β²) = 1/√(1 - 0.25) = 1/√0.75 = 1/0.866 ≈ 1.1547
```

**Paso 3:** Calcular el lado contraído
Solo se contrae el lado paralelo al movimiento:
```
b = b₀/γ = 0.75/1.1547 ≈ 0.6495 m
```

**Paso 4:** Calcular el área
```
A = a × b = 0.50 × 0.6495 = 0.3248 m²
```

**Respuesta parte a:** El área medida es aproximadamente **0.325 m²**.

**PARTE B:**

**Paso 1:** Condición para que sea un cuadrado
Para que parezca un cuadrado:
```
b = a
b₀/γ = 0.50
0.75/γ = 0.50
γ = 0.75/0.50 = 1.5
```

**Paso 2:** Calcular v a partir de γ
```
γ = 1/√(1 - v²/c²)
1.5 = 1/√(1 - v²/c²)
√(1 - v²/c²) = 1/1.5 = 2/3
```

**Paso 3:** Elevar al cuadrado
```
1 - v²/c² = 4/9
v²/c² = 1 - 4/9 = 5/9
```

**Paso 4:** Calcular v
```
v/c = √(5/9) = √5/3 ≈ 0.7454
v ≈ 0.745c
```

**Respuesta parte b:** Debe moverse a aproximadamente **0.745c**.

**Interpretación física:**
- A mayor velocidad, mayor contracción del lado paralelo al movimiento
- El lado perpendicular nunca se contrae
- Para que un rectángulo de 0.75m × 0.50m parezca cuadrado, el lado de 0.75m debe contraerse a 0.50m

---

### 📝 Ejercicio 4: Vida Media del Muón

**Enunciado:** La vida media de un muón es de 2 μs. Si viaja a una velocidad de 0.99c:
a) Calcular la vida media en el sistema de referencia terrestre.
b) Calcular la distancia que recorrerá antes de desintegrarse en el sistema terrestre.
c) Calcular la distancia que recorrerá en el sistema de referencia del muón.

**Solución paso a paso:**

**Paso 1:** Identificar los datos
- Vida media propia: τ₀ = 2 μs = 2 × 10⁻⁶ s
- Velocidad: v = 0.99c
- β = 0.99

**Paso 2:** Calcular el factor γ
```
γ = 1/√(1 - β²) = 1/√(1 - 0.99²) = 1/√(1 - 0.9801) = 1/√0.0199 ≈ 7.09
```

**PARTE A: Vida media en el sistema terrestre**

**Paso 3:** Aplicar dilatación temporal
```
τ = γτ₀ = 7.09 × 2 × 10⁻⁶ s ≈ 14.18 × 10⁻⁶ s = 14.18 μs
```

**Respuesta parte a:** La vida media en el sistema terrestre es **14.18 μs**.

**PARTE B: Distancia en el sistema terrestre**

**Paso 4:** Calcular la distancia con el tiempo dilatado
```
d_tierra = v × τ = 0.99c × 14.18 × 10⁻⁶ s
d_tierra = 0.99 × 3 × 10⁸ m/s × 14.18 × 10⁻⁶ s
d_tierra ≈ 4211.5 m
```

**Respuesta parte b:** Recorre **4211.5 m** según observadores terrestres.

**PARTE C: Distancia en el sistema del muón**

**Paso 5:** Desde el punto de vista del muón
Para el muón, su vida es τ₀ = 2 μs (tiempo propio).
Pero la distancia que ve recorrer está contraída:

**Método 1 (usando contracción de longitudes):**
```
d_muón = d_tierra/γ = 4211.5/7.09 ≈ 594 m
```

**Método 2 (usando tiempo propio):**
```
d_muón = v × τ₀ = 0.99c × 2 × 10⁻⁶ s
d_muón = 0.99 × 3 × 10⁸ × 2 × 10⁻⁶ ≈ 594 m
```

**Respuesta parte c:** En el sistema del muón, recorre **594 m**.

**Interpretación física:**
- Para observadores terrestres: el muón vive más tiempo (14.18 μs) y recorre 4211.5 m
- Para el muón: vive su tiempo normal (2 μs) pero la distancia terrestre está contraída a 594 m
- Ambos puntos de vista son consistentes: el muón llega al suelo porque:
  - Desde la Tierra: vive más tiempo
  - Desde el muón: la distancia es menor

---

### 📝 Ejercicio 5: Composición de Velocidades

**Enunciado:** Un objeto se mueve respecto a la Tierra a una velocidad de (3/4)c, y otro objeto se mueve respecto del primer objeto, en el mismo sentido, a una velocidad de (3/5)c.
a) ¿Cuál es la velocidad resultante?
b) ¿Cuál sería la velocidad resultante si el segundo objeto se moviera en sentido opuesto?

**Solución paso a paso:**

**PARTE A: Mismo sentido**

**Paso 1:** Identificar los datos
- v₁ = (3/4)c (velocidad del primer objeto respecto a Tierra)
- v₂ = (3/5)c (velocidad del segundo objeto respecto al primero)
- Ambos en el mismo sentido

**Paso 2:** Aplicar la fórmula de composición relativista
```
v = (v₁ + v₂)/(1 + v₁v₂/c²)
```

**Paso 3:** Sustituir valores
```
v = [(3/4)c + (3/5)c] / [1 + (3/4)c × (3/5)c / c²]
v = [(3/4)c + (3/5)c] / [1 + (3/4) × (3/5)]
v = [(15/20)c + (12/20)c] / [1 + 9/20]
v = (27/20)c / (29/20)
v = (27/29)c
```

**Paso 4:** Calcular el valor numérico
```
v = (27/29)c ≈ 0.931c
```

**Respuesta parte a:** La velocidad resultante es **(27/29)c ≈ 0.931c**.

**Nota importante:** ¡Si usáramos la suma clásica obtendríamos (3/4 + 3/5)c = (27/20)c = 1.35c > c, lo cual es imposible!

**PARTE B: Sentido opuesto**

**Paso 5:** Aplicar la fórmula con signo negativo
```
v = (v₁ - v₂)/(1 - v₁v₂/c²)
```

**Paso 6:** Sustituir valores
```
v = [(3/4)c - (3/5)c] / [1 - (3/4) × (3/5)]
v = [(15/20)c - (12/20)c] / [1 - 9/20]
v = (3/20)c / (11/20)
v = (3/11)c
```

**Paso 7:** Calcular el valor numérico
```
v = (3/11)c ≈ 0.273c
```

**Respuesta parte b:** La velocidad resultante es **(3/11)c ≈ 0.273c**.

**Interpretación física:**
- La fórmula relativista asegura que ninguna velocidad supera c
- Cuando las velocidades son del mismo sentido, el resultado es menor que la suma clásica
- El denominador (1 + v₁v₂/c²) siempre es mayor que 1, lo que "frena" la composición

---

### 📝 Ejercicio 6: Nave Espacial y Cohete

**Enunciado:** Desde la proa de una nave espacial que se aleja de la Tierra a una velocidad de 0.6c, se lanza un cohete a una velocidad de 0.9c (respecto a la nave). ¿Qué velocidad tiene el cohete respecto a la Tierra?

**Solución paso a paso:**

**Paso 1:** Identificar los datos
- v_nave = 0.6c (velocidad de la nave respecto a la Tierra)
- v_cohete/nave = 0.9c (velocidad del cohete respecto a la nave)
- Encontrar: v_cohete/Tierra = ?

**Paso 2:** Aplicar la fórmula de composición de velocidades
```
v = (v₁ + v₂)/(1 + v₁v₂/c²)
```

**Paso 3:** Sustituir valores
```
v = (0.6c + 0.9c)/(1 + 0.6 × 0.9)
v = 1.5c/(1 + 0.54)
v = 1.5c/1.54
v ≈ 0.974c
```

**Respuesta:** El cohete tiene una velocidad de aproximadamente **0.97c** respecto a la Tierra.

**Verificación con suma clásica (incorrecta):**
Si usáramos mecánica clásica: v = 0.6c + 0.9c = 1.5c > c ❌ ¡Imposible!

**Interpretación física:**
- Aunque la nave va a 0.6c y el cohete a 0.9c respecto a la nave
- El cohete NO va a 1.5c respecto a la Tierra
- La relatividad "limita" la velocidad a valores menores que c
- A velocidades cercanas a c, el efecto es muy significativo

---

### 📝 Ejercicio 7: Dilatación Temporal en Avión

**Enunciado:** Un avión que viaja a la velocidad del sonido (1224 km/h) realiza un viaje de 48 horas (tiempo medido desde la Tierra). Lleva un reloj atómico que puede medir nanosegundos (1 ns = 10⁻⁹ s). Determinar cuánto habrá retrasado el reloj del avión respecto a los relojes en Tierra.

**Solución paso a paso:**

**Paso 1:** Convertir unidades
```
v = 1224 km/h = 1224 × 1000/3600 m/s = 340 m/s
c = 3 × 10⁸ m/s
Δt = 48 h = 48 × 3600 s = 172,800 s
```

**Paso 2:** Calcular β
```
β = v/c = 340/(3 × 10⁸) = 1.133 × 10⁻⁶ ≈ 10⁻⁶
```

**Paso 3:** Como β << 1, usar aproximación
Para velocidades muy pequeñas comparadas con c, podemos expandir γ en serie de Taylor:
```
γ = 1/√(1-β²) = (1-β²)⁻¹/² ≈ 1 + β²/2 + 3β⁴/8 + ...
```

Para β muy pequeño, solo consideramos el primer término:
```
γ ≈ 1 + β²/2 = 1 + (1.133 × 10⁻⁶)²/2
```

**Paso 4:** Calcular la diferencia de tiempo
```
Δτ = Δt/γ ≈ Δt(1 - β²/2) = Δt - Δt·β²/2
```

El retraso es:
```
δt = Δt - Δτ = Δt·β²/2
```

**Paso 5:** Sustituir valores
```
δt = 172,800 × (1.133 × 10⁻⁶)²/2
δt = 172,800 × 1.284 × 10⁻¹²/2
δt ≈ 1.11 × 10⁻⁷ s
δt ≈ 111 ns
```

**Respuesta:** El reloj del avión habrá retrasado aproximadamente **112 ns**.

**Interpretación física:**
- Aunque la velocidad del sonido parece rápida (1224 km/h)
- Es extremadamente pequeña comparada con c (más de un millón de veces menor)
- El efecto relativista es minúsculo: solo 112 nanosegundos en 48 horas
- ¡Pero es medible con relojes atómicos modernos!
- Estos experimentos se han realizado y confirman la teoría de Einstein

**Dato curioso:** Los satélites GPS deben tener en cuenta estos efectos relativistas para funcionar correctamente.

---

## Estrategias para el Examen

### 🎯 Conceptos Clave que Debes Dominar

#### **1. Postulados de Einstein**
- **Principio de relatividad:** Todas las leyes físicas son iguales en sistemas inerciales
- **Constancia de c:** La velocidad de la luz es la misma para todos los observadores
- Saber explicar sus consecuencias y por qué son revolucionarios

#### **2. Factor de Lorentz γ**
```
γ = 1/√(1 - v²/c²)
```
- Es el corazón de casi todos los cálculos
- Memoriza que γ ≥ 1 siempre
- Cuando v → c, γ → ∞
- Cuando v << c, γ ≈ 1

#### **3. Efectos Relativistas**
| Efecto | Fórmula | Interpretación |
|--------|---------|----------------|
| Dilatación temporal | Δt = γΔτ | Los relojes en movimiento van más despacio |
| Contracción de longitudes | L = L₀/γ | Los objetos en movimiento se acortan |
| Composición de velocidades | v = (v₁+v₂)/(1+v₁v₂/c²) | Las velocidades no se suman aritméticamente |

---

### 📝 Metodología para Resolver Problemas

#### **Paso 1: Identificar el tipo de problema**
- ¿Es dilatación temporal? → Busca tiempos
- ¿Es contracción de longitudes? → Busca distancias
- ¿Es composición de velocidades? → Dos o más velocidades

#### **Paso 2: Identificar qué sistema es el "propio"**
- **Tiempo propio (τ):** El reloj que viaja con el objeto
- **Longitud propia (L₀):** La medida en el sistema de reposo del objeto
- Esto es crucial para saber qué fórmula aplicar

#### **Paso 3: Calcular γ primero**
Casi siempre necesitas γ:
1. Calcula β = v/c
2. Calcula γ = 1/√(1-β²)
3. Verifica que γ ≥ 1

#### **Paso 4: Aplicar la fórmula correcta**
- Dilatación temporal: Δt = γΔτ
- Contracción: L = L₀/γ
- Composición: v = (v₁+v₂)/(1+v₁v₂/c²)

#### **Paso 5: Verificar la coherencia**
- ¿El resultado tiene sentido físico?
- ¿v < c?
- ¿Los tiempos/distancias son positivos?
- ¿Las unidades son correctas?

---

### 🚨 Errores Comunes a Evitar

#### ❌ **Error 1: Confundir tiempo propio con tiempo dilatado**
- **Tiempo propio:** Menor, medido en el sistema del objeto
- **Tiempo dilatado:** Mayor, medido por observador externo
- Recuerda: Δt = γΔτ, donde γ ≥ 1, por tanto Δt ≥ Δτ

#### ❌ **Error 2: Usar suma clásica de velocidades**
- NO uses v = v₁ + v₂
- Siempre usa: v = (v₁+v₂)/(1+v₁v₂/c²)

#### ❌ **Error 3: Aplicar contracción en todas las direcciones**
- Solo se contrae en la dirección del movimiento
- Las dimensiones perpendiculares NO cambian

#### ❌ **Error 4: Olvidar que γ depende de β²**
- γ = 1/√(1-β²) donde β = v/c
- No confundas v con c

#### ❌ **Error 5: No convertir unidades**
- Siempre expresa velocidades en términos de c o en m/s
- Cuidado con km/h vs m/s
- Cuidado con μs vs s

---

### 🎓 Preguntas Teóricas Típicas de Examen

#### **Pregunta 1: Postulados de la Relatividad Especial**
**Qué esperar:**
- Enunciar los dos postulados
- Explicar sus consecuencias
- Relacionar con el experimento de Michelson-Morley

**Respuesta modelo:**
1. **Postulado 1 (Principio de Relatividad):** Todas las leyes físicas son iguales en sistemas de referencia inerciales.
2. **Postulado 2 (Constancia de c):** La velocidad de la luz en el vacío es constante para todos los observadores inerciales.
3. **Consecuencias:** Pérdida de simultaneidad absoluta, dilatación temporal, contracción de longitudes, límite de velocidad c.

#### **Pregunta 2: Experimento de Michelson-Morley**
**Qué esperar:**
- Describir el experimento
- Explicar qué buscaban demostrar
- Resultado y consecuencias

**Respuesta modelo:**
- Buscaban medir la velocidad de la Tierra respecto al éter
- Usaron un interferómetro con brazos perpendiculares
- Resultado: NO había diferencia de velocidad de la luz en distintas direcciones
- Consecuencia: Abandono del concepto de éter, evidencia de que c es constante

#### **Pregunta 3: Efectos Relativistas**
**Qué esperar:**
- Enumerar y explicar los principales efectos
- Dar fórmulas y explicar su significado físico

**Respuesta modelo:**
1. **Dilatación temporal:** Δt = γΔτ - Los relojes en movimiento van más despacio
2. **Contracción de longitudes:** L = L₀/γ - Los objetos en movimiento se acortan en la dirección del movimiento
3. **Relatividad de la simultaneidad:** Eventos simultáneos en un sistema no lo son en otro
4. **Límite de velocidad:** Ningún objeto con masa puede alcanzar c

---

### 📊 Tabla de Referencia Rápida

| Magnitud | Símbolo | Fórmula |
|----------|---------|---------|
| Factor de Lorentz | γ | 1/√(1-v²/c²) |
| Velocidad normalizada | β | v/c |
| Tiempo dilatado | Δt | γΔτ |
| Longitud contraída | L | L₀/γ |
| Composición velocidades | v | (v₁+v₂)/(1+v₁v₂/c²) |
| Velocidad de la luz | c | 3×10⁸ m/s |

### 💪 Valores Útiles de γ para Cálculos Rápidos

| v | β = v/c | γ |
|---|---------|---|
| 0.6c | 0.6 | 1.25 |
| 0.8c | 0.8 | 1.67 |
| 0.866c | 0.866 | 2 |
| 0.9c | 0.9 | 2.29 |
| 0.99c | 0.99 | 7.09 |
| 0.995c | 0.995 | 10 |

---

### 🎯 Checklist Final Antes del Examen

- [ ] Sé enunciar los dos postulados de Einstein
- [ ] Entiendo el experimento de Michelson-Morley
- [ ] Puedo calcular γ dado v (y viceversa)
- [ ] Distingo entre tiempo propio y tiempo dilatado
- [ ] Distingo entre longitud propia y longitud contraída
- [ ] Sé aplicar la fórmula de composición de velocidades
- [ ] Entiendo la paradoja de los gemelos
- [ ] Puedo explicar por qué c es la velocidad máxima
- [ ] Sé que solo se contrae en la dirección del movimiento
- [ ] Recuerdo convertir todas las unidades correctamente

---

## 📚 Resumen de Fórmulas Fundamentales

```
Factor de Lorentz:
γ = 1/√(1 - v²/c²) = 1/√(1 - β²)

Transformaciones de Lorentz:
x' = γ(x - vt)
t' = γ(t - vx/c²)

Dilatación Temporal:
Δt = γΔτ

Contracción de Longitudes:
L = L₀/γ = L₀√(1 - v²/c²)

Composición de Velocidades:
v = (v₁ + v₂)/(1 + v₁v₂/c²)

Energía-Momento (extra):
E² = (pc)² + (mc²)²
E = γmc²
p = γmv
```

---

## 🎓 Consejos Finales del Profesor

1. **Practica con los ejercicios resueltos** hasta que puedas hacerlos sin mirar
2. **Entiende la física**, no solo memorices fórmulas
3. **Dibuja diagramas** de los sistemas de referencia en tus problemas
4. **Verifica siempre** que tus resultados tengan sentido físico
5. **No tengas miedo de γ** - es tu amigo, úsalo siempre
6. **La simultaneidad es relativa** - este es el concepto más difícil de aceptar
7. **c es absoluta** - este es el punto de partida de toda la teoría

**Recuerda:** La relatividad especial no es solo matemáticas, es una nueva forma de entender el espacio y el tiempo. ¡La naturaleza del universo es más fascinante de lo que imaginamos!

---

**¡Mucho éxito en tu examen! 🚀**
