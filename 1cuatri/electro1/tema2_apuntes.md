# Tema 2: Ley de Gauss - Electromagnetismo I

## 📚 Resumen de la Teoría

### 1. Introducción

La **Ley de Gauss** es una forma alternativa y elegante de calcular el campo eléctrico, especialmente útil en sistemas con simetría. En lugar de realizar integrales complicadas como con la Ley de Coulomb, podemos aprovechar las propiedades de simetría para simplificar enormemente los cálculos.

**Objetivos del tema:**
- Entender el concepto de flujo eléctrico
- Aprender y aplicar la ley de Gauss
- Comprender la divergencia del campo eléctrico
- Resolver problemas con simetría usando superficies gaussianas

---

### 2. Flujo Eléctrico (Φ)

El **flujo eléctrico** representa el número de líneas de campo eléctrico que atraviesan una superficie.

#### 2.1 Definición básica

Para un campo uniforme **E** y una superficie plana **A** perpendicular al campo:

```
Φ = E⃗ · A⃗
```

**Unidades:** N·m²/C

#### 2.2 Caso general

Si el campo no es uniforme o la superficie es curva:

```
Φ = ∮ E⃗ · dA⃗
```

**Puntos clave:**
- Si el ángulo θ entre E⃗ y la normal a la superficie no es 0°: `Φ = E·A·cos(θ)`
- Para superficies curvas o campos variables, dividimos en elementos infinitesimales dA
- El flujo depende del producto escalar, por lo que solo cuenta la componente perpendicular

---

### 3. Ley de Gauss

**Enunciado:** El flujo eléctrico neto a través de una superficie cerrada es igual a la carga neta encerrada dividida por ε₀.

```
∮ E⃗ · dA⃗ = q_encerrada / ε₀
```

#### 3.1 Conceptos importantes

1. **Superficie gaussiana**: Superficie cerrada imaginaria que usamos como herramienta matemática
2. **Carga encerrada (q_in)**: Solo cuenta la carga dentro de la superficie
3. **Cargas externas**: No contribuyen al flujo neto (líneas que entran = líneas que salen)

#### 3.2 Relación con la densidad de carga

Si la carga está distribuida con densidad volumétrica ρ:

```
∮ E⃗ · dA⃗ = (1/ε₀) ∫ ρ dV
```

---

### 4. Aplicaciones de la Ley de Gauss

La ley de Gauss es especialmente útil cuando hay **simetría**. Los tres casos más comunes:

#### 4.1 Simetría Esférica
**Ejemplo:** Carga puntual, esfera cargada uniformemente

**Superficie gaussiana:** Esfera concéntrica
- El campo es radial y constante en la superficie
- `E · dA = E · dA` (paralelos)
- `∮ E dA = E · 4πr²`

**Resultado para carga puntual:**
```
E = q / (4πε₀r²)
```

#### 4.2 Simetría Cilíndrica
**Ejemplo:** Línea de carga infinita, cilindro cargado

**Superficie gaussiana:** Cilindro coaxial
- El campo es radial desde el eje
- En las tapas: E⃗ ⊥ dA⃗ → flujo = 0
- En la superficie lateral: E paralelo a dA

**Resultado para línea infinita con densidad λ:**
```
E = λ / (2πε₀r)
```

#### 4.3 Simetría Plana
**Ejemplo:** Plano infinito con carga uniforme

**Superficie gaussiana:** Cilindro perpendicular al plano
- El campo es perpendicular al plano
- Flujo solo por las dos tapas

**Resultado para plano con densidad σ:**
```
E = σ / (2ε₀)
```

**¡Importante!** El campo de un plano infinito es constante e independiente de la distancia.

---

### 5. El Teorema de la Divergencia (Teorema de Gauss Matemático)

Relaciona una integral de superficie con una integral de volumen:

```
∮_S E⃗ · dA⃗ = ∫_V (∇ · E⃗) dV
```

Donde `∇ · E⃗` es la **divergencia** del campo eléctrico.

---

### 6. Divergencia del Campo Eléctrico

Aplicando el teorema de la divergencia a la ley de Gauss:

```
∇ · E⃗ = ρ / ε₀
```

Esta es la **forma diferencial** de la ley de Gauss (una de las Ecuaciones de Maxwell).

**Interpretación física:**
- La divergencia mide cuánto "diverge" el campo desde un punto
- Donde hay carga positiva, las líneas de campo "nacen" (divergencia positiva)
- Donde hay carga negativa, las líneas de campo "mueren" (divergencia negativa)

