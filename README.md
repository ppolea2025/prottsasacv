# PROTTSA — Asesor de Pedido Guiado
## Instrucciones de uso y mantenimiento

---

## ESTRUCTURA DE CARPETAS

```
prottsa/
├── index.html       ← El asesor guiado (NO tocar)
├── catalogo.md      ← El catálogo editable por el cliente
├── vercel.json      ← Config Vercel (NO tocar)
├── logo.png         ← Logotipo PROTTSA
├── fonts/
│   └── KernelSSK.ttf  ← Tipografía de marca PROTTSA
├── imgs/            ← Carpeta de fotos de productos
│   ├── allen-14x1.jpg
│   ├── disco-corte.jpg
│   └── ... (agregar aquí las fotos)
└── README.md        ← Este archivo
```

---

## CÓMO ACTUALIZAR EL CATÁLOGO

Se edita SOLO el archivo `catalogo.md` — con cualquier editor de texto
(Bloc de notas, Word guardado como .txt, Notepad++, VS Code).

### Agregar un producto nuevo:
```
- PRODUCTO: Nombre con medida | Descripción corta. | codigo:IA7ES07501250UNC | precio:380 | mayoreo:5x350 | unidad:millar | foto:archivo.jpg
```

**La medida SIEMPRE va dentro del nombre del producto:**
```
- PRODUCTO: Tornillo Allen 1/4 x 1 pulg, Grado 8.8, Zincado | ...
```

**Código alfanumérico PROTTSA** (`codigo:`):
- Es el código interno que ya usa el cliente para identificar cada producto
  (ej. `IA7ES07501250UNC`, `I12HCP0375X1125Z`).
- Se muestra **antes del nombre** en la tarjeta del producto, en la lista de
  pedido, en el mensaje de WhatsApp y en la cotización PDF.
- También permite **buscar el producto directamente** desde el buscador en
  el header (por código exacto o por nombre/medida).
- Es opcional — si un producto no tiene código todavía, simplemente omite
  `| codigo:...` y no aparecerá ese campo (no rompe nada).

**Unidad de venta** (`unidad:millar` o `unidad:pieza`):
- Si se omite, el sistema asume **MILLAR** por default (catálogo de tornillería/consumibles).
- Usa `unidad:pieza` solo para productos sueltos: herramienta, equipo de seguridad,
  lámina, perfil, artículos grandes que no se venden por millar.

**Precio y mayoreo:**
- `precio:380` → precio normal por unidad (millar o pieza, según el campo `unidad:`)
- `mayoreo:5x350` → significa "desde 5 unidades, $350 c/u" (el escalón de mayoreo)
- Si el producto no tiene precio fijo (se cotiza directo), omite `| precio:...`

Si no hay foto, omitir `| foto: ...`:
```
- PRODUCTO: Nombre con medida | Descripción corta. | precio:380 | unidad:pieza
```

### Marcar producto sin stock:
```
- AGOTADO: Nombre del producto
```

### Cambiar el diálogo del asesor en una subcategoría:
```
dialogo: ¿Nueva pregunta que quieres que haga el asesor?
```

---

## NOTAS / OBSERVACIONES

Debajo del método de entrega hay un campo de **Notas / Observaciones**, con
3 frases rápidas precargadas (flete por cobrar, precios sujetos a cambio,
disponibilidad de almacén) más un cuadro de texto libre para cualquier
observación adicional. Lo que se escriba aquí viaja automáticamente al
mensaje de WhatsApp y a la cotización PDF.

Para editar o agregar las frases rápidas, búscalas en `index.html` dentro
del bloque `<div class="notas-chips">` — son 3 botones, cada uno llama a
`agregarFraseNota('texto de la frase')`.

---

## BUSCADOR POR CÓDIGO O NOMBRE

Arriba a la derecha, junto al botón "Mi pedido", hay un campo de búsqueda.
Funciona escribiendo a partir de 2 caracteres y busca coincidencias en:

- El **código** alfanumérico del producto (ej. escribir `IA7ES` encuentra
  todos los tornillos estructurales que empiecen con ese código)
- El **nombre/medida** del producto (ej. escribir `3/8` encuentra todo lo
  que tenga esa medida en el nombre)

Los resultados se muestran como tarjetas de producto normales — se puede
agregar al pedido directamente desde ahí, sin necesidad de navegar por
categoría y subcategoría. Es la forma rápida de trabajar cuando el cliente
o el ejecutivo ya conocen el código de memoria.

---

## CANTIDADES EN PRODUCTOS POR MILLAR (compra parcial)

