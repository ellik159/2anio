# Tema 4: Sistemas Autónomos - Mapas de Fase y Sistemas Dinámicos

## 📚 Resumen de Teoría

### 1. Introducción a Sistemas Autónomos

**Definición:** Un sistema autónomo es aquel que NO depende explícitamente de la variable independiente:

```
y' = f(y)
```

Para sistemas de dos ecuaciones:
```
ẋ = f₁(x, y)
ẏ = f₂(x, y)
```

O en forma vectorial: **ẋ = f(x)**

**Notación importante:**
- Variable independiente: `t` (tiempo)
- Variables dependientes: `x` e `y`
- Derivadas respecto al tiempo: ẋ ≡ dx/dt, ẍ ≡ d²x/dt²

### 2. Propiedades de Sistemas Autónomos

**Teorema 1:**
1. Si **x(t)** es solución → **x(t + C)** también es solución (invariancia temporal)
2. Solución de equilibrio: **x(t) = x₀** si **f(x₀) = 0**

**Consecuencias:**
- Las soluciones son invariantes bajo traslación temporal
- Un punto donde el sistema no varía (derivada = 0) es un **punto de equilibrio** o **punto crítico**

### 3. Mapas de Fases

**Conceptos clave:**

- **Plano de fases:** Plano formado por las variables (x, y)
- **Órbita:** Proyección de la solución (x(t), y(t)) en el plano de fases
- **Mapa de fases:** Conjunto de todas las órbitas del sistema
- **Punto crítico:** Punto de equilibrio donde f(x₀, y₀) = 0

**Ecuación diferencial de las órbitas:**

```
dy/dx = f₂(x,y) / f₁(x,y)
```

Esta ecuación relaciona directamente x e y sin necesidad de resolver el sistema completo.

**Teorema 2 - Propiedades de las órbitas:**
- Por cada punto del plano de fases pasa UNA ÚNICA órbita
- Si una órbita se corta a sí misma → solución periódica (curva cerrada simple)

**Tipos de órbitas:**
1. **Puntos críticos** → soluciones de equilibrio
2. **Curvas cerradas simples** → soluciones periódicas
3. **Arcos simples** → soluciones no periódicas

### 4. Clasificación de Puntos Críticos

#### A) SISTEMAS LINEALES: ẋ = Ax

Para el sistema lineal homogéneo con A = [[a₁₁, a₁₂], [a₂₁, a₂₂]] y |A| ≠ 0:

**Solución general:** x(t) = P e^(Jt) P⁻¹ C

##### Caso 1: Autovalores reales y distintos (λ₁ ≠ λ₂ ∈ ℝ)

| Condición | Tipo de punto | Estabilidad | Comportamiento |
|-----------|---------------|-------------|----------------|
| λ₂ < λ₁ < 0 | **Nodo estable** | Estable | Todas las órbitas entran al punto crítico con pendiente de v₁ |
| λ₂ > λ₁ > 0 | **Nodo inestable** | Inestable | Órbitas salen del punto crítico |
| λ₂ < 0 < λ₁ | **Punto silla** | Inestable | Órbitas se acercan por L₂ y se alejan por L₁ |

##### Caso 2: Autovalor doble (λ₁ = λ₂ = λ)

**Con J diagonal:**
- λ < 0 → **Nodo estelar estable**: órbitas entran por semirrectas
- λ > 0 → **Nodo estelar inestable**: órbitas salen por semirrectas

**Con J no-diagonal:**
- λ < 0 → **Nodo de una tangente estable**: todas las órbitas entran con pendiente v
- λ > 0 → **Nodo de una tangente inestable**: órbitas salen con pendiente v

##### Caso 3: Autovalores complejos (λ = p ± iq)

| Condición | Tipo de punto | Estabilidad | Comportamiento |
|-----------|---------------|-------------|----------------|
| p = 0 | **Centro** | Estable | Órbitas cerradas, soluciones periódicas |
| p < 0 | **Foco estable** | Estable | Espirales decrecientes hacia el punto |
| p > 0 | **Foco inestable** | Inestable | Espirales crecientes alejándose |