---

## 🎯 Estrategias para el Examen

### Tipos de problemas comunes:

1. **Cálculo de flujo a través de superficies** (Ejercicio 1 del tema)
   - Identifica cada cara/superficie
   - Calcula E⃗ · dA⃗ para cada una
   - Suma todos los flujos

2. **Aplicación directa de la ley de Gauss** (Ejercicios 2-6)
   - Identifica la simetría (esférica, cilíndrica, plana)
   - Elige la superficie gaussiana adecuada
   - Calcula la carga encerrada
   - Aplica ∮ E⃗ · dA⃗ = q_in / ε₀

3. **Conductores y cavidades** (Ejercicio 6)
   - Dentro del conductor: E = 0
   - Las cargas se distribuyen en las superficies
   - Usa superposición cuando sea necesario

### Consejos clave:

✅ **Identifica la simetría primero** - determina qué tipo de superficie gaussiana usar
✅ **Dibuja un diagrama** - visualiza el problema y la superficie gaussiana
✅ **Verifica las unidades** - asegúrate de que sean consistentes
✅ **Comprueba casos límite** - ¿tiene sentido cuando r→0 o r→∞?
✅ **Recuerda las fórmulas clave**: E = σ/(2ε₀) para plano, E = λ/(2πε₀r) para línea

---

## 📝 Ejercicios Resueltos Paso a Paso

### Ejercicio 1: Flujo a través de un cubo

**Enunciado:** Tenemos un campo E⃗ = 2x x̂ + y ŷ. Calcula el flujo eléctrico que atraviesa cada una de las caras de un cubo de lado 1m. ¿Cuál es el flujo total?

**Solución:**

El cubo tiene 6 caras. Vamos a calcular el flujo por cada una:

**Paso 1:** Identificar las caras del cubo de lado L = 1m
- C₁: cara en x = 1 (normal: x̂)
- C₂: cara en x = 0 (normal: -x̂)
- C₃: cara en y = 1 (normal: ŷ)
- C₄: cara en y = 0 (normal: -ŷ)
- C₅: cara en z = 1 (normal: ẑ)
- C₆: cara en z = 0 (normal: -ẑ)

**Paso 2:** Calcular flujo en cada cara

**Cara C₁ (x = 1, dA⃗ = dA x̂):**
```
E⃗ = 2(1) x̂ + y ŷ = 2 x̂ + y ŷ
Φ₁ = ∫∫ E⃗ · dA⃗ = ∫₀¹ ∫₀¹ (2 x̂ + y ŷ) · (dA x̂)
Φ₁ = ∫₀¹ ∫₀¹ 2 dy dz = 2 · 1 · 1 = 2
```

**Cara C₂ (x = 0, dA⃗ = -dA x̂):**
```
E⃗ = 2(0) x̂ + y ŷ = y ŷ
Φ₂ = ∫∫ (y ŷ) · (-dA x̂) = 0
```

**Cara C₃ (y = 1, dA⃗ = dA ŷ):**
```
E⃗ = 2x x̂ + 1 ŷ
Φ₃ = ∫∫ E⃗ · dA⃗ = ∫₀¹ ∫₀¹ 1 dx dz = 1
```

**Cara C₄ (y = 0, dA⃗ = -dA ŷ):**
```
E⃗ = 2x x̂ + 0 ŷ = 2x x̂
Φ₄ = ∫∫ (2x x̂) · (-dA ŷ) = 0
```

**Cara C₅ (z = 1, dA⃗ = dA ẑ):**
```
E⃗ = 2x x̂ + y ŷ
Φ₅ = ∫∫ (2x x̂ + y ŷ) · (dA ẑ) = 0
(no hay componente en z)
```

**Cara C₆ (z = 0, dA⃗ = -dA ẑ):**
```
Φ₆ = 0 (igual que C₅)
```

**Paso 3:** Flujo total
```
Φ_total = Φ₁ + Φ₂ + Φ₃ + Φ₄ + Φ₅ + Φ₆
Φ_total = 2 + 0 + 1 + 0 + 0 + 0 = 3 N·m²/C
```

**Verificación con el teorema de la divergencia:**
```
∇ · E⃗ = ∂(2x)/∂x + ∂(y)/∂y + ∂(0)/∂z = 2 + 1 + 0 = 3
Φ = ∫∫∫ (∇ · E⃗) dV = 3 · (1³) = 3 ✓
```

