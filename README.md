# Curso de Introducción a la IA — Equipo Roig
**Duración:** 1 hora · **Nivel:** Sin conocimientos previos · **Fecha:** Junio 2026

---

## Índice de bloques

| # | Bloque | Tiempo |
|---|--------|--------|
| 0 | Bienvenida y calibración | 5 min |
| 1 | La IA como asistente de texto y análisis | 15 min |
| 2 | La IA con documentos y archivos | 10 min |
| 3 | Marketing y comunicación con IA | 10 min |
| 4 | Recursos Humanos con IA | 10 min |
| 5 | Taller rápido: cada uno su prompt | 5 min |
| 6 | Buenas prácticas y cierre | 5 min |

---

## Bloque 0 — Bienvenida y calibración (5 min)

### Guía del formador
- Abrir en el navegador: **claude.ai** o **chatgpt.com** — sin instalar nada
- Explicar en dos frases qué es la IA generativa: *"Es un colaborador que sabe de todo pero puede equivocarse. Tú siempre revisas y firmas."*
- Regla de oro de la sesión: **Contexto + Tarea + Formato de salida** = prompt que funciona

### La regla de los 3 elementos

```
🔵 CONTEXTO  →  Quién eres, cuál es tu negocio, qué datos tienes
🟡 TAREA     →  Qué quieres que haga exactamente
🟢 FORMATO   →  Cómo quieres la respuesta (tabla, lista, informe, email...)
```

---

## Bloque 1 — La IA como asistente de texto y análisis (15 min)

### Guía del formador
Tres demos en directo, cada una ~4 min. Abrir el fichero de ejemplo correspondiente, copiar el contenido y pegarlo en el chat.

---

### Demo 1.1 — Filtrar y sumar tiques de parking
**Para:** Antonia Pons / Xisca Rigo · **Fichero:** `ejemplo_extracto_bancario.txt`

> **Caso real:** El extracto del prepago empresa (CaixaBank) tiene 74 operaciones. Hay que introducir en SAGE solo las partidas de AENA y SMAP, excluyendo recargas y establecimientos que no sean parking.

**Prompt:**
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

### Demo 1.2 — Informe de ventas comercial
**Para:** Alexia Alcañiz · **Fichero:** `ejemplo_datos_ventas.txt`

> **Caso real:** Cada mes Alexia necesita claridad sobre ventas por delegación. Sin CRM nuevo, la IA actúa como analista de datos.

**Prompt:**
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

### Demo 1.3 — Comparar presupuestos de proveedores
**Para:** Guillem Monserrat · **Fichero:** `ejemplo_presupuestos.txt`

> **Caso real:** Guillem recibe presupuestos de varios proveedores para el mismo producto y necesita una comparativa rápida.

**Prompt:**
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

## Bloque 2 — La IA con documentos y archivos (10 min)

### Guía del formador
Mostrar cómo arrastrar un fichero (Excel, PDF, imagen) directamente al chat. La IA lo lee y trabaja con él.

---

### Demo 2.1 — Generar nombres de carpeta por matrícula
**Para:** Antonia Pons · **Fichero:** `ejemplo_flota_vehiculos.txt`

> **Caso real:** El equipo escanea documentos de flota (permisos de circulación, fichas técnicas, recibos de seguro). Se necesitan carpetas individuales por vehículo con código asignado.

**Prompt:**
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

[ARRASTRAR EL FICHERO O PEGAR LA LISTA]
```

---

### Demo 2.2 — Diseñar el flujo de devoluciones
**Para:** Xisca Rigo

> **Caso real:** Cuando llega una solicitud de devolución, el flujo no está claro: quién la aprueba, cómo se tramita según el método de pago.

**Prompt:**
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

### Demo 2.3 — Extraer datos de un documento escaneado
**Para:** Antonia Pons / Cati Roig · **Fichero:** `ejemplo_factura_escaneada.txt`

**Prompt:**
```
🔵 CONTEXTO:
Tengo una factura de taller mecánico en formato PDF escaneado.

🟡 TAREA:
Extrae los datos principales del documento.

🟢 FORMATO:
Tabla con estas columnas: Nº Factura | Fecha | Proveedor | Matrícula vehículo | Base imponible | IVA | Total.
Si algún dato no es legible, escribe "no legible" en esa celda.

[ARRASTRAR EL PDF O IMAGEN]
```

---

## Bloque 3 — Marketing y comunicación con IA (10 min)

### Guía del formador
Demos para Helena. Mostrar también que se puede pedir a la IA que "mejore" un texto existente pasándolo directamente.

---

### Demo 3.1 — Ideas de blog con intención SEO
**Para:** Helena Bonnin

**Prompt:**
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

### Demo 3.2 — Adaptar un eslogan a tres idiomas
**Para:** Helena Bonnin

**Prompt:**
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

### Demo 3.3 — Crear buyer persona
**Para:** Helena Bonnin

**Prompt:**
```
🔵 CONTEXTO:
Somos una empresa de rent-a-car B2B en Mallorca. Queremos mejorar la segmentación de nuestras campañas
para el mercado de empresas alemanas que necesitan vehículos para desplazamientos de negocio en la isla.

