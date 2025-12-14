# Tema 3: Potencial Eléctrico y Energía
## Electromagnetismo I

---

## 📚 Índice

1. [Introducción y Objetivos](#introducción-y-objetivos)
2. [Teoría - Conceptos Clave](#teoría---conceptos-clave)
3. [Fórmulas Importantes](#fórmulas-importantes)
4. [Ejercicios Resueltos Paso a Paso](#ejercicios-resueltos-paso-a-paso)
5. [Estrategias para el Examen](#estrategias-para-el-examen)
6. [Consejos del Profesor](#consejos-del-profesor)

---

## Introducción y Objetivos

Hasta ahora hemos trabajado principalmente con el **campo eléctrico** $\vec{E}$, que es una magnitud vectorial. En este tema introduciremos el **potencial eléctrico** (también llamado **potencial escalar**), que nos permitirá describir los mismos fenómenos de manera más sencilla.

### ¿Por qué es importante el potencial?

✅ **Es una cantidad escalar** (no vectorial) → más fácil de calcular
✅ **Simplifica los problemas** → primero calculas φ, luego derivas para obtener E
✅ **Permite calcular energía** → fundamental para entender sistemas de cargas

### Objetivos del Tema

- Entender el significado físico del potencial escalar
- Aprender a calcular el potencial en sistemas discretos y continuos
- Comprender las superficies equipotenciales
- Dominar el concepto de energía potencial eléctrica
- Aplicar estos conceptos a problemas prácticos

---

## Teoría - Conceptos Clave

### 1️⃣ El Potencial Eléctrico

#### Definición

El **potencial eléctrico** φ(r⃗) es una función escalar que se relaciona con el campo eléctrico mediante:

$$\vec{E}(\vec{r}) = -\vec{\nabla}\phi(\vec{r})$$

Es decir, **el campo eléctrico es el gradiente negativo del potencial**.

#### Para cargas puntuales discretas:

$$\phi(\vec{r}) = \sum_{i=1}^{n} \frac{q_i}{4\pi\epsilon_0} \frac{1}{r_{qi}}$$

donde $r_{qi} = |\vec{r} - \vec{r}_i|$ es la distancia desde la carga $q_i$ al punto donde calculamos el potencial.

#### Para distribuciones continuas:

**Volumétrica:**
$$\phi(\vec{r}) = \frac{1}{4\pi\epsilon_0} \int_V \frac{\rho(\vec{r}')}{|\vec{r} - \vec{r}'|} dV'$$

**Superficial:**
$$\phi(\vec{r}) = \frac{1}{4\pi\epsilon_0} \int_S \frac{\sigma(\vec{r}')}{|\vec{r} - \vec{r}'|} dS'$$

**Lineal:**
$$\phi(\vec{r}) = \frac{1}{4\pi\epsilon_0} \int_L \frac{\lambda(\vec{r}')}{|\vec{r} - \vec{r}'|} dl'$$

### 2️⃣ Propiedades del Potencial

#### ✨ El campo eléctrico es conservativo

$$\vec{\nabla} \times \vec{E} = 0$$

Esto implica que la integral de línea es independiente del camino:

$$\oint_C \vec{E} \cdot d\vec{l} = 0$$

#### ✨ El potencial está definido salvo una constante

Normalmente elegimos que φ = 0 en el infinito (A = 0).

**⚠️ EXCEPCIÓN:** Para distribuciones infinitas (como una línea infinita), no podemos poner φ = 0 en el infinito. En estos casos, elegimos otro punto de referencia.

### 3️⃣ Diferencia de Potencial

La **diferencia de potencial** entre dos puntos es:

$$\phi(\vec{r}_2) - \phi(\vec{r}_1) = -\int_1^2 \vec{E} \cdot d\vec{l}$$

Esta expresión es muy útil cuando conocemos E⃗ y queremos calcular φ.

### 4️⃣ Superficies Equipotenciales

Una **superficie equipotencial** es aquella donde φ es constante.

#### Propiedades importantes:

- El campo eléctrico es **perpendicular** a las superficies equipotenciales
- El sentido del campo apunta hacia donde **disminuye el potencial**
- Para una carga puntual, las equipotenciales son **esferas concéntricas**

### 5️⃣ Ecuaciones de Poisson y Laplace

De la ley de Gauss y la relación E⃗ = -∇φ, obtenemos:

**Ecuación de Poisson:**
$$\nabla^2 \phi = -\frac{\rho}{\epsilon_0}$$

**Ecuación de Laplace** (en regiones sin carga):
$$\nabla^2 \phi = 0$$

### 6️⃣ Potencial en Conductores

#### Propiedades fundamentales:

1. **El potencial es constante** en toda la superficie del conductor
2. **El potencial es constante** en todo el interior del conductor
3. **La superficie del conductor es equipotencial**
4. **El campo dentro de una cavidad vacía es cero**

#### Ejemplo: Dos esferas conectadas

Si dos esferas conductoras de radios R₁ y R₂ están conectadas por un cable:

- Tienen el **mismo potencial**: φ₁ = φ₂
- La razón de cargas es: $\frac{Q_1}{Q_2} = \frac{R_1}{R_2}$
- La razón de campos es: $\frac{E_1}{E_2} = \frac{R_2}{R_1}$ ⚡ (¡el campo es mayor en la esfera más pequeña!)

### 7️⃣ Energía Potencial Eléctrica

La **energía potencial** de una carga q en un potencial φ es:

$$U_e(\vec{r}) = q\phi(\vec{r})$$

El **trabajo** para mover una carga del punto a al b es:

$$W_{a \to b} = q(\phi(\vec{r}_b) - \phi(\vec{r}_a)) = q\Delta\phi$$

### 8️⃣ Energía de un Sistema de Cargas

#### Para cargas discretas:

$$U_e = \frac{1}{2} \sum_{i=1}^{N} q_i \phi_i(\vec{r}_i)$$

El factor 1/2 evita contar pares repetidos.

#### Para dos cargas puntuales:

$$U_e = \frac{q_1 q_2}{4\pi\epsilon_0 d}$$

donde d es la distancia entre ellas.

#### Para distribuciones continuas:

**Volumétrica:**
$$U_e = \frac{1}{2} \int_V \rho(\vec{r}) \phi(\vec{r}) dV$$

**Superficial:**
$$U_e = \frac{1}{2} \int_S \sigma(\vec{r}) \phi(\vec{r}) dS$$

**Lineal:**
$$U_e = \frac{1}{2} \int_L \lambda(\vec{r}) \phi(\vec{r}) dl$$

### 9️⃣ Energía en Función del Campo

La energía también se puede expresar en términos del campo eléctrico:

$$U_e = \int \frac{\epsilon_0}{2} |\vec{E}(\vec{r})|^2 dV$$

La **densidad de energía** eléctrica es:

$$u_e(\vec{r}) = \frac{\epsilon_0}{2} |\vec{E}(\vec{r})|^2$$

---

## Fórmulas Importantes

### 📌 Relaciones Fundamentales

| Concepto | Fórmula |
|----------|---------|
| Campo desde potencial | $\vec{E} = -\vec{\nabla}\phi$ |
| Potencial de carga puntual | $\phi = \frac{q}{4\pi\epsilon_0 r}$ |
| Diferencia de potencial | $\Delta\phi = -\int \vec{E} \cdot d\vec{l}$ |
| Energía potencial | $U_e = q\phi$ |
| Energía de dos cargas | $U_e = \frac{q_1 q_2}{4\pi\epsilon_0 d}$ |
| Densidad de energía | $u_e = \frac{\epsilon_0}{2} E^2$ |

### 📌 Resultados Importantes

#### Esfera cargada uniformemente (radio a, carga total q):

**Fuera (r ≥ a):**
$$\phi_{fuera}(r) = \frac{q}{4\pi\epsilon_0 r}$$

**Dentro (r < a):**
$$\phi_{dentro}(r) = \frac{q}{8\pi\epsilon_0 a}\left(3 - \frac{r^2}{a^2}\right)$$

#### Línea infinita (densidad lineal λ):

$$\phi(\rho) = \frac{\lambda}{2\pi\epsilon_0} \ln\frac{\rho_0}{\rho}$$

(ρ₀ es un punto de referencia arbitrario donde φ = 0)

#### Anillo cargado (radio a, carga q, sobre su eje):

$$\phi(x) = \frac{q}{4\pi\epsilon_0\sqrt{x^2 + a^2}}$$

---

## Ejercicios Resueltos Paso a Paso

### 🎯 Ejercicio 1: Campo Electrostático y Potencial

**Enunciado:** Dado el campo $\vec{E} = (yz - 4x)\hat{x} + xz\hat{y} + xy\hat{z}$, ¿podría ser un campo electrostático? Si la respuesta es afirmativa, encontrar el potencial escalar.

#### 📝 Solución Paso a Paso

**Paso 1: Verificar que sea un campo electrostático**

Para que sea un campo electrostático, debe cumplirse que $\vec{\nabla} \times \vec{E} = 0$ (el rotacional debe ser nulo).

Calculamos el rotacional:

$$\vec{\nabla} \times \vec{E} = \begin{vmatrix} \hat{x} & \hat{y} & \hat{z} \\ \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\ yz - 4x & xz & xy \end{vmatrix}$$

Componente x̂:
$$\left(\frac{\partial(xy)}{\partial y} - \frac{\partial(xz)}{\partial z}\right) = x - x = 0$$

Componente ŷ:
$$\left(\frac{\partial(yz-4x)}{\partial z} - \frac{\partial(xy)}{\partial x}\right) = y - y = 0$$

Componente ẑ:
$$\left(\frac{\partial(xz)}{\partial x} - \frac{\partial(yz-4x)}{\partial y}\right) = z - z = 0$$

✅ **Conclusión:** Como $\vec{\nabla} \times \vec{E} = 0$, SÍ es un campo electrostático.

**Paso 2: Encontrar el potencial**

Sabemos que $\vec{E} = -\vec{\nabla}\phi$, entonces:

$$E_x = -\frac{\partial \phi}{\partial x} = yz - 4x$$

Integrando respecto a x:
$$\phi = -\int (yz - 4x)dx = -xyz + 2x^2 + f(y,z)$$

Ahora usamos la componente y:
$$E_y = -\frac{\partial \phi}{\partial y} = xz$$

$$-\frac{\partial}{\partial y}(-xyz + 2x^2 + f(y,z)) = xz$$
$$xz - \frac{\partial f}{\partial y} = xz$$

Por lo tanto: $\frac{\partial f}{\partial y} = 0$ → f no depende de y, f = f(z)

Finalmente, usando la componente z:
$$E_z = -\frac{\partial \phi}{\partial z} = xy$$

$$-\frac{\partial}{\partial z}(-xyz + 2x^2 + f(z)) = xy$$
$$xy - \frac{df}{dz} = xy$$

Por lo tanto: $\frac{df}{dz} = 0$ → f = constante

✅ **Respuesta:** $\phi = -xyz + 2x^2 + C$

---

### 🎯 Ejercicio 2: Campo Eléctrico desde Potencial

**Enunciado:** Dado un potencial escalar $\phi = 4x^2 - 3y^2$ en una cierta región del espacio, calcular el campo eléctrico en el punto P = (-2, -4, 6).

#### 📝 Solución Paso a Paso

**Paso 1: Calcular el campo eléctrico**

Usamos la relación $\vec{E} = -\vec{\nabla}\phi$:

$$E_x = -\frac{\partial \phi}{\partial x} = -\frac{\partial}{\partial x}(4x^2 - 3y^2) = -8x$$

$$E_y = -\frac{\partial \phi}{\partial y} = -\frac{\partial}{\partial y}(4x^2 - 3y^2) = 6y$$

$$E_z = -\frac{\partial \phi}{\partial z} = 0$$

Por lo tanto: $\vec{E} = -8x\hat{x} + 6y\hat{y}$

**Paso 2: Evaluar en P = (-2, -4, 6)**

$$E_x = -8(-2) = 16$$
$$E_y = 6(-4) = -24$$
$$E_z = 0$$

✅ **Respuesta:** $\vec{E} = 16\hat{x} - 24\hat{y}$ V/m

---

### 🎯 Ejercicio 3: Potencial y Trabajo con Dos Cargas

**Enunciado:** Tenemos dos cargas puntuales:
- q₁ = 2 μC en el origen (0, 0, 0)
- q₂ = -5 μC en (0, 3, 0) m

a) Calcula el potencial eléctrico en el punto P situado en (4, 0, 0) m
b) ¿Qué trabajo se necesita para llevar una carga de 4 μC desde el infinito al punto P?

#### 📝 Solución Paso a Paso

**Paso 1: Calcular las distancias**

Distancia de q₁ a P:
$$r_1 = \sqrt{(4-0)^2 + (0-0)^2 + (0-0)^2} = 4 \text{ m}$$

Distancia de q₂ a P:
$$r_2 = \sqrt{(4-0)^2 + (0-3)^2 + (0-0)^2} = \sqrt{16 + 9} = 5 \text{ m}$$

**Paso 2: Calcular el potencial en P**

El potencial es la suma de las contribuciones de ambas cargas:

$$\phi_P = \frac{1}{4\pi\epsilon_0}\left(\frac{q_1}{r_1} + \frac{q_2}{r_2}\right)$$

Usando $\frac{1}{4\pi\epsilon_0} = 9 \times 10^9$ N·m²/C²:

$$\phi_P = 9 \times 10^9 \left(\frac{2 \times 10^{-6}}{4} + \frac{-5 \times 10^{-6}}{5}\right)$$

$$\phi_P = 9 \times 10^9 \left(\frac{2 \times 10^{-6}}{4} - \frac{5 \times 10^{-6}}{5}\right)$$

$$\phi_P = 9 \times 10^9 \left(0.5 \times 10^{-6} - 1.0 \times 10^{-6}\right)$$

$$\phi_P = 9 \times 10^9 \times (-0.5 \times 10^{-6})$$

$$\phi_P = -4.5 \times 10^3 = -4500 \text{ V}$$

✅ **Respuesta a):** φₚ = -4.5 × 10³ V

**Paso 3: Calcular el trabajo**

El trabajo para traer una carga q desde el infinito (donde φ = 0) hasta P es:

$$W = q(\phi_P - \phi_\infty) = q \cdot \phi_P$$

$$W = 4 \times 10^{-6} \times (-4.5 \times 10^3)$$

$$W = -18 \times 10^{-3} = -0.018 \text{ J}$$

✅ **Respuesta b):** W = -18 × 10⁻³ J

**💡 Interpretación física:**
El trabajo es negativo porque el campo hace trabajo sobre la carga (la atrae). No necesitamos realizar trabajo externo; de hecho, el sistema libera energía.

---

### 🎯 Ejercicio 4: Potencial de un Cilindro Conductor Infinito

**Enunciado:** Encuentra el potencial de un cilindro conductor infinito con densidad de carga lineal λ. El radio del cilindro es R.

#### 📝 Solución Paso a Paso

**Paso 1: Calcular el campo eléctrico**

Para un cilindro infinito, por simetría y usando la ley de Gauss, el campo eléctrico fuera del cilindro (ρ > R) es:

$$\vec{E} = \frac{\lambda}{2\pi\epsilon_0 \rho}\hat{\rho}$$

Dentro del conductor (ρ < R), el campo es cero: E = 0

**Paso 2: Calcular el potencial usando la diferencia de potencial**

Usamos: $\phi(\rho_1) - \phi(\rho_2) = -\int_{\rho_2}^{\rho_1} \vec{E} \cdot d\vec{l}$

En coordenadas cilíndricas: $d\vec{l} = d\rho\hat{\rho}$

$$\phi(\rho) - \phi(R) = -\int_R^\rho \frac{\lambda}{2\pi\epsilon_0 \rho'} d\rho'$$

$$\phi(\rho) - \phi(R) = -\frac{\lambda}{2\pi\epsilon_0} \int_R^\rho \frac{d\rho'}{\rho'}$$

$$\phi(\rho) - \phi(R) = -\frac{\lambda}{2\pi\epsilon_0} [\ln\rho']_R^\rho$$

$$\phi(\rho) - \phi(R) = -\frac{\lambda}{2\pi\epsilon_0} (\ln\rho - \ln R)$$

$$\phi(\rho) = \phi(R) - \frac{\lambda}{2\pi\epsilon_0} \ln\frac{\rho}{R}$$

**Paso 3: Simplificar**

Si elegimos φ(R) = 0 como referencia (potencial cero en la superficie):

$$\phi(\rho) = -\frac{\lambda}{2\pi\epsilon_0} \ln\frac{\rho}{R} = \frac{\lambda}{2\pi\epsilon_0} \ln\frac{R}{\rho}$$

✅ **Respuesta:** $\phi(\rho) = \frac{\lambda}{2\pi\epsilon_0} \ln\frac{R}{\rho}$ (para ρ ≥ R)

**💡 Nota importante:** No podemos poner φ = 0 en el infinito porque daría φ = ∞ en cualquier punto finito. Por eso elegimos la referencia en la superficie del cilindro.

---

### 🎯 Ejercicio 5: Línea de Carga Finita

**Enunciado:** Tenemos una línea de carga finita de longitud L, con densidad de carga lineal λ y carga total Q = λL. La línea se encuentra a lo largo del eje x. Calcular el potencial eléctrico en un punto P sobre el eje y, a una distancia d de la línea.

#### 📝 Solución Paso a Paso

**Paso 1: Configurar el problema**

- Línea de carga: desde x = -L/2 hasta x = L/2
- Punto P: (0, d, 0)
- Elemento de carga: dq = λ dx

**Paso 2: Calcular la distancia de cada elemento a P**

Para un elemento en posición x sobre el eje x, la distancia a P es:

$$r = \sqrt{x^2 + d^2}$$

**Paso 3: Calcular el potencial**

$$\phi = \frac{1}{4\pi\epsilon_0} \int \frac{dq}{r}$$

$$\phi = \frac{\lambda}{4\pi\epsilon_0} \int_{-L/2}^{L/2} \frac{dx}{\sqrt{x^2 + d^2}}$$

**Paso 4: Resolver la integral**

Esta es una integral estándar: $\int \frac{dx}{\sqrt{x^2 + a^2}} = \ln(x + \sqrt{x^2 + a^2}) + C$

$$\phi = \frac{\lambda}{4\pi\epsilon_0} \left[\ln(x + \sqrt{x^2 + d^2})\right]_{-L/2}^{L/2}$$

$$\phi = \frac{\lambda}{4\pi\epsilon_0} \left[\ln\left(\frac{L}{2} + \sqrt{\frac{L^2}{4} + d^2}\right) - \ln\left(-\frac{L}{2} + \sqrt{\frac{L^2}{4} + d^2}\right)\right]$$

$$\phi = \frac{\lambda}{4\pi\epsilon_0} \ln\left(\frac{\frac{L}{2} + \sqrt{\frac{L^2}{4} + d^2}}{-\frac{L}{2} + \sqrt{\frac{L^2}{4} + d^2}}\right)$$

Multiplicando numerador y denominador por 2:

$$\phi = \frac{\lambda}{4\pi\epsilon_0} \ln\left(\frac{L + \sqrt{L^2 + 4d^2}}{-L + \sqrt{L^2 + 4d^2}}\right)$$

**Paso 5: Simplificar usando Q = λL**

$$\phi = \frac{Q}{4\pi\epsilon_0 L} \ln\left(\frac{L + \sqrt{L^2 + 4d^2}}{2d}\right)$$

✅ **Respuesta:** $\phi = \frac{Q}{4\pi\epsilon_0 L} \ln\frac{L + \sqrt{L^2 + d^2}}{d}$

**💡 Verificación:** Si L → ∞, recuperamos el resultado de la línea infinita (con logaritmo).

---

### 🎯 Ejercicio 6: Disco Cargado Uniformemente

**Enunciado:** Tenemos un disco cargado uniformemente con densidad superficial σ. El disco tiene radio a y su eje coincide con el eje x. Calcular:
a) El potencial en un punto P sobre el eje x
b) El campo eléctrico en ese punto

#### 📝 Solución Paso a Paso

**Paso 1: Configurar el problema con simetría**

Por simetría circular, usamos coordenadas cilíndricas (r', φ'):
- Elemento de superficie: dS = r' dr' dφ'
- Elemento de carga: dq = σ dS = σ r' dr' dφ'
- Distancia del elemento a P(x, 0, 0): $\sqrt{x^2 + r'^2}$

**Paso 2: Calcular el potencial**

$$\phi(x) = \frac{1}{4\pi\epsilon_0} \int \frac{dq}{\sqrt{x^2 + r'^2}}$$

$$\phi(x) = \frac{\sigma}{4\pi\epsilon_0} \int_0^{2\pi} d\phi' \int_0^a \frac{r' dr'}{\sqrt{x^2 + r'^2}}$$

La integral en φ' es trivial: $\int_0^{2\pi} d\phi' = 2\pi$

$$\phi(x) = \frac{\sigma}{2\epsilon_0} \int_0^a \frac{r' dr'}{\sqrt{x^2 + r'^2}}$$

**Paso 3: Resolver la integral**

Usamos la sustitución u = x² + r'², entonces du = 2r' dr'

$$\int \frac{r' dr'}{\sqrt{x^2 + r'^2}} = \frac{1}{2}\int \frac{du}{\sqrt{u}} = \sqrt{u} = \sqrt{x^2 + r'^2}$$

$$\phi(x) = \frac{\sigma}{2\epsilon_0} \left[\sqrt{x^2 + r'^2}\right]_0^a$$

$$\phi(x) = \frac{\sigma}{2\epsilon_0} \left(\sqrt{x^2 + a^2} - |x|\right)$$

Para x > 0 (donde está P):

✅ **Respuesta a):** $\phi(x) = \frac{\sigma}{2\epsilon_0}(\sqrt{x^2 + a^2} - x)$

**Paso 4: Calcular el campo eléctrico**

Por simetría, solo hay componente en x:

$$E_x = -\frac{\partial \phi}{\partial x}$$

$$E_x = -\frac{\sigma}{2\epsilon_0}\left(\frac{x}{\sqrt{x^2 + a^2}} - 1\right)$$

$$E_x = \frac{\sigma}{2\epsilon_0}\left(1 - \frac{x}{\sqrt{x^2 + a^2}}\right)$$

✅ **Respuesta b):** $\vec{E} = \frac{\sigma}{2\epsilon_0}\left(1 - \frac{x}{\sqrt{x^2 + a^2}}\right)\hat{x}$

**💡 Verificación:**
- Si x → 0 (centro del disco): $E = \frac{\sigma}{2\epsilon_0}$ ✓
- Si x → ∞ (muy lejos): $E \to 0$ ✓
- Si a → ∞ (plano infinito): $E = \frac{\sigma}{2\epsilon_0}$ ✓

---

### 🎯 Ejercicio 7: Esfera Conductora con Cavidad

**Enunciado:** Tenemos una esfera conductora de radio R que tiene una cavidad central de radio a. En el centro de la cavidad hay una carga puntual Q positiva. Calcular el potencial para:
a) r ≥ R
b) a ≤ r ≤ R
c) r < a

#### 📝 Solución Paso a Paso

**Paso 1: Analizar la distribución de cargas**

- Carga +Q en el centro
- En la superficie interna (r = a): se induce carga -Q (uniformemente distribuida)
- En la superficie externa (r = R): se distribuye carga +Q (uniformemente distribuida)
- Dentro del conductor (a < r < R): E = 0

**Paso 2: Calcular el campo eléctrico en cada región**

**Región I (r ≥ R):** Por ley de Gauss
$$E = \frac{Q}{4\pi\epsilon_0 r^2}$$

**Región II (a ≤ r ≤ R):** Dentro del conductor
$$E = 0$$

**Región III (r < a):** Por ley de Gauss (solo ve la carga central)
$$E = \frac{Q}{4\pi\epsilon_0 r^2}$$

**Paso 3: Calcular potenciales**

**a) Para r ≥ R:**

Desde el infinito hasta r:
$$\phi(r) = -\int_\infty^r E \, dr' = \frac{Q}{4\pi\epsilon_0} \int_\infty^r \frac{dr'}{r'^2} = \frac{Q}{4\pi\epsilon_0 r}$$

✅ **Respuesta a):** $\phi(r) = \frac{Q}{4\pi\epsilon_0 r}$ (como una carga puntual)

**b) Para a ≤ r ≤ R:**

El conductor es equipotencial, así que φ = constante = φ(R):

✅ **Respuesta b):** $\phi = \frac{Q}{4\pi\epsilon_0 R}$ (constante en todo el conductor)

**c) Para r < a:**

Desde el infinito hasta R, luego de R hasta a (E=0), y finalmente de a hasta r:

$$\phi(r) = \phi(R) + \int_a^r E \, dr'$$

Como $\phi(R) = \frac{Q}{4\pi\epsilon_0 R}$ y dentro de la cavidad $E = \frac{Q}{4\pi\epsilon_0 r'^2}$:

$$\phi(r) = \frac{Q}{4\pi\epsilon_0 R} - \int_a^r \frac{Q}{4\pi\epsilon_0 r'^2} dr'$$

$$\phi(r) = \frac{Q}{4\pi\epsilon_0 R} + \frac{Q}{4\pi\epsilon_0}\left[\frac{1}{r'}\right]_a^r$$

$$\phi(r) = \frac{Q}{4\pi\epsilon_0 R} + \frac{Q}{4\pi\epsilon_0}\left(\frac{1}{r} - \frac{1}{a}\right)$$

$$\phi(r) = \frac{Q}{4\pi\epsilon_0}\left(\frac{1}{R} + \frac{1}{r} - \frac{1}{a}\right)$$

✅ **Respuesta c):** $\phi(r) = \frac{Q}{4\pi\epsilon_0}\left(\frac{1}{R} + \frac{1}{r} - \frac{1}{a}\right)$

**💡 Gráfica del potencial:**
- En r = 0: máximo
- Decrece de 0 a a
- Constante de a a R
- Decrece de R a ∞

---

### 🎯 Ejercicio 8: Energía de una Esfera Conductora

**Enunciado:** Tenemos una esfera conductora de radio a con carga total Q. Calcular la energía potencial dentro y fuera de la esfera.

#### 📝 Solución Paso a Paso

**Paso 1: Recordar la distribución de carga**

En un conductor en equilibrio:
- Toda la carga está en la superficie
- El campo dentro es E = 0
- El potencial dentro es constante

**Paso 2: Calcular la energía usando densidad de energía**

La densidad de energía es:
$$u_e = \frac{\epsilon_0}{2}E^2$$

**Dentro de la esfera (r < a):**

Como E = 0:
$$U_{dentro} = \int_0^a \frac{\epsilon_0}{2} \times 0^2 \times 4\pi r^2 dr = 0$$

✅ **Respuesta:** $U_{dentro} = 0$

**Fuera de la esfera (r > a):**

El campo fuera es: $E = \frac{Q}{4\pi\epsilon_0 r^2}$

$$U_{fuera} = \int_a^\infty \frac{\epsilon_0}{2} \left(\frac{Q}{4\pi\epsilon_0 r^2}\right)^2 4\pi r^2 dr$$

$$U_{fuera} = \int_a^\infty \frac{\epsilon_0}{2} \times \frac{Q^2}{16\pi^2\epsilon_0^2 r^4} \times 4\pi r^2 dr$$

$$U_{fuera} = \frac{Q^2}{8\pi\epsilon_0} \int_a^\infty \frac{dr}{r^2}$$

$$U_{fuera} = \frac{Q^2}{8\pi\epsilon_0} \left[-\frac{1}{r}\right]_a^\infty$$

$$U_{fuera} = \frac{Q^2}{8\pi\epsilon_0} \times \frac{1}{a}$$

✅ **Respuesta:** $U_{fuera} = \frac{Q^2}{8\pi\epsilon_0 a}$

**💡 Interpretación física:**
Toda la energía está almacenada en el campo eléctrico fuera del conductor. Esta es la energía necesaria para ensamblar la esfera cargada.

---

## Estrategias para el Examen

### 🎓 Análisis de Exámenes Típicos

Basándome en los exámenes de Electromagnetismo I, estos son los tipos de problemas que suelen aparecer:

#### 1️⃣ **Verificar si un campo es electrostático**
- ✅ Calcular $\vec{\nabla} \times \vec{E}$
- ✅ Si es cero, es conservativo → es electrostático
- ✅ Luego encontrar φ integrando componentes

#### 2️⃣ **Calcular potencial de configuraciones simples**
- Cargas puntuales: suma directa
- Distribuciones continuas: integración cuidadosa
- Usar simetrías para simplificar

#### 3️⃣ **Calcular trabajo y energía**
- Trabajo = q × Δφ
- Energía de sistema: usar fórmulas apropiadas
- Cuidado con el factor 1/2 en sistemas

### 📋 Checklist para Resolver Problemas

#### ✅ Antes de empezar:
1. **Identificar el tipo de problema** (potencial → campo, campo → potencial, energía, etc.)
2. **Dibujar un esquema** con todas las cargas y puntos relevantes
3. **Identificar simetrías** (esférica, cilíndrica, planar)
4. **Elegir el sistema de coordenadas** apropiado

#### ✅ Durante la resolución:
1. **Escribir las ecuaciones fundamentales** que vas a usar
2. **Hacer los cálculos paso a paso**, sin saltarte pasos
3. **Llevar las unidades** siempre que sea posible
4. **Verificar dimensionalmente** tus resultados

#### ✅ Al finalizar:
1. **Verificar el signo** (¿tiene sentido físico?)
2. **Verificar límites** (¿qué pasa cuando r→∞, r→0, etc.?)
3. **Verificar unidades** (Voltios para φ, N/C o V/m para E, Julios para U)
4. **Comparar con casos conocidos**

### ⚡ Errores Comunes a Evitar

| ❌ Error Común | ✅ Solución |
|----------------|-------------|
| Olvidar el signo negativo en E = -∇φ | Siempre recordar el menos |
| No usar el factor 1/2 en energía de sistemas | Revisar si es energía de sistema o de una sola carga |
| Poner φ = 0 en ∞ para distribuciones infinitas | Elegir otro punto de referencia |
| Confundir potencial con energía potencial | U = qφ (no son lo mismo) |
| Olvidar que los conductores son equipotenciales | φ = constante en toda la superficie |
| Sumar mal contribuciones de varias cargas | Cuidado con los signos de las cargas |

### 🔑 Fórmulas Clave que Debes Memorizar

**Absolutamente esenciales:**
```
E⃗ = -∇φ
φ = q/(4πε₀r)  [carga puntual]
Ue = qφ
Ue(dos cargas) = q₁q₂/(4πε₀d)
ue = (ε₀/2)E²
```

**Muy útiles:**
```
φ(esfera, fuera) = q/(4πε₀r)
φ(esfera, dentro) = (q/8πε₀a)(3 - r²/a²)
E(línea infinita) = λ/(2πε₀ρ)
E(plano infinito) = σ/(2ε₀)
```

### 📊 Prioridades de Estudio

**⭐⭐⭐ Prioridad Alta:**
- Relación E⃗ = -∇φ (saber usarla en ambas direcciones)
- Potencial de cargas puntuales
- Energía potencial y trabajo
- Propiedades de conductores
- Cálculo de potencial por integración

**⭐⭐ Prioridad Media:**
- Superficies equipotenciales
- Ecuaciones de Poisson y Laplace
- Energía en función del campo
- Distribuciones específicas (esfera, línea, disco)

**⭐ Prioridad Baja:**
- Aplicaciones históricas (Van de Graaf, Millikan)
- Detalles de cálculos complejos
- Casos muy específicos

---

## Consejos del Profesor

### 💡 Conceptos que Debes Entender Profundamente

1. **El potencial es más fácil que el campo**
   - φ es escalar → una sola componente
   - E⃗ es vectorial → tres componentes
   - Estrategia: calcula φ primero, luego deriva para obtener E⃗

2. **El campo eléctrico es conservativo**
   - El trabajo solo depende de los puntos inicial y final
   - La integral de línea es independiente del camino
   - Esto es fundamental para definir el potencial

3. **Las superficies equipotenciales y las líneas de campo son perpendiculares**
   - Dibuja las dos cosas para visualizar el problema
   - Donde las equipotenciales están más juntas, el campo es más intenso

4. **Los conductores son equipotenciales**
   - Todo el conductor (superficie + interior) está al mismo potencial
   - Esto simplifica enormemente muchos problemas

### 🎯 Estrategias de Cálculo

**Para calcular potencial:**
1. **Si conoces las cargas:** Usa las fórmulas de integración directa
2. **Si conoces E⃗:** Usa $\Delta\phi = -\int \vec{E} \cdot d\vec{l}$
3. **Con simetría alta:** Usa ecuaciones de Laplace/Poisson

**Para calcular energía:**
1. **Sistema discreto pequeño:** Suma de pares
2. **Distribución continua:** Integral $U_e = \frac{1}{2}\int \rho \phi dV$
3. **Si conoces E⃗:** Usa $U_e = \int \frac{\epsilon_0}{2}E^2 dV$

### 📝 Cómo Estudiar Este Tema

1. **Día 1-2:** Teoría y conceptos fundamentales
   - Lee las secciones de teoría
   - Entiende las relaciones entre φ, E⃗, y Ue
   - Haz esquemas y dibujos

2. **Día 3-4:** Ejercicios básicos
   - Ejercicios 1, 2, 3 (campo ↔ potencial)
   - Practica derivar e integrar
   - Asegúrate de entender los signos

3. **Día 5-6:** Ejercicios intermedios
   - Ejercicios 4, 5, 6 (distribuciones continuas)
   - Practica las integrales típicas
   - Trabaja con diferentes sistemas de coordenadas

4. **Día 7-8:** Ejercicios avanzados y repaso
   - Ejercicios 7, 8, 9, 10 (conductores y energía)
   - Problemas de exámenes anteriores
   - Repasa las fórmulas clave

### 🔬 Intuición Física

**El potencial es "altura eléctrica"**
- Como la altura gravitatoria h
- Una carga positiva "cae" hacia potencial menor
- Una carga negativa "cae" hacia potencial mayor

**El trabajo es cambio de energía potencial**
- W = q × Δφ (como W = mg × Δh)
- Si W > 0: debes empujar la carga
- Si W < 0: el campo hace el trabajo

**La energía está en el campo**
- No está "en las cargas"
- Está distribuida en el espacio donde hay campo
- Densidad: $u_e = \frac{\epsilon_0}{2}E^2$

### 🎓 Preparación Final para el Examen

**Una semana antes:**
- ✅ Repasa toda la teoría
- ✅ Haz todos los ejercicios del tema
- ✅ Resuelve al menos 2 exámenes completos

**Un día antes:**
- ✅ Repasa las fórmulas clave
- ✅ Repasa los ejercicios que te costaron más
- ✅ Duerme bien (¡esto es importante!)

**Durante el examen:**
- ✅ Lee todo el examen primero
- ✅ Empieza por los problemas que te parezcan más fáciles
- ✅ Escribe todas las ecuaciones que uses
- ✅ Revisa las unidades y los signos
- ✅ Si tienes tiempo, verifica tus resultados

---

## Referencias y Material Complementario

### 📚 Referencias Bibliográficas

1. **Gillermo Terán Acosta, V. C. C. (2017).** Diseño y construcción de un prototipo de superficies equipotenciales como proceso de enseñanza investigadora.

2. **Julio Enrique Duarte, J. S. M. y. F. H. F. M. (2005).** Potencial de los campos eléctricos para la manipulación de microorganismos. *Revista UIS ingenierías*, 4(1), 53–63.

3. **Rodríguez, María A and Niaz, Mansoor (2001).** Experimento de la gota de aceite en manuales de laboratorio de física: una perspectiva basada en la historia y filosofía de la ciencia. *Journal of Science Education*, 2(2), 81.

### 🎬 Recursos Adicionales

- **Generador de Van de Graaf:** Busca videos explicativos sobre cómo funciona este generador electrostático
- **Experimento de Millikan:** Investiga cómo este experimento demostró la cuantización de la carga

---

## Resumen Final - Lo Más Importante

### 🎯 Las 10 Ideas Clave del Tema

1. **E⃗ = -∇φ** → El campo es el gradiente negativo del potencial
2. **φ es escalar** → Más fácil de calcular que E⃗
3. **El campo E⃗ es conservativo** → ∇ × E⃗ = 0
4. **Diferencia de potencial** → Δφ = -∫E⃗·dl⃗
5. **Superficies equipotenciales ⊥ E⃗** → Perpendiculares al campo
6. **Conductores son equipotenciales** → φ = constante
7. **Energía potencial** → Ue = qφ
8. **Trabajo** → W = qΔφ
9. **Energía de sistema** → Factor 1/2 para evitar repeticiones
10. **Densidad de energía** → ue = (ε₀/2)E²

### ✨ Tu Resumen de Una Página

**Potencial eléctrico:**
- φ = Σ qi/(4πε₀ri) [discretas]
- φ = ∫ ρdV/(4πε₀r) [continuas]
- E⃗ = -∇φ

**Energía:**
- Ue = qφ [una carga]
- Ue = (1/2)Σ qiφi [sistema]
- ue = (ε₀/2)E² [densidad]

**Conductores:**
- φ = constante
- E⃗superficie ⊥ superficie
- Qinterior = 0

**Para el examen:**
- Verifica ∇ × E⃗ = 0
- Usa simetrías
- Revisa signos y unidades
- Factor 1/2 en energía de sistemas

---

## ¡Mucho Éxito! 🚀

Recuerda: el potencial eléctrico es una herramienta poderosa que simplifica enormemente los problemas de electrostática. Domina los conceptos básicos, practica los ejercicios, y estarás perfectamente preparado para el examen.

**¡Ánimo y a por todas!** 💪⚡

---

*Estos apuntes han sido preparados como guía de estudio para Electromagnetismo I - Tema 3. Para dudas específicas, consulta con tu profesor o en las tutorías.*
