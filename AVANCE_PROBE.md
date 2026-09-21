# Avance del diagnóstico del parcial 1

**Estado: PAUSADO. No finalizado.**
Respaldo preparado el **21/09/2026**, con respuestas recopiladas el **20/09/2026**.
Objetivo: estudiar **todas las unidades 1 y 2 de Automatización Industrial**, no solo sistemas de numeración o lógica digital.

## Reanudar aquí

La última pregunta quedó **sin responder**:

> ¿El cambio de 001 a 011 cumple la regla de Gray? Explica qué posición cambia.

Mostrar solamente esa pregunta y esperar la respuesta. No anticipar la solución.
El estudiante prefirió continuar en otra computadora antes de terminar el diagnóstico.
Se propuso cerrarlo con diez preguntas adicionales, una por vez y sin repreguntas, pero **esa propuesta no fue aceptada ni iniciada**.

## Criterio para el tutor que continúe

- Hacer **una sola pregunta por turno** y detenerse hasta recibir respuesta.
- Dar retroalimentación breve, con la razón de la corrección; no convertir cada respuesta en una clase extensa.
- Alternar áreas de las unidades 1 y 2. Evitar concentrar todo el diagnóstico en binario o compuertas.
- No reiniciar el diagnóstico completo ni volver a pedir información que ya consta aquí.
- Distinguir un acierto inicial de uno posterior a una explicación; este último necesita comprobación independiente posterior.
- Admitir «no sé» como información diagnóstica, sin atribuir dominio ni fracaso general.
- No afirmar que se ha usado una skill de tutoría específica si no está disponible en el nuevo entorno.
- Acordar un cierre acotado si el estudiante lo solicita; diez preguntas no son un compromiso ya adquirido.

## Cómo interpretar la evidencia

Este registro **parafrasea** los intercambios. Solo las expresiones y respuestas numéricas se conservan literalmente cuando constan en el historial.
Las descripciones de situaciones no pretenden reconstruir preguntas textuales que no quedaron registradas.

| Marca | Significado |
|---|---|
| Inicial | Respuesta correcta antes de la explicación correctiva de ese ejercicio; no prueba dominio de todo el tema. |
| Asistido | Respuesta correcta después de enseñanza, corrección o un ejemplo muy próximo. |
| A reforzar | Hubo desconocimiento, confusión o razonamiento incorrecto que requiere otra comprobación. |
| No evaluado | No existe evidencia suficiente en este diagnóstico. |

No se asignó nota, porcentaje de dominio ni condición de preparación suficiente para el parcial.

## Registro de respuestas y correcciones

### 1. Lazos de control y operaciones básicas

| Situación o tema | Respuesta registrada | Lectura y corrección |
|---|---|---|
| Bomba funcionando por un tiempo fijo, sin medir el nivel | Lazo abierto, porque no hay medición para decidir cuándo parar. | **Inicial:** correcto. |
| `S = (A + B) · C`, con `A=1`, `B=0`, `C=0` | `0`, porque al multiplicar por `C=0` el resultado es cero. | **Inicial:** correcto; en lógica, `+` representa OR y `·` representa AND. |
| OR con ambas entradas en `1` | `1`, «prendido». | **Inicial:** correcto; «prendido» depende de cómo se defina la salida. |
| Control de nivel que actúa a partir de una medición | Lazo cerrado, porque actúa en función de la medición. | Correcto; se aclaró que «cerrado» significa realimentación, no que la válvula esté físicamente cerrada. |

### 2. Binario, BCD y hexadecimal