Para productos con `unidad:millar`, el sistema acepta cantidades en **decimales**,
porque muchos clientes compran menos de un millar completo (ej. 100, 250 o 350
piezas en vez de 1,000).

- Al agregar el producto, la cantidad inicial es **0.100 millares (100 piezas)**.
- Los botones **+ / −** avanzan de 100 en 100 piezas.
- Hay un campo numérico editable donde se puede **teclear directamente la
  cantidad de piezas** (ej. escribir `350` ahí pone 0.350 millares).
- En pantalla, en el pedido, en WhatsApp y en el PDF siempre se muestran
  **ambas unidades**: `0.350 millares (350 pzs)` — así no hay confusión
  entre el cliente y el área comercial.
- El precio y el escalón de mayoreo se calculan de forma proporcional y
  exacta sobre la cantidad real (decimales incluidos) — no hay redondeos
  que afecten el total.

Los productos con `unidad:pieza` no se ven afectados por este cambio —
siguen funcionando con números enteros, de 1 en 1, como siempre.

---

## MODO DE ATENCIÓN (Distribuidor vs Ejecutivo)

En la parte superior de la app hay un selector de **Modo de atención**:

- **Cliente Distribuidor (autoservicio):** el cliente distribuidor usa la app
  directamente desde su celular o computadora, sin asistencia.
- **Ejecutivo PROTTSA en tableta:** lo usa el equipo de ventas para atender en
  oficina a clientes de categoría Ferretería o Local de Herramientas. En este
  modo aparece un campo para capturar el **nombre del vendedor/ejecutivo**,
  que queda registrado tanto en el mensaje de WhatsApp como en la cotización PDF.

El modo seleccionado se guarda en el dispositivo (no se comparte entre
computadoras ni tabletas distintas) — cada equipo debe configurarlo una vez.

---

## MÉTODO DE ENTREGA

Dentro del panel de pedido el cliente o el ejecutivo eligen uno de tres
métodos antes de enviar:

1. **Recoge el cliente en almacén**
2. **Envío por transportista** (a cargo del cliente)
3. **Envío PROTTSA**

Esta selección se incluye automáticamente en el mensaje de WhatsApp y en
la cotización PDF.

---

## COTIZACIÓN EN PDF

El botón **"📄 Cotización PDF"** genera una hoja de cotización con:
- Folio, fecha, vendedor (si aplica modo ejecutivo) y método de entrega
- Tabla de productos, cantidades y subtotales
- Total estimado

Usa la función de impresión del navegador (`Ctrl+P` / `Cmd+P`) — el cliente
solo debe elegir **"Guardar como PDF"** como destino de impresión. No requiere
ningún servidor ni librería adicional.

> Nota: este documento es informativo y queda sujeto a confirmación de precio
> y disponibilidad por parte de PROTTSA — no es una factura.

---

## CÓMO AGREGAR FOTOS

1. Nombrar el archivo en minúsculas, sin espacios, con guiones: `allen-38x2.jpg`
2. Subir el archivo a la carpeta `imgs/` en Vercel
3. En el catálogo.md, agregar `| foto: allen-38x2.jpg` al producto

**Tamaño recomendado:** 600×600 px, JPG, máximo 200 KB por imagen.
Puedes comprimir en: squoosh.app

---

## CÓMO HACER DEPLOY EN VERCEL

1. Asegúrate de que la carpeta tenga:
   - `index.html`
   - `catalogo.md`
   - `vercel.json`
   - `logo.png`
   - carpeta `fonts/` con `KernelSSK.ttf`
   - carpeta `imgs/` (aunque esté vacía)

2. Arrastra la carpeta completa a **vercel.com/new**

3. Vercel genera una URL tipo: `prottsa-catalogo.vercel.app`

4. Para actualizar después: vuelve a arrastrar la carpeta o usa `vercel deploy`

**El catálogo.md tiene cache desactivado** — los cambios al catálogo
se ven inmediatamente sin necesidad de redesplegar.

---

## CONFIGURAR EL NÚMERO DE WHATSAPP

Antes de poner en producción, edita en `index.html` la línea:

```js
const WA_NUMERO = "5215500000000"; // ← Sustituir por el número real de PROTTSA
```

Formato: código de país + número, sin espacios ni símbolos (ej: `5215512345678`).

---

## PARA EL CLIENTE — Actualizar el catálogo sin Vercel

Si se quiere actualizar solo el catálogo.md sin pasar por el desarrollador:

1. Conectar a Vercel con cuenta de GitHub
2. Subir el catálogo.md a un repositorio privado
3. Cada vez que se empuje un cambio, Vercel redespliega automático

---

*PROTTSA · Forjando Calidad · Tecnología MAGNETIA · IMMERSIO Software*
