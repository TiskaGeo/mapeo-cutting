# Maptik

**Herramientas offline para el mapeo geológico de cutting y sondajes en minería.**

Maptik es una aplicación web instalable (PWA) pensada para el geólogo de terreno. Junta en un solo lugar las tablas de clasificación, una referencia visual para estimar porcentajes en bandejas de cutting, una guía de minerales de cobre y un registro diario de cutting y sondajes, con reporte listo para copiar y pegar.

Funciona **100 % sin internet** una vez instalada. Está optimizada para tablet (Samsung Galaxy Tab S6) y se puede usar en horizontal o en vertical.

---

## Funciones

### 📋 Tablas de clasificación
- **Zonas minerales (óxidos):** zona lixiviada, limonitas, óxidos de Cu, parcial lixiviada, enriquecimiento débil y fuerte, y primario, con sus códigos, rangos de ley de Cu y criterios.
- **Unidades de alteración y asociaciones de mena (sulfuros):** CMH, PF, PI, ZT, QSP y PIR, con su mineralogía, sulfuros totales, estilo y ley.
- **Asociaciones primarias (Chuquicamata):** agrupadas por etapa (temprana, intermedia y tardía), con los rasgos de cada alteración.
- **Buscador:** busca por código, mineral o alteración en todas las tablas. Por ejemplo, "209" o "Py-Cc".

### 🎯 % Visual
- **Bandeja de referencia** con la forma de una bandeja real. Muestra partículas negras angulosas sobre fondo blanco o gris claro.
- **Porcentajes rápidos** (2, 5, 10, 15, 20, 25, 30 y 40 %), un control deslizante y un campo para ingresar el valor a mano.
- **Distribución** dispersa o agrupada, y **tamaño de grano** fino, medio o grueso.
- **Cobertura medida en tiempo real:** la app mide cuánto cubren realmente las partículas dibujadas.
- **Ayudas opcionales:** cuadrícula de 10 × 10 (cada celda es el 1 %) y clastos de fondo tenues como referencia.
- **Calculadora de % relativo:** reparte varios componentes dentro del 100 % y calcula la razón entre ellos.
- **Calculadora de relativo a absoluto:** por ejemplo, si el 70 % del 10 % es malaquita, entrega 7 %.
- **Práctica de estimación:** la app muestra bandejas con un % oculto y tú escribes tu estimación. Lleva tus estadísticas de calibración: error medio, % de aciertos y si tiendes a sobreestimar o subestimar. Las separa por tamaño de grano y por rango de %.

### 💎 Minerales de cobre
- **Sulfuros:** calcopirita, pirita, bornita, calcosina, digenita, covelina y enargita.
- **Óxidos:** malaquita, atacamita, brocantita y crisocola.
- **Ficha de cada mineral:** fórmula, color, raya, brillo, dureza, densidad, sistema cristalino y % de Cu, con un tip de reconocimiento en cutting.
- **Color principal y colores posibles de observar,** basados en las descripciones de mindat.org. Puedes elegir tú qué color se muestra como principal.
- **Fotos:** enlace a la galería de mindat (requiere internet) y fotos propias tomadas con la cámara de la tablet, que quedan guardadas offline.

### 🗂️ Registro de mapeo
- **Cutting:** rangos correlativos PEX (subterránea) y HT (rajo abierto), con la cantidad de muestras calculada sola. En "Hasta" basta escribir los últimos dígitos.
- **Sondajes:** tramos en metros por sondaje, con tres tipos de mapeo:
  - Estructural
  - Detalle (con leyes o sin leyes)
  - Orientado (con rayo o sin rayo)