🟡 TAREA:
Crea un buyer persona detallado para este perfil de cliente.
Incluye: perfil demográfico, motivaciones de compra, puntos de dolor, canales que usa para informarse
y objeciones habituales antes de contratar.

🟢 FORMATO:
Ficha estructurada con secciones claramente separadas. Máximo una página.
```

---

## Bloque 4 — Recursos Humanos con IA (10 min)

### Guía del formador
Tres demos para Mariano. Cubren selección, relaciones laborales e itinerarios formativos.

---

### Demo 4.1 — Matriz de evaluación de candidatos
**Para:** Mariano · **Fichero:** `ejemplo_cvs_candidatos.txt`

> **Caso real:** Mariano recibe varios CVs y necesita una comparativa objetiva por competencias sin leer cada CV entero.

**Prompt:**
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

### Demo 4.2 — Simulación de negociación laboral
**Para:** Mariano · **Fichero:** `ejemplo_negociacion_rrll.txt`

> **Caso real:** Antes de reunirse con la RLT, Mariano necesita anticipar argumentos y preparar respuestas.

**Prompt:**
```
🔵 CONTEXTO:
Soy el responsable de RRHH de una empresa de rent-a-car en Mallorca con 78 trabajadores.
Tenemos que negociar con el comité de empresa una ampliación del horario en verano para la delegación del aeropuerto.
Te adjunto el contexto completo de nuestra posición y los datos de apoyo.

🟡 TAREA:
Simula los argumentos que podría plantear la representación sindical en contra de nuestra propuesta.
Para cada argumento, dame el contraargumento más sólido desde nuestra posición.
Al final, propón una posible propuesta de acuerdo intermedio que sea equilibrada y defendible para ambas partes.

🟢 FORMATO:
Tabla de dos columnas: Argumento sindical | Nuestro contraargumento.
Luego un párrafo con la propuesta de acuerdo intermedio.

[PEGAR EL CONTEXTO O ARRASTRAR EL FICHERO]
```

---

### Demo 4.3 — Plan de onboarding
**Para:** Mariano

> **Caso real:** Las nuevas incorporaciones se acogen de forma informal. Mariano quiere estructurar un plan de 30 días.

**Prompt:**
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

### Otros prompts útiles para RRHH

- **Descripción de puesto:** *"Redacta una descripción de puesto para [CARGO]... Incluye misión, responsabilidades, competencias y condiciones."*
- **Análisis de convenio:** *"Resume los puntos clave del siguiente convenio colectivo en relación a [TEMA]..."*
- **KPIs de RRHH:** *"Propón 8 KPIs para el cuadro de mando de RRHH de una empresa de 80 personas en rent-a-car..."*

---

## Bloque 5 — Taller rápido: cada uno su prompt (5 min)

### Guía del formador
- Cada participante dice su caso en voz alta
- El formador construye el prompt en directo siguiendo la regla **Contexto + Tarea + Formato**
- Objetivo: cada persona sale con 1 prompt listo para usar mañana

### Casos preparados por si salen

**Adriana — Valoración de daños en coche:**
```
🔵 CONTEXTO:
Trabajo en una empresa de rent-a-car. Un cliente ha devuelto un vehículo (PEUGEOT 2008, año 2023) con daños.
Adjunto fotos del estado del vehículo.

🟡 TAREA:
A partir de las imágenes, haz una valoración aproximada del coste de reparación de los daños visibles.

🟢 FORMATO:
Tabla con columnas: Zona del vehículo | Tipo de daño | Reparación probable | Coste estimado (€).
```

**Alexia — CRM ligero con notas de visitas:**
```
🔵 CONTEXTO:
Soy responsable comercial de una empresa de rent-a-car. Tengo notas de visitas comerciales escritas
en formato libre durante la semana.

🟡 TAREA:
Para cada nota, extrae: nombre del cliente, empresa, fecha, tema tratado, próxima acción y fecha de seguimiento.
Evalúa la urgencia de cada cliente.

🟢 FORMATO:
Tabla con columnas: Cliente | Empresa | Fecha visita | Tema | Próxima acción | Fecha seguimiento | Prioridad (Alta/Media/Baja).