#### B) SISTEMAS NO-LINEALES

**Método de análisis:**
1. Encontrar puntos críticos: resolver f₁(x₀, y₀) = 0 y f₂(x₀, y₀) = 0
2. Desarrollar Taylor alrededor del punto crítico
3. Aproximación lineal: u' = Au donde u = x - x₀
4. Calcular matriz jacobiana A en el punto crítico:

```
A = [[∂f₁/∂x, ∂f₁/∂y],
     [∂f₂/∂x, ∂f₂/∂y]]
```

5. Calcular autovalores de A
6. Clasificar según Teorema 3

**Teorema 3 - Relación lineal/no-lineal:**

| En aproximación lineal | En ecuación no-lineal |
|------------------------|----------------------|
| Nodo, Punto silla, Foco | **Mismo tipo y estabilidad** |
| Nodo estelar, Nodo de una tangente | **Misma estabilidad** (si f₁, f₂ tienen derivadas continuas) |
| Centro | **Centro, foco estable o foco inestable** (si f₁, f₂ son analíticas) |

### 5. Ecuaciones Autónomas de Segundo Orden

Una ecuación de segundo orden: **ẍ = f(x, ẋ)**

Se convierte en sistema de primer orden:
```
ẋ = y
ẏ = f(x, y)
```

**Variables:**
- x: posición
- y = ẋ: velocidad
- Plano de fases (x, y) = plano posición-velocidad

### 6. Sistemas Dinámicos - Conceptos Avanzados

#### Integrales Primeras (Constantes de Movimiento)

**Definición:** Una función C(t, x₁, x₂, ..., xₘ) es integral primera si permanece constante a lo largo de las trayectorias del sistema.

**Teorema 5:** Un sistema de m dimensiones tiene exactamente m integrales primeras independientes.

#### Sistemas Exactos

**Definición:** Un sistema es exacto si:
```
∂f₁/∂x + ∂f₂/∂y = 0
```

**Consecuencia:** Existe una función H(x, y) tal que:
- f₁(x, y) = ∂H/∂y
- f₂(x, y) = -∂H/∂x

Las órbitas vienen dadas por: **H(x, y) = C** (constante)

**Teorema 6:** Los puntos críticos elementales de un sistema exacto solo pueden ser **centros** o **puntos silla**.

#### Sistemas Hamiltonianos

**Ecuaciones de Hamilton:**
```
q̇ᵢ = ∂H/∂pᵢ
ṗᵢ = -∂H/∂qᵢ
```

Donde:
- qᵢ: coordenadas generalizadas
- pᵢ: momentos conjugados
- H: Hamiltoniano

**Propiedad importante:** Los sistemas hamiltonianos son SIEMPRE exactos.

---

## 🎯 Objetivos del Tema

1. ✅ Encontrar puntos críticos de sistemas autónomos
2. ✅ Determinar tipo y estabilidad de puntos críticos
3. ✅ Dibujar mapas de fases y extraer conclusiones

---

## 📝 Ejercicios Resueltos Paso a Paso

### EJEMPLO 1: Oscilador Armónico

**Ecuación:** ẍ + ω²x = 0

**Paso 1:** Convertir a sistema de primer orden
```
ẋ = y
ẏ = -ω²x
```

En forma matricial:
```
ẋ = [[0,    1  ],  * x
     [-ω², 0  ]]
```

**Paso 2:** Solución general
```
x(t) = c₁ cos(ωt) + c₂ sin(ωt)
y(t) = -c₁ω sin(ωt) + c₂ω cos(ωt)
```

**Paso 3:** Punto crítico
- f₁ = y = 0
- f₂ = -ω²x = 0
- Punto crítico: (0, 0)

