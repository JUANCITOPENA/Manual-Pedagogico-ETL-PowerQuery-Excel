# 📊 Manual Pedagógico ETL para Power Query & Microsoft Excel 365
## 🏆 Plataforma Interactiva de Ingeniería de Datos, Limpieza ETL en Lenguaje M, Tablas Dinámicas 3D y Simulador de Excel en Vivo

**Versión Actual:** `v7.5-PRO (Universal Multi-PC Folder ETL, 125 Analytical Questions, 3D Excel Simulator & Interactive Video Release)`  
**Fecha de Actualización:** 25 de Octubre de 2026  
**Autor & Arquitecto:** Ing. Juancito Peña Vizcaíno  
**Repositorio GitHub:** [https://github.com/JUANCITOPENA/Manual-Pedagogico-ETL-PowerQuery-Excel](https://github.com/JUANCITOPENA/Manual-Pedagogico-ETL-PowerQuery-Excel)  
**Despliegue en Producción (GitHub Pages):** [https://juancitopena.github.io/Manual-Pedagogico-ETL-PowerQuery-Excel/](https://juancitopena.github.io/Manual-Pedagogico-ETL-PowerQuery-Excel/)  
**Estado General:** `🟢 100% FUNCIONAL | ESTABLE | SINCRONIZADO EN 5 INDUSTRIAS | EN PRODUCCIÓN`

---

## 📌 1. Propósito del Proyecto

Esta plataforma web interactiva fue diseñada para enseñar, practicar y dominar el ciclo completo de **Analítica de Datos Empresarial con Microsoft Excel 365 y Power Query** desde cero hasta nivel avanzado, sin depender de fórmulas engorrosas cuando el trabajo puede automatizarse con **Power Query (Lenguaje M)** y **Tablas Dinámicas (100% Arrastrar y Soltar)**.

El sistema adapta en tiempo real **todo su contenido, datos crudos, scripts M, preguntas de auditoría, tablas dinámicas y dashboards** a **5 sectores empresariales reales**:
1. 🛒 **1. Supermercado & Retail Masivo** *(POS, Facturación, ITBIS 18% y Margen Comercial)*
2. 🚛 **2. Logística, Transporte & Fletes** *(Manifiestos de Carga, Toneladas, Tarifas y Peajes)*
3. 🏦 **3. Finanzas, Cartera de Crédito & Cobranzas** *(Préstamos, Días de Mora, Intereses y Provisión)*
4. 👥 **4. Recursos Humanos, Nómina & TSS** *(Sueldos, Horas Extras, SFS/AFP/ISR y Rotación)*
5. 🏥 **5. Salud, Clínicas Privadas & Coberturas ARS** *(Autorizaciones, Glosas, Copagos y Margen Clínico)*

---

## 🧭 2. Mapa de los 6 Módulos de la Plataforma

| Pestaña / Módulo | Descripción y Funcionalidades Clave |
| :--- | :--- |
| **1. Fundamentos** | Explica la *Paradoja del ERP/CRM*, la evolución histórica de Excel (1985–2026), la Matriz de 6 Niveles de Seniority en Datos, comparativa salarial global con prima por IA/MCP y gráficos interactivos con Chart.js. |
| **2. Manual ETL** | Guía paso a paso (Pasos 1 al 6) de limpieza en Power Query personalizada para cada sector. Incluye resaltado sintáctico Prism.js para Lenguaje M, botones **`Copiar`** en cada instrucción `= Table.*` y en el **Script M Completo**, más autodetección universal de la carpeta `ANALISIS ETL\BD`. |
| **3. Generador + Datos** | Generador de datasets de **500 a 5,000 registros** con selector de rango de fechas e interruptor de impurezas reales (*espacios fantasmas, leetspeak `@/4/3/0/1/#`, valores `null` y fechas sucias*). Exporta a **Excel `.xlsx`** (con tabla nombrada `Datos_Crudos_ETL` y hoja `Receta_Maestra_PowerQuery`), **`.csv`** y **`.json`**. |
| **3.1 Hoja de Trabajo** | Mandato formal de auditoría con **125 preguntas analíticas (25 preguntas por cada uno de los 5 sectores)**, guía exacta de qué arrastrar a Filas/Valores en la Tabla Dinámica, checklist de avance persistente y exportación a PDF. |
| **4. Dashboard** | Incluye el **Reproductor de Video / Simulador Animado Interactivo de Excel 365** (con voz narrada en español y cursor *Drag & Drop*), el **Manual Paso a Paso con Secciones Independientes 3D (Fase 1 y Fase 2)** y el **Simulador 100% Excel 365** (`A1:P48`) con Slicers `[S1]-[S3]`, Mini-TDs KPI `[K1]-[K6]`, Gráficos `[G1]-[G4]` y Tabla `[T5]`. |
| **5. Tabla Dinámica** | Modelado tridimensional isométrico (`pivot-3d-scene`) de las 3 capas de una Tabla Dinámica (Origen Power Query $\rightarrow$ 4 Cuadrantes $\rightarrow$ Matriz Agregada) y configuración detallada de las 6 Tablas Dinámicas Maestras. |

---

## 📁 3. Flujo Universal de Consolidación Automática (`ANALISIS ETL\BD`)

Para lograr que el estudiante o analista descargue múltiples cortes de datos (`.xlsx`, `.csv` o `.json` de 1,000, 2,000 o 2,500 filas) y consolide todo con un solo clic en **Datos $\rightarrow$ Actualizar todo (`Ctrl + Alt + F5`)**, los 5 Scripts M implementan **Autodetección Universal Multi-PC**:

```text
📁 Escritorio (o Disco C:\ / D:\)
 └── 📁 ANALISIS ETL
      ├── 📄 DB_CONSOLIDADA.xlsx          <-- Libro Maestro donde pegas el Script M y armas tu Dashboard
      └── 📁 BD                           <-- Carpeta donde guardas TODOS los archivos descargados
           ├── 📊 Supermercado_1000_Filas.xlsx
           ├── 📊 Supermercado_2000_Filas.xlsx
           ├── 📄 Supermercado_Dataset.csv
           └── 🗂️ Supermercado_Dataset.json
```

### ¿Cómo funciona la Autodetección en cualquier computadora Windows?
1. El Script M consulta automáticamente `Folder.Contents("C:\Users")` para detectar todos los perfiles de usuario de la PC sin importar cómo se llame la cuenta de Windows.
2. Busca la carpeta `ANALISIS ETL\BD` en `Desktop`, `Escritorio`, `OneDrive\Desktop`, `OneDrive\Escritorio`, `C:\ANALISIS ETL\BD` y `D:\ANALISIS ETL\BD`.
3. Evalúa de forma segura dentro de un bloque `try` booleano (`try Table.RowCount(archivos) > 0 otherwise false`) qué carpeta existe y contiene archivos válidos (`.xlsx`, `.xls`, `.csv`, `.json`), ignorando archivos temporales (`~$`) y el propio libro consolidador.
4. Además, en el **Paso 6 del Manual ETL**, el usuario dispone de una **caja de texto opcional** donde puede pegar cualquier otra ruta personalizada de su PC y actualizar el código M en tiempo real antes de copiarlo.

---

## 🎬 4. Reproductor de Video Simulador Interactivo & Modelado 3D en Excel (`4. Dashboard`)

En la pestaña **4. Dashboard**, antes del tablero simulado, el usuario cuenta con:

1. **Reproductor de Video Tutorial Interactivo en Vivo (`00:00` a `00:36`):**
   - **6 escenas animadas paso a paso**:
     - *Escena 1 (`00:00`):* Insertar Tabla Dinámica (`Alt + N + V`) hacia `Aux_Tablas_Dinamicas`.
     - *Escena 2 (`00:06`):* Crear las 6 Tarjetas KPI `[K1]-[K6]` en `E3:P5` dejando `Filas` vacío y soltando en `∑ Valores`.
     - *Escena 3 (`00:12`):* Crear `TD_1` en `A10:C16` y el Gráfico de Columnas `[G1]`.
     - *Escena 4 (`00:18`):* Crear `TD_2` con *Mostrar valores como $\rightarrow$ % del total general* y el Anillo `[G2]`.
     - *Escena 5 (`00:24`):* Agrupar fechas por Meses en `TD_3` y filtrar el Top 8 en `TD_4`.
     - *Escena 6 (`00:30`):* Insertar Segmentadores `[S1]-[S3]` y vincular las 6 Tablas Dinámicas en *Conexiones de informes*.
   - Incluye **cursor animado *Drag & Drop***, **barra de progreso**, **botones Anterior / Reproducir / Pausar / Siguiente** y **Narración por Voz en Español (`ON / OFF`)**.

2. **Fase 1 y Fase 2 en Secciones Independientes con Emulación 3D de Celdas de Excel:**
   - **Fase 1 (Ancho Completo):** 6 tarjetas 3D (`TD_KPIs`, `TD_1` a `TD_5`) que muestran los 4 cuadrantes de Excel (`🔎 Filtros`, `🏛️ Columnas`, `☰ Filas`, `∑ Valores`) y la cuadrícula de celdas resultante con datos reales en vivo.
   - **Fase 2 (Ancho Completo debajo de Fase 1):** 6 tarjetas 3D (`[K1]` a `[K6]`) que emulan las celdas `E3:F5` a `O3:P5` (Fila 3: Encabezado `∑`, Fila 4: Valor formateado en `RD$` o `%`, Fila 5: Subtítulo y acción *Drag & Drop*).

---

## 📂 5. Archivos de Documentación y Control del Proyecto

- [`index.html`](./index.html): Aplicación web completa (Single-Page Application autocontenida en HTML5, Tailwind CSS, Chart.js, SheetJS y motor M/3D).
- [`README_ESTATUS_PROYECTO.md`](./README_ESTATUS_PROYECTO.md): **Archivo de estatus actualizado, bitácora de ingeniería y notas críticas para retomar el proyecto en futuras sesiones.**
- [`PLAN_DE_TRABAJO_MAESTRO.md`](./PLAN_DE_TRABAJO_MAESTRO.md): Plan arquitectónico y pedagógico original.
- [`README_PROMPT_MAESTRO.md`](./README_PROMPT_MAESTRO.md): Especificación de contexto y prompts del sistema.

---

## 🚀 6. Ejecución Local y Despliegue

### 🌐 Producción en Vivo (GitHub Pages)
👉 **[https://juancitopena.github.io/Manual-Pedagogico-ETL-PowerQuery-Excel/](https://juancitopena.github.io/Manual-Pedagogico-ETL-PowerQuery-Excel/)**

### 💻 Ejecución Local
Abre directamente el archivo [`index.html`](./index.html) en cualquier navegador moderno (Chrome, Edge, Firefox, Safari).

---
*Desarrollado y documentado por el **Ing. Juancito Peña Vizcaíno** — Arquitecto de Datos, BI & Desarrollo de Software.*
