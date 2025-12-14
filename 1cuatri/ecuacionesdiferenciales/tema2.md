# Tema 2: Ecuaciones Diferenciales Ordinarias de Primer Orden

## 📚 Resumen de Teoría - Lo Más Importante

### 1. Introducción

Una **Ecuación Diferencial Ordinaria (EDO) de primer orden** es aquella donde solo aparece la derivada primera de la función y(x):

```
f(dy/dx, y, x) = 0
```

**Problema de Cauchy o Problema de Valores Iniciales (PVI):**
- Resolver la EDO con una condición inicial: y(x₀) = y₀

### 2. Métodos Elementales de Resolución

#### 2.1 Ecuaciones Separables

**Forma:** y' = p(x)q(y)

**Método de resolución:**
1. Separar variables: dy/q(y) = p(x)dx
2. Integrar ambos lados: ∫ dy/q(y) = ∫ p(x)dx + C
3. Despejar y (si es posible)

**Ejemplo tipo:**
```
dy/dx = xy
→ dy/y = x dx
→ ln|y| = x²/2 + C
→ y = Ke^(x²/2)
```

#### 2.2 Ecuaciones Lineales

**Forma:** y' + a(x)y = f(x)

**Método de resolución:**
1. Calcular factor integrante: μ(x) = e^(∫a(x)dx)
2. Solución general: y(x) = (1/μ(x))[∫μ(x)f(x)dx + C]

**Solución particular con condición inicial y(x₀) = y₀:**
```
y(x) = y₀·e^(-∫[x₀,x]a(s)ds) + e^(-∫[x₀,x]a(s)ds)·∫[x₀,x]f(s)e^(∫[x₀,s]a(u)du)ds
```

#### 2.3 Ecuaciones Exactas

**Forma:** M(x,y)dx + N(x,y)dy = 0

**Condición de exactitud:** ∂M/∂y = ∂N/∂x

**Método de resolución:**
1. Verificar que es exacta
2. Encontrar F(x,y) tal que ∂F/∂x = M y ∂F/∂y = N
3. La solución es: F(x,y) = C

### 3. Cambios de Variable

#### 3.1 Ecuaciones Homogéneas

**Forma:** y' = f(y/x)

**Cambio de variable:** u = y/x, entonces y = ux y y' = u + xu'

#### 3.2 Ecuación de Bernoulli

**Forma:** y' + a(x)y = b(x)y^p (con p ≠ 0, 1)

**Cambio de variable:** z = y^(1-p)

Entonces: z' = (1-p)y^(-p)y'

#### 3.3 Ecuación de Ricatti

**Forma:** y' = a(x)y + b(x)y² + f(x)

**Requisito:** Conocer una solución particular y₀(x)

**Cambio de variable:** u = y - y₀ (se convierte en Bernoulli con p=2)

### 4. Teoremas Fundamentales

#### 4.1 Teorema de Existencia (Peano)

Si f(x,y) es **continua** en un entorno de (x₀,y₀), entonces el PVI tiene **al menos una solución**.

#### 4.2 Teorema de Existencia y Unicidad

Si f(x,y) y ∂f/∂y son **continuas** en un entorno de (x₀,y₀), entonces el PVI tiene **solución única**.

**¿Cómo aplicarlo?**
1. Verificar continuidad de f(x,y) → garantiza existencia
2. Verificar continuidad de ∂f/∂y → garantiza unicidad

### 5. Estabilidad de Soluciones

#### 5.1 Definiciones

- **Estable:** Si y₀* está cerca de y₀, entonces y*(x) permanece cerca de y(x) para todo x
- **Asintóticamente estable:** Además lim(x→∞)|y*(x) - y(x)| = 0
- **Inestable:** No es estable

#### 5.2 Estabilidad en Ecuaciones Autónomas

**Ecuación:** y' = f(y)

**Para solución de equilibrio y = a:**
- Si f'(a) < 0 → **asintóticamente estable**
- Si f'(a) > 0 → **inestable**

#### 5.3 Estabilidad en Ecuaciones Lineales

**Ecuación:** y' = a(x)y + f(x)

Todas las soluciones tienen la misma estabilidad:
- **Estable** si e^(∫[x₀,x]a(s)ds) está acotada
- **Asintóticamente estable** si e^(∫[x₀,x]a(s)ds) → 0 cuando x → ∞

---

## 🎯 Ejercicios Resueltos Paso a Paso

