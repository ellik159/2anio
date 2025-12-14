# Tema 1: Introducción a la Teoría de Campos

## 📚 Resumen de Teoría

### 🎯 Objetivos del Tema

Este tema es fundamental para entender la física matemática. Nos introduce a:
- Campos escalares y vectoriales
- Operadores vectoriales (gradiente, divergencia, rotacional, laplaciano)
- Integración de campos (circulación y flujo)
- Propiedades especiales de campos
- Teoremas fundamentales (Gauss, Stokes, Helmholtz)

### 1. Conceptos Básicos

#### 1.1 ¿Qué es un Campo?

**Definición física**: Un campo reemplaza el concepto de "fuerza a distancia". Una magnitud activa (como una carga eléctrica o una masa) genera un campo que se extiende por todo el espacio. Otras magnitudes "sienten" este campo en su posición.

**Ejemplo**: Las limaduras de hierro alrededor de un imán forman líneas de fuerza que visualizan el campo magnético.

#### 1.2 Campo Escalar

**Definición**: Función que asigna a cada punto del espacio un valor escalar (número).

**Fórmula**: φ(x, y, z) o φ(r⃗)

**Ejemplos**: 
- Temperatura en una habitación
- Presión atmosférica
- Densidad de un material

**Superficies de nivel**: Lugares donde el campo escalar tiene el mismo valor (isotermas para temperatura).

#### 1.3 Campo Vectorial

**Definición**: Función que asigna a cada punto del espacio un vector.

**Fórmula**: E⃗(x, y, z) = Ex i⃗ + Ey j⃗ + Ez k⃗

**Ejemplos**:
- Campo eléctrico
- Campo magnético
- Campo gravitatorio
- Campo de velocidades de un fluido

**Líneas de campo**: Curvas tangentes al vector campo en cada punto. Se obtienen resolviendo:
```
dx/Ex = dy/Ey = dz/Ez
```

### 2. Operadores Vectoriales Fundamentales

#### 2.1 Gradiente (∇φ)

**Aplicación**: Campo escalar → Campo vectorial

**Fórmula en coordenadas cartesianas**:
```
∇φ = (∂φ/∂x) i⃗ + (∂φ/∂y) j⃗ + (∂φ/∂z) k⃗
```

**Propiedades físicas**:
- Apunta en la dirección de máximo crecimiento del campo
- Es perpendicular a las superficies de nivel
- Su módulo indica qué tan rápido cambia el campo

**Ejemplo**: Si φ es la temperatura, ∇φ apunta hacia donde la temperatura aumenta más rápidamente.

#### 2.2 Divergencia (∇·E⃗)

**Aplicación**: Campo vectorial → Campo escalar

**Fórmula**:
```
∇·E⃗ = ∂Ex/∂x + ∂Ey/∂y + ∂Ez/∂z
```

**Interpretación física**:
- Mide cuánto "divergen" las líneas de campo desde un punto
- ∇·E⃗ > 0: hay una **fuente** (manantial) en ese punto
- ∇·E⃗ < 0: hay un **sumidero** (desagüe) en ese punto
- ∇·E⃗ = 0: el campo es **solenoidal** (sin fuentes ni sumideros)

**Visualización**: En un fluido, la divergencia positiva significa que entra más fluido del que sale.

#### 2.3 Rotacional (∇×E⃗)

**Aplicación**: Campo vectorial → Campo vectorial

**Fórmula (determinante)**:
```
      | i⃗    j⃗    k⃗   |
∇×E⃗ = | ∂/∂x ∂/∂y ∂/∂z |
      | Ex   Ey   Ez  |
```

**Resultado**:
```
∇×E⃗ = (∂Ez/∂y - ∂Ey/∂z) i⃗ + (∂Ex/∂z - ∂Ez/∂x) j⃗ + (∂Ey/∂x - ∂Ex/∂y) k⃗
```

**Interpretación física**:
- Mide la "rotación" o circulación del campo alrededor de un punto
- Si ∇×E⃗ = 0: el campo es **irrotacional**

**Visualización**: En un remolino de agua, el rotacional es máximo en el centro.

#### 2.4 Laplaciano (∇²φ)

**Aplicación**: Campo escalar → Campo escalar

**Fórmula**:
```
∇²φ = ∂²φ/∂x² + ∂²φ/∂y² + ∂²φ/∂z²
```