**Paso 4:** Ecuación de las órbitas
```
dy/dx = -ω²x / y

Separando variables:
∫ y dy = -ω² ∫ x dx

y²/2 = -ω²x²/2 + C/2

Resultado: y² + ω²x² = C  (ELIPSE)
```

**Paso 5:** Clasificación del punto crítico
- Autovalores: λ² + ω² = 0 → λ = ±iω
- Autovalores imaginarios puros (p = 0)
- **Tipo:** CENTRO (estable)
- **Interpretación física:** Movimiento armónico simple sin amortiguamiento

---

### EJEMPLO 2: Sistema de Lotka-Volterra (Predador-Presa)

**Sistema:**
```
ẋ = ax - bxy     (presas)
ẏ = -cy + dxy    (predadores)
```

Donde a, b, c, d > 0

**Paso 1:** Encontrar puntos críticos

Punto 1: (0, 0)
- ẋ = 0: a(0) - b(0)(0) = 0 ✓
- ẏ = 0: -c(0) + d(0)(0) = 0 ✓

Punto 2: (c/d, a/b)
- ẋ = 0: a(c/d) - b(c/d)(a/b) = ac/d - ac/d = 0 ✓
- ẏ = 0: -c(a/b) + d(c/d)(a/b) = -ac/b + ac/b = 0 ✓

**Paso 2:** Analizar el punto (c/d, a/b)

Traslación al origen: u = x - c/d, v = y - a/b

Sistema transformado:
```
u' = -(bc/d)v - buv
v' = (ad/b)u + duv
```

**Paso 3:** Aproximación lineal (ignorar términos no-lineales)
```
u' = -(bc/d)v
v' = (ad/b)u
```

Matriz jacobiana:
```
A = [[0,      -bc/d],
     [ad/b,    0   ]]
```

**Paso 4:** Calcular autovalores
```
det(A - λI) = λ² + (bc/d)(ad/b) = λ² + ac = 0

λ = ±i√(ac)
```

**Paso 5:** Clasificación
- Autovalores imaginarios puros
- **Tipo:** CENTRO (en aproximación lineal)

**Paso 6:** Verificar en sistema completo (sistema exacto)
```
∂f₁/∂x + ∂f₂/∂y = (a - by) + (-c + dx) ≠ 0
```

No es exacto, pero se puede encontrar la integral primera:

```
(c/x - d)dx + (a/y - b)dy = 0

Integrando: c ln(x) - dx + a ln(y) - by = C

ln(x^c y^a) = bxy + dx + C

Órbitas: x^c y^a e^(-bxy-dx) = K  (curvas cerradas)
```

**Interpretación física:**
- Poblaciones oscilan periódicamente
- Si hay más presas → predadores aumentan
- Si hay muchos predadores → presas disminuyen
- El sistema vuelve al equilibrio cíclicamente

---

### EJEMPLO 3: Competencia entre Especies

**Sistema:**
```
ẋ = ax - bx² - cxy
ẏ = a*y - b*y² - c*xy
```

**Caso A: Competencia alta (cc* > bb*)**

Ejemplo concreto:
```
ẋ = 20x - 2x² - 5xy
ẏ = 30y - 5y² - 4xy
```

**Paso 1:** Puntos críticos
1. (0, 0)
2. (10, 0): cuando y = 0 → 20x - 2x² = 0 → x = 10
3. (0, 6): cuando x = 0 → 30y - 5y² = 0 → y = 6
4. (5, 2): resolver sistema 2x + 5y = 20 y 4x + 5y = 30

**Paso 2:** Análisis de (0, 0)

Sistema linealizado:
```
ẋ = 20x
ẏ = 30y
```

Autovalores: λ₁ = 20, λ₂ = 30 (ambos positivos)
**Tipo:** Nodo inestable

**Paso 3:** Análisis de (0, 6)

Cambio: u = x, v = y - 6

Sistema linealizado:
```
u' = -10u
v' = -24u - 30v
```

