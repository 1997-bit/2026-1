# 📋 FÓRMULAS DE PLANILLA — CONTABILIDAD GENERAL
### Universidad Tecnológica de Panamá · Guía de Parcial

---

## 1. SALARIO BASE POR UNIDAD DE TIEMPO

### 1.1 Salario por hora → mes

$$S_{mes} = S_{hora} \times 48 \times 4.3333$$

> 48 horas/semana × 4.3333 semanas/mes (promedio)

### 1.2 Salario por semana

$$S_{semana} = S_{hora} \times 48$$

### 1.3 Salario mensual → hora

$$S_{hora} = \frac{S_{mes}}{48 \times 4.3333} = \frac{S_{mes}}{208}$$

---

## 2. SALARIO BRUTO

$$\text{Salario Bruto} = \text{Salario Base} + \text{Otras Remuneraciones}$$

> Otras remuneraciones: comisiones, bonificaciones, horas extras, primas, etc.

---

## 3. SEGURO SOCIAL (CSS)

### 3.1 Cuota del Empleado

| Período | % Empleado |
|---|---|
| 13/03/2025 – 31/12/2026 | 9.75% |
| 01/01/2027 – 28/02/2029 | 9.75% |
| 01/03/2029 en adelante | 9.75% |

$$\text{CSS}_{empleado} = S_{bruto} \times 9.75\%$$

### 3.2 Cuota del Patrono (Gasto del Empleador)

| Período | % Patrono |
|---|---|
| 13/03/2025 – 31/12/2026 | 13.25% |
| 01/01/2027 – 28/02/2029 | 14.25% |
| 01/03/2029 en adelante | 15.25% |

$$\text{CSS}_{patrono} = S_{bruto} \times 13.25\% \quad \text{(período vigente)}$$

---

## 4. SEGURO EDUCATIVO

### 4.1 Cuota del Empleado

$$\text{SE}_{empleado} = S_{bruto} \times 1.25\%$$

### 4.2 Cuota del Patrono (Gasto)

$$\text{SE}_{patrono} = S_{bruto} \times 1.50\%$$

---

## 5. RIESGO PROFESIONAL (solo paga el patrono)

$$\text{Riesgo Prof.} = S_{bruto} \times \%_{\text{clase asignada}}$$

| Clase | Descripción | % Promedio |
|---|---|---|
| I | Ordinario de vida | 0.56% |
| II | Bajo | 0.98% |
| III | Medio | 2.10% |
| IV | Alto | 3.64% |
| V | Máximo | 5.67% |

> El porcentaje exacto depende del grado de riesgo asignado por la CSS a la empresa.

---

## 6. IMPUESTO SOBRE LA RENTA (ISR)

### Paso 1 — Calcular la Renta Bruta Anual

$$\text{Renta Bruta} = (S_{mensual} \times 12) + \text{XIII mes}$$

> El XIII mes = 1 salario mensual (se suma porque es ingreso gravable)

### Paso 2 — Aplicar la tarifa

$$\text{ISR} = \begin{cases} 0 & \text{si } RN \leq 11{,}000 \\ (RN - 11{,}000) \times 15\% & \text{si } 11{,}000 < RN \leq 50{,}000 \\ 5{,}850 + (RN - 50{,}000) \times 25\% & \text{si } RN > 50{,}000 \end{cases}$$

### Paso 3 — Deducción por cónyuge (Art. 709 / Ley 8-2010)

Solo aplica si el contribuyente es **casado/unido (categoría E)**:

$$\text{Base ISR} = RN - 800.00$$

Luego aplica la tarifa del Paso 2 sobre esa base reducida.

### Paso 4 — ISR mensual (quincena)

$$\text{ISR}_{mensual} = \frac{\text{ISR anual}}{12}$$

$$\text{ISR}_{quincenal} = \frac{\text{ISR mensual}}{2}$$

---

## 7. TOTALES DE LA PLANILLA

### 7.1 Total Deducciones del Empleado

$$\text{Total Deduc.} = \text{CSS}_{emp} + \text{SE}_{emp} + \text{ISR}_{mensual} + \text{Otros descuentos}$$

### 7.2 Salario Neto

$$\boxed{S_{neto} = S_{bruto} - \text{Total Deducciones}}$$

### 7.3 Gastos del Patrono (Cargas Sociales)

$$\text{Cargas Sociales} = \text{CSS}_{patrono} + \text{SE}_{patrono} + \text{Riesgo Prof.}$$

---

## 8. PRESTACIONES LABORALES

### 8.1 Vacaciones

$$\text{Reserva Vacaciones} = \frac{S_{bruto}}{11} = S_{bruto} \times 9.0909\%$$

> 1 mes de salario por cada 11 meses trabajados.

### 8.2 Décimo Tercer Mes (XIII)

$$\text{Reserva XIII} = \frac{S_{bruto}}{12} = S_{bruto} \times 8.3333\%$$

> Pagado en 3 partidas: 15 de abril, 15 de agosto y 15 de diciembre.

---

## 9. HORAS EXTRAORDINARIAS

$$\text{Valor H.E.} = S_{hora} \times 1.25 \quad \text{(25\% de recargo mínimo)}$$

$$S_{hora} = \frac{S_{mensual}}{208}$$

$$\text{Total H.E.} = S_{hora} \times 1.25 \times \text{No. horas extras}$$

