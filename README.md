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
   - **Texto completo**: todo el ART en un bloque, para copiar, compartir o guardar.
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

## Catálogo de peligros

Vienen cargados los 11 que aparecen en los ART reales de la obra:

`01 Golpeado contra · 02 Caída mismo Nivel · 03 Caída Distinto Nivel · 04 Caída de Altura ·
12 Exposición a Sílice · 13 Exposición a Ruido · 15 Exposición a vibraciones ·
17 Proyección de partículas · 18 Sobreesfuerzo · 27 Caída de materiales · 28 Contacto Eléctrico`

Foco tiene más números (05 a 11, 14, 16, 19 a 26). Cuando aparezca uno nuevo en un ART:
pestaña **Peligros → + Agregar peligro**, se pone el número que usa Foco, el nombre y sus medidas
(una por línea). Desde ahí queda disponible para cualquier labor.

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