### Ejercicio 1: Ecuaciones Separables

**Problema:** Resolver y' = 1 + cos²(y - x) con y(0) = 0

**Solución paso a paso:**

**Paso 1:** Hacer el cambio de variable u = y - x

Entonces: y = u + x → y' = u' + 1

**Paso 2:** Sustituir en la ecuación original:
```
u' + 1 = 1 + cos²(u)
u' = cos²(u)
```

**Paso 3:** Separar variables:
```
du/cos²(u) = dx
sec²(u) du = dx
```

**Paso 4:** Integrar ambos lados:
```
∫ sec²(u) du = ∫ dx
tan(u) = x + C
```

**Paso 5:** Deshacer el cambio de variable:
```
tan(y - x) = x + C
```

**Paso 6:** Aplicar condición inicial y(0) = 0:
```
tan(0 - 0) = 0 + C
tan(0) = C
C = 0
```

**Solución particular:** tan(y - x) = x

o despejando: y = x + arctan(x)

---

### Ejercicio 2: Ecuaciones Lineales

**Problema:** Resolver xy' = 2y + x con y(1) = 2

**Solución paso a paso:**

**Paso 1:** Escribir en forma estándar (dividir por x):
```
y' - (2/x)y = 1
```

Aquí: a(x) = -2/x, f(x) = 1

**Paso 2:** Calcular el factor integrante:
```
μ(x) = e^(∫a(x)dx) = e^(∫-2/x dx) = e^(-2ln|x|) = e^(ln(x^(-2))) = x^(-2) = 1/x²
```

**Paso 3:** Aplicar la fórmula de la solución general:
```
y(x) = x²[∫(1/x²)·1 dx + C]
y(x) = x²[∫1/x² dx + C]
y(x) = x²[-1/x + C]
y(x) = -x + Cx²
```

**Paso 4:** Aplicar condición inicial y(1) = 2:
```
2 = -1 + C·1
C = 3
```

**Solución particular:** y = 3x² - x

---

### Ejercicio 3: Ecuación de Bernoulli

**Problema:** Resolver 3y' + y = (1 - 2x)y⁴ con y(1) = 1

**Solución paso a paso:**

**Paso 1:** Identificar la forma de Bernoulli y' + a(x)y = b(x)y^p

Dividiendo por 3:
```
y' + (1/3)y = ((1-2x)/3)y⁴
```

Aquí: a(x) = 1/3, b(x) = (1-2x)/3, p = 4

**Paso 2:** Hacer el cambio z = y^(1-p) = y^(-3)

Entonces: z' = -3y^(-4)y'

**Paso 3:** Dividir la ecuación original por y⁴:
```
y^(-4)y' + (1/3)y^(-3) = (1-2x)/3
```

**Paso 4:** Sustituir z y z':
```
-z'/3 + (1/3)z = (1-2x)/3
```

Multiplicando por -3:
```
z' - z = -(1-2x) = 2x - 1
```

**Paso 5:** Esta es una ecuación lineal. Factor integrante:
```
μ(x) = e^(∫-1 dx) = e^(-x)
```

**Paso 6:** Solución general:
```
z(x) = e^x[∫e^(-x)(2x-1)dx + C]
```

Calculamos la integral por partes:
```
∫e^(-x)(2x-1)dx = -2e^(-x)(x+1) + C₁
```

Entonces:
```
z(x) = e^x[-2e^(-x)(x+1) + C] = -2(x+1) + Ce^x
```

**Paso 7:** Volver a la variable original: y = z^(-1/3)
```
y^(-3) = -2(x+1) + Ce^x
y = [-2(x+1) + Ce^x]^(-1/3)
```

**Paso 8:** Aplicar condición inicial y(1) = 1:
```
1^(-3) = -2(1+1) + Ce^1
1 = -4 + Ce
C = 5/e
```

**Solución particular:** y = [-2(x+1) + 5e^(x-1)]^(-1/3)

---

### Ejercicio 4: Existencia y Unicidad

**Problema:** Estudiar la existencia y unicidad de y' = (y-x)/(y+x)

**Solución paso a paso:**

**Paso 1:** Identificar f(x,y) = (y-x)/(y+x)

**Paso 2:** Verificar continuidad de f(x,y):
- f(x,y) es continua en todo ℝ² excepto donde y + x = 0
- **Conclusión:** Existe solución para todo (x₀,y₀) tal que y₀ + x₀ ≠ 0