Ecuación característica: λ² + 40λ + 300 = 0
Autovalores: λ₁, λ₂ < 0 (ambos negativos)
**Tipo:** Nodo asintóticamente estable

**Paso 4:** Análisis de (10, 0)

Cambio: u = x - 10, v = y

Sistema linealizado:
```
u' = -20u - 50v
v' = -10v
```

Autovalores: λ₁, λ₂ < 0 (ambos negativos)
**Tipo:** Nodo asintóticamente estable

**Paso 5:** Análisis de (5, 2)

Cambio: u = x - 5, v = y - 2

Sistema linealizado:
```
u' = -10u - 25v
v' = -8u - 10v
```

Ecuación característica: λ² + 20λ + 100 - 200 = λ² + 20λ - 100 = 0

λ = (-20 ± √(400 + 400))/2 = (-20 ± 20√2)/2

λ₁ = 10(√2 - 1) > 0
λ₂ = -10(√2 + 1) < 0

**Tipo:** Punto silla (inestable)

**Interpretación:**
- Solo sobrevive UNA especie
- Cuál sobrevive depende de las condiciones iniciales
- Hay dos atractores estables: (0, 6) y (10, 0)

---

### EJERCICIO RESUELTO 1: ẍ = -2ẋ - 2x

**Como un profesor te lo explicaría:**

¡Muy bien! Vamos a resolver este problema paso a paso. Es una ecuación de segundo orden con amortiguamiento.

**PASO 1: Convertir a sistema de primer orden**

Definimos:
- x: posición
- y = ẋ: velocidad

Entonces:
```
ẋ = y
ẏ = ẍ = -2ẋ - 2x = -2y - 2x
```

Sistema:
```
ẋ = y
ẏ = -2x - 2y
```

**PASO 2: Encontrar puntos críticos**

Igualamos a cero:
```
y = 0
-2x - 2y = 0
```

De la primera: y = 0
Sustituyendo en la segunda: -2x = 0 → x = 0

**Punto crítico: (0, 0)** ← ¡Solo hay uno!

**PASO 3: Matriz del sistema y autovalores**

Matriz:
```
A = [[0,   1 ],
     [-2, -2 ]]
```

Ecuación característica:
```
det(A - λI) = det([[-λ,     1   ],
                   [-2,   -2-λ ]]) = 0

-λ(-2-λ) - (1)(-2) = 0
λ² + 2λ + 2 = 0
```

Fórmula general:
```
λ = (-2 ± √(4 - 8))/2 = (-2 ± √(-4))/2 = (-2 ± 2i)/2

λ = -1 ± i
```

**PASO 4: Clasificar el punto crítico**

- Autovalores complejos: λ = p ± iq
- p = -1 < 0
- q = 1

**Tipo: FOCO ESTABLE** 🎯

**PASO 5: Dibujar el mapa de fases**

Características:
- Espirales que convergen al origen
- Sentido: determinado por el campo vectorial
- En (1, 0): V = (0, -2) → hacia abajo
- Las órbitas giran en sentido horario hacia (0,0)

**Interpretación física:**
- Sistema oscilatorio con amortiguamiento
- La energía se disipa con el tiempo
- Todas las trayectorias tienden al reposo (0, 0)

---

### EJERCICIO RESUELTO 2: Sistema no-lineal

**Sistema:**
```
ẋ = x³ - y
ẏ = x + y³
```

**PASO 1: Encontrar puntos críticos**

```
x³ - y = 0  →  y = x³
x + y³ = 0  →  x + (x³)³ = 0
```

x + x⁹ = 0
x(1 + x⁸) = 0

Como 1 + x⁸ > 0 para todo x real → x = 0
Si x = 0 → y = 0³ = 0

**Punto crítico: (0, 0)** ✓

**PASO 2: Matriz jacobiana**

```
J = [[∂f₁/∂x,  ∂f₁/∂y],     [[3x²,   -1 ],
     [∂f₂/∂x,  ∂f₂/∂y]]  =  [1,     3y²]]
```

