# Tema 1: Introducción a las Ecuaciones Diferenciales

## 📚 Resumen de Teoría - Conceptos Más Importantes

### ¿Qué es una Ecuación Diferencial?

**Definición fundamental:** Una ecuación diferencial es una ecuación que relaciona una función desconocida con alguna de sus derivadas.

#### Tipos de Ecuaciones Diferenciales

**1. Ecuaciones Diferenciales Ordinarias (EDO)**

Si la función es de una sola variable, llamada y(x), tenemos:

```
f(d^n y/dx^n, ..., d²y/dx², dy/dx, y, x) = 0
```

**Ejemplo:** `y'' + 3y' + y = 3e^x`

**2. Ecuaciones en Derivadas Parciales (EDP)**

Si la función depende de varias variables, por ejemplo u(x,y):

```
f(∂^n u/∂y^n, ..., ∂²u/∂x∂y, ∂²u/∂x², ∂u/∂y, ∂u/∂x, u, x, y) = 0
```

**Ejemplo:** `∂²u/∂t² = c² ∂²u/∂x²` (ecuación de ondas)

### Notación Importante

**Para EDOs:**
- `y'(x) ≡ dy/dx` (primera derivada)
- `y''(x) ≡ d²y/dx²` (segunda derivada)
- `y^(n)(x) ≡ d^n y/dx^n` (n-ésima derivada)

**Para EDPs:**
- `u_x ≡ ∂u/∂x`
- `u_y ≡ ∂u/∂y`
- `u_xx ≡ ∂²u/∂x²`
- `u_xy ≡ ∂²u/∂x∂y`

### Conceptos Clave

#### 1. Orden de una Ecuación Diferencial
El orden es la derivada de mayor orden que aparece en la ecuación.

**Ejemplos:**
- `y' + 2y = x` → **Orden 1**
- `y'' + 3y' + y = 0` → **Orden 2**
- `y^(4) + 3y'' - y = 0` → **Orden 4**

#### 2. Solución General vs Solución Particular

**Solución General:** Expresión que recoge todas las soluciones de la ecuación. Contiene constantes de integración (tantas como el orden de la ecuación).

**Solución Particular:** Solución que cumple condiciones específicas (condiciones iniciales o de contorno).

#### 3. Problema de Valores Iniciales (PVI)
Consiste en resolver una ecuación diferencial con condiciones iniciales dadas, es decir, valores específicos de la función y sus derivadas en un punto dado.

**Ejemplo:** Resolver `y'' = a` con `y(0) = 2, y'(0) = 5`

#### 4. Ecuaciones Lineales vs No Lineales

**Ecuación Lineal:** Si la función y sus derivadas aparecen elevadas a la primera potencia y no se multiplican entre sí.

**Ejemplos lineales:**
- `y'' + 3y' + y = x`
- `y' + P(x)y = Q(x)`

**Ejemplos no lineales:**
- `y' + sin(y) = x` (función no lineal de y)
- `(y')² + y = 0` (derivada al cuadrado)

#### 5. Ecuaciones Homogéneas vs No Homogéneas

**Homogénea:** Todos los términos dependen de la función y sus derivadas (no hay término independiente).

**Ejemplo homogéneo:** `y'' + 3y' + y = 0`

**No homogénea:** Tiene términos independientes.

**Ejemplo no homogéneo:** `y'' + 3y' + y = 3e^x`

### Ecuaciones Diferenciales Importantes en Física

#### 1. Movimiento Uniformemente Acelerado
```
d²x/dt² = a
```
donde a es la aceleración constante.

#### 2. Oscilador Armónico Libre
```
d²x/dt² + ω₀² x = 0
```
- Ecuación lineal homogénea de 2º orden
- **Propiedad importante:** Si x₁(t) y x₂(t) son soluciones, entonces α x₁(t) + β x₂(t) también lo es
- **Reversible en el tiempo:** invariante bajo t → -t

#### 3. Oscilador Armónico Amortiguado
```
d²x/dt² + 2ζω₀ dx/dt + ω₀² x = 0
```
- ζ: coeficiente de amortiguamiento
- **No reversible** (tiene derivada de primer orden)

#### 4. Oscilador Armónico Forzado
```
d²x/dt² + 2ζω₀ dx/dt + ω₀² x = F(t)/m
```
- Ecuación no homogénea
- F(t): fuerza externa, m: masa