---

### Ejercicio 2: Plano infinito y línea de carga

**Enunciado:** Tenemos un plano infinito con densidad superficial σₛ = 4 μC/m² situado en z = 1 m, y también tenemos una línea uniforme situada en el eje y, con una densidad λ = -3 μC/m. Calcula qué flujo neto atraviesa un cubo de lado 2 m que está centrado en el origen.

**Solución:**

**Paso 1:** Entender la geometría
- Cubo centrado en el origen: desde (-1,-1,-1) hasta (1,1,1)
- Plano en z = 1 (justo en la cara superior del cubo)
- Línea en el eje y (atraviesa el cubo)

**Paso 2:** Aplicar la Ley de Gauss
```
Φ = q_encerrada / ε₀
```

**Paso 3:** Calcular la carga encerrada

**Del plano:**
El plano en z = 1 está justo en la superficie del cubo. La carga encerrada es el área de la cara superior multiplicada por σₛ:
```
q_plano = σₛ · A = 4 μC/m² · (2m × 2m) = 16 μC
```

**De la línea:**
La línea atraviesa el cubo desde y = -1 hasta y = 1, longitud L = 2m:
```
q_línea = λ · L = (-3 μC/m) · 2m = -6 μC
```

**Paso 4:** Carga total y flujo
```
q_total = q_plano + q_línea = 16 μC + (-6 μC) = 10 μC

Φ = q_total / ε₀ = 10 μC / ε₀
```

**Respuesta:** Φ = 10 μC / ε₀ = 10 × 10⁻⁶ C / ε₀ ≈ 1.13 × 10⁶ N·m²/C

(donde se usa ε₀ = 8.854 × 10⁻¹² C²/(N·m²))

**Nota del profesor:** Observa que aunque el plano es infinito, solo cuenta la parte que está dentro del cubo para calcular la carga encerrada. El resto del plano contribuye con líneas que entran y salen, pero no al flujo neto.

---

### Ejercicio 3: Cilindro con densidad de carga variable

**Enunciado:** Un cilindro infinitamente largo tiene una carga por unidad de volumen ρ = ρ₀(1 - r²/a²). Si tenemos un cilindro concéntrico a este cilindro de radio r y longitud L: ¿cuál será la carga dentro de ese cilindro? ¿Cuál es el campo eléctrico en el interior del cilindro de radio r?

**Solución:**

**Paso 1:** Calcular la carga encerrada

Usamos coordenadas cilíndricas. El elemento de volumen es: dV = r' dr' dθ dz

```
q_in = ∫∫∫ ρ dV = ∫₀ᴸ ∫₀²ᵖⁱ ∫₀ʳ ρ₀(1 - r'²/a²) r' dr' dθ dz
```

**Paso 2:** Resolver la integral radial primero
```
∫₀ʳ ρ₀(1 - r'²/a²) r' dr' = ρ₀ ∫₀ʳ (r' - r'³/a²) dr'
                            = ρ₀ [r'²/2 - r'⁴/(4a²)]₀ʳ
                            = ρ₀ [r²/2 - r⁴/(4a²)]
                            = ρ₀ r²/2 (1 - r²/(2a²))
                            = ρ₀ r²/2 · (2a² - r²)/(2a²)
                            = ρ₀ r²(2a² - r²)/(4a²)
```

**Paso 3:** Integrar en θ y z
```
q_in = ∫₀ᴸ ∫₀²ᵖⁱ ρ₀ r²(2a² - r²)/(4a²) dθ dz
     = ρ₀ r²(2a² - r²)/(4a²) · 2π · L
     = πρ₀Lr²(2a² - r²)/(2a²)
```

**Respuesta parte 1:** q_in = πρ₀Lr²(2a² - r²)/(2a²)

**Paso 4:** Calcular el campo eléctrico usando la Ley de Gauss

Por simetría cilíndrica, E⃗ es radial y constante a distancia r:
```
∮ E⃗ · dA⃗ = E · (2πrL) = q_in/ε₀
```

**Paso 5:** Despejar E
```
E · 2πrL = πρ₀Lr²(2a² - r²)/(2a²ε₀)

E = πρ₀Lr²(2a² - r²)/(2a²ε₀ · 2πrL)

E = ρ₀r²(2a² - r²)/(2a²ε₀ · 2r)

E = ρ₀r(2a² - r²)/(4a²ε₀)
```

**Respuesta parte 2:** E = ρ₀r(2a² - r²)/(4ε₀a²)

