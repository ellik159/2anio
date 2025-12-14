# Tema 3: Sistemas de Partículas - Teoría de Campos

## 📚 Resumen de Teoría - Conceptos Clave

### 1. Sistema de Partículas

Un **sistema de partículas** es un conjunto de puntos materiales en interacción entre sí, separados del resto del universo por una pared real o imaginaria.

**Fuerzas en el sistema:**
- **Fuerzas externas** (F⃗ᵢ): Ejercidas por elementos externos al sistema
- **Fuerzas internas** (f⃗ᵢⱼ): Ejercidas entre las partículas del sistema

---

### 2. Momento Lineal del Sistema

#### Definición
El momento lineal de un sistema es la suma vectorial de los momentos lineales de todas sus partículas:

```
p⃗ = Σᵢ p⃗ᵢ = Σᵢ mᵢv⃗ᵢ
```

#### Segunda Ley de Newton para Sistemas
```
F⃗ = dp⃗/dt
```

Donde F⃗ es la resultante de todas las fuerzas **exteriores** (las fuerzas internas se cancelan si obedecen la ley de acción y reacción).

#### ⭐ Principio de Conservación del Momento Lineal
**Si F⃗ = 0 (sistema aislado) ⟹ p⃗ = constante**

---

### 3. Centro de Masas (CM)

#### Definición
El centro de masas es el punto cuya posición R⃗ es el promedio de las posiciones de las partículas, pesadas por sus masas:

```
R⃗ = (Σᵢ mᵢr⃗ᵢ) / M
```

Donde M = Σᵢ mᵢ es la masa total del sistema.

#### Propiedades Importantes del CM

1. **El momento del CM coincide con el momento del sistema:**
   ```
   MV⃗ = p⃗
   ```

2. **Segunda ley para el CM:**
   ```
   F⃗ = M(dV⃗/dt)
   ```
   El CM se mueve como si toda la masa estuviera concentrada en él.

3. **En el sistema de referencia del CM:**
   ```
   Σᵢ mᵢv⃗'ᵢ = 0
   ```
   La suma de momentos es cero.

4. **Si el sistema está aislado (F⃗ = 0):**
   - El CM se mueve con velocidad constante (MRU)

---

### 4. Sistemas de Masa Variable: Ecuación del Cohete

Para un cohete que eyecta gases con velocidad V respecto al cohete:

```
m(dv/dt) = -V(dm/dt) + Fₑₓₜ
```

**Sin fuerzas externas** (espacio exterior):
```
v = v₀ - V·ln(m/m₀)
```

**Velocidad máxima** (cuando m = M₀, masa útil):
```
vₘₐₓ = v₀ - V·ln(1 + M/M₀)
```

Donde M es la masa inicial de combustible.

**⚠️ Conclusión importante:** Para que vₘₐₓ >> V (velocidad de eyección), se necesita M ≫ M₀ (mucho combustible).

---

### 5. Momento Angular del Sistema

#### Definición
```
L⃗ = Σᵢ (r⃗ᵢ × p⃗ᵢ)
```

#### Ecuación del Movimiento
```
N⃗ₑₓₜ = dL⃗/dt
```

Donde N⃗ₑₓₜ es el momento de las fuerzas exteriores. Las fuerzas internas no contribuyen si obedecen la **tercera ley de Newton en su forma fuerte** (fuerzas iguales, opuestas y sobre la línea que une las partículas).

#### ⭐ Conservación del Momento Angular
**Si N⃗ₑₓₜ = 0 ⟹ L⃗ = constante**

---

### 6. Momento Angular Orbital e Interno (Espín)

El momento angular se descompone en:

```
L⃗ = L⃗orbital + S⃗
L⃗ = R⃗ × MV⃗ + Σᵢ(r⃗'ᵢ × mᵢv⃗'ᵢ)
```

Donde:
- **L⃗orbital**: Momento angular del CM respecto al origen
- **S⃗** (espín): Momento angular interno (suma de momentos respecto al CM)