#### 5. Desintegración Radiactiva
```
dN/dt = -λN
```
- Ecuación **autónoma** (no depende explícitamente de t)
- λ: ritmo de desintegración
- N: número de partículas

#### 6. Ecuación de Ondas (1D)
```
∂²u/∂t² - c² ∂²u/∂x² = f(x,t)
```
- EDP lineal de 2º orden
- c: velocidad de fase
- f(x,t): fuerza externa

#### 7. Ecuación del Calor (1D)
```
∂u/∂t - α ∂²u/∂x² = f(x,t)
```
- u(x,t): distribución de temperatura
- α: difusividad térmica
- f(x,t): fuente externa de calor

#### 8. Ecuación de Laplace
```
∂²u/∂x² + ∂²u/∂y² = 0
```
- Fundamental en teoría de campos

#### 9. Ecuación de Poisson (versión no homogénea de Laplace)
```
∂²u/∂x² + ∂²u/∂y² = f(x,y)
```

#### 10. Ecuación de Schrödinger (independiente del tiempo)
```
-ℏ²/(2m) ∂²ψ/∂x² + V(x)ψ(x) = Eψ(x)
```
- Ecuación central de mecánica cuántica

### Tipos de Problemas en Ecuaciones Diferenciales

1. **Resolver la ecuación:** Encontrar la solución general y/o particular
2. **Existencia y unicidad:** Determinar si hay solución y si es única
3. **Dependencia continua:** Estudiar cómo afectan pequeñas variaciones en condiciones iniciales
4. **Estabilidad:** Analizar el comportamiento cuando x → ∞
5. **Problemas de autovalores:** Encontrar valores de λ para los que existen soluciones no triviales

---

## 📝 Ejercicios Resueltos Paso a Paso

### Ejercicio 1: Clasificar las siguientes ecuaciones

Como profesor, te enseñaré a identificar las características de cada ecuación:

#### a) x²y'' - y' = eˣ

**Paso 1:** ¿Es EDO o EDP?
- Solo tiene derivadas ordinarias (d/dx) → **EDO**

**Paso 2:** ¿Qué orden tiene?
- La derivada más alta es y'' (segunda derivada) → **Orden 2**

**Paso 3:** ¿Es lineal?
- y'' y y' aparecen elevadas a la primera potencia
- No se multiplican entre sí → **Lineal**

**Paso 4:** ¿Es homogénea?
- Tiene término independiente eˣ → **No homogénea**

**Respuesta:** EDO lineal de segundo orden no homogénea

---

#### b) y' + sin(y) = x

**Paso 1:** EDO (solo una variable independiente)

