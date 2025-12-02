# Simulador Interactivo de Pila

El producto del proyecto se define como una aplicación web educativa diseñada para visualizar y comprender el funcionamiento de la estructura de datos "pila" de manera interactiva. Implementa completamente la lógica LIFO (Last-In, First-Out) con una interfaz visual intuitiva.

## Propósito
El propósito principal de esta herramienta es facilitar el aprendizaje de:
1.	La estructura de datos pila y sus operaciones fundamentales
2.	El concepto LIFO (último en entrar, primero en salir)
3.	Operaciones aritméticas utilizando pilas
4.	El control de flujo mediante llamadas y retornos de subrutinas
5.	Manejo de casos límite (pila llena, vacía, errores de operación)

## Tecnologías Utilizadas
1.	HTML: Estructura semántica de la aplicación
2.	CSS: Estilos responsivos con diseño moderno y limpio
3.	JavaScript :Lógica completa del simulador sin dependencias externas
4.	Almacenamiento: Todos los datos se gestionan en tiempo real en el navegador

## Implementaciones

### 1. Operaciones Básicas de Pila

| Operación | Descripción | Implementación |
|-----------|-------------|----------------|
| **PUSH** | Inserta un valor en la pila | `pila.push(valor)` con validación de límite |
| **POP** | Remueve y retorna el valor superior | `pila.pop()` con validación de pila vacía |
| **TOP** | Muestra el valor superior sin eliminarlo | `pila[pila.length - 1]` |
| **IsEmpty** | Verifica si la pila está vacía | `pila.length === 0` |
| **IsFull** | Verifica si la pila está llena | `pila.length >= capacidadMaxima` |
| **CLEAR** | Vacía completamente la pila | `pila = []` |

### 2. Operaciones Aritméticas

| Operación | Descripción | Funcionamiento |
|-----------|-------------|----------------|
| **ADD** | Suma los dos valores superiores | POP dos valores, suma, PUSH resultado |
| **MUL** | Multiplica los dos valores superiores | POP dos valores, multiplica, PUSH resultado |
| **DIV** | División entera de los dos valores superiores | POP dos valores, divide, PUSH resultado (con validación de división por 0) |


### 3. Control de Subrutinas

| Operación | Descripción | Funcionamiento |
|-----------|-------------|----------------|
| **CALL** | Simula llamada a subrutina | PUSH de dirección de retorno simulada (ej: DIR_1, DIR_2, etc.) |
| **RET** | Simula retorno de subrutina | POP de dirección de retorno y actualización de estado |


### 4. Sistema de Visualización

### Representación Gráfica de la Pila
1.	Elementos llenos: Celdas con fondo azul claro mostrando valores
2.	Elemento TOP: Celda resaltada en amarillo con borde más grueso
3.	Elementos vacíos: Celdas grises con texto "Vacío" y borde punteado
4.	Orden LIFO: Los elementos se muestran verticalmente con el TOP siempre en la posición superior visual

### Panel de Estado
1.	Indicadores en tiempo real de isEmpty y isFull (con coloración verde/rojo)
2.	Valor actual del TOP
3.	Última dirección de retorno registrada por RET

### Sistema de Mensajes
1.	Mensajes de éxito: Operaciones completadas correctamente (verde)
2.	Mensajes de error: Operaciones fallidas (rojo)
3.	Mensajes informativos: Resultados de consultas (azul)
4.	Auto-eliminación: Los mensajes desaparecen después de 3 segundos

### Bitácora de Operaciones
1.	Registro cronológico de todas las operaciones ejecutadas
2.	Registro de tiempo de cada operación

6. Configuración Flexible
1.	Capacidad de pila ajustable (1-20 elementos)
2.	Re-inicialización automática de la interfaz al cambiar configuración


## Diseño de Interfaz

### Principios de Diseño
1.	Simplicidad: Interfaz limpia sin elementos superfluos
2.	Claridad: Agrupación lógica de funcionalidades
3.	Accesibilidad: Contraste adecuado y tamaño de elementos táctiles
4.	Responsividad: Adaptación a diferentes tamaños de pantalla


## Arquitectura Técnica

### Estructura de Datos
// Variables principales

let pila = []; // Array que simula la estructura de pila

let capacidadMaxima = 8; // Límite configurable de elementos

let contadorDirecciones = 0; // Contador para direcciones de CALL

let ultimaDireccionRet = '-'; // Última dirección retornada

### Flujo de Datos
1.	Entrada de usuario → Validación → Ejecución → Actualización visual
2.	Estado persistente en variables JavaScript durante la sesión
3.	Renderizado inmediato tras cada operación
Sistema de Validación

1.	Validación de tipo: Entrada numérica para valores
2.	Validación de límites: Capacidad máxima respetada
3.	Validación de estado: Pila no vacía para POP, RET, operaciones aritméticas
4.	Validación de operaciones: División por cero prevenida


## Manual de usuario

### Pasos Básicos
1.	Configurar capacidad: Establecer el tamaño máximo de la pila
2.	Insertar valores: Usar el campo de texto y botón PUSH
3.	Operar: Ejecutar operaciones básicas, aritméticas o de control
4.	Observar: Ver cambios en tiempo real en la visualización
5.	Consultar: Usar TOP, IsEmpty, IsFull para conocer el estado

### Ejemplo 
1. Configurar pila con capacidad 5
2. PUSH(10), PUSH(20), PUSH(30)
3. Verificar IsEmpty (false) y IsFull (false)
4. Ejecutar TOP (muestra 30)
5. Ejecutar ADD (resultado: 50)
6. Ejecutar CALL (guarda DIR_1)
7. Ejecutar PUSH(5)
8. Ejecutar RET (retorna a DIR_1)
9. Ejecutar CLEAR


Este simulador representa una herramienta educativa completa para entender la estructura de datos pila. Combina una implementación técnica precisa con una interfaz intuitiva que hace accesibles conceptos complejos. Su diseño autónomo (un solo archivo HTML) lo hace ideal para distribución en entornos educativos, demostraciones en clase o estudio individual.
La aplicación cumple exhaustivamente con todos los requisitos solicitados, añadiendo valor educativo adicional a través de su sistema de retroalimentación, historial de operaciones y manejo robusto de errores, creando una experiencia de aprendizaje efectiva y atractiva.

##
#
#
## Autores/Desarrolladores

### - Raul Emiliano Aguayo Avila
### - Eduardo Sebastian Calan Canche
### - Edwin Roberto Cauich Aguilar