**Equivalente**: ∇²φ = ∇·(∇φ)

**Ecuaciones importantes**:
- ∇²φ = 0: **Ecuación de Laplace** → φ es armónica
- ∇²φ = ρ: **Ecuación de Poisson**

### 3. Integrales de Campo

#### 3.1 Circulación

**Definición**: Integral de línea de un campo vectorial a lo largo de una curva.

**Fórmula**:
```
Γ = ∫C E⃗·dr⃗
```

**Significado físico**: 
- Trabajo realizado por una fuerza a lo largo de un camino
- Mide cuánto "ayuda" el campo al movimiento a lo largo de la curva

**Cálculo paramétrico**: Si r⃗(t) parametriza la curva:
```
Γ = ∫[tA→tB] E⃗(r⃗(t))·(dr⃗/dt) dt
```

#### 3.2 Flujo

**Definición**: Integral de superficie de un campo vectorial a través de una superficie.

**Fórmula**:
```
Φ = ∫∫S E⃗·dS⃗
```

**Significado físico**:
- Cantidad de campo que "atraviesa" una superficie
- En fluidos: caudal (cantidad de fluido por unidad de tiempo)

**Vector superficie**: dS⃗ es perpendicular a la superficie y apunta hacia afuera.

### 4. Teoremas Fundamentales

#### 4.1 Teorema de Gauss (Divergencia)

**Enunciado**: El flujo de un campo a través de una superficie cerrada es igual a la integral de volumen de su divergencia.

**Fórmula**:
```
∮S E⃗·dS⃗ = ∫V (∇·E⃗) dV
```

**Interpretación**: Las fuentes internas determinan el flujo total que sale.

**Aplicación**: Ley de Gauss en electromagnetismo.

#### 4.2 Teorema de Stokes

**Enunciado**: La circulación de un campo a lo largo de una curva cerrada es igual al flujo del rotacional a través de cualquier superficie limitada por esa curva.

**Fórmula**:
```
∮C E⃗·dr⃗ = ∫∫S (∇×E⃗)·dS⃗
```

**Aplicación**: Ley de Faraday en electromagnetismo.

### 5. Propiedades Importantes de Campos

#### 5.1 Campos Conservativos

Un campo es **conservativo** si cumple cualquiera de estas condiciones equivalentes:

1. La integral de línea es independiente del camino
2. La circulación en cualquier camino cerrado es cero: ∮C E⃗·dr⃗ = 0
3. El campo es irrotacional: ∇×E⃗ = 0
4. El campo deriva de un potencial: E⃗ = -∇φ

**Ejemplos**: Campo gravitatorio, campo electrostático.

**Consecuencia importante**: En un campo conservativo, el trabajo solo depende de los puntos inicial y final, no del camino.

#### 5.2 Campos Solenoidales

**Definición**: Campo cuya divergencia es cero en todos los puntos.

**Condición**: ∇·E⃗ = 0

**Propiedades**:
1. No tiene fuentes ni sumideros
2. Las líneas de campo son cerradas o van al infinito
3. Se puede expresar como el rotacional de otro campo: E⃗ = ∇×A⃗

**Ejemplo**: Campo magnético (no hay monopolos magnéticos).

#### 5.3 Campos Irrotacionales

**Definición**: Campo cuyo rotacional es cero.

**Condición**: ∇×E⃗ = 0

**Propiedad**: Equivale a ser conservativo.

#### 5.4 Campos Centrales

**Definición**: Campo que depende solo de la distancia r y apunta radialmente.

**Forma**: E⃗ = f(r) u⃗r

**Propiedades**:
- Siempre son irrotacionales (∇×E⃗ = 0)
- Por tanto, siempre son conservativos
- Ejemplos: campo gravitatorio (f(r) = -GM/r²), campo electrostático de carga puntual

#### 5.5 Campos Armónicos

**Definición**: Campos escalares que satisfacen la ecuación de Laplace.

**Condición**: ∇²φ = 0

**Propiedades**:
1. **Teorema del valor medio**: El valor en un punto es el promedio sobre una esfera centrada en ese punto
2. **No tienen máximos ni mínimos** en el interior del dominio
3. **Unicidad**: Dadas las condiciones de frontera, el campo está determinado (salvo constante)

**Ejemplos**: Potencial gravitatorio en el vacío, potencial electrostático sin cargas.

### 6. Teoremas Importantes

