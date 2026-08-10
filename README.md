# ART Rápida — generador de ART para Foco Prevención

App de un solo archivo (`ART.html`) para armar el **Análisis de Riesgos de la Tarea** en segundos
y después copiarlo campo por campo dentro de la app **Foco Prevención**.

Obra: Condominio Alberto Fuchslocher, Osorno.

## La idea

En vez de escribir el ART entero cada mañana, se parte por **quién trabaja hoy**:

```
personas presentes → sus labores → peligros (01, 02, 04, 12…) → medidas de control + RCO + checklist
```

Si alguien falta, su labor sale del ART y con ella sus peligros y sus riesgos críticos.
Si alguien hace hoy una labor que normalmente no hace, se activa como "parcial" con un toque.

## Uso diario (3 minutos)

1. **Paso 1 · Datos** — fecha, área de trabajo, charla de seguridad. El "trabajo a realizar" se
   autocompleta con las labores de la cuadrilla si lo dejas vacío.
2. **Paso 2 · Cuadrilla** — toca a los presentes. Bajo cada uno aparecen sus labores: naranjas
   las principales, con borde las parciales. Botón *Misma cuadrilla que la última* para repetir.
3. **Paso 3 · Revisión** — etapas ya armadas y numeradas, con sus peligros. Se pueden reordenar (↑↓),
   quitar (✕), agregar a mano, y tocar `+ peligros` para sumar o sacar peligros de una etapa.
   Debajo van el checklist previo (SÍ/NO/N-A con observación) y los 19 RCO ya precargados.
4. **Paso 4 · Salida** — dos modos:
   - **Campo por campo**: cada tarjeta lleva la etiqueta exacta de Foco Prevención y un botón
     *Copiar*. Al copiar queda en verde, así no se pierde el hilo al saltar entre las dos apps.
     Las etapas vienen **comprimidas, una por acordeón**: se abre solo la que se está pasando a
     Foco y el resto queda fuera del camino. Dentro de cada una: el texto de la etapa (editable,
     con contador de 100 caracteres y botón *Copiar texto de la etapa*), los peligros a
     seleccionar y las medidas a marcar. *Restaurar* devuelve el texto original del catálogo.
     Arriba hay *Copiar las N etapas*, *Abrir todas* y *Cerrar todas*.
   - **Texto completo**: todo el ART en un bloque, para copiar, compartir o guardar.

**Editar el texto de una etapa** cambia solo ese ART; el catálogo de labores queda intacto. Para
cambiarlo de forma permanente hay que hacerlo en la pestaña **Labores**.

**El texto oficial de las 13 preguntas previas** está dentro de la app: bajo cada pregunta hay una
viñeta *texto oficial de la pregunta* que despliega el enunciado completo tal cual aparece en
Foco Prevención, en letra chica. Está tanto en el paso de revisión como en la salida.
5. **Guardar en historial** para poder reusarlo otro día.

## Las 4 pestañas de mantención

| Pestaña | Para qué |
|---|---|
| **ART** | El del día (los 4 pasos de arriba) |
| **Personal** | Nómina por **iniciales** y cargo, y qué labores hace cada uno (principales / parciales). El RUT es un campo opcional que queda solo en el teléfono |
| **Labores** | Cada labor = una etapa del ART: su texto, su orden, sus peligros y qué fuerza en el checklist |
| **Peligros** | Catálogo numerado igual que Foco (01 Golpeado contra, 04 Caída de Altura, …) con sus medidas de control |
| **Historial** | ART guardados: copiar de nuevo o reusar como borrador |

Las labores marcadas **BASE** entran siempre: ingreso a obra, traslado, orden y aseo, retiro de obra.

## Partida cargada: instalación de ventanas

| # | Labor | Quién |
|---|---|---|
| BASE | Ingreso a obra · Traslado y desplazamiento por escaleras · Orden y aseo · Retiro de obra | todos |
| 10 | Traslado, movimiento y distribución de ventanas y elementos pesados | M.N, A.T, A.O |
| 20 | Instalación de ventanas: rotomartillo y atornillador inalámbrico, nivel láser | C.R, F.A, C.Ñ · (A.T parcial) |
| 30 | Sellos exteriores **en altura** con pistola calafatera y silicona | C.R, F.A, C.Ñ |
| 40 | Corte de tornillos, enfierradura y rasgos con esmeril angular | A.T |
| 50 | Carpintería en madera: sierra circular, serrucho, tizador | A.T |
| 60 | Pulido de rasgos con pulidora de hormigón y picado con cango | A.O |
| 70 | Pruebas de estanqueidad: cinta de aluminio y llenado de agua | A.C, C.F |
| 75 | Impermeabilización con Sikatop 107 Seal, mezclador eléctrico y brocha | M.N, A.T, C.F |
| 80 | Rectificación de rasgos y albañilería EIFS | M.N (parcial — hoy nadie fijo) |

Cargos: M.N jornal · A.T ayudante de carpintero · A.O jornal pulidor · C.R, F.A y C.Ñ ventaneros ·
A.C y C.F por definir.

