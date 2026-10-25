# 📋 REPORTE DE ESTATUS ACTUALIZADO & BITÁCORA TÉCNICA DE INGENIERÍA
## Proyecto: Manual Pedagógico ETL para Power Query & Microsoft Excel 365
**Fecha de Actualización:** 25 de Octubre de 2026  
**Versión Consolidada:** `v7.5-PRO (Universal Multi-PC Folder ETL, 125 Analytical Questions, 3D Excel Simulator & Interactive Video Release)`  
**Autor & Arquitecto:** Ing. Juancito Peña Vizcaíno  
**Ubicación Local:** `C:\Users\User\Desktop\Manual Pedagógico ETL para Power Query & Excel\`  
**Repositorio Oficial:** [https://github.com/JUANCITOPENA/Manual-Pedagogico-ETL-PowerQuery-Excel](https://github.com/JUANCITOPENA/Manual-Pedagogico-ETL-PowerQuery-Excel)  
**URL en Producción (GitHub Pages):** [https://juancitopena.github.io/Manual-Pedagogico-ETL-PowerQuery-Excel/](https://juancitopena.github.io/Manual-Pedagogico-ETL-PowerQuery-Excel/)

---

## 🟢 1. ESTADO GENERAL DEL PROYECTO: 100% ESTABLE, SINCRONIZADO Y DESPLEGADO

El sistema cuenta con **6 módulos pedagógicos e interactivos completos**, sincronizados dinámicamente para **5 sectores industriales reales** (*1. Supermercado & Retail Masivo, 2. Logística & Fletes, 3. Finanzas & Cobranzas, 4. Recursos Humanos & TSS, 5. Salud, Clínicas & ARS*):

1. **`1. Fundamentos`**: Paradoja del ERP/CRM, Evolución histórica de Excel (1985-2026), Matriz de 6 Niveles de Seniority, Salarios Globales con Prima IA/MCP y Gráficos Chart.js.
2. **`2. Manual ETL (Power Query)`**: Guía paso a paso (Pasos 1 al 6) adaptada a cada uno de los 5 datasets, resaltador sintáctico Prism.js para Lenguaje M, botones `Copiar` en cada instrucción `= Table.*` y en el Script M Completo, y autodetección universal de la carpeta `ANALISIS ETL\BD` en cualquier PC Windows.
3. **`3. Generador + Datos`**: Generador sintético de 500 a 5,000 registros con inyección controlada de impurezas (`leetspeak`, espacios fantasmas, nulos, fechas con texto basura) y exportación a `.xlsx` (con Rango Con Nombre `Datos_Crudos_ETL` y hoja `Receta_Maestra_PowerQuery`), `.csv` (UTF-8 con BOM) y `.json`.
4. **`3.1 Hoja de Trabajo (125 Preguntas)`**: Mandato ejecutivo y banco interactivo de **125 preguntas de negocio (25 por cada uno de los 5 sectores)** con guía de resolución en Power Query / Tabla Dinámica, barra de progreso y exportación a PDF.
5. **`4. Dashboard`**:
   - **Reproductor de Video / Simulador Animado Interactivo de Excel 365**: 6 escenas animadas (`00:00` a `00:36`) con cursor flotante *Drag & Drop*, narración por voz en español (`SpeechSynthesis` ON/OFF) y subtítulos en vivo.
   - **Manual Paso a Paso 100% con Tablas Dinámicas (0 Fórmulas)**: Secciones independientes a ancho completo para **Fase 1** (Emulación 3D en celdas de Excel de las 6 Tablas Dinámicas `TD_KPIs` y `TD_1` a `TD_5`) y **Fase 2** (Emulación 3D en celdas `E3:P5` de las 6 Mini-Tablas Dinámicas KPI `[K1]` a `[K6]`), más **Fases 3, 4 y 5** (Segmentadores `[S1]-[S3]`, Gráficos `[G1]-[G4]`, colores, etiquetas `[+]` y sección desplegable opcional de fórmulas).
   - **Simulador Visual 100% Fiel a Microsoft Excel 365**: Cinta verde `#107c41`, barra de fórmulas `fx`, encabezados de columnas `A:P` y filas `1:48`, Slicers nativos, Mini-TDs KPI, 4 Gráficos Dinámicos y Tabla Tabular `[T5]`.
6. **`5. Tabla Dinámica`**: Anatomía tridimensional (`pivot-3d-scene`) de 3 capas y las 6 Tablas Dinámicas Maestras adaptadas dinámicamente al sector seleccionado.

---

## 🧠 2. LOGROS TÉCNICOS RECIENTES (HISTORIAL DE SOLUCIONES CLAVE)