#### 6.1 Rotacional de un Gradiente

**Teorema**: ∇×(∇φ) = 0

**Significado**: Todo campo que derive de un potencial es irrotacional.

#### 6.2 Divergencia de un Rotacional

**Teorema**: ∇·(∇×E⃗) = 0

**Significado**: Todo campo rotacional es solenoidal.

#### 6.3 Rotacional del Rotacional

**Identidad**: ∇×(∇×E⃗) = ∇(∇·E⃗) - ∇²E⃗

### 7. Delta de Dirac

#### En una dimensión

**Definición**:
- δ(x) = 0 si x ≠ 0
- δ(x) = ∞ si x = 0
- ∫[-∞→∞] δ(x) dx = 1

**Propiedad importante**:
```
∫[a→b] f(x)δ(x-x₀) dx = f(x₀) si x₀ ∈ (a,b), 0 si x₀ ∉ [a,b]
```

**Interpretación**: "Selecciona" el valor de la función en un punto.

#### En tres dimensiones

**Definición**: δ(r⃗) = δ(x)δ(y)δ(z)

**Relación importante**:
```
∇²(1/|r⃗ - r⃗₀|) = -4πδ(r⃗ - r⃗₀)
```

Esta fórmula es fundamental en electromagnetismo y gravitación.

### 8. Ángulo Sólido

**Definición**: Extensión tridimensional del concepto de ángulo plano.

**Fórmula**:
```
Ω = ∫S (dS⃗·u⃗r)/r² = ∫S (r⃗·dS⃗)/r³
```

**Unidad**: Estereorradián (sr)

**Propiedades**:
1. Ángulo sólido de una esfera completa: 4π sr
2. Desde un punto fuera del volumen cerrado: Ω = 0
3. Desde un punto dentro del volumen cerrado: Ω = 4π

### 9. Teorema de Helmholtz

**Enunciado**: Un campo vectorial está completamente determinado si se conocen:
1. Su divergencia en todo el espacio: ∇·E⃗
2. Su rotacional en todo el espacio: ∇×E⃗
3. Las condiciones de frontera apropiadas

**Descomposición de Helmholtz**: Todo campo se puede expresar como:
```
E⃗ = -∇φ + ∇×A⃗
```
donde φ es un potencial escalar y A⃗ es un potencial vectorial.

---

## 🔧 Ejercicios Resueltos

### Ejercicio 1: Integral de línea de un campo escalar

**Enunciado**: Dado el campo escalar φ = x²yz + 3x²z - y, calcular la integral de línea ∫C φ dr⃗ a lo largo de la curva y = x², z = 2 entre los puntos A(1, 1, 2) y B(2, 4, 2).

**Solución paso a paso**:

**Paso 1**: Identificar el camino
- Curva: y = x², z = 2
- Límites: x varía de 1 a 2
- Parametrización: x = t, y = t², z = 2, con t ∈ [1, 2]

**Paso 2**: Calcular dr⃗
```
r⃗(t) = t i⃗ + t² j⃗ + 2 k⃗
dr⃗/dt = i⃗ + 2t j⃗ + 0 k⃗
dr⃗ = (i⃗ + 2t j⃗) dt
```

**Paso 3**: Sustituir φ en la curva
```
φ(t) = t²·t²·2 + 3t²·2 - t²
φ(t) = 2t⁴ + 6t² - t²
φ(t) = 2t⁴ + 5t²
```

**Paso 4**: Calcular la integral
```
∫C φ dr⃗ = ∫₁² φ(t)(i⃗ + 2t j⃗) dt
       = i⃗ ∫₁² (2t⁴ + 5t²) dt + j⃗ ∫₁² 2t(2t⁴ + 5t²) dt
       = i⃗ ∫₁² (2t⁴ + 5t²) dt + j⃗ ∫₁² (4t⁵ + 10t³) dt
```

**Paso 5**: Resolver las integrales
```
Para i⃗: ∫₁² (2t⁴ + 5t²) dt = [2t⁵/5 + 5t³/3]₁²
        = (2·32/5 + 5·8/3) - (2/5 + 5/3)
        = 64/5 + 40/3 - 2/5 - 5/3
        = 62/5 + 35/3
        = 186/15 + 175/15 = 361/15

Para j⃗: ∫₁² (4t⁵ + 10t³) dt = [4t⁶/6 + 10t⁴/4]₁²
        = [2t⁶/3 + 5t⁴/2]₁²
        = (2·64/3 + 5·16/2) - (2/3 + 5/2)
        = 128/3 + 40 - 2/3 - 5/2
        = 126/3 + 75/2
        = 252/6 + 225/6 = 477/6 = 159/2
```

