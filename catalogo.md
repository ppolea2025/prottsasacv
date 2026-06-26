# CATÁLOGO — PROTTSA
# Comercializadora de Productos Metalmecánicos
#
# INSTRUCCIONES PARA EDITAR:
# — Cada categoría empieza con ## CATEGORIA: Nombre
# — Cada subcategoría empieza con ### SUB: Nombre
# — Los productos van con:
#   - PRODUCTO: nombre con medida | descripción | codigo:IA7ES07501250UNC | precio:50 | mayoreo:500x42 | unidad:millar | foto:archivo.jpg
# — La MEDIDA va siempre dentro del nombre del producto (ej: "Tornillo Allen 1/4 x 1 pulg")
# — codigo: el código alfanumérico interno PROTTSA del producto. Se muestra ANTES
#   del nombre en pantalla y permite buscar el producto directo en el buscador.
#   Si se omite, el producto simplemente no tiene código visible (no es obligatorio).
# — precio: precio normal por unidad (sin $ o con $, ambos funcionan)
# — mayoreo: 500x42 significa "desde 500 unidades, $42 c/u"
# — unidad: "millar" o "pieza". Si se omite, el sistema asume MILLAR por default.
#   Usa unidad:pieza SOLO para productos que se venden sueltos/por pieza individual
#   (ej. herramienta, equipo de seguridad, artículos grandes).
# — Si un producto no tiene foto, omite | foto:...
# — Si no hay precio fijo (cotización directa), omite | precio:...
# — Para marcar producto sin stock: - AGOTADO: nombre
# — No borres las líneas que empiezan con #

## CATEGORIA: Tornillería
icono: 🔩
descripcion: Tornillos, tuercas y birlos en medidas estándar y especiales.

### SUB: Tornillo Allen (Cabeza Hexagonal Hueca)
descripcion: Tornillería Allen grado 8.8 y grado 12.9, acabado zincado o negro.
dialogo: ¿Qué medida y longitud de tornillo Allen necesitas?

- PRODUCTO: Tornillo Allen 1/4 x 1 pulg, Grado 8.8, Zincado | Rosca estándar UNC, cabeza hexagonal hueca. | codigo:IA4ES02501000UNC | precio:380 | mayoreo:5x350 | unidad:millar | foto:allen-14x1.jpg
- PRODUCTO: Tornillo Allen 3/8 x 2 pulg, Grado 8.8, Zincado | Rosca estándar UNC, alta resistencia. | codigo:IA6ES03752000UNC | precio:620 | mayoreo:5x580 | unidad:millar | foto:allen-38x2.jpg
- PRODUCTO: Tornillo Allen 1/2 x 3 pulg, Grado 12.9, Negro Oxidado | Para uniones estructurales de alta exigencia. | codigo:IA8EN05003000UNC | precio:1450 | mayoreo:3x1380 | unidad:millar | foto:allen-12x3.jpg
- PRODUCTO: Tornillo Allen M8 x 25mm, Grado 8.8 | Métrico, rosca fina, zincado. | codigo:IA8ES0800025MM | precio:410 | mayoreo:5x390 | unidad:millar

### SUB: Tornillo Hexagonal (Cabeza de Tuerca)
descripcion: Tornillería hexagonal estándar para ensamble general.
dialogo: ¿Para qué tipo de ensamble necesitas el tornillo hexagonal?

- PRODUCTO: Tornillo Hexagonal 1/4 x 1 pulg, Grado 5, Zincado | Uso general, cabeza hexagonal estándar. | codigo:I12HE02501000UNC | precio:320 | mayoreo:5x300 | unidad:millar
- PRODUCTO: Tornillo Hexagonal 3/8 x 1.5 pulg, Grado 5, Zincado | Para ensamble estructural ligero. | codigo:I12HE03751500UNC | precio:520 | mayoreo:5x490 | unidad:millar
- PRODUCTO: Tornillo Hexagonal 1/2 x 2 pulg, Grado 8, Zincado | Alta resistencia para carga. | codigo:I12HE05002000UNC | precio:980 | mayoreo:3x920 | unidad:millar
- PRODUCTO: Tornillo Hexagonal Estructural A325 3/4"-10 UNC x 1 1/4" IM | Grado estructural A325, importado. | codigo:IA7ES07501250UNC | precio:1850 | mayoreo:3x1750 | unidad:millar
- PRODUCTO: Tornillo Hexagonal Estructural A325 1"-8 UNC x 4 1/4" IMP | Grado estructural A325, importado, alta longitud. | codigo:IA7ES10004250UNC | precio:3200 | mayoreo:3x3050 | unidad:millar

### SUB: Tuercas
descripcion: Tuercas hexagonales estándar y de seguridad.
dialogo: ¿Necesitas tuerca hexagonal estándar o tuerca de seguridad (con nylon)?

- PRODUCTO: Tuerca Hexagonal 1/4 pulg, Zincada | Rosca UNC estándar. | codigo:I12HX0250Z | precio:180 | mayoreo:5x165 | unidad:millar
- PRODUCTO: Tuerca Hexagonal 3/8 pulg, Zincada | Rosca UNC estándar. | codigo:I12HX0375Z | precio:240 | mayoreo:5x220 | unidad:millar
- PRODUCTO: Tuerca de Seguridad (Nylock) 1/4 pulg | Con inserto de nylon, evita aflojamiento por vibración. | codigo:I12NY0250Z | precio:310 | mayoreo:5x290 | unidad:millar
- PRODUCTO: Tuerca Cople Hexagonal 3/8" - 16 x 1 1/8" Zinc | Tuerca cople para unión y extensión de roscas, acabado zincado. | codigo:I12HCP0375X1125Z | precio:290 | mayoreo:5x270 | unidad:millar