### 2.1. Consolidación Automática Multi-PC desde Carpeta (`ANALISIS ETL\BD`)
- **Problema Resuelto:** Al conectar un libro maestro (`DB_CONSOLIDADA.xlsx`) o compartir el Script M con otro estudiante/PC donde el usuario de Windows no se llama `"User"`, una ruta estática fallaba o requería editar código manualmente. Además, en Power Query M, `Folder.Files(ruta)` tiene evaluación perezosa (*lazy evaluation*), por lo que un simple `try Folder.Files(ruta)` no capturaba el error `DataSource.NotFound` cuando una ruta candidata (como `C:\ANALISIS ETL\BD`) no existía.
- **Solución Implementada en los 5 Scripts M (`MANUAL_ETL_DATA`):**
  1. Escaneo automático de perfiles de Windows mediante `Folder.Contents("C:\Users")` (forzando evaluación con `if List.Count(nombres) >= 0`).
  2. Construcción de `RutasCandidatas` cubriendo `Desktop\ANALISIS ETL\BD`, `Escritorio\ANALISIS ETL\BD`, `OneDrive\Desktop\ANALISIS ETL\BD`, `OneDrive\Escritorio\ANALISIS ETL\BD`, `C:\ANALISIS ETL\BD` y `D:\ANALISIS ETL\BD`.
  3. **Evaluación Booleana Estricta dentro de `try`**:
     ```powerquery
     TieneDatos = (try Table.RowCount(archivos) > 0 otherwise false)
     ```
     Al evaluar un booleano (`> 0`) **dentro del bloque `try`**, Power Query está obligado a abrir la carpeta dentro del `try`; si la carpeta no existe en esa ruta candidata, captura `DataSource.NotFound` silenciosamente, devuelve `false` y pasa a la siguiente ubicación.
  4. **Prevención de Referencia Circular al "Cerrar y cargar"**: Tanto en la consolidación de carpeta (`TablasDelSector`) como en el respaldo del libro actual (`TablasOrigenValidas`), el script exige que la tabla contenga la columna cruda del sector (ej. `"CLIENTE"`) y **NO contenga** la primera columna calculada (ej. `not List.Contains(..., "SUBTOTAL_VALIDADO")`), ignorando además archivos bloqueados (`~$`) o con `"CONSOLIDADA"` en el nombre.
  5. **Input Opcional en Vivo en Paso 6 (`#customEtlFolderPathInput`)**: Permite que cualquier usuario pegue una ruta personalizada y actualice `RutaDirecta` en los 5 scripts en tiempo real antes de copiar.

### 2.2. Botones de Copiado Rápido y Resaltado Sintáctico M (Prism.js)
- Tokenizador dedicado `highlightPowerQueryM(rawCode, withLineNumbers)` para colorear palabras clave (`let`, `in`, `each`, `try`, `otherwise`), funciones (`Table.AddColumn`, `Folder.Files`, `Excel.Workbook`), tipos (`Currency.Type`, `Percentage.Type`), referencias de columnas (`[COLUMNA]`) y comentarios.
- Botones **`Copiar`** integrados directamente dentro de cada caja oscura `= Table.*` en **Paso 2** (`= Table.TransformColumns`), **Paso 3** (`= Table.ReplaceValue`), **Paso 5** (los 5 cálculos `= Table.AddColumn` más sus fórmulas individuales) y **Paso 6** (Script M Completo).

### 2.3. Fase 1 y Fase 2 Independientes con Modelado 3D + Video Simulador Interactivo
- **Secciones Independientes a Ancho Completo (`renderDashboardManual`)**: Fase 1 y Fase 2 ya no comparten una cuadrícula de 2 columnas; cada una ocupa el 100% del ancho con tarjetas de modelado 3D que simulan los 4 cuadrantes de Excel y las celdas reales (`A10:C16`, `E3:F5`, etc.) con datos en vivo del dataset activo.
- **Reproductor de Video Interactivo (`#excelVideoPlayerRoot` + `setExcelVideoScene`)**: Simula en 6 escenas animadas (`00:00` a `00:36`) la creación de las Tablas Dinámicas y KPIs con cursor animado *Drag & Drop*, subtítulos y narración por voz en español (`window.speechSynthesis`).

---

## ⚠️ 3. NOTAS CRÍTICAS PARA FUTURAS SESIONES (CUANDO RETOMES EL PROYECTO)

> [!IMPORTANT]
> **Lee estas 6 reglas técnicas antes de realizar cualquier modificación futura en `index.html`:**