| Conversión o tema | Respuesta registrada | Lectura y corrección |
|---|---|---|
| `101₂` a decimal, primer intento | `3` en base diez. | **A reforzar:** se explicó el peso de las posiciones: `4 + 0 + 1 = 5`. |
| `100₂`, `111₂`, nuevo intento de `101₂`, y `1010₂` a decimal | `4`, `7`, `5` y `10`, respectivamente. | **Asistido:** todos correctos después de trabajar los pesos. |
| Decimal `9` a binario de cuatro bits | `1001`. | Correcto en la práctica posterior. |
| Decimal `45` a binario de ocho bits | `101101`. | Valor correcto; faltaba el ancho solicitado: **`00101101`**. Los ceros iniciales no cambian el valor. |
| Decimal `128` a binario de ocho bits | `10000000`. | Correcto en la práctica posterior. |
| Decimal `205` a binario de ocho bits | `11001101`. | Correcto: `128 + 64 + 8 + 4 + 1 = 205`. |
| Diferencia entre binario puro y BCD | Confundió binario puro con el rango `0–9` y BCD con llegar a `15`. | **A reforzar:** cuatro bits binarios sin signo representan `0–15`; en BCD 8421 cada dígito decimal usa cuatro bits y solo admite `0000–1001`. |
| Ejemplo enseñado para `45` | Se compararon binario `00101101` y BCD `0100 0101`. | Fue una explicación, **no un acierto evaluado**. |
| Decimal `27` a BCD | `0010 0111`. | **Asistido:** correcto después de la explicación. |
| Valor decimal del dígito hexadecimal `F` | `15`. | **Inicial:** correcto. |
| Decimal `45` a hexadecimal | `2B`. | Incorrecto; `0010 1101₂ = 2D₁₆`, porque `D=13` y `B=11`. |
| `1011₂` como dígito hexadecimal | `B`. | **Asistido:** correcto después de corregir la equivalencia anterior. |

### 3. Código Gray: punto inmediatamente anterior a la pausa

- Al preguntar por su propiedad distintiva, respondió que no sabía.
- Se explicó que, en una secuencia Gray, dos códigos consecutivos difieren en **un solo bit**; ejemplo de dos bits: `00, 01, 11, 10`.
- Para la transición propuesta `001 → 111`, respondió que no cumplía, pero justificó que «el último número tiene que ser 0».
- El resultado era correcto, pero **el motivo era incorrecto**: cambian las dos primeras posiciones; el último bit no tiene obligación de valer cero.
- La pregunta del bloque de reanudación es la comprobación siguiente. Aún no hay evidencia de que esta corrección se haya comprendido.
- No se evaluó el algoritmo de conversión de binario a Gray.

### 4. Potencia, mando y contactos

| Tema | Respuesta o situación registrada | Lectura y corrección |
|---|---|---|
| Diferencia entre potencia y mando | Inicialmente no sabía. | Se explicó: potencia entrega energía a la carga; mando determina su funcionamiento. Bobina del contactor en mando y contactos principales en potencia. |
| Pulsador de parada | Lo clasificó como mando porque detiene el circuito. | **Asistido:** correcto; no significa que el pulsador interrumpa directamente la potencia del motor. |
| Contacto normalmente cerrado (NC) | Cerrado en reposo y abierto al pulsarlo; añadió que siempre circula corriente por la bobina. | Estados del contacto correctos; **cerrado no implica corriente** si falta alimentación o algún otro tramo está abierto. |
| Parada cerrada y marcha abierta, sin camino paralelo | No circula corriente; al mantener marcha pulsada podría circular. | Correcto si también se cumplen alimentación y demás condiciones del circuito. |
| Autorretención | Se explicó el contacto auxiliar normalmente abierto en paralelo con marcha. | **No evaluado de forma independiente.** Sin retención, al soltar marcha la bobina se desenergiza. |

### 5. Compuertas, Boole y Karnaugh

| Tema | Respuesta registrada | Lectura y corrección |
|---|---|---|
| Diferencia OR/XOR | OR: basta al menos una entrada activa. Para XOR describió igualdad de entradas. | OR correcto; confundió **XOR con XNOR**. XOR vale `1` si las dos entradas son diferentes; XNOR si son iguales. |
| `1 XOR 1` | `0`, porque las entradas son iguales. | **Asistido:** correcto después de la corrección. |
| NAND con entradas `1,1` | `0`, por negar el resultado de AND. | Correcto en ese ejercicio. |
| De Morgan, primer contacto | No sabía. | Se enseñó `¬(A·B) = ¬A + ¬B` y que la negación intercambia AND/OR. |
| Negación de `A+B` | Negación de A multiplicada por negación de B. | **Asistido:** correcto: `¬(A+B) = ¬A·¬B`. |
| Karnaugh, primer contacto | No sabía. | Se explicó su finalidad de simplificar conservando la tabla de verdad. |
| Mapa de dos variables: filas `A=0,1`, columnas `B=0,1`; ambas filas `[0,1]` | Coincide con `B`. | **Asistido:** correcto, `S=B`. |
| Mismo orden del mapa, ambas filas `[1,0]` | `B=1`. | Incorrecto; la función es **`S=¬B`**. |
| Evaluación de ese segundo mapa con `A=1`, `B=0` | `1`, porque es negación de B. | **Asistido:** correcto después de corregir la función. |