#### Casos especiales donde S⃗ = 0:
1. Movimiento radial puro (r⃗'ᵢ ∥ v⃗'ᵢ)
2. Traslación pura (v⃗'ᵢ = 0, todas las partículas se mueven con el CM)

#### Momento respecto al CM
```
N⃗ₒₘ = dS⃗/dt
```

---

### 7. Masa Reducida (Problema de Dos Cuerpos)

Para dos partículas interactuando sin fuerzas externas:

```
μ = (m₁m₂)/(m₁ + m₂)
```

**Ecuación del movimiento relativo:**
```
F⃗₁₂ = μa⃗ᵣ
```

**Posiciones respecto al CM:**
```
r⃗'₁ = (m₂/(m₁ + m₂))r⃗     (proporcional a m₂)
r⃗'₂ = -(m₁/(m₁ + m₂))r⃗    (proporcional a m₁)
```

**Momentos respecto al CM:**
```
p⃗'₁ = μv⃗ = -p⃗'₂
```

---

### 8. Energía Cinética del Sistema

La energía cinética se descompone en:

```
Eₖ = EₖCM + Eₖinterna

Eₖ = (1/2)MV² + Σᵢ(1/2)mᵢv'ᵢ²
```

Donde:
- **EₖCM**: Energía del CM (como si toda la masa estuviera en él)
- **Eₖinterna**: Energía del movimiento relativo al CM

---

### 9. Trabajo y Energía

#### Teorema del Trabajo y Energía Cinética
```
Wₑₓₜ + Wᵢₙₜ = ΔEₖ
```

#### Para Fuerzas Conservativas
Si las fuerzas derivan de una energía potencial:
```
Wₑₓₜ = -ΔU    ⟹    ΔEₖ + ΔU = -Wᵢₙₜ
```

#### ⭐ Conservación de la Energía Mecánica
**Si las fuerzas internas son conservativas** (Wᵢₙₜ = 0):
```
Eₘₑ꜀ = Eₖ + U = constante
```

---

### 10. Energía Propia e Interna

**Energía propia** E₀: Energía del sistema en el sistema de referencia del CM
```
E₀ = Eₖinterna + Uinterna
```

**Energía interna** Eᵢₙₜ: Para sistemas en reposo (V⃗ = 0)
```
Eᵢₙₜ = E₀
```

---

## 🎯 Principios de Conservación - Resumen

| Magnitud | Condición de Conservación | Ecuación |
|----------|---------------------------|----------|
| **Momento Lineal** | F⃗ₑₓₜ = 0 | p⃗ = constante |
| **Momento Angular** | N⃗ₑₓₜ = 0 | L⃗ = constante |
| **Energía Mecánica** | Fuerzas conservativas + Sistema aislado | E = constante |

Estos teoremas son tan importantes que han sido elevados a la categoría de **principios y postulados** en física.

---

## 📝 Ejercicios Resueltos Paso a Paso

### Ejercicio 1: Retroceso de una Escopeta

**Enunciado:** Una escopeta de masa 5.8 kg dispara una bala de 20 g de masa, con una velocidad de 2700 km/h. Calcular la velocidad de retroceso de la escopeta.

#### Solución paso a paso:

**Paso 1: Identificar el sistema y el principio a usar**
- Sistema: escopeta + bala
- Sistema aislado ⟹ Conservación del momento lineal
- Inicialmente todo está en reposo: p⃗ᵢₙᵢ꜀ᵢₐₗ = 0

**Paso 2: Convertir unidades**
```
m_bala = 20 g = 0.02 kg
m_escopeta = 5.8 kg
v_bala = 2700 km/h = 2700/3.6 m/s = 750 m/s
```

**Paso 3: Aplicar conservación del momento lineal**
```
p⃗ᵢₙᵢ꜀ᵢₐₗ = p⃗fᵢₙₐₗ
0 = m_bala·v_bala + m_escopeta·v_escopeta
```

**Paso 4: Despejar la velocidad de retroceso**
```
v_escopeta = -(m_bala·v_bala)/m_escopeta
v_escopeta = -(0.02 kg × 750 m/s)/(5.8 kg)
v_escopeta = -15/5.8 = -2.59 m/s
```

**Resultado:** La escopeta retrocede a **2.59 m/s** (el signo negativo indica sentido opuesto a la bala).

**💡 Consejo:** En problemas de conservación del momento, siempre verifica que el sistema esté aislado (sin fuerzas externas netas).

---

### Ejercicio 2: Fuerza Media en un Golpe

**Enunciado:** Una pelota de tenis de masa 100 g lleva una velocidad de 20 m/s. Tras ser golpeada por una raqueta, se mueve en sentido contrario con una velocidad de 40 m/s. Si la pelota ha estado en contacto con la raqueta 10⁻² s, calcular el módulo de la fuerza media del golpe.

#### Solución paso a paso:

**Paso 1: Datos del problema**
```
m = 100 g = 0.1 kg
v₁ = 20 m/s (dirección positiva)
v₂ = -40 m/s (dirección negativa, sentido contrario)
Δt = 10⁻² s = 0.01 s
```

**Paso 2: Calcular la variación del momento lineal**
```
Δp⃗ = m·v₂ - m·v₁
Δp = m(v₂ - v₁)
Δp = 0.1 kg × (-40 - 20) m/s
Δp = 0.1 × (-60) = -6 kg·m/s
```

**Paso 3: Aplicar el teorema del impulso**
```
F⃗·Δt = Δp⃗
F = Δp/Δt
```

**Paso 4: Calcular el módulo de la fuerza media**
```
|F| = |Δp|/Δt = 6/(0.01) = 600 N
```

**Resultado:** La fuerza media del golpe es **600 N**.

**💡 Consejo:** El signo de Δp indica la dirección de la fuerza. El módulo siempre es positivo. En este caso, la fuerza es grande porque el tiempo de contacto es muy pequeño.

---

### Ejercicio 3: Centro de Masas del Sistema Tierra-Luna

**Enunciado:** La masa de la Luna es 0.012 veces la masa de la Tierra; la distancia media entre sus centros es 60.3 radios terrestres. Calcular, en función del radio terrestre Rₜ, la situación del centro de masas del sistema Luna-Tierra.

#### Solución paso a paso:

**Paso 1: Definir el sistema de coordenadas y datos**
- Origen: Centro de la Tierra
- m_Luna = 0.012 × m_Tierra = 0.012 M
- m_Tierra = M
- Distancia Tierra-Luna: d = 60.3 Rₜ

**Paso 2: Posiciones de las partículas**
```
r_Tierra = 0 (en el origen)
r_Luna = 60.3 Rₜ
```

**Paso 3: Fórmula del centro de masas**
```
R_CM = (m_Tierra × r_Tierra + m_Luna × r_Luna)/(m_Tierra + m_Luna)
```

**Paso 4: Sustituir valores**
```
R_CM = (M × 0 + 0.012M × 60.3Rₜ)/(M + 0.012M)
R_CM = (0.012M × 60.3Rₜ)/(1.012M)
R_CM = (0.7236Rₜ)/1.012
R_CM ≈ 0.715 Rₜ ≈ 0.72 Rₜ
```

**Resultado:** El centro de masas está a **0.72 Rₜ** del centro de la Tierra.

**💡 Interpretación física:** El CM está dentro de la Tierra (ya que Rₜ = 6371 km, y 0.72 Rₜ ≈ 4587 km del centro). Esto es porque la Tierra es mucho más masiva que la Luna.

---

### Ejercicio 4: Centro de Masas y Aceleración de Tres Partículas

**Enunciado:** Sean tres partículas de masas m₁ = 2 kg, m₂ = 4 kg, m₃ = 6 kg que se encuentran en las posiciones A(1, 2, 3) m, B(2, -1, -4) m, C(0, 3, 1) m. Sobre ellas actúan las fuerzas externas F⃗₁ = (3, -2, 0) N, F⃗₂ = (0, 3, 2) N y F⃗₃ = (3, -4, 0) N. Determinar:
a) La posición del centro de masas
b) La aceleración del centro de masas