- **Validaciones:** avisa si un rango o tramo se solapa con otro, o si "Hasta" es menor que "Desde".
- **Reporte del día** en tres formatos: **Simple**, **Detallado** y **Excel** (se separa en columnas al pegarlo). Puedes incluir o excluir el cutting o los sondajes, agregar observaciones y copiar todo con un toque.
- **Historial** por día y mes, con un buscador que te dice en qué día mapeaste una muestra (PEX/HT) o un sondaje.
- **Productividad:** muestras de cutting y metros de sondaje por día, semana o mes, con gráficos y promedios.
- **Respaldo:** exporta a CSV y guarda o restaura un respaldo completo en .json.

### ✅ Validar planilla
- Carga el Excel o CSV exportado del sistema de mapeo de cutting. Funciona offline, en tablet y en PC.
- **Revisa la alteración** con los porcentajes recalculados sin dilución (QS + QSCP):
  - **303:** QS entre 20 y 80 %.
  - **301 y 309:** QS ≥ 80 %. Se distinguen por la ley: 301 tiene CuT < 0,8 y 309 tiene CuT ≥ 0,8.
  - **307:** QS < 20 % y además KSIL ≥ 30 % o SV ≥ 10 %.
  - **318:** QS < 20 %, con KSIL < 30 % y SV < 10 %.
  - **312:** vetas de cuarzo ≥ 40 %.
- **Revisa la mineralización:** el código debe coincidir con los dos sulfuros de mayor porcentaje y con el límite de Ts de 1 %. Los empates se marcan como advertencia.
- **Casillas obligatorias:** Alteración, Mineralización, Molibdenita y Blenda no pueden estar vacías.
- **Sumas:** la alteración y los sulfuros deben sumar 100. También revisa la composición de la dilución.
- **Leyes:** compara la ley empírica con la de laboratorio y marca las diferencias mayores a 0,2 % en Cu o en As. También comprueba que la ley empírica coincida con la fórmula.
- **Filtros** por geólogo, fechas y muestra. Cada muestra tiene una ficha de detalle con el valor sugerido.
- **Excel de salida** con tres hojas: Resumen, Hallazgos y Datos marcados (celdas en rojo o amarillo).
- **Umbrales editables** desde "Reglas y umbrales".

### 🎨 Interfaz
- **Tema claro y oscuro,** con acento color cobre.
- **Diseño táctil para tablet,** con botones grandes y textos legibles en terreno.

---

## Instalación en la tablet

1. Abre en **Chrome** la dirección de la app: `https://TU-USUARIO.github.io/mapeo-cutting/`
2. Toca el menú **⋮** → **Instalar app** (o **Agregar a pantalla de inicio**).
3. Abre Maptik desde su ícono. Desde ese momento funciona sin internet.

## Actualizar a una versión nueva

1. En este repositorio toca **Add file → Upload files**.
2. Sube los archivos nuevos (normalmente `index.html` y `sw.js`) y toca **Commit changes**.
3. Espera 1–2 minutos y abre la app en la tablet con internet. Se actualiza sola. La versión instalada aparece abajo a la izquierda, bajo el botón del tema.

## Tus datos

- **Todo se guarda solo en el dispositivo:** registros, fotos, colores elegidos y estadísticas de práctica. No se envía nada a ningún servidor.
- **Haz respaldos de vez en cuando:** usa **Registro → Respaldo (.json)** y guarda el archivo fuera de la tablet (Drive, correo o PC).
- **Repositorio público:** cualquiera con el enlace puede ver la app y sus tablas de clasificación. Las tablas pueden ser información interna de tu faena, así que revísalo antes de compartir el enlace.

## Archivos

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La aplicación completa (interfaz, datos y lógica en un solo archivo) |
| `sw.js` | *Service worker*: guarda la app en la tablet para que funcione offline |
| `manifest.webmanifest` | Nombre, ícono y colores de la app instalada |
| `icon-*.png` | Íconos de la app |

## Créditos

- **Propiedades de los minerales y descripciones de color:** [mindat.org](https://www.mindat.org).
- **Tablas de clasificación:** criterios de mapeo usados en faena.
- **Tipografía:** IBM Plex Sans y IBM Plex Mono.