**Respuesta**: ∫C φ dr⃗ = (361/15) i⃗ + (159/2) j⃗

**Comprobación**: Verificamos que los límites estén correctos y las integrales bien calculadas. ✓

---

### Ejercicio 2: Circulación de un campo vectorial

**Enunciado**: Dado el campo vectorial v⃗ = (x + y)² i⃗ + xy j⃗, calcular la circulación ∫C v⃗·dr⃗ a lo largo de la recta y = x + 1 entre los puntos A(0, 1) y B(1, 2).

**Solución paso a paso**:

**Paso 1**: Parametrizar la curva
- Recta: y = x + 1
- Parámetro: x = t, y = t + 1, con t ∈ [0, 1]

**Paso 2**: Calcular dr⃗
```
r⃗(t) = t i⃗ + (t + 1) j⃗
dr⃗/dt = i⃗ + j⃗
dr⃗ = (i⃗ + j⃗) dt
```

**Paso 3**: Sustituir el campo en la curva
```
v⃗(t) = (t + t + 1)² i⃗ + t(t + 1) j⃗
v⃗(t) = (2t + 1)² i⃗ + (t² + t) j⃗
```

**Paso 4**: Calcular v⃗·dr⃗
```
v⃗·dr⃗ = [(2t + 1)² i⃗ + (t² + t) j⃗]·(i⃗ + j⃗) dt
      = [(2t + 1)² + (t² + t)] dt
```

**Paso 5**: Expandir y simplificar
```
(2t + 1)² = 4t² + 4t + 1
v⃗·dr⃗ = [4t² + 4t + 1 + t² + t] dt
      = [5t² + 5t + 1] dt
```

**Paso 6**: Integrar
```
∫C v⃗·dr⃗ = ∫₀¹ (5t² + 5t + 1) dt
         = [5t³/3 + 5t²/2 + t]₀¹
         = 5/3 + 5/2 + 1
         = 10/6 + 15/6 + 6/6
         = 31/6
```

**Respuesta**: ∫C v⃗·dr⃗ = 31/6

**Interpretación física**: Esta circulación representa el trabajo que haría el campo v⃗ al mover una partícula desde A hasta B.

---

### Ejercicio 3: Campo solenoidal

**Enunciado**: Dado el campo vectorial v⃗ = (x + 3y) i⃗ + (y - 2z) j⃗ + (x + az) k⃗, hallar el valor de la constante a para que el campo sea solenoidal.

**Solución paso a paso**:

**Paso 1**: Recordar la condición de campo solenoidal
Un campo es solenoidal si: ∇·v⃗ = 0

**Paso 2**: Identificar las componentes
```
vₓ = x + 3y
vᵧ = y - 2z
vz = x + az
```

**Paso 3**: Calcular la divergencia
```
∇·v⃗ = ∂vₓ/∂x + ∂vᵧ/∂y + ∂vᵧ/∂z
     = ∂(x + 3y)/∂x + ∂(y - 2z)/∂y + ∂(x + az)/∂z
     = 1 + 1 + a
     = 2 + a
```

**Paso 4**: Aplicar la condición solenoidal
```
∇·v⃗ = 0
2 + a = 0
a = -2
```

**Respuesta**: a = -2

**Verificación**: Con a = -2:
- v⃗ = (x + 3y) i⃗ + (y - 2z) j⃗ + (x - 2z) k⃗
- ∇·v⃗ = 1 + 1 + (-2) = 0 ✓

**Interpretación física**: Con a = -2, el campo no tiene fuentes ni sumideros netos. Las líneas de campo son cerradas o van al infinito.

---

### Ejercicio 4: Rotacional de un campo vectorial

**Enunciado**: Dado el campo vectorial A⃗ = xz³ i⃗ - 2x²yz j⃗ + 2yz⁴ k⃗, hallar su rotacional ∇×A⃗ en el punto (1, -1, 1).

**Solución paso a paso**:

**Paso 1**: Identificar las componentes
```
Aₓ = xz³
Aᵧ = -2x²yz
Az = 2yz⁴
```