---

## 10. LIQUIDACIÓN DE EMPLEADOS

### 10.1 Tiempo Computado

$$t = \text{Años} + \frac{\text{Meses}}{12} + \frac{\text{Días}}{360}$$

### 10.2 Salario Mensual Promedio (con horas extras)

$$\bar{S}_{mensual} = \frac{\sum_{i=1}^{6}(S_{base,i} + H.E._i)}{6}$$

> Se toman los últimos 6 meses.

### 10.3 Salario Semanal Promedio

$$\bar{S}_{semana} = \frac{\bar{S}_{mensual}}{4.3333}$$

### 10.4 Indemnización (despido injustificado)

$$\text{Indemnización} = \bar{S}_{semana} \times 3.4 \times t$$

> 3.4 semanas de salario por cada año laborado.

### 10.5 Antigüedad

**Salario fijo:**

$$\text{Antigüedad} = \frac{S_{anual}}{52} \times n_{años}$$

**Salario variable (últimos 5 años):**

$$\text{Antigüedad} = \frac{\sum_{i=1}^{5} S_{anual,i}}{52 \times 5} \times n_{años} = \frac{\sum S_{anual}}{260} \times n_{años}$$

---

## 11. DISPONIBILIDAD DE SALARIO (Art. 161 Código de Trabajo)

El descuento total no puede superar el **35%** del salario, ni dejar menos del **50%** libre al empleado.

| Tipo de descuento | Límite máximo |
|---|---|
| Hipotecas | 30% |
| Préstamos bancarios / créditos | 20% |
| Préstamos de la empresa | 15% |
| Productos de la empresa | 10% |
| Embargos (del 50% libre) | 15% |

$$S_{disponible} = S_{neto} - \text{Descuentos opcionales permitidos}$$

---

---

# 🧮 CÓMO USAR LA SUMADORA CASIO AX-120B

La Casio AX-120B es una sumadora de 12 dígitos con impresora, muy útil para planillas porque imprime el registro de cada operación.

---

## Teclas clave que necesitas conocer

| Tecla | Función |
|---|---|
| `AC` | Limpia todo (All Clear) |
| `C/CE` | Borra el último dato ingresado |
| `+` | Suma y registra en acumulador |
| `-` | Resta y registra |
| `×` | Multiplicar |
| `÷` | Dividir |
| `%` | Porcentaje |
| `=` | Ejecuta la operación |
| `*` o `♦` | Subtotal (muestra acumulado sin limpiar) |
| `GT` | Gran Total (suma todos los subtotales) |
| `+/−` | Cambia signo |

---

## Secuencias por fórmula

### A. Calcular porcentaje (CSS, SE, ISR parcial)

**Ejemplo:** `900 × 9.75%`

```
9 0 0  ×  9 . 7 5  %
```
> La máquina muestra y registra el resultado directamente. No se presiona `=`.

---

### B. Salario Bruto (Suma acumulada)

**Ejemplo:** Salario base 800 + comisión 120 + H.E. 35.40

```
AC
8 0 0  +
1 2 0  +
3 5 . 4 0  +
*          ← Subtotal = 955.40
```

---

### C. Deducciones del empleado (suma en columna)

```
AC
[CSS empleado]     +
[SE empleado]      +
[ISR mensual]      +
[Otros descuentos] +
*                  ← Total de deducciones
```

---

### D. Salario Neto

```
[Salario Bruto]  +
[Total Deduc.]   -
=
```

---

### E. Cargas Sociales del Patrono

```
AC
[CSS patrono]    +
[SE patrono]     +
[Riesgo Prof.]   +
*                ← Total cargas sociales
```

---

### F. Reserva de Vacaciones (÷ 11)

```
[Salario Bruto]  ÷  1 1  =
```

---

### G. Reserva de XIII (÷ 12)

```
[Salario Bruto]  ÷  1 2  =
```

---

### H. Cálculo de ISR anual (flujo completo)

1. **Renta Bruta:**
```
AC
[S. mensual]  ×  1 3  =   ← (12 meses + XIII)
```
> Guarda ese resultado mentalmente o en papel.

2. **Excedente sobre 11,000:**
```
[Renta Bruta]  -  1 1 0 0 0  =
```

3. **ISR anual al 15%:**
```
[Excedente]  ×  1 5  %
```

4. **ISR mensual:**
```
[ISR anual]  ÷  1 2  =
```

5. **ISR quincenal:**
```
[ISR mensual]  ÷  2  =
```

---

### I. Indemnización

1. Calcula salario semanal promedio: `[Prom. mensual] ÷ 4.3333 =`
2. Multiplica por 3.4: `[S. semanal] × 3.4 =`
3. Multiplica por tiempo computado: `[Resultado] × [t] =`

---

### J. Gran Total de una planilla con varios empleados

Después de calcular el neto de cada empleado con `=`, presiona `GT` al final para obtener la suma global de todos los resultados acumulados en el Gran Total.

```
[Neto emp. 1]  =
[Neto emp. 2]  =
...
GT             ← Total general de la planilla
```

---

> **Tip:** Activa el modo de impresión (`PRINT ON`) para tener el registro en papel de todos tus cálculos. Si solo quieres verificar sin imprimir, usa `IC` (Item Count) apagado.