**Paso 2:** Orden 1 (derivada más alta es y')

**Paso 3:** ¿Es lineal?
- Aparece sin(y), que es una función no lineal de y → **No lineal**

**Respuesta:** EDO no lineal de primer orden

---

#### c) y⁽⁴⁾ + 3y'' - y + ln(x) = 0

**Paso 1:** EDO

**Paso 2:** Orden 4 (y⁽⁴⁾ es la cuarta derivada)

**Paso 3:** Lineal (y y sus derivadas aparecen a la primera potencia)

**Paso 4:** No homogénea (tiene ln(x))

**Respuesta:** EDO lineal de cuarto orden no homogénea

---

#### d) uₓₓ + xuᵧᵧ = 0 (ecuación de Tricomi)

**Paso 1:** ¿EDO o EDP?
- Tiene derivadas parciales (∂/∂x y ∂/∂y) → **EDP**

**Paso 2:** Orden 2 (derivadas más altas son de segundo orden)

**Paso 3:** Lineal (u y sus derivadas a primera potencia)

**Paso 4:** Homogénea (no hay término independiente)

**Respuesta:** EDP lineal de segundo orden homogénea

---

#### e) y' + P(x)y = Q(x)yⁿ (ecuación de Bernoulli)

**Paso 1:** EDO

**Paso 2:** Orden 1

**Paso 3:** ¿Es lineal?
- Aparece yⁿ (y elevada a la n) → **No lineal** (excepto si n=0 o n=1)

**Respuesta:** EDO no lineal de primer orden (para n ≠ 0, 1)

**Nota del profesor:** Esta es una ecuación famosa que tiene métodos especiales de resolución.

---

#### f) x²y'' + xy' + (x² - n²)y = 0 (ecuación de Bessel)

**Paso 1:** EDO

**Paso 2:** Orden 2

**Paso 3:** Lineal

**Paso 4:** Homogénea

**Respuesta:** EDO lineal de segundo orden homogénea con coeficientes variables

**Nota del profesor:** Esta ecuación es muy importante en física y define las funciones de Bessel.

---

#### g) ∂ρ/∂t + ∇·j = σ (ecuación de continuidad)

**Paso 1:** EDP (deriva parcial respecto a t, más operador nabla)

**Paso 2:** Orden 1

**Paso 3:** Lineal

**Paso 4:** No homogénea (si σ ≠ 0)

**Respuesta:** EDP lineal de primer orden

**Contexto físico:** Describe conservación de masa/carga. ρ es densidad, j es corriente, σ es fuente.

---

#### h) -ℏ²/(2m) ∂²ψ/∂x² + V(x)ψ(x) = Eψ(x) (Schrödinger independiente del tiempo)

**Paso 1:** EDO (una variable espacial x, E es constante)

**Paso 2:** Orden 2

**Paso 3:** Lineal (si V(x) es función conocida)

**Paso 4:** Homogénea (se puede reescribir como: -ℏ²/(2m) ∂²ψ/∂x² + [V(x) - E]ψ = 0)

**Respuesta:** EDO lineal de segundo orden homogénea

**Nota física:** Esta es la ecuación fundamental de la mecánica cuántica. E son los autovalores (energías permitidas).

---

#### i) ∂p/∂t = -∂/∂x[μ(x,t)p] + ∂²/∂x²[D(x,t)p] (Fokker-Planck)

**Paso 1:** EDP (variables x y t)

**Paso 2:** Orden 2 (derivada más alta es segunda)

**Paso 3:** Puede ser no lineal si μ y D dependen de p

**Respuesta:** EDP de segundo orden (lineal si μ y D son funciones conocidas de x,t)

**Contexto:** Describe evolución de distribuciones de probabilidad en procesos estocásticos.

---

#### j) y' = y(1 - y) (ecuación logística)

**Paso 1:** EDO

**Paso 2:** Orden 1

**Paso 3:** No lineal (tiene y²)

**Paso 4:** Autónoma (no depende explícitamente de x)

**Respuesta:** EDO no lineal autónoma de primer orden

**Contexto:** Modela crecimiento de poblaciones con recursos limitados.

---

#### k) Sistema de Lotka-Volterra:
```
dx/dt = αx - βxy
dy/dt = δxy - γy
```

**Paso 1:** Sistema de EDOs (dos ecuaciones acopladas)

**Paso 2:** Orden 1 cada ecuación

**Paso 3:** No lineal (aparecen productos xy)

**Paso 4:** Autónomo (no depende explícitamente de t)

**Respuesta:** Sistema de EDOs no lineales autónomas de primer orden

**Contexto:** Modelo depredador-presa en ecología. x: presas, y: depredadores.

---

### Ejercicio 2: Hallar la solución general de d⁴y/dx⁴ = 0

Este ejercicio nos enseña cómo integrar sucesivamente.

**Paso 1:** Integramos una vez
```
d³y/dx³ = C₁
```
donde C₁ es la primera constante de integración.

**Paso 2:** Integramos segunda vez
```
d²y/dx² = C₁x + C₂
```

**Paso 3:** Integramos tercera vez
```
dy/dx = C₁x²/2 + C₂x + C₃
```

**Paso 4:** Integramos cuarta vez
```
y(x) = C₁x³/6 + C₂x²/2 + C₃x + C₄
```

**Solución general:**
```
y(x) = C₁x³/6 + C₂x²/2 + C₃x + C₄
```

**Pregunta:** ¿Cuántas condiciones iniciales necesitamos?

**Respuesta:** Como la ecuación es de orden 4, necesitamos **4 condiciones iniciales** para determinar C₁, C₂, C₃, y C₄.

Por ejemplo:
- y(0) = a
- y'(0) = b
- y''(0) = c
- y'''(0) = d

**Interpretación física:** Imagina que y(x) es la posición de una partícula. Las 4 condiciones nos dan: posición inicial, velocidad inicial, aceleración inicial, y la derivada de la aceleración inicial.

---

### Ejercicio 3: Soluciones particulares del oscilador armónico

Dada la solución general: **y(x) = A cos(x) + B sin(x)**

Esta es la solución general de la ecuación: **y'' + y = 0**

#### Caso a) y(0) = 1, y'(0) = 0

**Paso 1:** Calculamos y'(x)
```
y'(x) = -A sin(x) + B cos(x)
```

**Paso 2:** Aplicamos la primera condición y(0) = 1
```
y(0) = A cos(0) + B sin(0) = A = 1
```
Por tanto: **A = 1**

**Paso 3:** Aplicamos la segunda condición y'(0) = 0
```
y'(0) = -A sin(0) + B cos(0) = B = 0
```
Por tanto: **B = 0**

**Solución particular:**
```
y(x) = cos(x)
```

**Interpretación:** Esta solución representa un oscilador que comienza en su amplitud máxima (1) con velocidad cero.

---

#### Caso b) y(0) = 0, y'(0) = 1

**Paso 1:** Aplicamos y(0) = 0
```
y(0) = A cos(0) + B sin(0) = A = 0
```
Por tanto: **A = 0**

**Paso 2:** Aplicamos y'(0) = 1
```
y'(0) = -A sin(0) + B cos(0) = B = 1
```
Por tanto: **B = 1**

**Solución particular:**
```
y(x) = sin(x)
```

**Interpretación:** El oscilador comienza en el origen (posición 0) con velocidad máxima (1).

---

#### Caso c) y(0) = 0, y(π) = 0

Este es un **problema de contorno** (las condiciones se dan en dos puntos diferentes).

**Paso 1:** Aplicamos y(0) = 0
```
y(0) = A cos(0) + B sin(0) = A = 0
```
Por tanto: **A = 0**

La solución se reduce a: **y(x) = B sin(x)**

**Paso 2:** Aplicamos y(π) = 0
```
y(π) = B sin(π) = 0
```

**¡Observación importante!** Como sin(π) = 0, esta ecuación se satisface para **cualquier valor de B**.

**Respuesta:** Este problema tiene **infinitas soluciones**:
```
y(x) = B sin(x)  para cualquier B ∈ ℝ
```

**Nota del profesor:** Este es un ejemplo típico de problema de contorno. A diferencia de los problemas de valores iniciales:
- Puede no tener solución
- Puede tener una única solución
- Puede tener infinitas soluciones

En este caso, tenemos infinitas soluciones porque las condiciones de contorno son compatibles con la forma de la solución general.

**Pregunta adicional:** ¿Qué pasaría si las condiciones fueran y(0) = 0, y(π/2) = 0?

Tendríamos:
- y(0) = A = 0
- y(π/2) = B sin(π/2) = B = 0

En este caso: **solución única y(x) = 0** (la solución trivial).

---

## 🎯 Estrategias para el Examen

### Lo que Suelen Pedir en los Exámenes

Basándome en el examen de ejemplo, estos son los tipos de problemas típicos:

#### 1. Teoría (Problema 1 del examen)
- **Qué esperan:** Desarrollo de temas teóricos como:
  - Ecuaciones diferenciales lineales de orden n
  - Existencia y unicidad de soluciones
  
**Consejo:** Memoriza las definiciones principales, teoremas de existencia y unicidad, y ejemplos representativos.

#### 2. EDO Lineal de Segundo Orden No Homogénea
**Ejemplo del examen:** y'' + 3y' + y = 3eˣ

**Estrategia:**
1. Resolver la homogénea asociada (y'' + 3y' + y = 0)
   - Ecuación característica: r² + 3r + 1 = 0
   - Resolver para r₁, r₂
2. Encontrar solución particular por método de coeficientes indeterminados
3. Solución general = solución homogénea + solución particular

#### 3. Sistemas de EDOs
**Ejemplo del examen:**
```
x' = 5x - y
y' = 2x + 5y
```

**Estrategia:**
1. Escribir en forma matricial
2. Encontrar autovalores y autovectores
3. Clasificar el punto de equilibrio (nodo, foco, silla, etc.)

**Tipos de puntos de equilibrio:**
- **Nodo estable/inestable:** autovalores reales del mismo signo
- **Punto silla:** autovalores reales de signos opuestos
- **Foco estable/inestable:** autovalores complejos conjugados
- **Centro:** autovalores imaginarios puros

#### 4. EDP: Ecuación de Ondas
**Ejemplo del examen:** Resolver con separación de variables y condiciones de contorno

**Estrategia:**
1. Proponer solución separable: u(x,t) = X(x)T(t)
2. Separar variables
3. Resolver las EDOs resultantes
4. Aplicar condiciones de contorno para determinar autovalores
5. Construir solución general como serie de Fourier
6. Aplicar condiciones iniciales para determinar coeficientes

### Consejos del Profesor

✅ **HACER:**
- Identifica siempre primero el tipo de ecuación
- Comprueba tu solución sustituyendo en la ecuación original
- En problemas de contorno, verifica todas las condiciones
- Dibuja diagramas de fase cuando sea apropiado
- Escribe pasos intermedios claramente

❌ **NO HACER:**
- No olvides las constantes de integración
- No confundas EDO con EDP
- No te saltes pasos en las integraciones
- No olvides verificar la existencia y unicidad cuando se pida

### Fórmulas Clave para Memorizar

1. **Ecuación característica para EDO lineal de 2º orden:**
   - ay'' + by' + cy = 0 → ar² + br + c = 0

2. **Soluciones según discriminante:**
   - Δ > 0: y = C₁e^(r₁x) + C₂e^(r₂x)
   - Δ = 0: y = (C₁ + C₂x)e^(rx)
   - Δ < 0: y = e^(αx)[C₁cos(βx) + C₂sin(βx)]

3. **Wronskiano (para independencia lineal):**
   - W(y₁, y₂) = y₁y₂' - y₂y₁'

4. **Método de variación de parámetros**

5. **Series de Fourier para condiciones de contorno**

---

## 📖 Resumen Final

### Los 10 Conceptos Que Debes Dominar

1. **Clasificación de ecuaciones** (EDO/EDP, orden, lineal/no lineal, homogénea/no homogénea)
2. **Solución general vs particular**
3. **Problemas de valores iniciales**
4. **Problemas de contorno**
5. **Ecuaciones de la física** (oscilador armónico, ondas, calor, Laplace)
6. **Existencia y unicidad de soluciones**
7. **Estabilidad de soluciones**
8. **Sistemas de ecuaciones y puntos de equilibrio**
9. **Autovalores y autofunciones**
10. **Métodos de resolución** (separación de variables, coeficientes indeterminados, variación de parámetros)

### Panorámica del Curso Completo

El curso se divide en dos partes:

**Parte I: Ecuaciones Diferenciales Ordinarias**
- Tema 1: Introducción (este tema)
- Tema 2: Métodos elementales de resolución
- Tema 3: Existencia y unicidad
- Tema 4: Sistemas lineales a coeficientes constantes
- Tema 5: Diagonalización y forma canónica de Jordan
- Tema 6: Ecuaciones de orden n
- Tema 7: Mapas de fases y puntos críticos
- Tema 8: EDOs autónomas de segundo orden
- Tema 9: Sistemas Hamiltonianos
- Tema 10: Problemas de Sturm-Liouville
- Tema 11: Métodos numéricos para EDOs

**Parte II: Ecuaciones en Derivadas Parciales**
- Tema 12: Métodos numéricos para problemas de contorno
- Tema 13: EDPs clásicas en física
- Tema 14: Ecuación de ondas
- Tema 15: Ecuación del calor
- Tema 16: Ecuaciones de Laplace y Poisson

---

## 🔍 Problemas Adicionales para Practicar

### Problema de Práctica 1
Clasifica: y''' - 2y'' + y' = sin(x)

<details>
<summary>Solución</summary>
EDO lineal de tercer orden no homogénea
</details>

### Problema de Práctica 2
¿Cuántas condiciones iniciales se necesitan para resolver: y⁽⁵⁾ + y' = x² ?

<details>
<summary>Solución</summary>
5 condiciones (orden de la ecuación = 5)
</details>

### Problema de Práctica 3
Verifica que y = 2e³ˣ es solución de y' - 3y = 0

<details>
<summary>Solución</summary>
y = 2e³ˣ → y' = 6e³ˣ
Sustituyendo: 6e³ˣ - 3(2e³ˣ) = 6e³ˣ - 6e³ˣ = 0 ✓
</details>

---

## 📚 Referencias Bibliográficas Recomendadas

1. **Boyce & DiPrima** - Ecuaciones diferenciales y problemas con valores en la frontera
2. **Zill & Cullen** - Ecuaciones diferenciales con problemas de valores en la frontera
3. **Simmons & Robertson** - Ecuaciones diferenciales: con aplicaciones y notas históricas
4. **Strauss** - Partial Differential Equations: An Introduction
5. **Kiseliov et al.** - Problemas de ecuaciones diferenciales ordinarias (problemas resueltos)

---

**¡Ánimo con el estudio! Recuerda que la práctica es fundamental. Resuelve muchos ejercicios y verifica siempre tus soluciones.**

*Profesor de Física - Ecuaciones Diferenciales*