**Paso 3:** Calcular la derivada parcial ∂f/∂y:
```
∂f/∂y = ∂/∂y[(y-x)/(y+x)]
      = [(y+x)·1 - (y-x)·1]/(y+x)²
      = [y+x-y+x]/(y+x)²
      = 2x/(y+x)²
```

**Paso 4:** Verificar continuidad de ∂f/∂y:
- ∂f/∂y es continua en todo ℝ² excepto donde y + x = 0
- **Conclusión:** La solución es única para todo (x₀,y₀) tal que y₀ + x₀ ≠ 0

**Respuesta final:** El problema de valores iniciales tiene solución única para cualquier condición inicial (x₀,y₀) donde y₀ + x₀ ≠ 0.

---

### Ejercicio 5: Existencia y Unicidad (con trampa)

**Problema:** Estudiar existencia y unicidad de y' = -2y/x + 4x

**Solución paso a paso:**

**Paso 1:** Identificar f(x,y) = -2y/x + 4x

**Paso 2:** Verificar continuidad de f(x,y):
- f(x,y) tiene una discontinuidad en x = 0
- **Conclusión:** Existe solución para todo (x₀,y₀) con x₀ ≠ 0

**Paso 3:** Calcular ∂f/∂y:
```
∂f/∂y = -2/x
```

**Paso 4:** Verificar continuidad de ∂f/∂y:
- ∂f/∂y es continua para x ≠ 0
- **Conclusión:** Solución única para x₀ ≠ 0

**Respuesta final:** Existe solución única para cualquier condición inicial con x₀ ≠ 0.

---

### Ejercicio 6: Ecuación de Homogénea

**Problema:** Resolver x²y' = 2xy - y² con y(1) = -1

**Solución paso a paso:**

**Paso 1:** Dividir por x²:
```
y' = (2xy - y²)/x² = 2y/x - (y/x)²
```

**Paso 2:** Identificar que es homogénea: y' = f(y/x)

**Paso 3:** Hacer el cambio u = y/x, entonces y = ux y y' = u + xu'

**Paso 4:** Sustituir:
```
u + xu' = 2u - u²
xu' = u - u²
xu' = u(1 - u)
```

**Paso 5:** Separar variables:
```
du/[u(1-u)] = dx/x
```

**Paso 6:** Descomponer en fracciones parciales:
```
1/[u(1-u)] = A/u + B/(1-u)
1 = A(1-u) + Bu
```

Para u = 0: A = 1
Para u = 1: B = 1

```
∫[1/u + 1/(1-u)]du = ∫dx/x
ln|u| - ln|1-u| = ln|x| + C
ln|u/(1-u)| = ln|x| + C
u/(1-u) = Kx
```

**Paso 7:** Deshacer el cambio de variable:
```
(y/x)/(1-y/x) = Kx
y/(x-y) = Kx
y = Kx(x-y)
y = Kx² - Kxy
y + Kxy = Kx²
y(1 + Kx) = Kx²
y = Kx²/(1 + Kx)
```

**Paso 8:** Aplicar condición inicial y(1) = -1:
```
-1 = K·1²/(1 + K)
-1(1 + K) = K
-1 - K = K
-1 = 2K
K = -1/2
```

**Solución particular:**
```
y = -x²/2/(1 - x/2) = -x²/(2 - x)
```

---

### Ejercicio 7: Estabilidad en Ecuaciones Autónomas

**Problema:** Sea y' = y²/³ - y. Averiguar si existe solución única que satisfaga y(0) = 0 y si es estable la solución que verifica y(0) = 1.

**Solución paso a paso:**

**Parte 1: Existencia y unicidad para y(0) = 0**

**Paso 1:** Identificar f(y) = y²/³ - y

**Paso 2:** Verificar continuidad de f(y):
- f(y) es continua para todo y ∈ ℝ → **existe solución**

**Paso 3:** Calcular f'(y):
```
f'(y) = (2/3)y^(-1/3) - 1
```

**Paso 4:** Evaluar en y = 0:
- f'(0) = (2/3)·0^(-1/3) - 1 → No está definida (discontinua)
- **Conclusión:** No hay unicidad para y(0) = 0

**Parte 2: Estabilidad para y(0) = 1**