En (0, 0):
```
J(0,0) = [[0,  -1],
          [1,   0]]
```

**PASO 3: Autovalores**

```
det(J - λI) = det([[-λ,  -1],
                   [1,   -λ]]) = 0

λ² + 1 = 0
λ = ±i
```

**PASO 4: Clasificación**

- Autovalores imaginarios puros (p = 0)
- En aproximación lineal: **CENTRO**

**PASO 5: Verificar si es sistema exacto**

```
∂f₁/∂x + ∂f₂/∂y = 3x² + 3y² ≠ 0 (excepto en el origen)
```

NO es exacto → No podemos garantizar que sea centro en el sistema no-lineal

Según Teorema 3: puede ser **centro, foco estable o foco inestable**

**PASO 6: Análisis más profundo (método de energía)**

Consideremos V(x, y) = x² + y² (función de Lyapunov candidata)

```
V̇ = 2x·ẋ + 2y·ẏ
  = 2x(x³ - y) + 2y(x + y³)
  = 2x⁴ - 2xy + 2xy + 2y⁴
  = 2x⁴ + 2y⁴ > 0  (para (x,y) ≠ (0,0))
```

Como V̇ > 0 → el sistema se aleja del origen

**Conclusión: FOCO INESTABLE** (espirales divergentes)

---

### EJERCICIO RESUELTO 3: Estudiar estabilidad según parámetro

**Ecuación:** ẍ = a sin(x) cos(x)

**Como profesor:** Vamos a estudiar cómo el parámetro 'a' afecta la estabilidad. Este tipo de problemas es muy común en exámenes.

**PASO 1: Sistema de primer orden**

```
ẋ = y
ẏ = a sin(x) cos(x) = (a/2) sin(2x)
```

**PASO 2: Puntos críticos**

```
y = 0
(a/2) sin(2x) = 0
```

sin(2x) = 0 → 2x = nπ → x = nπ/2, n ∈ ℤ

**Puntos críticos:** (nπ/2, 0) para n = 0, ±1, ±2, ...

Estudiemos x = 0: punto (0, 0)

**PASO 3: Matriz jacobiana**

```
J = [[∂f₁/∂x,  ∂f₁/∂y],     [[0,              1          ],
     [∂f₂/∂x,  ∂f₂/∂y]]  =  [a cos(2x),       0          ]]
```

En (0, 0):
```
J(0,0) = [[0,  1],
          [a,  0]]
```

**PASO 4: Autovalores**

```
det(J - λI) = -λ² - a = 0
λ² = -a
```

**PASO 5: Análisis según valores de 'a'**

| Caso | Condición | Autovalores | Tipo | Estabilidad |
|------|-----------|-------------|------|-------------|
| 1 | a > 0 | λ = ±i√a | Centro | Estable |
| 2 | a = 0 | λ = 0 (doble) | Degenerado | Requiere más análisis |
| 3 | a < 0 | λ = ±√\|a\| | Punto silla | Inestable |

**Interpretación física (si x es posición angular):**

- **a > 0:** Fuerza restauradora → oscilaciones estables alrededor de x = 0
- **a < 0:** Fuerza expulsora → punto de equilibrio inestable
- **a = 0:** Sin fuerzas → todo punto es equilibrio (caso degenerado)

**Conclusión:**
- La solución x = 0 es **ESTABLE** si y solo si **a > 0**
- Es **INESTABLE** si **a < 0**

---

## 💡 Estrategias para el Examen

### 1. Metodología General

**Para cualquier sistema autónomo:**

1. **Identificar el tipo de sistema** (lineal o no-lineal)
2. **Encontrar puntos críticos** (igualar ẋ = 0, ẏ = 0)
3. **Calcular la matriz jacobiana** en cada punto crítico
4. **Calcular autovalores**
5. **Clasificar** según la tabla de autovalores
6. **Dibujar** el mapa de fases aproximado