#### Solución paso a paso:

**Paso 1: Calcular la masa total**
```
M = m₁ + m₂ + m₃ = 2 + 4 + 6 = 12 kg
```

**Paso 2: Calcular la posición del CM (componente a componente)**

Componente X:
```
X_CM = (m₁x₁ + m₂x₂ + m₃x₃)/M
X_CM = (2×1 + 4×2 + 6×0)/12 = (2 + 8 + 0)/12 = 10/12 = 5/6 m
```

Componente Y:
```
Y_CM = (m₁y₁ + m₂y₂ + m₃y₃)/M
Y_CM = (2×2 + 4×(-1) + 6×3)/12 = (4 - 4 + 18)/12 = 18/12 = 3/2 m
```

Componente Z:
```
Z_CM = (m₁z₁ + m₂z₂ + m₃z₃)/M
Z_CM = (2×3 + 4×(-4) + 6×1)/12 = (6 - 16 + 6)/12 = -4/12 = -1/3 m
```

**Resultado a):** R⃗_CM = **(5/6, 3/2, -1/3) m**

**Paso 3: Calcular la fuerza total externa**

```
F⃗_total = F⃗₁ + F⃗₂ + F⃗₃
F⃗_total = (3, -2, 0) + (0, 3, 2) + (3, -4, 0)
F⃗_total = (6, -3, 2) N
```

