<p align="center">
  <img src="logo.png" width="96" alt="Brikka">
</p>

<h1 align="center">Brikka</h1>

<p align="center">
  <b>Presupuestos, precios unitarios y estimaciones de obra para arquitectos y constructores.</b><br>
  Funciona sin internet, sin suscripción y todo se guarda en tu computadora.
</p>

<p align="center">
  <a href="https://brikkaapp.github.io/brikka"><b>⬇️ Descargar en brikkaapp.github.io/brikka</b></a>
</p>

---

## ¿Qué es Brikka?

Brikka es una aplicación de escritorio (Windows, Linux y pronto Mac) para armar el **presupuesto de una obra** de principio a fin:

- 🧱 **Catálogo de conceptos** — organiza la obra por partidas (Cimentación, Muros, Losas…). Cada concepto tiene su **cantidad × precio unitario = importe**, y cada partida suma sola.
- 🧮 **Análisis de precios unitarios (APU)** — desglosa de qué se compone el precio de un m², m³ o pieza: **materiales + mano de obra + herramienta + equipo**.
- 📦 **Biblioteca de insumos regionales** — trae ~50 insumos típicos de México (incluido **BTC**, bloque de tierra comprimida). Los precios empiezan en $0 para que captures los de **tu** región — Brikka nunca inventa precios.
- 💰 **Cierre del presupuesto** — aplica tus **indirectos, financiamiento, imprevistos, utilidad e IVA** configurables, y te da el **Subtotal → Total** con importe en letra.
- 📈 **Estimaciones por corte** — cobra al cliente **solo lo avanzado en cada periodo** (ver abajo).
- 🧾 **Gastos contra presupuesto** — registra lo que realmente gastas (facturas, raya, destajo) y compáralo con lo presupuestado por partida y concepto.
- 📓 **Bitácora de obra** — notas diarias con clima, personal, fotos, incidencias y avance fechado; modo interno u obra pública con firmas.
- 🛒 **Compras** — órdenes de compra, recepciones en obra y facturas que pasan solas a Gastos, con alertas de sobreprecio.
- ✅ **Checklists por etapa** — trámites, preliminares, obra negra, acabados y entrega, con avance por concepto.
- 📐 **Planos y gráficos** — guarda imágenes, PDF, DWG y SketchUp dentro del mismo archivo del proyecto.
- 📄 **Exporta a PDF y Excel** — catálogos "para cotizar", presupuestos completos y estimaciones listas para firmar, en Carta, Oficio o A4. El Excel lleva fórmulas que dan lo mismo que Brikka.

Cada proyecto es **un solo archivo `.brikka`** que puedes copiar a una USB o enviar por correo.

## Lo nuevo en Brikka 3.0

- **Una sola app.** Brikka y Brikka IA ahora son lo mismo: Brikka, con el asistente de IA **opcional** ya incluido. Si tenías cualquiera de las dos, instala encima y tus proyectos, precios y ajustes se conservan.
- El asistente te guía paso a paso para activarlo (instalar Ollama y bajar el modelo), **sin usar la terminal**.
- **Cálculos verificados** con más de 130 pruebas automáticas: estimaciones por cantidad ejecutada, anticipo y 5 al millar, P.U. directo o integrado.
- **Excel de la estimación** y Excel del catálogo con fórmulas.
- PDF en **Carta, Oficio o A4**, con encabezado en cada hoja y **firmas** a tu gusto (Elaboró, Revisó, Autorizó).
- Búsqueda (Ctrl+K) que encuentra aunque escribas con faltas.
- Proyectos grandes abren sin congelarse; aviso si el mismo proyecto está abierto en otra ventana.

---

## Estimaciones por corte

Una **estimación** es el documento con el que cobras **solo lo que se avanzó en un periodo** (una semana, una quincena…). Así funciona en Brikka:

1. Durante el periodo capturas la **cantidad ejecutada** de cada concepto (por ejemplo 100 m² de 1,234 m²) en el Catálogo o en la Bitácora, o su % de avance.
2. Al cierre creas un **corte**: Brikka toma una "foto" del avance de ese momento, con sus precios.
3. Brikka calcula lo de **este periodo = lo ejecutado hasta hoy − lo ya cobrado en el corte anterior** (en pesos, así cuadra aunque cambies cantidades o precios entre cortes), y le aplica tus indirectos, utilidad, anticipo, IVA y 5 al millar si aplica.
4. Exportas la estimación en **PDF o Excel**, lista para firmar y cobrar.

El avance se pondera por dinero (no por número de partidas), así que la estimación refleja el valor real ejecutado.

---

## Asistente de IA (opcional)

Brikka trae un asistente que corre **en tu propia computadora** con [Ollama](https://ollama.com) (gratis). No manda tus datos a ningún servidor y no cuesta suscripción. **Brikka funciona completo sin él**: si quieres usarlo, abre el *Asistente IA* y Brikka te guía para instalar Ollama y descargar el modelo con un clic.

> El asistente no es fuente de precios: los precios solo vienen de tus **Precios de insumos**. La IA no puede cambiar nada de tu proyecto, y si en una respuesta menciona precios que no salen de tus insumos, Brikka te lo advierte.

---

## Descarga e instalación

Ve a **[brikkaapp.github.io/brikka](https://brikkaapp.github.io/brikka)** y elige tu sistema.

### Windows
Descarga el `.exe`, ábrelo y sigue el instalador. Si Windows muestra un aviso de "editor desconocido", haz clic en **Más información → Ejecutar de todas formas** (es normal en apps gratuitas sin firma de pago).

### Linux
Descarga el **AppImage**, dale permiso de ejecución y ábrelo (no necesita instalación):
```bash
chmod +x Brikka-Linux.AppImage
./Brikka-Linux.AppImage
```
En **Ubuntu 22.04 o más nuevo**, si no abre, instala primero el componente que usan los AppImage:
```bash
sudo apt install libfuse2      # en Ubuntu 24.04: sudo apt install libfuse2t64
```

### Comprobar la descarga (opcional)
Cada versión trae un archivo `SHA256SUMS.txt` en [Releases](https://github.com/brikkaapp/brikka/releases). En Windows puedes comparar con `certutil -hashfile Brikka-Setup.exe SHA256`; en Linux con `sha256sum Brikka-Linux.AppImage`.

### Si compartes proyectos con otras personas
Pídeles que usen la versión más reciente. Brikka 1.5 y Brikka IA 2.1 (o anteriores) abren los proyectos nuevos, pero **al guardar borran** Gastos, Bitácora y Compras.

### Mac
Próximamente. 🍎

---

## Requisitos

- **Windows** 10 u 11 (64 bits) · **Linux** 64 bits · Mac (próximamente)
- No necesita internet ni cuenta.
- Para el asistente (opcional): [Ollama](https://ollama.com) y 8 GB de RAM o más. Brikka te guía para instalarlo.

---

## Privacidad

Brikka es **local**: tus proyectos, precios y datos del despacho viven **solo en tu computadora**. No hay nube, no hay cuentas, no hay rastreo. Tú decides cuándo compartir un archivo `.brikka` o un PDF.

---

<p align="center">
  <img src="pato-pixel.png" width="340" alt="PATO PIXEL — Estudio de Software · Hecho en México">
</p>

<p align="center">
  Hecho con 🧱 por <b>PATO PIXEL</b> · <a href="https://brikkaapp.github.io/brikka">brikkaapp.github.io/brikka</a>
</p>
