# Curso de Introducción a la IA — Equipo Roig
**Duración:** 1 hora · **Fecha:** Junio 2026

Bienvenido/a al curso. Esta guía es tuya para seguir los ejercicios durante la sesión y consultar después cuando quieras aplicar la IA en tu día a día.

---

## La regla de los 3 elementos

Todo buen prompt tiene estas tres partes:

```
🔵 CONTEXTO  →  Quién eres, cuál es tu negocio, qué datos tienes
🟡 TAREA     →  Qué quieres que haga exactamente
🟢 FORMATO   →  Cómo quieres la respuesta (tabla, lista, informe, email...)
```

Cuanto más concreto seas en cada bloque, mejor será la respuesta.

**Herramientas que usaremos:** [claude.ai](https://claude.ai) · [chatgpt.com](https://chatgpt.com) — sin instalar nada, solo el navegador.

---

## Ejercicio 1 — Filtrar y sumar tiques de parking
**Para:** Antonia / Xisca · [📎 Descargar fichero de ejemplo](https://raw.githubusercontent.com/rafaadrover/curs-ia-roig/main/ejemplos/ejemplo_extracto_bancario.txt)

**Situación:** Tienes el extracto mensual del prepago empresa con 40 operaciones mezcladas. Hay que identificar solo las de parking para introducirlas en SAGE, sin recargas ni otros establecimientos.

**Cómo hacerlo:** descarga el fichero, ábrelo, copia todo el contenido y pégalo al final del prompt.

```
🔵 CONTEXTO:
Soy responsable de facturación en una empresa de rent-a-car.
Tengo el extracto mensual de una tarjeta prepago de empresa con 40 operaciones mezcladas.

🟡 TAREA:
Filtra únicamente los movimientos de parking.
Los establecimientos de parking contienen "AENA" o "SMAP" en el nombre.
Ignora las recargas (importes positivos) y otros establecimientos como ferreterías.

🟢 FORMATO:
Muestra una tabla con columnas: Fecha | Establecimiento | Importe.
Al final añade el total gastado en parking.

Datos: [PEGAR EL EXTRACTO AQUÍ]
```

---

## Ejercicio 2 — Informe de ventas comercial
**Para:** Alexia · [📎 Descargar fichero de ejemplo](https://raw.githubusercontent.com/rafaadrover/curs-ia-roig/main/ejemplos/ejemplo_datos_ventas.txt)

**Situación:** Tienes los datos de ventas de mayo por delegación. Necesitas un informe ejecutivo claro para tomar decisiones, sin tener que interpretar los números tú misma.

```
🔵 CONTEXTO:
Soy responsable comercial de una empresa de rent-a-car con 5 delegaciones en Mallorca e Ibiza.
Te adjunto los datos de ventas de mayo: contratos, importes, objetivos e incidencias por delegación.

🟡 TAREA:
Redacta un informe ejecutivo de máximo una página con:
- Puntos destacados positivos del mes
- Puntos de mejora o alertas
- 3 recomendaciones concretas para el próximo mes

🟢 FORMATO:
Texto corrido con subtítulos. Tono profesional y directo. Sin tecnicismos.

Datos: [PEGAR AQUÍ]
```

---

## Ejercicio 3 — Comparar presupuestos de proveedores
**Para:** Guillem · [📎 Descargar fichero de ejemplo](https://raw.githubusercontent.com/rafaadrover/curs-ia-roig/main/ejemplos/ejemplo_presupuestos.txt)

**Situación:** Has recibido dos presupuestos de neumáticos. El precio total es igual, pero hay diferencias en otros factores. La IA los analiza y te dice cuál elegir.

```
🔵 CONTEXTO:
Soy responsable de compras de una empresa de rent-a-car.
He recibido dos presupuestos de proveedores distintos para el mismo pedido de neumáticos.

🟡 TAREA:
Compara los dos presupuestos teniendo en cuenta: precio total, plazo de entrega, condiciones de pago,
garantía y cualquier diferencia relevante.
Indícame cuál recomiendas y por qué.
Si falta algún dato importante para decidir, dímelo.

🟢 FORMATO:
Primero una tabla comparativa con los puntos clave.
Luego un párrafo corto con la recomendación final.

Presupuesto 1: [PEGAR]
Presupuesto 2: [PEGAR]
```

---

## Ejercicio 4 — Generar nombres de carpeta por matrícula
**Para:** Antonia · [📎 Descargar fichero de ejemplo](https://raw.githubusercontent.com/rafaadrover/curs-ia-roig/main/ejemplos/ejemplo_flota_vehiculos.txt)

**Situación:** Tienes la lista de vehículos de la flota y necesitas crear carpetas individuales para guardar los documentos escaneados de cada uno (permiso de circulación, ficha técnica, seguro...).

```
🔵 CONTEXTO:
Gestiono la documentación de una flota de 16 vehículos de alquiler.
Tengo una lista con los datos de cada vehículo: bastidor, matrícula, modelo y marca.

🟡 TAREA:
Para cada vehículo genera el nombre de carpeta donde guardaremos sus documentos.
El formato exacto es: [CODIGO]_[MARCA]_[MODELO]_[MATRICULA]
El código empieza en B1 y sube en orden correlativo.

🟢 FORMATO:
Una línea por vehículo. Todo en mayúsculas, sin espacios, usando guiones bajos.

[PEGAR LA LISTA O ARRASTRAR EL FICHERO AL CHAT]
```

---

## Ejercicio 5 — Extraer datos de una factura escaneada
**Para:** Antonia / Cati · [📎 Descargar factura PDF de ejemplo](https://github.com/rafaadrover/curs-ia-roig/raw/main/ejemplos/factura_taller_bauza.pdf)

**Situación:** Tienes una factura de taller en PDF. En lugar de leerla y copiar los datos a mano, arrastras el fichero al chat y la IA extrae todo automáticamente.

```
🔵 CONTEXTO:
Tengo una factura de taller mecánico en formato PDF escaneado.

🟡 TAREA:
Extrae los datos principales del documento.

🟢 FORMATO:
Tabla con estas columnas: Nº Factura | Fecha | Proveedor | Matrícula vehículo | Base imponible | IVA | Total.
Si algún dato no es legible, escribe "no legible" en esa celda.

[ARRASTRAR EL PDF O IMAGEN AL CHAT]
```

---

## Ejercicio 6 — Flujo de devoluciones
**Para:** Xisca

**Situación:** Cuando llega una solicitud de devolución, no siempre está claro a quién corresponde gestionarla. Este prompt convierte la IA en un asistente que guía el proceso paso a paso.

```
🔵 CONTEXTO:
Soy responsable de facturación en una empresa de rent-a-car.
Cuando un cliente solicita una devolución, necesitamos seguir un proceso claro según el método de pago original.

🟡 TAREA:
Actúa como asistente de procesos. Cuando recibas una solicitud de devolución, haz estas preguntas en orden:
1. Nombre del cliente y número de contrato
2. Motivo de la devolución
3. Importe a devolver
4. Método de pago original (tarjeta o transferencia)
Luego indica la derivación correcta:
- Tarjeta → gestiona Xisca
- Transferencia → deriva a Guillem con justificante

🟢 FORMATO:
Al terminar, genera un resumen en tabla lista para copiar al sistema de gestión.
```

---

## Ejercicio 7 — Ideas de blog con intención SEO
**Para:** Helena

```
🔵 CONTEXTO:
Somos una empresa de rent-a-car en Mallorca que también ofrece servicios de gestión de flotas para empresas.
Nuestro público objetivo son empresas locales y turistas de negocios.
Queremos posicionarnos mejor en Google con contenido de blog relevante.

🟡 TAREA:
Dame 10 ideas de artículos para el blog ordenadas de mayor a menor potencial de búsqueda.

🟢 FORMATO:
Tabla con columnas: Título del artículo | Intención de búsqueda del usuario | Palabras clave principales.
```

---

## Ejercicio 8 — Adaptar un eslogan a tres idiomas
**Para:** Helena

```
🔵 CONTEXTO:
Somos una empresa de rent-a-car en Mallorca. Nuestros principales mercados son España, Alemania y Reino Unido.
Tenemos el eslogan: "Tu flota, nuestra responsabilidad".

🟡 TAREA:
Adapta el eslogan al inglés, alemán y francés.
No hagas traducción literal — busca el equivalente que resuene culturalmente en cada mercado
manteniendo el tono de confianza y profesionalidad.

🟢 FORMATO:
Una línea por idioma con el eslogan propuesto y una frase corta explicando por qué funciona en ese mercado.
```

---

## Ejercicio 8b — Propuesta visual de mejora web para TI
**Para:** Helena

**Situación:** Helena detecta que el motor de búsqueda de booking.roig.com puede mejorar la conversión, pero no sabe programar. Con una captura de pantalla y un prompt, la IA genera un rediseño en HTML listo para enviar al equipo de TI como propuesta concreta.

**Cómo hacerlo:** haz una captura de la pantalla que quieres mejorar, arrástrala al chat y usa este prompt:

```
🔵 CONTEXTO:
Soy responsable de marketing de una empresa de rent-a-car.
Adjunto una captura de pantalla de nuestro motor de búsqueda de vehículos (booking.roig.com).

🟡 TAREA:
Propón mejoras de UX/UI para esta pantalla con el objetivo de aumentar la conversión.
Céntrate en cómo se presentan las tarifas y cómo el usuario toma la decisión de reserva.
Luego genera el HTML completo con el diseño mejorado, usando los mismos datos y precios de la captura.

🟢 FORMATO:
Primero lista los 3-5 problemas de UX que has detectado y cómo los resuelves.
Luego el código HTML completo del rediseño, listo para copiar y enviar al equipo de TI.
```

**Lo que obtendrás:** un análisis de problemas de conversión + código HTML con el rediseño visual. Sin saber programar, Helena puede hacer propuestas concretas a TI en minutos en lugar de semanas.

> **Tip:** Este mismo prompt funciona para cualquier pantalla de la web — fichas de vehículo, formulario de reserva, página de inicio...

---

## Ejercicio 9 — Matriz de evaluación de candidatos
**Para:** Mariano · Descargar CVs: [📎 Laura Méndez](https://github.com/rafaadrover/curs-ia-roig/raw/main/ejemplos/cv_laura_mendez.pdf) · [📎 Tomás García](https://github.com/rafaadrover/curs-ia-roig/raw/main/ejemplos/cv_tomas_garcia.pdf) · [📎 Priya Nair](https://github.com/rafaadrover/curs-ia-roig/raw/main/ejemplos/cv_priya_nair.pdf)

**Situación:** Tienes 3 CVs para el puesto de Agente de Atención al Cliente. En lugar de leer cada uno y comparar mentalmente, la IA genera una matriz con puntuaciones objetivas.

```
🔵 CONTEXTO:
Soy responsable de RRHH en una empresa de rent-a-car.
Estoy en proceso de selección para el puesto de Agente de Atención al Cliente.
Tengo 3 candidatos y necesito comparar su idoneidad de forma objetiva.

🟡 TAREA:
A partir de los CVs adjuntos, crea una matriz comparativa con estas competencias:
orientación al cliente, comunicación, resolución de problemas, idiomas, experiencia en sector.
Puntúa cada competencia del 1 al 5 por candidato y justifica brevemente cada puntuación.
Añade una recomendación final indicando qué candidato seleccionarías y por qué.

🟢 FORMATO:
Primero la tabla de puntuaciones. Luego un párrafo de recomendación por cada candidato.

[PEGAR LOS CVs O ARRASTRAR EL FICHERO]
```

---

## Ejercicio 10 — Simulación de negociación laboral
**Para:** Mariano · [📎 Descargar fichero de ejemplo](https://raw.githubusercontent.com/rafaadrover/curs-ia-roig/main/ejemplos/ejemplo_negociacion_rrll.txt)

**Situación:** Antes de reunirte con el comité de empresa, necesitas anticipar sus argumentos y preparar respuestas. La IA actúa como la parte contraria para que llegues preparado.

```
🔵 CONTEXTO:
Soy el responsable de RRHH de una empresa de rent-a-car en Mallorca con 78 trabajadores.
Tenemos que negociar con el comité de empresa una ampliación del horario en verano para la delegación del aeropuerto.
Te adjunto el contexto completo de nuestra posición y los datos de apoyo.

🟡 TAREA:
Simula los argumentos que podría plantear la representación sindical en contra de nuestra propuesta.
Para cada argumento, dame el contraargumento más sólido desde nuestra posición.
Al final, propón una posible propuesta de acuerdo intermedio equilibrada y defendible para ambas partes.

🟢 FORMATO:
Tabla de dos columnas: Argumento sindical | Nuestro contraargumento.
Luego un párrafo con la propuesta de acuerdo intermedio.

[PEGAR EL CONTEXTO O ARRASTRAR EL FICHERO]
```

---

## Ejercicio 11 — Plan de onboarding
**Para:** Mariano

```
🔵 CONTEXTO:
Soy responsable de RRHH en una empresa de rent-a-car en Mallorca con delegaciones en aeropuerto,
Palma centro y zonas turísticas. Acabamos de contratar a un nuevo agente comercial.

🟡 TAREA:
Diseña un plan de onboarding de 30 días para esta incorporación.
Incluye: objetivos de cada semana, actividades de formación, con quién debe reunirse
y cómo mediremos que la integración va bien.

🟢 FORMATO:
Tabla con columnas: Semana | Objetivos | Actividades | Responsable | Indicador de éxito.
```

---

## Ejercicio 12 — Redactar un acta de reunión
**Para:** Todos · [📎 Descargar fichero de ejemplo](https://raw.githubusercontent.com/rafaadrover/curs-ia-roig/main/ejemplos/ejemplo_notas_reunion.txt)

**Situación:** El secretario de una reunión ha tomado notas en bruto mientras todo el mundo hablaba — abreviaturas, frases incompletas, sin formato. Hay que convertir esas notas en un acta profesional lista para archivar y compartir.

**Cómo hacerlo:** descarga el fichero, ábrelo, copia todo el contenido y pégalo al final del prompt.

```
🔵 CONTEXTO:
Soy el secretario de una reunión de dirección en Roig Rent-a-Car celebrada el 16 de junio de 2026.
Tengo las notas en bruto que tomé durante la reunión.

🟡 TAREA:
Redacta el acta formal de la reunión a partir de mis notas.
Incluye: lista de asistentes con su cargo, hora de inicio y fin, orden del día deducido de los temas tratados,
resumen de lo que aportó cada persona, acuerdos y compromisos adoptados con responsable y fecha límite.

🟢 FORMATO:
Documento estructurado con secciones: Datos de la reunión | Asistentes | Orden del día |
Desarrollo de la reunión (por participante) | Acuerdos y compromisos | Próxima reunión.
Tono formal y redacción en tercera persona.

Notas: [PEGAR LAS NOTAS AQUÍ]
```

---

## Lo que NO funciona — prompts malos

#### ❌ El prompt vacío
```
Ayúdame con las ventas.
```
> La IA no sabe nada de ti ni de tu empresa. Responderá con consejos genéricos de manual.

#### ❌ Mucho relleno, poca sustancia
```
Hola, buenos días, espero que estés bien. Soy una persona que trabaja en una empresa
y me gustaría que pudieras ayudarme si no es mucha molestia con una cosa relacionada
con mi trabajo. Básicamente lo que necesito es como un informe o algo así de las ventas.
```
> Mucho texto, cero información útil. La respuesta será igual de vaga.

#### ❌ Sin datos adjuntos
```
Analiza estos datos y haz un informe.
```
> ¿Qué datos? Si no pegas nada, la IA no tiene nada que analizar.

#### ❌ Demasiadas tareas a la vez
```
Necesito un informe de ventas, una presentación para gerencia, un email para clientes
y un plan de acción para el próximo trimestre.
```
> Cuatro tareas en un mensaje = resultados superficiales en todo. Una tarea por prompt.

#### ✅ El mismo caso, bien planteado
```
🔵 CONTEXTO:
Soy responsable comercial de una empresa de rent-a-car en Mallorca.
Te adjunto los datos de ventas de mayo por delegación.

🟡 TAREA:
Redacta un informe ejecutivo de máximo una página con puntos positivos,
puntos de mejora y 3 recomendaciones concretas.

🟢 FORMATO:
Texto con subtítulos. Tono profesional y directo.

Datos: [PEGAR AQUÍ]
```

---

## Cómo mejorar un prompt que no funciona

1. **Añade contexto** — cuanto más sabe la IA de tu situación, mejor responde
2. **Sé más específico** — "haz un informe" → "haz un informe de una página con 3 secciones"
3. **Pide el formato** — tabla, lista, email formal, ficha estructurada...
4. **Pídele que mejore** — "hazlo más conciso" / "cambia el tono" / "añade una columna de prioridad"

---

## Cheatsheet — Para guardar y usar mañana

| Caso de uso | 🔵 Contexto | 🟡 Tarea | 🟢 Formato |
|-------------|-------------|----------|------------|
| Filtrar extracto bancario | Tarjeta prepago empresa | Filtra parking (AENA/SMAP), ignora recargas | Tabla fecha/establecimiento/importe + total |
| Informe de ventas | Empresa rent-a-car, datos por delegación | Informe: positivos, mejoras, 3 recomendaciones | Texto con subtítulos |
| Comparar presupuestos | Responsable compras, 2 presupuestos | Compara precio, plazo, garantía y recomienda | Tabla + párrafo recomendación |
| Nombres de carpetas flota | Lista vehículos con bastidor/matrícula | Genera B1_MARCA_MODELO_MATRICULA | Una línea por vehículo, mayúsculas |
| Extraer datos de factura | Factura escaneada PDF | Extrae nº, fecha, proveedor, matrícula, totales | Tabla con esos campos |
| Ideas de blog SEO | Rent-a-car Mallorca, público empresas | 10 ideas por potencial de búsqueda | Tabla título/intención/palabras clave |
| Adaptar eslogan a idiomas | Rent-a-car, mercados ES/DE/UK | Adapta manteniendo tono, no traducción literal | Una línea por idioma + justificación |
| Matriz candidatos RRHH | 3 CVs, puesto atención al cliente | Compara 5 competencias, puntúa 1-5 | Tabla + párrafo recomendación |
| Negociación laboral | RRHH, negociación con comité empresa | Simula argumentos sindicales + contraargumentos | Tabla + propuesta intermedia |
| Plan de onboarding | RRHH, nueva incorporación comercial | Plan 30 días con objetivos y KPIs | Tabla semanal 5 columnas |

---

*Curso preparado por Informática Roig · Junio 2026*