**Paso 4: Calcular la aceleración del CM usando F⃗ = Ma⃗**

```
a⃗_CM = F⃗_total/M

a_x = 6/12 = 1/2 m/s²
a_y = -3/12 = -1/4 m/s²
a_z = 2/12 = 1/6 m/s²
```

**Resultado b):** a⃗_CM = **(1/2, -1/4, 1/6) m/s²**

**💡 Consejo:** En problemas con vectores en 3D, calcula componente por componente para evitar errores. Verifica que las unidades sean coherentes.

---

### Ejercicio 5: Centro de Masas de un Semicírculo

**Enunciado:** Sea un disco de forma semicircular de radio a. Determinar la posición del centro de masas. El origen está en el centro del semicírculo y el eje X pasa por los extremos del semicírculo.

#### Solución paso a paso:

**Paso 1: Análisis por simetría**
- Por simetría, X_CM = 0 (el semicírculo es simétrico respecto al eje Y)
- Solo necesitamos calcular Y_CM

**Paso 2: Configurar la integral**
Para una distribución continua con densidad uniforme σ:

```
Y_CM = ∫ y·dm / ∫ dm
```

**Paso 3: Expresar dm en coordenadas polares**
```
dm = σ·dA = σ·r·dr·dθ
y = r·sen(θ)
```

Límites: r ∈ [0, a], θ ∈ [0, π]

**Paso 4: Calcular el numerador**
```
∫ y·dm = ∫₀^π ∫₀^a (r·sen(θ))·σ·r·dr·dθ
        = σ ∫₀^π sen(θ)·dθ ∫₀^a r²·dr
        = σ·[-cos(θ)]₀^π · [r³/3]₀^a
        = σ·(1-(-1))·(a³/3)
        = σ·2·a³/3
```

**Paso 5: Calcular el denominador (masa total)**
```
M = ∫ dm = σ·(πa²/2)
```

(Área del semicírculo)

**Paso 6: Calcular Y_CM**
```
Y_CM = (σ·2·a³/3) / (σ·πa²/2)
Y_CM = (2a³/3) × (2/πa²)
Y_CM = 4a/(3π)
```

**Resultado:** r⃗_CM = **(0, 4a/3π)** ≈ **(0, 0.424a)**

Expresado con vectores unitarios: **r⃗_CM = (4a/3π)ĵ**

**💡 Consejo:** Para distribuciones continuas, usa simetría siempre que sea posible para simplificar cálculos. El CM de formas simétricas está sobre el eje de simetría.

---

### Ejercicio 6: Momento Angular respecto al CM

**Enunciado:** Dos masas de 2 kg y 3 kg tienen las posiciones r⃗₁ = (1, 1, -1) m y r⃗₂ = (2, -3, 0) m y las velocidades v⃗₁ = (1, 1, 1) m/s y v⃗₂ = (3, -2, -1) m/s. Determinar el momento angular del sistema respecto al centro de masas.

#### Solución paso a paso:

**Paso 1: Calcular la posición del CM**
```
M = m₁ + m₂ = 2 + 3 = 5 kg

R⃗_CM = (m₁r⃗₁ + m₂r⃗₂)/M
R⃗_CM = (2(1,1,-1) + 3(2,-3,0))/5
R⃗_CM = ((2,2,-2) + (6,-9,0))/5
R⃗_CM = (8,-7,-2)/5 = (8/5, -7/5, -2/5) m
```

**Paso 2: Calcular las posiciones relativas al CM**
```
r⃗'₁ = r⃗₁ - R⃗_CM = (1,1,-1) - (8/5,-7/5,-2/5)
r⃗'₁ = (5/5 - 8/5, 5/5 + 7/5, -5/5 + 2/5)
r⃗'₁ = (-3/5, 12/5, -3/5) m

r⃗'₂ = r⃗₂ - R⃗_CM = (2,-3,0) - (8/5,-7/5,-2/5)
r⃗'₂ = (10/5 - 8/5, -15/5 + 7/5, 0 + 2/5)
r⃗'₂ = (2/5, -8/5, 2/5) m
```