**Paso 1:** Encontrar puntos de equilibrio (y' = 0):
```
y²/³ - y = 0
y²/³ = y
y^(-1/3) = 1
y = 1
```

**Paso 2:** Evaluar f'(y) en y = 1:
```
f'(1) = (2/3)·1^(-1/3) - 1 = 2/3 - 1 = -1/3 < 0
```

**Paso 3:** Aplicar el teorema de estabilidad:
- Como f'(1) < 0 → la solución y = 1 es **asintóticamente estable**

**Respuesta final:**
- Para y(0) = 0: Existe solución pero no es única
- Para y(0) = 1: La solución es asintóticamente estable

---

### Ejercicio 8: Estabilidad según valores de a

**Problema:** Estudiar la estabilidad de la solución que satisface y(1) = a para y' = sin y

**Solución paso a paso:**

**Paso 1:** Identificar que es autónoma: f(y) = sin y

**Paso 2:** Encontrar puntos de equilibrio:
```
sin y = 0
y = nπ, n ∈ ℤ
```

**Paso 3:** Calcular f'(y):
```
f'(y) = cos y
```

**Paso 4:** Evaluar estabilidad en cada punto de equilibrio:
```
Para y = 0, ±2π, ±4π, ... : f'(y) = cos(2nπ) = 1 > 0 → INESTABLE
Para y = ±π, ±3π, ±5π, ... : f'(y) = cos((2n+1)π) = -1 < 0 → ASINTÓTICAMENTE ESTABLE
```

**Paso 5:** Analizar según el valor de a:
- Si a está cerca de 0, ±2π, ±4π, ... → **inestable**
- Si a está cerca de ±π, ±3π, ±5π, ... → **asintóticamente estable**
- Para otros valores de a, la solución no es de equilibrio

**Respuesta final:**
- a = 2nπ (n entero) → inestable
- a = (2n+1)π (n entero) → asintóticamente estable
- Otros valores → no es punto de equilibrio (la estabilidad depende del punto más cercano)

---

### Ejercicio 9: Aplicación - Desintegración Radiactiva

**Problema:** Tenemos 1 gramo de una sustancia radiactiva que se desintegra a un ritmo proporcional a la raíz cuadrada de la cantidad existente. Si al cabo de un año solo queda 1/4 gramo, ¿al cabo de cuántos años tendremos 0.1 gramos? ¿Cuándo se desintegra totalmente?

**Solución paso a paso:**

**Paso 1:** Plantear la ecuación diferencial:
```
dm/dt = -k√m  (el signo negativo porque disminuye)
```

donde m(t) es la masa en el tiempo t.

**Paso 2:** Separar variables:
```
dm/√m = -k dt
m^(-1/2) dm = -k dt
```

**Paso 3:** Integrar:
```
∫ m^(-1/2) dm = ∫ -k dt
2√m = -kt + C
√m = -kt/2 + C₁
```

**Paso 4:** Aplicar condición inicial m(0) = 1:
```
√1 = -k·0/2 + C₁
C₁ = 1
```

Por tanto: √m = 1 - kt/2

o: m = (1 - kt/2)²

**Paso 5:** Aplicar condición m(1) = 1/4:
```
1/4 = (1 - k/2)²
1/2 = 1 - k/2  (tomando raíz positiva)
k/2 = 1/2
k = 1
```

**Paso 6:** La ecuación es: m(t) = (1 - t/2)²

**Paso 7:** Calcular cuándo m = 0.1:
```
0.1 = (1 - t/2)²
√0.1 = 1 - t/2
t/2 = 1 - √0.1
t = 2(1 - √0.1) ≈ 2(1 - 0.316) ≈ 1.368 años
```

**Paso 8:** Calcular cuándo m = 0:
```
0 = (1 - t/2)²
0 = 1 - t/2
t = 2 años
```

**Respuesta final:**
- Tendremos 0.1 gramos a los **1.37 años** (aproximadamente)
- La sustancia se desintegra totalmente a los **2 años**

---

### Ejercicio 10: Aplicación - Reacción Química

**Problema:** Una reacción química: A + B → X. Sea x(t) la concentración de X, y sean a y b las concentraciones iniciales de A y B. La variación de x(t) es proporcional al producto de las concentraciones de A y B, con x(0) = 0. Hallar x(t).

**Solución paso a paso:**

**Paso 1:** Plantear la ecuación:
- Concentración de A en tiempo t: a - x(t)
- Concentración de B en tiempo t: b - x(t)
```
dx/dt = k(a - x)(b - x)
```

**Paso 2:** Separar variables:
```
dx/[(a-x)(b-x)] = k dt
```

**Paso 3:** Caso 1: a ≠ b

Descomponer en fracciones parciales:
```
1/[(a-x)(b-x)] = A/(a-x) + B/(b-x)
1 = A(b-x) + B(a-x)
```

Para x = a: 1 = A(b-a) → A = 1/(b-a)
Para x = b: 1 = B(a-b) → B = -1/(b-a) = 1/(a-b)

```
∫[1/(b-a)·1/(a-x) + 1/(a-b)·1/(b-x)]dx = ∫k dt
1/(b-a)[-ln|a-x| + ln|b-x|] = kt + C
1/(b-a)·ln|(b-x)/(a-x)| = kt + C
```

**Paso 4:** Aplicar x(0) = 0:
```
1/(b-a)·ln(b/a) = C
```

**Paso 5:** Resolver para x:
```
ln|(b-x)/(a-x)| = (b-a)kt + ln(b/a)
(b-x)/(a-x) = (b/a)e^((b-a)kt)
```

Despejando x:
```
b - x = (b/a)(a-x)e^((b-a)kt)
ab - ax = b(a-x)e^((b-a)kt)
ab - ax = abe^((b-a)kt) - bxe^((b-a)kt)
ab - abe^((b-a)kt) = ax - bxe^((b-a)kt)
ab[1 - e^((b-a)kt)] = x[a - be^((b-a)kt)]
```

**Solución final (a ≠ b):**
```
x(t) = ab[1 - e^((b-a)kt)]/[a - be^((b-a)kt)]
```

**Paso 6:** Caso 2: a = b

```
dx/dt = k(a-x)²
dx/(a-x)² = k dt
∫(a-x)^(-2) dx = ∫k dt
1/(a-x) = kt + C
```

Con x(0) = 0: C = 1/a

**Solución final (a = b):**
```
1/(a-x) = kt + 1/a
x(t) = a - a/(1 + akt) = a²kt/(1 + akt)
```

---

## 📝 Consejos y Estrategias para el Examen

### 1. Identificación Rápida del Tipo de Ecuación

**Crea un checklist mental:**
1. ¿Es separable? → ¿Puedo escribirla como y' = p(x)q(y)?
2. ¿Es lineal? → ¿Tiene la forma y' + a(x)y = f(x)?
3. ¿Es exacta? → ¿Es M(x,y)dx + N(x,y)dy = 0 con ∂M/∂y = ∂N/∂x?
4. ¿Es homogénea? → ¿Puedo escribirla como y' = f(y/x)?
5. ¿Es de Bernoulli? → ¿Tiene la forma y' + a(x)y = b(x)y^p?

### 2. Pasos Fundamentales en Cualquier Ejercicio

**SIEMPRE:**
1. **Identifica el tipo** de ecuación
2. **Escribe el método** que vas a usar
3. **Verifica** las condiciones (si te piden existencia/unicidad)
4. **Aplica el método** paso a paso, sin saltarte pasos
5. **Aplica condiciones iniciales** al final
6. **Comprueba** derivando (si tienes tiempo)

### 3. Errores Comunes a Evitar

❌ **NO olvides:**
- El valor absoluto en los logaritmos
- La constante de integración
- Verificar el dominio de las soluciones
- En ecuaciones homogéneas: y' = u + xu' (no solo u')
- En Bernoulli: dividir primero por y^p

❌ **Cuidado con:**
- Las divisiones por cero
- Los signos en las integrales
- Despejar correctamente en ecuaciones implícitas

### 4. Estrategia para Problemas de Existencia y Unicidad

**Método sistemático:**
1. Escribe f(x,y) claramente
2. Busca puntos de discontinuidad de f(x,y)
3. Calcula ∂f/∂y
4. Busca puntos de discontinuidad de ∂f/∂y
5. **Conclusión:**
   - Si f continua → existe solución
   - Si f y ∂f/∂y continuas → solución única

### 5. Estrategia para Problemas de Estabilidad

**Para ecuaciones autónomas:**
1. Encuentra puntos de equilibrio (f(y) = 0)
2. Calcula f'(y)
3. Evalúa f'(y) en cada punto de equilibrio
4. Aplica el criterio: f'(a) < 0 → estable, f'(a) > 0 → inestable

**Para ecuaciones lineales:**
1. Identifica a(x)
2. Calcula ∫a(s)ds
3. Analiza e^(∫a(s)ds): ¿acotada?, ¿tiende a 0?

### 6. Qué Suelen Pedir en Exámenes

Según el análisis de exámenes típicos:
- **Resolver ecuaciones** (separables, lineales, Bernoulli) - 40%
- **Existencia y unicidad** - 20%
- **Estabilidad** - 15%
- **Problemas aplicados** (física, química, biología) - 15%
- **Teoría** (enunciar teoremas, demostrar propiedades) - 10%

### 7. Tiempo Recomendado por Tipo

- Ecuación separable: 8-10 minutos
- Ecuación lineal: 10-12 minutos
- Ecuación de Bernoulli: 12-15 minutos
- Existencia y unicidad: 5-7 minutos
- Estabilidad: 8-10 minutos
- Problema aplicado: 15-20 minutos

### 8. Fórmulas Clave para Memorizar

**Ecuación lineal:**
```
y = (1/μ)[∫μf dx + C]  donde μ = e^(∫a dx)
```

**Bernoulli (cambio):**
```
z = y^(1-p)
```

**Factor integrante:**
```
μ(x) = e^(∫a(x)dx)
```

**Criterio de estabilidad (autónomas):**
```
f'(a) < 0 → estable
f'(a) > 0 → inestable
```

### 9. Repaso Rápido Pre-Examen (30 minutos antes)

✓ Repasar los 3 métodos principales: separables, lineales, exactas
✓ Repasar cambios de variable: homogéneas, Bernoulli
✓ Recordar teoremas de existencia y unicidad
✓ Repasar criterios de estabilidad
✓ Hacer un ejercicio de cada tipo (mental)

---

## 🎓 Resumen de Teoremas Importantes

### Teorema 1: Existencia (Peano)
**Si** f(x,y) continua en entorno de (x₀,y₀)  
**Entonces** ∃ al menos una solución

### Teorema 2: Existencia y Unicidad (Picard-Lindelöf simplificado)
**Si** f(x,y) y ∂f/∂y continuas en entorno de (x₀,y₀)  
**Entonces** ∃! solución única

### Teorema 3: Estabilidad en Ecuaciones Autónomas
Para y' = f(y) con solución y = a:
- f'(a) < 0 → asintóticamente estable
- f'(a) > 0 → inestable

### Teorema 4: Estabilidad en Ecuaciones Lineales
Todas las soluciones de y' = a(x)y + f(x) tienen la misma estabilidad, que depende de e^(∫a(s)ds)

---

## 📖 Conceptos Clave para No Olvidar

1. **Solución general** vs **Solución particular**
   - General: familia de funciones con constante C
   - Particular: una función específica que satisface condición inicial

2. **Problema de Cauchy**
   - EDO + condición inicial y(x₀) = y₀

3. **Resolución por cuadraturas**
   - Expresar la solución mediante integrales (resolubles o no)

4. **Ecuación autónoma**
   - y' = f(y), no depende explícitamente de x

5. **Punto de equilibrio**
   - Solución constante donde f(y) = 0

6. **Prolongabilidad**
   - ¿Hasta dónde se puede extender la solución?

7. **Dependencia continua**
   - Pequeños cambios en condiciones iniciales → pequeños cambios en solución

---

## ✅ Checklist de Preparación

- [ ] Sé resolver ecuaciones separables
- [ ] Sé resolver ecuaciones lineales con factor integrante
- [ ] Sé verificar si una ecuación es exacta y resolverla
- [ ] Sé hacer el cambio de variable para homogéneas
- [ ] Sé resolver ecuaciones de Bernoulli
- [ ] Sé verificar existencia y unicidad de soluciones
- [ ] Sé estudiar la estabilidad de ecuaciones autónomas
- [ ] Sé estudiar la estabilidad de ecuaciones lineales
- [ ] He resuelto todos los ejercicios del cuaderno
- [ ] He practicado con exámenes anteriores

---

## 📚 Referencias y Material Adicional

- Tema 2 completo: `tema2.pdf`
- Exámenes resueltos: `examenes/ExamenesGFUNIR.pdf`
- Lista de temas: `temasteoria.md`

---

**¡Buena suerte en el examen!** 🍀

Recuerda: la práctica hace al maestro. Resuelve muchos ejercicios y no te quedes con dudas.
