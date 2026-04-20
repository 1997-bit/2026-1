# Estructura de Datos

**Prof. Aly Manuel Martín**

## Bit

Binary Digit.  
Un dígito binario solo puede tener dos valores: 0 o 1.

## Byte

Conjunto de 8 bits.  
Unidad básica de almacenamiento de información.  
En un byte podemos tener hasta 256 combinaciones diferentes de 1 y 0.

## Código ASCII

- _American Standard Code for Information Interchange_: código alfanumérico universalmente aceptado.
- La mayoría de los teclados se estandarizan según ASCII. Al pulsar una tecla, se introduce su código ASCII.
- ASCII dispone de 128 caracteres representados mediante código binario de 7 bits (puede usarse como código de 8 bits con MSB = 0).

### Tabla ASCII (extracto)

| Binario   | Dec | Hex | Representación | Binario   | Dec | Hex | Representación | Binario   | Dec | Hex | Representación |
| --------- | --- | --- | -------------- | --------- | --- | --- | -------------- | --------- | --- | --- | -------------- |
| 0010 0000 | 32  | 20  | espacio        | 0100 0000 | 64  | 40  | @              | 0110 0000 | 96  | 60  | `              |
| 0010 0001 | 33  | 21  | !              | 0100 0001 | 65  | 41  | A              | 0110 0001 | 97  | 61  | a              |
| ...       | ... | ... | ...            | ...       | ... | ... | ...            | ...       | ... | ... | ...            |

## Día del Programador (2⁸ = 256)

Se celebra el día 256 del año (2⁸ = máximo número con 8 bits: 11111111).

- Años normales: 13 de septiembre.
- Años bisiestos: 12 de septiembre.  
  **2026:** domingo 13 de septiembre.

## Diferencia entre byte y bit

- **Velocidad de transmisión** (ancho de banda): se mide en kilobits por segundo (kbps).
- **Almacenamiento** (tamaño de archivos): se mide en bytes (KB, MB, etc.).
- Algunos equipos y programas muestran la velocidad en kilobytes por segundo.

## Palabra

Conjunto de bytes.  
Unidad elemental de información que procesa el computador.  
Tamaño típico: 4 u 8 bytes.

## Memoria

Dividida en celdas o bloques de memoria.

- **Palabra de memoria:** menor conjunto de celdas que se pueden leer/escribir simultáneamente (ancho del bus).
- **Dirección de memoria:** número que identifica unívocamente cada palabra de memoria.

> Ejemplo: memoria de 1024 palabras de 1 byte cada una = memoria de 1KB.

## Datos

Valores simples o conjuntos de valores.  
Clasificación:

1. **Datos Simples**
2. **Datos Estructurados**

### Tipos de Datos

- **Simples o básicos:** ocupan una sola casilla de memoria. Ej: inicial de un nombre `J`.
- **Estructurados o compuestos:** con un nombre se hace referencia a un grupo de casillas. Ej: nombre `JUAN`.

## Estructura de Datos

Analogía: es el "recipiente informático" de los datos.  
Los datos toman el comportamiento de la estructura donde se almacenan.

**Definición formal:** colección lógica de elementos de datos cuya asignación se caracteriza por las operaciones de acceso usadas para almacenar, organizar y recuperar los elementos individuales.

## Clasificación de las Estructuras de Datos

### Por su organización

- **Lineales:** Arreglos, Pilas, Colas, Listas Enlazadas
- **No Lineales:** Árboles, Grafos

### Por su tamaño en memoria

- **Estáticas:** tamaño definido en compilación (no cambia en ejecución). Ej: arreglos, pilas, colas.
- **Dinámicas:** tamaño puede cambiar durante la ejecución. Ej: listas enlazadas, árboles, grafos.

## Estructuras Estáticas Lineales

### Arreglos (Array)

Colección finita, homogénea y ordenada de elementos almacenados en celdas consecutivas de memoria.  
Referenciados por un nombre de variable y una posición relativa (índice).

- **Componentes:** elementos del arreglo (valores)
- **Índices:** referencia a cada componente

**Tipos:**

- **Unidimensionales (Vectores):** un solo índice.
- **Bidimensionales (Matrices):** dos índices (filas y columnas).

**Características:**

- Finitos, homogéneos, ordenados.
- Celdas consecutivas.
- Acceso directo.
- Deben definirse al inicio del programa.

### Pilas (Stack)

Estructura lineal estática.  
Los elementos se introducen (añaden) y eliminan (sacan) por el mismo extremo: **la cima**.  
Comportamiento: **LIFO** (Last In, First Out) – el último en entrar es el primero en salir.

**Representación en memoria:** mediante arreglos o listas enlazadas.  
Si se usa arreglo: se define `TAMAÑO` o `MAX` y un puntero `TOPE` o `CIMA`.

- Pila vacía: `TOPE = 0`
- Pila llena: `TOPE = TAMAÑO`

**Operaciones básicas:**

- **Push:** insertar un elemento en la cima.
- **Pop:** eliminar el elemento de la cima.

### Colas (Queue)

Estructura lineal estática.  
Los elementos se introducen por un extremo (**FINAL**) y se eliminan por el otro (**FRENTE**).  
Comportamiento: **FIFO** (First In, First Out) – el primero en entrar es el primero en salir.

**Representación en memoria:** mediante arreglos o listas enlazadas.  
Si se usa arreglo: se define `MAX`, y dos punteros:

- `FRENTE`: posición del primer elemento.
- `FINAL`: posición del último elemento.

## Estructuras Dinámicas Lineales

### Listas Enlazadas

Estructura lineal dinámica.  
Número no limitado de elementos homogéneos llamados **NODOS**.  
El acceso se hace mediante punteros (no índices).

**Nodo:** consta de dos partes:

- **INFO:** información asociada al elemento.
- **ENLACE:** dirección de memoria del siguiente nodo (el último nodo tiene `NULL` o 0).

**Representación en memoria:**  
Se usan dos arreglos paralelos: `INFO(k)` y `ENLACE(k)`, más una variable puntero `COMIENZO` que apunta al primer nodo.

**Operaciones:**

- **Recorrido:** visitar cada nodo.
- **Búsqueda:** recorrer hasta encontrar el elemento buscado.
- **Inserción:** agregar un nuevo nodo.
- **Eliminación:** quitar un nodo re-direccionando los enlaces.

---

# Muchas Gracias