**Paso 3: Calcular la velocidad del CM**
```
V⃗_CM = (m₁v⃗₁ + m₂v⃗₂)/M
V⃗_CM = (2(1,1,1) + 3(3,-2,-1))/5
V⃗_CM = ((2,2,2) + (9,-6,-3))/5
V⃗_CM = (11,-4,-1)/5 m/s
```

**Paso 4: Calcular las velocidades relativas al CM**
```
v⃗'₁ = v⃗₁ - V⃗_CM = (1,1,1) - (11/5,-4/5,-1/5)
v⃗'₁ = (-6/5, 9/5, 6/5) m/s

v⃗'₂ = v⃗₂ - V⃗_CM = (3,-2,-1) - (11/5,-4/5,-1/5)
v⃗'₂ = (4/5, -6/5, -4/5) m/s
```

**Paso 5: Calcular el momento angular interno (espín)**
```
S⃗ = r⃗'₁ × m₁v⃗'₁ + r⃗'₂ × m₂v⃗'₂
```

Para r⃗'₁ × m₁v⃗'₁:
```
L⃗₁ = m₁(r⃗'₁ × v⃗'₁) = 2 × |  î    ĵ    k̂  |
                            |-3/5  12/5 -3/5|
                            |-6/5  9/5  6/5 |

L⃗₁ᵢ = 2[(12/5)(6/5) - (-3/5)(9/5)] = 2[72/25 + 27/25] = 2(99/25) = 198/25
L⃗₁ⱼ = 2[(-3/5)(-6/5) - (-3/5)(6/5)] = 2[18/25 + 18/25] = 2(36/25) = 72/25
L⃗₁ₖ = 2[(-3/5)(9/5) - (12/5)(-6/5)] = 2[-27/25 + 72/25] = 2(45/25) = 90/25
```

Para r⃗'₂ × m₂v⃗'₂:
```
L⃗₂ = m₂(r⃗'₂ × v⃗'₂) = 3 × | î    ĵ     k̂  |
                            |2/5  -8/5  2/5 |
                            |4/5  -6/5  -4/5|

L⃗₂ᵢ = 3[(-8/5)(-4/5) - (2/5)(-6/5)] = 3[32/25 + 12/25] = 3(44/25) = 132/25
L⃗₂ⱼ = 3[(2/5)(4/5) - (2/5)(-4/5)] = 3[8/25 + 8/25] = 3(16/25) = 48/25
L⃗₂ₖ = 3[(2/5)(-6/5) - (-8/5)(4/5)] = 3[-12/25 + 32/25] = 3(20/25) = 60/25
```

**Paso 6: Sumar las contribuciones**
```
S⃗ = L⃗₁ + L⃗₂
S⃗ᵢ = 198/25 + 132/25 = 330/25 = 66/5
S⃗ⱼ = 72/25 + 48/25 = 120/25 = 24/5
S⃗ₖ = 90/25 + 60/25 = 150/25 = 6
```

**Resultado:** L⃗_CM = **(66/5, 24/5, 6) kg·m²/s**

**💡 Consejo:** Los productos vectoriales son laboriosos. Trabaja con cuidado y verifica cada componente. Usa la regla del determinante para el producto vectorial.

---

### Ejercicio 7: Energía Cinética Total, del CM e Interna

**Enunciado:** Un sistema está formado por tres partículas de masas m₁ = 2 kg, m₂ = 3 kg y m₃ = 5 kg, con velocidades v⃗₁ = (1, -1, 0) m/s, v⃗₂ = (0, 3, -1) m/s y v⃗₃ = (1, 1, 1) m/s. Calcular:
a) La energía cinética total del sistema
b) La energía cinética del centro de masas
c) La energía cinética interna
d) Verificar que Eₖ_total = Eₖ_CM + Eₖ_interna

#### Solución paso a paso:

**Paso 1: Calcular la energía cinética total**
```
Eₖ_total = (1/2)m₁v₁² + (1/2)m₂v₂² + (1/2)m₃v₃²
```

Magnitudes de las velocidades:
```
v₁² = 1² + (-1)² + 0² = 2
v₂² = 0² + 3² + (-1)² = 10
v₃² = 1² + 1² + 1² = 3
```

```
Eₖ_total = (1/2)(2×2 + 3×10 + 5×3)
Eₖ_total = (1/2)(4 + 30 + 15)
Eₖ_total = (1/2)(49) = 49/2 = 24.5 J
```