### 6. P&ID e identificación de instrumentos

- Al comenzar, desconocía qué era un P&ID. Se explicó como representación de proceso, tuberías e instrumentación, no como plano de cableado.
- Se usó el ejemplo de nivel `LT101 → LIC101 → FCV101` del boceto suministrado para hablar de medición, control y actuación.
- No sabía interpretar `TIC102`; se enseñó **controlador indicador de temperatura**, con `102` como identificación del lazo, no un valor de temperatura.
- Después interpretó `LIC101` como **controlador indicador de nivel del lazo 101**: acierto asistido.
- Quedan sin evaluar de forma amplia los símbolos, tipos de línea y ubicación de los instrumentos.

### 7. Memoria y temporizadores

| Tema | Respuesta registrada | Lectura y corrección |
|---|---|---|
| Combinacional frente a secuencial | Propuso serie frente a paralelo. | Se corrigió: combinacional depende de entradas actuales; secuencial incorpora estado/memoria. Serie/paralelo describe conexiones. |
| Alarma que permanece activa cuando desaparece la falla, hasta un rearme | Secuencial, porque la alarma sigue activa. | **Asistido:** correcto después de explicar memoria. |
| Retardo a la conexión, primer contacto | No sabía. | Se explicó un temporizador no retentivo ajustado a cinco segundos: exige mantener la entrada activa hasta cumplir el tiempo. |
| Entrada activa tres segundos con retardo a la conexión de cinco segundos | No se activa la salida porque no llega a cinco segundos. | **Asistido:** correcto. |
| Qué retrasa un temporizador a la desconexión | La desactivación de su salida. | Correcto; se explicó la permanencia de la salida tras retirar la orden. |

## Qué falta diagnosticar

### Unidad 1