**Paso 2**: Calcular las derivadas necesarias
Para el rotacional necesitamos:
```
∂Aᵧ/∂y = ∂(2yz⁴)/∂y = 2z⁴
∂Aᵧ/∂z = ∂(-2x²yz)/∂z = -2x²y

∂Aₓ/∂z = ∂(xz³)/∂z = 3xz²
∂Aᵧ/∂x = ∂(2yz⁴)/∂x = 0

∂Aᵧ/∂x = ∂(-2x²yz)/∂x = -4xyz
∂Aₓ/∂y = ∂(xz³)/∂y = 0
```

**Paso 3**: Aplicar la fórmula del rotacional
```
∇×A⃗ = (∂Aᵧ/∂y - ∂Aᵧ/∂z) i⃗ + (∂Aₓ/∂z - ∂Aᵧ/∂x) j⃗ + (∂Aᵧ/∂x - ∂Aₓ/∂y) k⃗
```

**Paso 4**: Sustituir
```
Componente i⃗: 2z⁴ - (-2x²y) = 2z⁴ + 2x²y
Componente j⃗: 3xz² - 0 = 3xz²
Componente k⃗: -4xyz - 0 = -4xyz
```

Por lo tanto:
```
∇×A⃗ = (2z⁴ + 2x²y) i⃗ + 3xz² j⃗ - 4xyz k⃗
```

**Paso 5**: Evaluar en el punto (1, -1, 1)
```
x = 1, y = -1, z = 1

Componente i⃗: 2(1)⁴ + 2(1)²(-1) = 2 - 2 = 0
Componente j⃗: 3(1)(1)² = 3
Componente k⃗: -4(1)(-1)(1) = 4
```

**Respuesta**: ∇×A⃗|(1,-1,1) = 0 i⃗ + 3 j⃗ + 4 k⃗ = 3 j⃗ + 4 k⃗

**Interpretación**: El rotacional en ese punto indica la dirección y magnitud de la "rotación" del campo.

---

### Ejercicio 5: Campo irrotacional

**Enunciado**: Sea el campo vectorial v⃗ = (x + 2y + az) i⃗ + (bx - 3y - z) j⃗ + (4x + cy + 2z) k⃗. Hallar el valor de las constantes a, b y c para que el campo sea irrotacional.

**Solución paso a paso**:

**Paso 1**: Condición de campo irrotacional
∇×v⃗ = 0

**Paso 2**: Identificar componentes
```
vₓ = x + 2y + az
vᵧ = bx - 3y - z
vz = 4x + cy + 2z
```

**Paso 3**: Calcular el rotacional
```
∇×v⃗ = (∂vᵧ/∂y - ∂vᵧ/∂z) i⃗ + (∂vₓ/∂z - ∂vᵧ/∂x) j⃗ + (∂vᵧ/∂x - ∂vₓ/∂y) k⃗
```

**Paso 4**: Calcular cada componente

**Componente i⃗**:
```
∂vᵧ/∂y = ∂(4x + cy + 2z)/∂y = c
∂vᵧ/∂z = ∂(bx - 3y - z)/∂z = -1
Componente i⃗ = c - (-1) = c + 1
```

**Componente j⃗**:
```
∂vₓ/∂z = ∂(x + 2y + az)/∂z = a
∂vᵧ/∂x = ∂(4x + cy + 2z)/∂x = 4
Componente j⃗ = a - 4
```

**Componente k⃗**:
```
∂vᵧ/∂x = ∂(bx - 3y - z)/∂x = b
∂vₓ/∂y = ∂(x + 2y + az)/∂y = 2
Componente k⃗ = b - 2
```

**Paso 5**: Aplicar la condición ∇×v⃗ = 0
```
(c + 1) i⃗ + (a - 4) j⃗ + (b - 2) k⃗ = 0

Esto implica:
c + 1 = 0  →  c = -1
a - 4 = 0  →  a = 4
b - 2 = 0  →  b = 2
```

**Respuesta**: a = 4, b = 2, c = -1

**Verificación**: Con estos valores:
```
v⃗ = (x + 2y + 4z) i⃗ + (2x - 3y - z) j⃗ + (4x - y + 2z) k⃗
∇×v⃗ = 0 ✓
```

**Consecuencia**: Como el campo es irrotacional, es conservativo y deriva de un potencial: v⃗ = -∇φ

---

### Ejercicio 6: Divergencia de un producto