**Resultado a):** Eₖ_total = **49/2 J = 24.5 J**

**Paso 2: Calcular la velocidad del CM**
```
M = m₁ + m₂ + m₃ = 2 + 3 + 5 = 10 kg

V⃗_CM = (m₁v⃗₁ + m₂v⃗₂ + m₃v⃗₃)/M
V⃗_CM = (2(1,-1,0) + 3(0,3,-1) + 5(1,1,1))/10
V⃗_CM = ((2,-2,0) + (0,9,-3) + (5,5,5))/10
V⃗_CM = (7,12,2)/10 = (0.7, 1.2, 0.2) m/s
```

**Paso 3: Calcular la energía cinética del CM**
```
V_CM² = 0.7² + 1.2² + 0.2² = 0.49 + 1.44 + 0.04 = 1.97

Eₖ_CM = (1/2)MV_CM²
Eₖ_CM = (1/2)(10)(1.97) = 9.85 J
```

O con fracciones:
```
V_CM² = (7/10)² + (12/10)² + (2/10)² = 49/100 + 144/100 + 4/100 = 197/100

Eₖ_CM = (1/2)(10)(197/100) = 197/20 J
```

**Resultado b):** Eₖ_CM = **197/20 J = 9.85 J**

**Paso 4: Calcular las velocidades relativas al CM**
```
v⃗'₁ = v⃗₁ - V⃗_CM = (1,-1,0) - (7/10,12/10,2/10)
v⃗'₁ = (3/10, -22/10, -2/10) m/s

v⃗'₂ = v⃗₂ - V⃗_CM = (0,3,-1) - (7/10,12/10,2/10)
v⃗'₂ = (-7/10, 18/10, -12/10) m/s

v⃗'₃ = v⃗₃ - V⃗_CM = (1,1,1) - (7/10,12/10,2/10)
v⃗'₃ = (3/10, -2/10, 8/10) m/s
```

**Paso 5: Calcular la energía cinética interna**
```
v'₁² = (3/10)² + (-22/10)² + (-2/10)² = 9/100 + 484/100 + 4/100 = 497/100
v'₂² = (-7/10)² + (18/10)² + (-12/10)² = 49/100 + 324/100 + 144/100 = 517/100
v'₃² = (3/10)² + (-2/10)² + (8/10)² = 9/100 + 4/100 + 64/100 = 77/100

Eₖ_interna = (1/2)(m₁v'₁² + m₂v'₂² + m₃v'₃²)
Eₖ_interna = (1/2)(2×497/100 + 3×517/100 + 5×77/100)
Eₖ_interna = (1/2)(994/100 + 1551/100 + 385/100)
Eₖ_interna = (1/2)(2930/100) = 2930/200 = 293/20 J
```

**Resultado c):** Eₖ_interna = **293/20 J = 14.65 J**

**Paso 6: Verificar la relación**
```
Eₖ_CM + Eₖ_interna = 197/20 + 293/20 = 490/20 = 49/2 J ✓
```

**¡Verificado!** Eₖ_total = Eₖ_CM + Eₖ_interna

**💡 Consejo:** La descomposición de la energía cinética es fundamental. La energía interna representa el movimiento "oculto" en el sistema de referencia del laboratorio.

---

## 🎓 Consejos y Estrategias para el Examen

### 📋 Temas que Suelen Preguntar (según exámenes)

#### En Teoría:
1. **Segunda Ley de Newton** para sistemas de partículas
2. **Ecuación del movimiento del momento angular** y su conservación
3. **Versión fuerte vs débil de la 3ª Ley de Newton**
4. **Condiciones de los campos conservativos**
5. **Principios de conservación** (momento lineal, angular, energía)

#### En Problemas:
1. **Sistemas de masa variable (cohetes)** - muy importante
2. **Choques elásticos** entre partículas
3. **Cálculo de centros de masas**
4. **Conservación de momento lineal** (retrocesos, colisiones)
5. **Momento angular** en sistemas de partículas

---

### ✅ Estrategia de Estudio

#### 1. **Domina los Conceptos Fundamentales**
   - Centro de masas: qué es y por qué es útil
   - Las tres leyes de conservación y sus condiciones
   - Diferencia entre fuerzas internas y externas