### 2. Trucos y Consejos del Profesor

**✅ HACER:**

- **Siempre verifica** que has encontrado TODOS los puntos críticos
- **Dibuja un esquema** aunque sea aproximado del mapa de fases
- **Interpreta físicamente** el resultado cuando sea posible
- **Revisa** si el sistema es exacto o hamiltoniano (simplifica mucho)
- **Usa simetría** del sistema para reducir cálculos

**❌ EVITAR:**

- NO confundas estabilidad con tipo de punto
- NO olvides que centros en sistema lineal pueden ser focos en no-lineal
- NO calcules autovectores si solo piden clasificación
- NO ignores el signo de los autovalores (determina estabilidad)

### 3. Tabla Resumen de Autovalores

**¡MEMORIZA ESTA TABLA!**

| Autovalores | Condición | Tipo de Punto | Estabilidad |
|-------------|-----------|---------------|-------------|
| λ₁, λ₂ reales | λ₂ < λ₁ < 0 | Nodo | Estable |
| λ₁, λ₂ reales | λ₂ > λ₁ > 0 | Nodo | Inestable |
| λ₁, λ₂ reales | λ₂ < 0 < λ₁ | Silla | Inestable |
| λ = λ₁ = λ₂ | λ < 0 | Nodo estelar/tangente | Estable |
| λ = λ₁ = λ₂ | λ > 0 | Nodo estelar/tangente | Inestable |
| λ = p ± iq | p = 0 | Centro | Estable |
| λ = p ± iq | p < 0 | Foco | Estable |
| λ = p ± iq | p > 0 | Foco | Inestable |

### 4. Qué Suelen Pedir en Exámenes

Basado en el análisis de exámenes anteriores:

1. **Clasificar puntos críticos de un sistema** (70% probabilidad)
   - Sistema lineal a coeficientes constantes
   - Identificar tipo y estabilidad

2. **Dibujar mapa de fases** (50% probabilidad)
   - No necesita ser perfecto, pero debe mostrar:
     - Dirección de las órbitas
     - Tipo de puntos críticos
     - Comportamiento asintótico

3. **Teoría** (30% probabilidad)
   - Definiciones: sistema autónomo, punto crítico, órbita
   - Propiedades de sistemas exactos
   - Teoremas de clasificación

4. **Aplicaciones físicas** (40% probabilidad)
   - Oscilador armónico (amortiguado o no)
   - Sistemas de poblaciones
   - Sistemas hamiltonianos

### 5. Checklist Pre-examen

- [ ] Sé convertir ecuación de 2º orden a sistema de 1º orden
- [ ] Sé calcular puntos críticos
- [ ] Sé calcular matriz jacobiana
- [ ] Sé calcular autovalores de matriz 2×2
- [ ] Memoricé la tabla de clasificación de puntos críticos
- [ ] Sé cuándo un sistema es exacto
- [ ] Sé identificar sistemas hamiltonianos
- [ ] Practicé dibujar mapas de fases

### 6. Fórmulas Clave para el Examen

**Ecuación característica (matriz 2×2):**
```
Para A = [[a, b], [c, d]]:
λ² - (a+d)λ + (ad-bc) = 0
λ² - tr(A)λ + det(A) = 0
```

**Criterio rápido:**
- Si det(A) < 0 → **Punto silla** (siempre inestable)
- Si det(A) > 0 y tr(A) ≠ 0:
  - tr(A) < 0 → **Estable**
  - tr(A) > 0 → **Inestable**
- Si det(A) > 0 y tr(A) = 0 → **Centro**

**Discriminante:**
Δ = (tr(A))² - 4det(A)
- Δ > 0 → autovalores reales → **Nodo o Silla**
- Δ = 0 → autovalor doble → **Nodo estelar/tangente**
- Δ < 0 → autovalores complejos → **Centro o Foco**

---

## 🎓 Ejercicios para Practicar