### SUB: Birlos y Espárragos
descripcion: Birlos roscados en ambos extremos, medidas a solicitud.
dialogo: ¿Qué diámetro y longitud de birlo necesitas?

- PRODUCTO: Birlo 1/2 x 4 pulg, Grado 5 | Roscado en ambos extremos. | precio:1100 | mayoreo:3x1050 | unidad:millar
- PRODUCTO: Birlos Medida Especial | Fabricación a medida según especificación del cliente. Consultar con ejecutivo.


## CATEGORIA: Soldadura
icono: 🔥
descripcion: Electrodos, alambre y consumibles para soldadura.

### SUB: Electrodos
descripcion: Electrodos revestidos para soldadura por arco.
dialogo: ¿Qué tipo de electrodo y calibre necesitas?

- PRODUCTO: Electrodo E6011, Calibre 1/8 pulg | Para soldadura general, todas las posiciones. | precio:680 | mayoreo:10x640 | unidad:pieza | foto:electrodo-6011.jpg
- PRODUCTO: Electrodo E7018, Calibre 1/8 pulg | Bajo hidrógeno, para acero estructural. | precio:920 | mayoreo:10x870 | unidad:pieza
- PRODUCTO: Electrodo E6013, Calibre 3/32 pulg | Uso general, fácil manejo, para lámina delgada. | precio:610 | mayoreo:10x580 | unidad:pieza

### SUB: Alambre para Soldadura MIG
descripcion: Alambre sólido y tubular para proceso MIG/MAG.
dialogo: ¿Qué calibre de alambre MIG necesitas?

- PRODUCTO: Alambre MIG ER70S-6, Calibre 0.035 pulg | Rollo de 15 kg, para acero al carbón. | precio:1850 | unidad:pieza
- PRODUCTO: Alambre MIG ER70S-6, Calibre 0.045 pulg | Rollo de 15 kg, mayor penetración. | precio:1920 | unidad:pieza


## CATEGORIA: Herramienta
icono: 🛠️
descripcion: Herramienta manual e industrial para taller y obra.

### SUB: Herramienta Manual
descripcion: Herramienta de uso general para taller, ferretería y obra.
dialogo: ¿Qué herramienta manual estás buscando?

- PRODUCTO: Juego de Llaves Allen Métricas (1.5-10mm) | Set de 9 piezas en estuche. | precio:185 | unidad:pieza | foto:llaves-allen.jpg
- PRODUCTO: Llave de Cruz para Birlo, 4 Vías | Para ensamble y desensamble de birlos. | precio:320 | unidad:pieza
- PRODUCTO: Llave Perica Ajustable 10 pulg | Acero al cromo vanadio. | precio:280 | unidad:pieza

### SUB: Herramienta de Corte
descripcion: Discos y herramienta para corte y desbaste.
dialogo: ¿Necesitas disco de corte, de desbaste, o ambos?

- PRODUCTO: Disco de Corte 4.5 pulg para Metal | Para esmeriladora angular. | codigo:HDC04500045 | precio:35 | mayoreo:20x30 | unidad:pieza | foto:disco-corte.jpg
- PRODUCTO: Disco de Desbaste 4.5 pulg para Metal | Para esmeriladora angular, alta resistencia. | codigo:HDD04500045 | precio:42 | mayoreo:20x37 | unidad:pieza
- PRODUCTO: Disco de Corte 7 pulg para Metal | Para esmeriladora grande. | codigo:HDC07000070 | precio:65 | mayoreo:10x58 | unidad:pieza


## CATEGORIA: Equipo de Seguridad
icono: 🦺
descripcion: Equipo de protección personal para taller e industria.

### SUB: Protección Personal
descripcion: EPP básico para trabajo en taller y obra.
dialogo: ¿Qué equipo de protección personal necesitas?

- PRODUCTO: Casco de Soldar Fotosensible | Ajuste automático de sombra, batería solar. | precio:450 | unidad:pieza | foto:casco-soldar.jpg
- PRODUCTO: Guantes de Soldador, Carnaza | Par, resistentes a altas temperaturas. | precio:95 | mayoreo:12x85 | unidad:pieza
- PRODUCTO: Lentes de Seguridad, Transparentes | Anti-empañante, certificados. | precio:38 | mayoreo:24x32 | unidad:pieza
- PRODUCTO: Casco de Protección Industrial | Ajustable, certificado para obra. | precio:120 | unidad:pieza


## CATEGORIA: Lámina y Perfil
icono: 📐
descripcion: Lámina, perfil estructural y tubería de acero.

### SUB: Lámina
descripcion: Lámina de acero en distintos calibres y medidas.
dialogo: ¿Qué calibre y medida de lámina necesitas? Si manejas placa o lámina especial, indícalo abajo.

- PRODUCTO: Lámina Negra Calibre 18, 1.22 x 2.44 m | Acero al carbón, uso estructural. | unidad:pieza
- PRODUCTO: Lámina Galvanizada Calibre 20, 1.22 x 2.44 m | Para uso exterior, resistente a corrosión. | unidad:pieza

### SUB: Perfil y Tubería Estructural
descripcion: Perfil PTR, ángulo y tubería de acero estructural.
dialogo: ¿Qué tipo y medida de perfil o tubería necesitas?

- PRODUCTO: PTR (Tubular) 2 x 2 pulg, Cal. 14, 6m | Perfil tubular cuadrado, acero estructural. | unidad:pieza
- PRODUCTO: Ángulo Estructural 2 x 2 x 1/4 pulg, 6m | Ángulo de acero al carbón. | unidad:pieza
- PRODUCTO: Medidas y Calibres Especiales | Consultar disponibilidad y precio con ejecutivo PROTTSA según proyecto.