**Verificación:** 
- Cuando r = 0: E = 0 ✓ (en el eje, el campo debe ser cero por simetría)
- Cuando r → a: E → ρ₀a/(4ε₀) (valor finito)

---

### Ejercicio 4: Esfera metálica cargada

**Enunciado:** Tenemos una esfera metálica que tiene una densidad de carga superficial σ. El radio de la esfera es R. Calcula el campo eléctrico fuera de la esfera a una distancia 'a' de la superficie exterior.

**Solución:**

**Paso 1:** Entender el problema
- Esfera conductora de radio R
- Punto de interés a distancia 'a' de la superficie → r = R + a
- La carga está en la superficie (conductores: E = 0 dentro)

**Paso 2:** Calcular la carga total
```
Q_total = σ · 4πR²
```

**Paso 3:** Aplicar Ley de Gauss con superficie gaussiana esférica de radio r = R + a
```
∮ E⃗ · dA⃗ = Q_total/ε₀
E · 4πr² = σ · 4πR²/ε₀
```

**Paso 4:** Despejar E
```
E = σR²/(ε₀r²)
E = σR²/(ε₀(R + a)²)
E = σR²/(ε₀R²(1 + a/R)²)
E = σ/(ε₀(1 + a/R)²)
```

**Respuesta:** E = σ/[ε₀(1 + a/R)²]

**Análisis físico:**
- Cuando a → 0 (justo en la superficie): E → σ/ε₀ ✓
- Cuando a → ∞: E → 0 (el campo decae como 1/r²)
- La forma (1 + a/R)⁻² es equivalente a escribir r² = (R+a)²

---

### Ejercicio 5: Dos cascarones esféricos conductores

**Enunciado:** Tenemos dos cascarones esféricos conductores, de radios a y b (con b > a). La carga en su interior es de 5Q (en el cascarón interno) y -Q (en el cascarón externo). Calcula el campo eléctrico en: a) r < a, b) a < r < b y c) r > b.

**Solución:**

**Paso 1:** Entender la distribución de cargas

En conductores en equilibrio electrostático:
- Interior del conductor: E = 0
- Cargas en las superficies

Cascarón interno (radio a): carga total 5Q
Cascarón externo (radio b): carga total -Q

**Paso 2:** Caso a) r < a (dentro del cascarón interno)

Superficie gaussiana esférica con r < a.

Dentro de un conductor: **E = 0**

**Respuesta a):** E = 0

**Paso 3:** Caso b) a < r < b (entre los cascarones)

Superficie gaussiana esférica con a < r < b.

La carga encerrada es solo la del cascarón interno: q_in = 5Q

```
∮ E⃗ · dA⃗ = 5Q/ε₀
E · 4πr² = 5Q/ε₀
E = 5Q/(4πε₀r²)
```

**Respuesta b):** E = 5Q/(4πε₀r²)

**Paso 4:** Caso c) r > b (fuera de ambos cascarones)

Superficie gaussiana esférica con r > b.

La carga encerrada es la suma de ambos cascarones:
```
q_in = 5Q + (-Q) = 4Q

E · 4πr² = 4Q/ε₀
E = 4Q/(4πε₀r²)
E = Q/(πε₀r²)
```

**Respuesta c):** E = Q/(πε₀r²)

**Nota del profesor:** 
- Observa cómo el campo entre los cascarones solo "ve" la carga del cascarón interno
- Desde fuera, solo importa la carga neta total (5Q - Q = 4Q)
- La simplificación: E = 4Q/(4πε₀r²) = Q/(πε₀r²)
- El conductor externo redistribuye su carga: -5Q en su superficie interna (para cancelar el campo del cascarón interno) y +4Q en su superficie externa

---

### Ejercicio 6: Esfera conductora con cavidad y carga central

**Enunciado:** Tenemos una esfera conductora de radio R. Esta esfera tiene una cavidad central de radio a, y en el centro de la cavidad hay una carga Q. Calcula: 
a) ¿Cuál es la carga en la superficie externa del conductor, y en la interna? 
b) Calcula el campo en todos los puntos (r < a, a < r < R, r > R).

**Solución:**

**Parte a) Distribución de cargas**

**Paso 1:** Analizar usando la Ley de Gauss y propiedades de conductores

En un conductor en equilibrio: E = 0 en su interior (material conductor)

**Paso 2:** Carga en la superficie interna (radio a)