Los únicos con trabajo en altura son **C.R**, **F.A** y **C.Ñ**, así que el RCO N°1 (caída por
trabajos en altura) solo se enciende cuando alguno de los tres está marcado presente.

## Catálogo de peligros

Están cargados los **31 de Foco Prevención**, con su numeración exacta. De esos, **18 se usan**
en la partida de instalación de ventanas:

| N° | Peligro | Dónde aparece |
|---|---|---|
| 01 | Golpeado contra | todas |
| 02 | Caída mismo Nivel | todas |
| 03 | Caída Distinto Nivel | todas menos ingreso y retiro |
| 04 | Caída de Altura | solo sellos exteriores |
| 05 | Aprisionamiento | movimiento de ventanas, instalación |
| 06 | Atrapamiento | instalación, corte, carpintería, pulido, impermeabilización, albañilería |
| 08 | Contacto con fuentes de calor | corte con esmeril |
| 09 | Contacto con elementos corto punzante | movimiento, instalación, corte, carpintería, estanqueidad, aseo, albañilería |
| 10 | Contacto con sustancias peligrosas | sellos (silicona), impermeabilización, albañilería |
| 11 | Intoxicación | sellos, impermeabilización |
| 12 | Exposición a Sílice | instalación, corte, pulido, albañilería |
| 13 | Exposición a Ruido | instalación, corte, carpintería, pulido, albañilería |
| 15 | Exposición a vibraciones | instalación, corte, pulido, albañilería |
| 17 | Proyección de partículas | instalación, corte, carpintería, pulido, impermeabilización, albañilería |
| 18 | Sobreesfuerzo | todas menos ingreso y retiro |
| 27 | Caída de materiales | todas menos ingreso y retiro |
| 28 | Contacto Eléctrico | instalación, corte, carpintería, pulido, impermeabilización, albañilería |
| 30 | Contaminación Ambiental | impermeabilización, albañilería, aseo |

Los otros 13 (07, 14, 16, 19, 20 a 26, 29, 31) existen en la app para que la numeración calce con
Foco, pero quedan **sin medidas de control** porque no aplican a esta partida (conducción,
radiación UV, incendio, túneles, tronaduras, izaje, buceo, maquinaria pesada, soldadura, flora y
fauna). Si alguna vez se necesita uno, se le escriben las medidas en **Peligros → Editar**;
mientras tanto, si se selecciona uno vacío la app avisa en el paso de revisión.

**Origen de las medidas de control:** todas están transcritas del propio selector
"Seleccione elementos" de Foco Prevención, así que el texto calza palabra por palabra con lo que
hay que marcar. No queda ninguna medida redactada a mano.

## Cómo se ve la salida de una etapa

Cada etapa produce las tres columnas que pide el formulario:

1. **Etapa** — el texto breve de la labor (máx. 100 caracteres)
2. **Identificación de peligros y riesgos** — `01.Golpeado contra, 02.Caída mismo Nivel, …`
3. **Medidas de control operacional** — agrupadas por peligro, con casilla para ir marcando:

```
04.Caída de Altura
   [ ] Mantener protegidas con barreras duras trabajos en altura
   [ ] Uso de arnés de seguridad con dos cabos de vida, 100% amarrado a un punto fijo
   [ ] Verificar que cuente con línea de vida independiente o punto de anclaje
   [ ] Verificar que plataforma de trabajo cuente con la tarjeta verde de aprobado
```

El botón *Copiar* de esa tarjeta entrega el mismo contenido en el formato de una línea que usa
Foco (`04.Mantener protegidas…,04.Uso de arnés…`), por si conviene pegarlo en vez de marcarlo.

El texto de medidas se genera con el mismo formato del documento impreso:

```
01.Coordinación de trabajos con mas de una persona en traslado de materiales,01.Mantener distancia segura…
```

## Respaldo

Pestaña **Peligros** → *Exportar respaldo (JSON)* guarda personal, labores, peligros e historial.
*Importar respaldo* lo devuelve. Conviene exportar después de cargar la nómina completa: los datos
viven solo en el navegador del teléfono (localStorage), no hay servidor.

## Instalar en el celular

Abrir la URL en Chrome → menú → **Agregar a pantalla de inicio**. Funciona sin señal.

## Publicar

GitHub Pages sobre este repo. Cada vez que se edita `ART.html` hay que subir el número de
`CACHE` en `sw.js` (`art-v1` → `art-v2`), si no los teléfonos siguen con la versión vieja.

## Probar en el PC

```bash
npx http-server C:\Proyectos\ART -p 8082 -c-1
```

Después abrir `http://localhost:8082/ART.html`.

## Notas

- Foco limita varios campos a 100 caracteres; la app avisa en rojo cuando un texto se pasa.
- El formulario acepta 13 etapas como máximo; si se pasan, sale aviso en el paso de revisión.
- Los RCO se encienden solos según los peligros presentes (04 → RCO 1, 27 → RCO 2, 28 → RCO 8 y 18,
  03 → RCO 19). Igual se pueden cambiar uno por uno a mano.
