# LIBRO DIARIO — CASOS COMPLETOS

---

## 1. COMPRAS

### Contado sin descuento

Db Compras
Db ITBMS-Tesoro Nacional
Cr Banco/Caja

### Contado con descuento

Db Compras ← monto bruto
Db ITBMS-Tesoro Nacional ← calculado sobre el neto
Cr Banco/Caja ← total neto
Cr Descuento en compras ← descuento recibido

### Crédito sin descuento

Db Compras
Db ITBMS-Tesoro Nacional
Cr Ctas. por pagar

### Crédito con descuento

Db Compras ← monto bruto
Db ITBMS-Tesoro Nacional ← sobre el neto
Cr Ctas. por pagar ← total neto
Cr Descuento en compras

### Devolución sin descuento previo

Db Banco/Caja ← contado: te devuelven dinero
o Ctas. por pagar ← crédito: reducen tu deuda
Cr Devolución en compras ← monto bruto devuelto
Cr ITBMS-Tesoro Nacional ← impuesto devuelto

### Devolución con descuento previo

Db Banco/Ctas. por pagar
Db Descuento en compras ← devuelves el descuento proporcional
Cr Devolución en compras ← monto bruto
Cr ITBMS-Tesoro Nacional ← impuesto del neto devuelto

### Abono a proveedor

Db Ctas. por pagar
Cr Banco

### Cancelación sin descuento, sin abono

Db Ctas. por pagar ← deuda completa
Cr Banco

### Cancelación con descuento, sin abono

Db Ctas. por pagar ← deuda completa
Cr Banco ← neto a pagar
Cr Descuento mercancía ← dcto sobre saldo mercancía
Cr ITBMS-Tesoro Nacional ← dcto sobre saldo ITBMS

### Cancelación sin descuento, con abono previo

← el abono ya fue registrado antes, solo cancelas el saldo
Db Ctas. por pagar ← saldo que queda
Cr Banco

### Cancelación con descuento, con abono previo

← saldo = compra − abono, dcto sobre ese saldo
Db Ctas. por pagar ← saldo actualizado
Cr Banco ← saldo − dcto − ITBMS ajuste
Cr Descuento mercancía
Cr ITBMS-Tesoro Nacional

### Cancelación con abono + devolución + descuento

← saldo = compra − devolución − abono, dcto sobre ese saldo
Db Ctas. por pagar ← saldo actualizado
Cr Banco
Cr Descuento mercancía
Cr ITBMS-Tesoro Nacional

---

## 2. VENTAS (Sistema físico)

### Contado sin descuento

Db Caja/Banco
Cr Ventas de mercancía
Cr ITBMS-Tesoro Nacional

### Contado con descuento

Db Caja/Banco ← neto cobrado
Db Descuento en ventas ← descuento concedido
Cr Ventas de mercancía ← monto bruto
Cr ITBMS-Tesoro Nacional ← sobre el neto

### Crédito sin descuento

Db Ctas. por cobrar
Cr Ventas de mercancía
Cr ITBMS-Tesoro Nacional

### Crédito con descuento

Db Ctas. por cobrar ← neto a cobrar
Db Descuento en ventas
Cr Ventas de mercancía ← monto bruto
Cr ITBMS-Tesoro Nacional ← sobre el neto

### Devolución de venta contado

Db Devoluciones en ventas
Db ITBMS-Tesoro Nacional
Cr Banco/Caja ← se devuelve el dinero

### Devolución de venta crédito

Db Devoluciones en ventas
Db ITBMS-Tesoro Nacional
Cr Ctas. por cobrar ← reduce lo que te deben

### Abono de cliente

Db Caja/Banco
Cr Ctas. por cobrar

### Cancelación sin descuento, sin abono

Db Caja/Banco
Cr Ctas. por cobrar

### Cancelación con descuento, sin abono

Db Caja/Banco ← neto cobrado
Db Descuento en ventas ← dcto sobre saldo mercancía
Db ITBMS-Tesoro Nacional ← dcto sobre saldo ITBMS
Cr Ctas. por cobrar ← deuda completa

### Cancelación sin descuento, con abono previo

Db Caja/Banco ← saldo que queda
Cr Ctas. por cobrar ← saldo actualizado

### Cancelación con descuento, con abono previo

← saldo = total − abono, dcto sobre ese saldo
Db Caja/Banco
Db Descuento en ventas
Db ITBMS-Tesoro Nacional
Cr Ctas. por cobrar ← saldo actualizado

---

## 3. VENTAS (Sistema perpetuo)

← Todo igual que sistema físico + asiento de costo simultáneo

### Venta (cualquier tipo) — asiento de costo adicional

Db Costo de mercancía vendida
Cr Inventario de mercancía

### Devolución (cualquier tipo) — asiento de costo adicional

Db Inventario de mercancía
Cr Costo de mercancía vendida

---

## 4. SERVICIOS

### Contado (cobro total)

Db Caja/Banco
Cr Ingresos por servicios
Cr ITBMS-Tesoro Nacional

### Crédito (sin cobro hoy)

Db Ctas. por cobrar
Cr Ingresos por servicios
Cr ITBMS-Tesoro Nacional

### Contrato con anticipo (cobras X% hoy)

Db Caja/Banco ← el % cobrado hoy
Db Ctas. por cobrar ← el % pendiente
Cr Ingresos por servicios← monto total
Cr ITBMS-Tesoro Nacional ← impuesto total