Tomamos una superficie gaussiana dentro del conductor (a < r_gauss < R):
```
∮ E⃗ · dA⃗ = 0  (porque E = 0 en el conductor)
```

Por tanto: q_encerrada = 0

Pero dentro hay una carga +Q, entonces debe haber -Q en la superficie interna:
```
q_superficie_interna = -Q
```

**Paso 3:** Carga en la superficie externa (radio R)

El conductor es neutro globalmente, tiene una cavidad, por lo que:
```
Carga total del conductor = q_interna + q_externa = 0
-Q + q_externa = 0
q_externa = +Q
```

**Respuestas parte a):** 
- Carga superficie interna: q_i = -Q
- Carga superficie externa: q_e = +Q

**Parte b) Campo eléctrico en las tres regiones**

**Caso 1: r < a (dentro de la cavidad)**

Superficie gaussiana esférica con r < a.
Solo encierra la carga puntual Q en el centro:
```
E · 4πr² = Q/ε₀
E = Q/(4πε₀r²)
```

**Respuesta:** E = Q/(4πε₀r²)  (campo radial hacia afuera)

**Caso 2: a < r < R (dentro del material conductor)**

Dentro del conductor: **E = 0**

**Respuesta:** E = 0

**Caso 3: r > R (fuera de la esfera)**

Superficie gaussiana esférica con r > R.
Carga encerrada: Q (central) - Q (sup. interna) + Q (sup. externa) = Q

```
E · 4πr² = Q/ε₀
E = Q/(4πε₀r²)
```

**Respuesta:** E = Q/(4πε₀r²)  (campo radial hacia afuera)

**Resumen visual:**

```
        r < a         |  a < r < R  |    r > R
   E = Q/(4πε₀r²)    |    E = 0    | E = Q/(4πε₀r²)
   (cavidad)          | (conductor) | (exterior)
```

**Nota del profesor:** 
- Es notable que el campo dentro de la cavidad es el mismo que si no hubiera conductor
- El campo fuera es también el mismo que si toda la carga estuviera concentrada en el centro
- El conductor "apantalla" perfectamente: el campo dentro del material es cero
- Este es el principio de la **jaula de Faraday**

---

## 💡 Consejos Finales

### ¿Cuándo usar la Ley de Gauss?

✅ **SÍ usar Ley de Gauss cuando hay:**
- Simetría esférica (cargas puntuales, esferas)
- Simetría cilíndrica (líneas, cables, cilindros infinitos)
- Simetría plana (planos infinitos)
- Conductores (E = 0 dentro)

❌ **NO usar Ley de Gauss (usar Coulomb) cuando:**
- No hay simetría clara
- Distribuciones de carga irregulares
- Necesitas el campo en puntos sin simetría

### Errores comunes a evitar:

1. **Olvidar que la superficie gaussiana es imaginaria** - puedes elegirla donde quieras
2. **No verificar que E sea constante en la superficie** - si no lo es, Gauss es complicado
3. **Confundir carga total con carga encerrada** - solo cuenta lo que está dentro
4. **Errores de signo** - revisa la dirección de dA⃗ (siempre hacia afuera)
5. **En conductores:** olvidar que E = 0 dentro y las cargas van a las superficies

### Fórmulas para memorizar:

```
Ley de Gauss:        ∮ E⃗ · dA⃗ = q_in / ε₀
Forma diferencial:   ∇ · E⃗ = ρ / ε₀
Plano infinito:      E = σ / (2ε₀)
Línea infinita:      E = λ / (2πε₀r)
Esfera/punto:        E = Q / (4πε₀r²)
```

---

## 📖 Relación con Exámenes

Revisando los exámenes de la asignatura, los problemas de la Ley de Gauss típicamente aparecen como:

1. **Cálculo directo de flujos** - Similar al Ejercicio 1
2. **Aplicaciones con conductores y dieléctricos** - Problema 3 del examen
3. **Simetría cilíndrica con corrientes** - Problema 5 del examen (tema posterior, pero usa Gauss)

**Estrategia de examen:**
- Lee bien si piden campo E, potencial V, o flujo Φ
- Dibuja SIEMPRE un esquema de la situación
- Identifica la simetría antes de empezar cálculos
- Verifica dimensionalmente tu respuesta
- Si tienes tiempo, comprueba casos límite (r→0, r→∞)

---

**¡Mucho ánimo con el estudio! La Ley de Gauss es una herramienta poderosa que te acompañará en toda la física electromagnética.** 🚀