#### 2. **Memoriza las Fórmulas Clave**
```
• p⃗ = MV⃗                    (momento = masa × velocidad del CM)
• F⃗ = dp⃗/dt                 (2ª Ley para el sistema)
• R⃗_CM = Σ(mᵢr⃗ᵢ)/M         (definición de CM)
• L⃗ = R⃗×MV⃗ + S⃗             (momento angular orbital + espín)
• μ = m₁m₂/(m₁+m₂)          (masa reducida)
• Eₖ = (1/2)MV² + Eₖ_int    (energía cinética total)
• v = v₀ - V·ln(m/m₀)       (ecuación del cohete)
```

#### 3. **Practica el Método de Resolución**
   - **Paso 1:** Identifica el sistema y dibuja un diagrama
   - **Paso 2:** Determina qué principio aplicar (conservación de p, L, o E)
   - **Paso 3:** Verifica las condiciones (¿sistema aislado?, ¿fuerzas conservativas?)
   - **Paso 4:** Plantea las ecuaciones con sistema de referencia claro
   - **Paso 5:** Resuelve algebraicamente antes de sustituir números
   - **Paso 6:** Verifica unidades y razonabilidad del resultado

#### 4. **Casos Especiales Importantes**

**Problema de dos cuerpos:**
- Usa masa reducida μ
- El problema se reduce a uno equivalente de una partícula

**Cohetes:**
- Recuerda: sin fuerzas externas, usa v = v₀ - V·ln(m/m₀)
- Con gravedad: añade término -gt

**Choques:**
- Elásticos: se conservan p y Eₖ
- Inelásticos: solo se conserva p

---

### ⚠️ Errores Comunes a Evitar

1. **Confundir fuerzas internas con externas**
   - Solo las fuerzas externas afectan al movimiento del CM

2. **Olvidar que las fuerzas internas se cancelan**
   - Pero solo si obedecen la 3ª Ley de Newton

3. **No verificar si el sistema está aislado**
   - La conservación requiere que F⃗_ext = 0 o N⃗_ext = 0

4. **Errores de signos en productos vectoriales**
   - Usa la regla de la mano derecha
   - Ten cuidado con el orden: a⃗×b⃗ = -b⃗×a⃗

5. **Confundir masa reducida con masa total**
   - μ ≠ M, y μ < m₁, μ < m₂ siempre

6. **No distinguir entre momento angular orbital y espín**
   - L⃗_orbital depende del movimiento del CM
   - S⃗ depende del movimiento relativo al CM

---

### 🔑 Puntos Clave para Recordar el Día del Examen

1. **Las fuerzas internas NO cambian:**
   - El momento lineal total
   - El momento angular total (si obedecen 3ª Ley fuerte)
   - La posición del CM

2. **El CM se comporta como si toda la masa estuviera concentrada en él**

3. **En el sistema de referencia del CM:**
   - Σp⃗'ᵢ = 0 (suma de momentos = 0)

4. **Para que se conserve el momento angular:**
   - Las fuerzas deben estar dirigidas sobre la línea que une las partículas

5. **La energía se conserva solo si:**
   - El sistema está aislado (F⃗_ext = 0)
   - Las fuerzas son conservativas

---

### 📚 Relación con Otros Temas

- **Tema 1-2:** Leyes de Newton (base de todo)
- **Tema 4:** Movimiento oscilatorio (usa energía)
- **Tema 5+:** Campos (usa conceptos de fuerzas conservativas)
- **Relatividad:** Modifica estas leyes a altas velocidades

---

## 🎯 Resumen Final - Lo Más Importante

| Concepto | Fórmula | Condición de Conservación |
|----------|---------|--------------------------|
| **Momento Lineal** | p⃗ = MV⃗ | F⃗_ext = 0 |
| **Centro de Masas** | R⃗ = Σ(mᵢr⃗ᵢ)/M | Define el sistema |
| **Momento Angular** | L⃗ = R⃗×MV⃗ + S⃗ | N⃗_ext = 0 |
| **Energía Cinética** | Eₖ = ½MV² + Eₖ_int | Fuerzas conservativas |
| **Masa Reducida** | μ = m₁m₂/(m₁+m₂) | Problema de 2 cuerpos |
| **Ecuación Cohete** | v = v₀ - V·ln(m/m₀) | Sin fuerzas externas |

---

**¡Mucha suerte en el examen!** 🚀

Recuerda: La física de sistemas de partículas es la base de la mecánica. Comprende los conceptos, practica los ejercicios y verifica siempre las condiciones de conservación. 

---

*Última actualización: Diciembre 2024*