**Enunciado**: Si A⃗ es un vector constante y r⃗ = x i⃗ + y j⃗ + z k⃗, determinar ∇·(r⃗·A⃗).

**Solución paso a paso**:

**Paso 1**: Entender qué es r⃗·A⃗
```
A⃗ = Aₓ i⃗ + Aᵧ j⃗ + Az k⃗ (constante)
r⃗·A⃗ = xAₓ + yAᵧ + zAz = escalar
```

**Paso 2**: Aplicar el gradiente
Como r⃗·A⃗ es un escalar, primero calculamos su gradiente:
```
∇(r⃗·A⃗) = ∂(r⃗·A⃗)/∂x i⃗ + ∂(r⃗·A⃗)/∂y j⃗ + ∂(r⃗·A⃗)/∂z k⃗
        = ∂(xAₓ + yAᵧ + zAz)/∂x i⃗ + ∂(xAₓ + yAᵧ + zAz)/∂y j⃗ + ∂(xAₓ + yAᵧ + zAz)/∂z k⃗
        = Aₓ i⃗ + Aᵧ j⃗ + Az k⃗
        = A⃗
```

**Paso 3**: Interpretar el problema
En realidad, el ejercicio pide ∇·(r⃗·A⃗), pero r⃗·A⃗ es un escalar, no un vector. La divergencia se aplica a vectores.

Hay dos interpretaciones posibles:

**Interpretación 1**: Se pide ∇(r⃗·A⃗)
```
∇(r⃗·A⃗) = A⃗
```

**Interpretación 2**: Se pide ∇·[(r⃗·A⃗)algo], pero el enunciado es ambiguo.

La interpretación más razonable y útil es la primera.

**Respuesta**: ∇(r⃗·A⃗) = A⃗

**Resultado general importante**: Para un vector constante A⃗:
- ∇(r⃗·A⃗) = A⃗
- ∇×(r⃗×A⃗) = 2A⃗
- ∇·r⃗ = 3

---

### Ejercicio 7: Laplaciano

**Enunciado**: Calcular ∇² ln r, donde r = √(x² + y² + z²).

**Solución paso a paso**:

**Paso 1**: Método directo (coordenadas esféricas)

El laplaciano en coordenadas esféricas es:
```
∇²f = (1/r²) ∂/∂r(r² ∂f/∂r) + (1/r²sinθ) ∂/∂θ(sinθ ∂f/∂θ) + (1/r²sin²θ) ∂²f/∂φ²
```

Para f = ln r, que solo depende de r:
```
∇²(ln r) = (1/r²) ∂/∂r(r² ∂(ln r)/∂r)
```

**Paso 2**: Calcular ∂(ln r)/∂r
```
∂(ln r)/∂r = 1/r
```

**Paso 3**: Calcular ∂/∂r(r² · 1/r)
```
∂/∂r(r² · 1/r) = ∂/∂r(r) = 1
```

**Paso 4**: Dividir por r²
```
∇²(ln r) = (1/r²) · 1 = 1/r²
```

**Método alternativo (coordenadas cartesianas)**:

**Paso 1**: Calcular ∂(ln r)/∂x
```
∂(ln r)/∂x = (1/r) · ∂r/∂x = (1/r) · x/r = x/r²
```

**Paso 2**: Calcular ∂²(ln r)/∂x²
Usando la regla del producto:
```
∂²(ln r)/∂x² = ∂/∂x(x/r²)
             = 1/r² + x · ∂/∂x(1/r²)
             = 1/r² + x · (-2/r³) · ∂r/∂x
             = 1/r² - 2x²/r⁴
```

**Paso 3**: Por simetría
```
∂²(ln r)/∂y² = 1/r² - 2y²/r⁴
∂²(ln r)/∂z² = 1/r² - 2z²/r⁴
```

**Paso 4**: Sumar
```
∇²(ln r) = 3/r² - 2(x² + y² + z²)/r⁴
         = 3/r² - 2r²/r⁴
         = 3/r² - 2/r²
         = 1/r²
```

**Respuesta**: ∇²(ln r) = 1/r²

**Nota importante**: Esta función NO es armónica (∇² ≠ 0), excepto en r = ∞.

---

## 📝 Consejos para el Examen

### Estrategias Generales

1. **Conoce las definiciones clave**: El examen suele empezar con preguntas teóricas sobre campos conservativos, solenoidales, etc.