- Conceptos, objetivos e historia de la automatización; pirámide y niveles de campo, control, supervisión, MES y ERP.
- Tablas de verdad completas, comprobación independiente de compuertas, leyes de Boole y simplificación; formas canónicas SOP/POS.
- Karnaugh de tres y cuatro variables: agrupaciones, bordes y condiciones indiferentes (*don't care*).
- Conversión binario–Gray y comprobación independiente de los códigos trabajados.
- MUX/DEMUX, codificadores y decodificadores.
- Biestables RS, JK, D y T; temporizador 555 astable/monoestable y contadores binarios/de década.

### Unidad 2

- Lectura más amplia de P&ID, símbolos ISA, tipos de señales y ubicación de instrumentos; símbolos eléctricos IEC/ANSI.
- Esquemas unifilares y multifilares; identificación y numeración de conductores y bornes.
- Resolución independiente de autorretención, prioridad de parada y enclavamientos.
- Cronogramas de temporizadores, diagramas de secuencia e interconexiones/borneras.
- **Práctica real en CADeSIMU: no evaluada.** Ninguna respuesta verbal sustituye dibujar, simular y comprobar un circuito.

### Prioridades al continuar

1. Resolver la pregunta pendiente de Gray y registrar tanto el resultado como su justificación.
2. Alternar diagnóstico de los bloques aún no evaluados de ambas unidades, sin prolongar indefinidamente cada error con repreguntas.
3. Reforzar las confusiones observadas mediante ejercicios nuevos: XOR/XNOR, BCD/binario, hexadecimal, memoria y complementación.
4. Reservar una instancia práctica de mando, temporización y enclavamientos en CADeSIMU, según los requisitos del curso.
5. Al cerrar el diagnóstico, separar resultados independientes, asistidos y no evaluados; luego acordar el plan de estudio.

## Fuentes revisadas y límites

La carpeta original contenía **28 archivos: 27 PDF y un PPTX**, con **1.612 páginas/diapositivas** en conjunto.
Se revisaron clases, guías y fichas. Los dos libros de referencia suman **1.174 páginas** y se consultaron selectivamente: **no hubo lectura exhaustiva de cada página de los libros**.
La presentación se revisó mediante texto y elementos visuales seleccionados; no se afirma una verificación visual íntegra de todas sus diapositivas.

El programa y la planificación sitúan el parcial 1 en las unidades 1 y 2, con práctica individual en CADeSIMU, el **22/09/2026**.
La fecha es documental; no se comprobó si hubo cambios posteriores. `Sesion_07_Instrumentacion_Sensores_Comandos.pdf` corresponde principalmente a contenido de unidad 3/apoyo, no al núcleo asumido del primer parcial.

### Referencias textuales principales — originales no incluidos

| Archivo | Uso principal |
|---|---|
| `Sesion_01_Fundamentos_Automatizacion_e_Industria_4.0.pdf` | Fundamentos, lazos y sistemas de numeración. |
| `Sesion_02_Puertas_Logicas_y_Algebra_de_Boole.pdf` | Compuertas, tablas y álgebra de Boole. |
| `Sesion_03_Minimizacion_Karnaugh_Circuitos_Combinacionales_Secuenciales.pdf` | Karnaugh, combinacionales y secuenciales. |
| `Guia_Practica_01_Algebra_de_Boole_y_Tablas_de_Verdad.pdf` | Conversiones y ejercicios de lógica. |
| `Guia_Practica_02_Minimizacion_y_Logica_Secuencial.pdf` | Minimización y lógica con memoria. |
| `Sesion_05_Esquemas_Potencia_Mando_Marcado_Bornes_CADeSIMU.pptx` | Potencia, mando, bornes y autorretención. |
| `CONTROL_INDUSTRIAL.pdf` y `CADe_SIMU_Manual.pdf` | Circuitos, temporización y simulación. |
| `Boceto_Diagrama_PID_Proceso_Industrial.pdf` | Lectura de lazos de nivel y temperatura. |
| `Automatizacion_Procesos_Industriales_Alf.pdf` e `Instrumentacion_industrial_Creus_8th.pdf` | Referencias consultadas selectivamente. |
| Guías prácticas T1–T5 y guía integradora de cinco tableros | Aplicaciones de contactos, sensores y secuencias, con las salvedades siguientes. |

### Advertencias para no enseñar errores de los materiales

- **Karnaugh:** la página 13 del PDF de sesión 03 propone `¬A+CD` para `F=Σm(1,3,7,11,15)+d(0,2,5)`. Esa expresión es incorrecta: incluye ceros obligatorios. Son válidas `¬A¬B+CD` o `¬AD+CD`, con el orden habitual de variables `A,B,C,D`.
- La extracción de texto puede perder o añadir barras de negación. Cuando una fórmula sea dudosa, comprobarla visualmente en el original antes de corregir al estudiante.
- Las guías T1, T3, T5 y la integradora presentan contradicciones de contactos, secuencias o interpretación de sensores. Usarlas con análisis crítico, no como diseños de seguridad industrial ya validados.
- Las fichas no son intercambiables: `IFM204-06_ES-ES.pdf` describe un sensor inductivo, no la barrera O5P701; `MY.pdf` es de Omron, no de Thomelex; el documento Phoenix identifica internamente el artículo `2966171`, distinto del número del nombre del archivo. No generalizar bornes ni polaridades sin el modelo exacto.
- El indicador conectado en paralelo con una bobina muestra su orden/energización, no demuestra por sí solo que el motor esté girando. Los ejemplos didácticos tampoco certifican seguridad de personas.

## Actualizar este registro después de continuar

Añadir la respuesta a la pregunta pendiente, el razonamiento y la corrección si corresponde.
Actualizar el siguiente punto de reanudación y las áreas efectivamente evaluadas, preservando la distinción entre aciertos iniciales y asistidos.
No marcar como completados bloques solo por haber sido explicados.