1. **Cuidado con las Barras Invertidas (`\`) dentro de Template Literals (`` `...` ``) en JavaScript:**
   - Los 5 bloques `fullMCode` dentro de `MANUAL_ETL_DATA` están definidos con *backticks* (`` fullMCode: `...` ``).
   - **NUNCA termines una línea de comentario `// ...` con una barra invertida `\`** (por ejemplo `// ... Disco C:\`), porque JavaScript interpreta `\` al final de línea como continuación de línea, eliminando el salto de línea y comentando la primera línea de código M (`RutaDirecta = ...`).
   - Dentro de `` fullMCode: `...` ``, toda ruta de Windows debe tener barras dobles (`C:\\Users\\...`), y si la generas desde un script de Node.js, debes escaparlas doblemente (`\\\\`).

2. **Regla de Oro de Evaluación Perezosa (*Lazy Evaluation*) en Power Query M:**
   - En Power Query M, `Folder.Files(...)`, `Folder.Contents(...)`, las listas `{...}` y los registros `[...]` se evalúan de manera perezosa.
   - Si agregas nuevas rutas o validaciones de archivos en M, el bloque `try ... otherwise false` **siempre debe envolver una expresión escalar booleana o numérica** (como `try Table.RowCount(archivos) > 0 otherwise false` o `try List.Count(lista) >= 0 otherwise {}`), **nunca** solo `try Folder.Files(ruta)`.

3. **Evitar Referencias Circulares en `Excel.CurrentWorkbook()` y `Folder.Files()`:**
   - Cuando el usuario pulsa **Inicio $\rightarrow$ Cerrar y cargar**, Excel crea una tabla de salida en el libro que incluye las 5 columnas calculadas.
   - Mantén siempre el filtro de exclusión de la primera columna calculada de cada sector:
     - `retail`: requiere `"CLIENTE"` y excluye `"SUBTOTAL_VALIDADO"`
     - `logistica`: requiere `"EMPRESA_CLIENTE"` y excluye `"SUBTOTAL_FLETE_CALC"`
     - `finanzas`: requiere `"NOMBRE_DEUDOR"` y excluye `"INTERES_MORA_CALC"`
     - `rrhh`: requiere `"NOMBRE_COLABORADOR"` y excluye `"PAGO_HORAS_EXTRAS_CALC"`
     - `salud`: requiere `"EXPEDIENTE_PACIENTE"` y excluye `"COPAGO_VALIDADO"`

4. **Sincronización de los 5 Sectores (`syncIndustryChange(industryKey)`):**
   - Al cambiar de sector en cualquiera de los selectores, `syncIndustryChange` actualiza simultáneamente:
     - `2. Manual ETL` (`renderManualEtl`)
     - `3. Generador + Datos` (`generateDataAndRefresh`)
     - `3.1 Hoja de Trabajo` (`selectHojaTrabajoCase`)
     - `4. Dashboard` (`updateDashboardMappedEnhancements` + `renderDashboardManual` + `setExcelVideoScene`)
     - `5. Tabla Dinámica` (`renderPivotManualByIndustry`)
   - Cualquier nuevo componente debe leer de `ACTIVE_INDUSTRY` y actualizarse dentro de este ciclo.

5. **Validación Sintáctica Obligatoria antes de Hacer Commit:**
   - Ejecuta siempre este comando en PowerShell antes de confirmar cambios en `index.html`:
     ```powershell
     node -e 'const fs=require("fs"); const h=fs.readFileSync("index.html","utf8"); const s=[...h.matchAll(/<script\b[^>]*>([\s\S]*?)<\/script>/gi)].map(m=>m[1]); new Function(s[s.length-1]); console.log("JS OK!");'
     ```

6. **Estructura de Carpetas para Laboratorios en Vivo del Usuario:**
   - Carpeta raíz de pruebas del usuario en su Escritorio: `C:\Users\User\Desktop\ANALISIS ETL\`
   - Libro maestro consolidador: `C:\Users\User\Desktop\ANALISIS ETL\DB_CONSOLIDADA.xlsx`
   - Subcarpeta donde se depositan los archivos `.xlsx`, `.csv` y `.json` descargados: `C:\Users\User\Desktop\ANALISIS ETL\BD\`

---

## 🚀 4. PRÓXIMOS PASOS SUGERIDOS (ROADMAP FUTURO OPCIONAL)

1. **Exportación de Video Tutorial en Archivo `.mp4` Descargable (Opción #1):**
   - Si en el futuro deseas un archivo `.mp4` físico para subir a YouTube, WhatsApp o aulas virtuales, se puede generar automáticamente grabando las 6 escenas del simulador con `Playwright` + `FFmpeg` + voz TTS neuronal (`edge-tts`).
2. **Modo Examen / Autoevaluación Interactiva en la Pestaña `3.1 Hoja de Trabajo`:**
   - Permitir que el estudiante ingrese el resultado numérico que obtuvo en su Tabla Dinámica de Excel para cada una de las 25 preguntas y que la plataforma valide automáticamente con un check verde (`✅ Respuesta Exacta`) contra las cifras de control del dataset generado.
3. **Plantilla Descargable de `DB_CONSOLIDADA.xlsx` Pre-Conectada:**
   - Botón opcional para descargar un libro maestro `.xlsx` limpio listo para colocar en `ANALISIS ETL\`.

---
**Dictamen:** `🟢 CHECKPOINT v7.5-PRO GUARDADO, DOCUMENTADO Y DESPLEGADO EN GITHUB PAGES`