Notas: [PEGAR AQUÍ]
```

---

## Bloque 6 — Buenas prácticas y cierre (5 min)

### Lo que nunca hay que hacer
- No pegar **datos personales de clientes** (DNI, datos bancarios, direcciones)
- No compartir **contraseñas ni credenciales**
- No subir información **confidencial de contratos con terceros**

---

### Prompts que NO funcionan — y por qué

#### ❌ El prompt vacío
```
Ayúdame con las ventas.
```
> **Problema:** La IA no sabe nada de ti, de tu empresa ni de lo que necesitas.
> Responderá con consejos genéricos de manual que no te sirven de nada.

---

#### ❌ El prompt con mucho relleno y poca sustancia
```
Hola, buenos días, espero que estés bien. Soy una persona que trabaja en una empresa
y me gustaría que pudieras ayudarme si no es mucha molestia con una cosa relacionada
con mi trabajo que tengo que hacer y que me está costando un poco. Básicamente lo que
necesito es como un informe o algo así de las ventas si puedes. Gracias de antemano
y quedo a tu disposición para cualquier aclaración que necesites.
```
> **Problema:** Mucho texto, cero información útil. La IA no sabe qué ventas, de qué periodo,
> en qué formato, ni para qué sirve el informe. Recibirás una respuesta igual de vaga.

---

#### ❌ El prompt demasiado corto sin datos
```
Analiza estos datos y haz un informe.
```
> **Problema:** ¿Qué datos? ¿Qué tipo de informe? ¿Para quién? ¿En qué formato?
> Sin contexto ni instrucciones concretas, la IA inventa o pregunta de vuelta.

---

#### ❌ El prompt que pide demasiadas cosas a la vez
```
Necesito que me hagas un informe de ventas, una presentación para gerencia, un email
para enviar a los clientes, ideas para mejorar el negocio, un análisis de la competencia
y un plan de acción para el próximo trimestre.
```
> **Problema:** Seis tareas distintas en un solo mensaje. El resultado será superficial en todo.
> Mejor hacer un prompt por tarea, uno detrás del otro.

---

#### ✅ El mismo caso, bien planteado
```
🔵 CONTEXTO:
Soy responsable comercial de una empresa de rent-a-car en Mallorca.
Te adjunto los datos de ventas de mayo por delegación.

🟡 TAREA:
Redacta un informe ejecutivo de máximo una página con:
puntos positivos, puntos de mejora y 3 recomendaciones concretas.

🟢 FORMATO:
Texto con subtítulos. Tono profesional y directo.

Datos: [PEGAR AQUÍ]
```
> **Resultado:** La IA tiene todo lo que necesita para darte exactamente lo que pediste.

---

### Cómo mejorar un prompt que no funciona
1. **Añade más contexto** — cuanto más sabe la IA de tu situación, mejor responde
2. **Sé más específico en la tarea** — "haz un informe" → "haz un informe de una página con 3 secciones"
3. **Especifica el formato** — tabla, lista numerada, email formal, ficha...
4. **Pídele que lo mejore** — "hazlo más conciso" / "añade una columna de prioridad" / "cambia el tono"

### Recursos para seguir aprendiendo
- **Claude** — claude.ai (recomendado para tareas de negocio)
- **ChatGPT** — chatgpt.com (el más conocido)
- **Perplexity** — para búsquedas con fuentes verificadas

---

## Cheatsheet de prompts — Para imprimir y guardar

| Caso de uso | 🔵 Contexto | 🟡 Tarea | 🟢 Formato |
|-------------|-------------|----------|------------|
| Filtrar extracto bancario | Tarjeta prepago empresa, extracto mensual | Filtra solo parking (AENA/SMAP), ignora recargas | Tabla fecha/establecimiento/importe + total |
| Informe de ventas | Empresa rent-a-car, datos por delegación | Informe ejecutivo: positivos, mejoras, 3 recomendaciones | Texto con subtítulos, tono profesional |
| Comparar presupuestos | Responsable de compras, 2 presupuestos recibidos | Compara precio, plazo, garantía y recomienda | Tabla comparativa + párrafo de recomendación |
| Nombres de carpetas | Lista de vehículos con bastidor/matrícula/modelo | Genera nombre formato B1_MARCA_MODELO_MATRICULA | Una línea por vehículo, mayúsculas |
| Extraer datos de factura | Factura escaneada en PDF | Extrae nº factura, fecha, proveedor, matrícula, totales | Tabla con esos campos |
| Ideas de blog SEO | Rent-a-car Mallorca, público empresas y turismo negocio | 10 ideas de artículos por potencial de búsqueda | Tabla título/intención/palabras clave |
| Matriz de candidatos | RRHH, proceso selección, 3 CVs | Compara por 5 competencias, puntúa 1-5, recomienda | Tabla de puntuaciones + párrafo recomendación |
| Negociación laboral | RRHH, contexto de negociación con comité | Simula argumentos sindicales + contraargumentos | Tabla argumento/contraargumento + propuesta |
| Plan de onboarding | RRHH, nueva incorporación commercial | Plan 30 días con objetivos, actividades, KPIs | Tabla semanal 4 columnas |
| CRM con notas de visitas | Comercial, notas en formato libre | Extrae cliente, acción, fecha seguimiento, prioridad | Tabla estructurada |

---

*Curso preparado por Informática Roig · Junio 2026*