### Ejercicio Propuesto 1
Dibuja el mapa de fases de:
```
ẋ = xy
ẏ = x + y²
```

**Pistas:**
- Encuentra los puntos críticos
- Calcula la jacobiana en cada punto
- Clasifica cada punto
- Dibuja el campo vectorial aproximado

### Ejercicio Propuesto 2
Encuentra la ecuación de las órbitas y dibuja el mapa de fases:
```
ẋ = x + 2xy
ẏ = y² - 2
```

**Pistas:**
- dy/dx = (y² - 2)/(x + 2xy)
- Simplifica y separa variables si es posible
- Identifica los puntos críticos primero

### Ejercicio Propuesto 3
Clasifica los puntos críticos de:
```
ẋ = x² - y
ẏ = xe^y
```

**Pistas:**
- Este es no-lineal, usa aproximación lineal
- Cuidado con el término e^y al calcular derivadas
- En (0,0): e^0 = 1

### Ejercicio Propuesto 4
Estudia según los valores de k la estabilidad de x = 0 para:
```
ẍ + kẋ + e^x = 1
```

**Pistas:**
- Convierte a sistema de primer orden
- En x = 0: e^0 = 1, así que hay punto crítico
- El parámetro k aparece en el término de amortiguamiento
- Analiza casos: k > 0, k = 0, k < 0

### Ejercicio Propuesto 5
Clasifica los puntos críticos de:
```
ẍ = 1 - x² - kẋ  con k ≥ 0
```

Y dibuja el mapa de fases para k = 0, k = 1, k = 3.

**Pistas:**
- Hay dos puntos críticos: x = ±1
- El parámetro k determina el amortiguamiento
- Para k = 0: sistema conservativo (centro o silla)
- Para k > 0: sistema disipativo (foco o nodo)

---

## 📖 Resumen Final - Lo MÁS IMPORTANTE

### Los 10 Puntos Clave del Tema 4

1. **Sistema autónomo:** NO depende explícitamente de t
   - Forma: ẋ = f(x, y), ẏ = g(x, y)

2. **Punto crítico:** Donde f = 0 y g = 0
   - Es solución de equilibrio del sistema

3. **Plano de fases:** Espacio (x, y) donde se dibujan órbitas
   - NO incluye el tiempo explícitamente

4. **Ecuación de órbitas:** dy/dx = g(x,y)/f(x,y)
   - Relaciona x e y directamente

5. **Clasificación:** Depende de autovalores
   - Reales → Nodo o Silla
   - Complejos → Centro o Foco

6. **Estabilidad:** Depende del signo de parte real
   - Re(λ) < 0 → Estable
   - Re(λ) > 0 → Inestable
   - Re(λ) = 0 → Centro (caso especial)

7. **Sistemas no-lineales:** Aproximación lineal
   - Jacobiana en punto crítico
   - Teorema 3 para clasificar

8. **Sistemas exactos:** ∂f/∂x + ∂g/∂y = 0
   - Solo centros o sillas
   - Tienen función H conservada

9. **Sistemas hamiltonianos:** Casos especiales exactos
   - H = constante en órbitas
   - Muy importantes en física

10. **Conversión 2º orden:** ẍ = F(x, ẋ)
    - ẋ = y, ẏ = F(x, y)
    - Plano de fases = posición-velocidad

---

## 🔑 Palabras Clave

- Sistema autónomo
- Punto crítico / Punto de equilibrio
- Plano de fases
- Órbita
- Mapa de fases
- Estabilidad
- Nodo (estable/inestable)
- Punto silla
- Centro
- Foco (estable/inestable)
- Matriz jacobiana
- Autovalores
- Sistema exacto
- Sistema hamiltoniano
- Integral primera

---

**¡Buena suerte en tu examen!** 🍀

Recuerda: La práctica hace al maestro. Resuelve muchos ejercicios y dibuja muchos mapas de fases hasta que te salgan naturalmente.