### Abono posterior de cliente

Db Caja/Banco
Cr Ctas. por cobrar

### Cancelación sin descuento, sin abono

Db Caja/Banco
Cr Ctas. por cobrar

### Cancelación con descuento, sin abono

Db Caja/Banco
Db Descuento en servicios
Db ITBMS-Tesoro Nacional ← ajuste proporcional
Cr Ctas. por cobrar

### Cancelación sin descuento, con abono previo

Db Caja/Banco ← saldo que queda
Cr Ctas. por cobrar ← saldo actualizado

### Cancelación con descuento, con abono previo

← saldo = total − abono, dcto sobre ese saldo
Db Caja/Banco
Db Descuento en servicios
Db ITBMS-Tesoro Nacional
Cr Ctas. por cobrar ← saldo actualizado

### Gasto (servicios que tú pagas)

Db Electricidad / Teléfono / Seguro / etc.
Cr Banco ← contado
o Gastos acum. por pagar← crédito

---

## 5. ESTABLECIMIENTO DE EMPRESA

### Persona natural (un solo dueño)

Db Banco
Cr Capital [nombre del dueño]

### Persona jurídica (sociedad anónima)

Db Banco
Cr Capital Social

### Adquisición de activo fijo contado

Db Mobiliario / Equipo / etc.
Cr Banco

### Adquisición de activo fijo crédito

Db Mobiliario / Equipo / etc.
Cr Ctas. por pagar

## 6. GASTOS Y SERVICIOS BÁSICOS (los que TÚ pagas)

### Electricidad / Teléfono / Agua — contado

DICE: "recibo de electricidad" / "factura de teléfono" / "cheque #"
Db Electricidad / Teléfono / Agua
Cr Banco

### Electricidad / Teléfono / Agua — crédito

DICE: "consumo del mes" / sin mención de cheque / "se acumula"
Db Electricidad / Teléfono / Agua
Cr Gastos acumulados por pagar

### Seguro anticipado — contado

DICE: "póliza de seguro" / "prima de X por mes" / "X meses" + "cheque #"
ACCIÓN: total = prima × meses
Db Seguros anticipados ← activo, no gasto directo
Cr Banco

### Seguro anticipado — crédito

DICE: igual pero sin cheque / sin pago
Db Seguros anticipados
Cr Gastos acumulados por pagar

---

## DIFERENCIA CLAVE: Gasto vs Anticipado

Gasto directo → se consume HOY → Db Electricidad / Teléfono
Servicio futuro → se pagó pero aún no se usa → Db Seguros anticipados
/ Alquileres anticipados

DICE "mes de julio" → ya se consumió → cuenta de GASTO
DICE "por 7 meses" → se pagó por adelantado → cuenta ANTICIPADA (activo)

---

## 7. ADQUISICIÓN DE ACTIVOS FIJOS (bienes para la empresa)

### Contado

DICE: "compra escritorio / equipo / vehículo" + "cheque #"
OJO: el ITBMS NO se registra separado en activos fijos
se incluye en el costo del activo
Db Mobiliario / Equipo de oficina / Vehículo / etc.
Cr Banco

### Crédito

DICE: mismo pero "al crédito" / sin cheque
Db Mobiliario / Equipo / etc.
Cr Ctas. por pagar

---

## DIFERENCIA CLAVE: Activo fijo vs Compra de mercancía

Activo fijo → para USO de la empresa → Db Mobiliario/Equipo
DICE: "escritorio para la empresa" / "equipo para la oficina"

Compra mercancía → para VENDER → Db Compras / Inventario
DICE: "para la venta" / "mercancía" / "inventario"

---

## REGLA DE ORO

¿Entra dinero HOY? → Caja/Banco DÉBITO
¿Sale dinero HOY? → Caja/Banco CRÉDITO
¿Te deben? → Ctas. por cobrar DÉBITO
¿Les debes? → Ctas. por pagar CRÉDITO
¿Vendes/prestas? → Ingresos CRÉDITO
¿Compras mercancía? → Compras DÉBITO
¿Impuesto generado? → ITBMS-Tesoro CRÉDITO
¿Impuesto ajustado? → ITBMS-Tesoro DÉBITO
¿Descuento recibido? → Descuento compras CRÉDITO
¿Descuento concedido? → Descuento ventas DÉBITO
Σ Débitos = Σ Créditos → siempre

## ÁRBOL DE DECISIÓN RÁPIDO

1. ¿Dice "compra" o "vende" o "servicio"?
   → define el tipo de empresa y cuenta principal

2. ¿Dice "cheque" o "recibo"?
   → SÍ = entra/sale dinero hoy = Caja/Banco
   → NO = es crédito = Ctas×cobrar o Ctas×pagar

3. ¿Dice "descuento"?
   → SÍ ahora = aplica en este asiento
   → SÍ en condiciones X/Y = aplica solo al cancelar si es a tiempo

4. ¿Dice "devolución" o "devuelve"?
   → reversa parcial del asiento original

5. ¿Dice "cancelación" o "cancela factura"?
   → busca si hubo abono o devolución antes
   → verifica si la fecha aplica para el descuento

6. ¿Dice "X% a la firma" o "abono de X%"?
   → contrato mixto: Caja por ese % + Ctas×cobrar el resto