2. **Domina los operadores**: 
   - Gradiente: escalar → vector
   - Divergencia: vector → escalar
   - Rotacional: vector → vector
   - Laplaciano: escalar → escalar

3. **Memoriza los teoremas importantes**:
   - Gauss (relaciona flujo con divergencia)
   - Stokes (relaciona circulación con rotacional)
   - Helmholtz (descomposición de campos)

### Tipos de Problemas Frecuentes

Según los exámenes revisados, los problemas típicos son:

1. **Cálculo de integrales de línea**: Parametriza correctamente y no olvides dr⃗/dt
2. **Determinar constantes para que un campo sea solenoidal/irrotacional**: Calcula divergencia o rotacional e iguala a cero
3. **Calcular rotacional/divergencia en un punto**: Deriva correctamente cada componente
4. **Propiedades de campos**: Demuestra si es conservativo, solenoidal, etc.

### Errores Comunes a Evitar

1. ❌ **Confundir los operadores**: 
   - Gradiente NO es lo mismo que divergencia
   - Rotacional es un vector, divergencia es escalar

2. ❌ **Errores en el cálculo del rotacional**: Recuerda el determinante correctamente
   ```
   | i⃗    j⃗    k⃗   |
   | ∂/∂x ∂/∂y ∂/∂z |
   | Ex   Ey   Ez  |
   ```

3. ❌ **Olvidar dr⃗/dt en integrales de línea**: Siempre parametriza completamente

4. ❌ **No verificar las respuestas**: Si te dicen que un campo es solenoidal con cierta constante, verifica que ∇·E⃗ = 0

### Checklist Antes del Examen

- [ ] Puedo calcular gradiente, divergencia, rotacional y laplaciano
- [ ] Conozco las condiciones para campos conservativos
- [ ] Sé aplicar los teoremas de Gauss y Stokes
- [ ] Puedo parametrizar curvas para integrales de línea
- [ ] Entiendo la diferencia entre circulación y flujo
- [ ] Conozco las propiedades de campos solenoidales e irrotacionales
- [ ] Puedo trabajar con la delta de Dirac
- [ ] Entiendo el concepto de ángulo sólido

### Fórmulas Clave para Memorizar

**Operadores en coordenadas cartesianas**:
```
∇φ = (∂φ/∂x, ∂φ/∂y, ∂φ/∂z)
∇·E⃗ = ∂Ex/∂x + ∂Ey/∂y + ∂Ez/∂z
∇×E⃗ = determinante 3×3
∇²φ = ∂²φ/∂x² + ∂²φ/∂y² + ∂²φ/∂z²
```

**Teoremas**:
```
Gauss: ∮S E⃗·dS⃗ = ∫V (∇·E⃗) dV
Stokes: ∮C E⃗·dr⃗ = ∫S (∇×E⃗)·dS⃗
```

**Identidades**:
```
∇×(∇φ) = 0
∇·(∇×E⃗) = 0
∇×(∇×E⃗) = ∇(∇·E⃗) - ∇²E⃗
```

**Delta de Dirac**:
```
∇²(1/r) = -4πδ(r⃗)
∫ f(x)δ(x-x₀) dx = f(x₀)
```

---

## 🎓 Resumen Final

Los conceptos más importantes de este tema son:

1. **Campos**: Funciones que asignan escalares (campo escalar) o vectores (campo vectorial) a cada punto del espacio

2. **Operadores diferenciales**: Gradiente, divergencia, rotacional y laplaciano son herramientas para analizar campos

3. **Integrales de campo**: Circulación (integral de línea) y flujo (integral de superficie) cuantifican propiedades globales

4. **Teoremas fundamentales**: Gauss y Stokes relacionan integrales de contorno con integrales de volumen/superficie

5. **Clasificación de campos**: Conservativo (∇×E⃗ = 0), solenoidal (∇·E⃗ = 0), armónico (∇²φ = 0), central (E⃗ = f(r)u⃗r)

**¡Practica mucho los ejercicios! La teoría de campos es fundamental para electromagnetismo, mecánica de fluidos y muchas otras áreas de la física.**

---

📖 **Bibliografía recomendada**:
- López Rupérez, F. et al. (1979). La física de los operadores vectoriales diferenciales.
- Conde (2023). Demostraciones intuitivas de los teoremas de Gauss y Stokes.
