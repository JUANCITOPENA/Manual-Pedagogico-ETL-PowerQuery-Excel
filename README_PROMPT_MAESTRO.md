# 📜 PROMPT MAESTRO CONSOLIDADO: PLATAFORMA PEDAGÓGICA ETL, POWER QUERY, EXCEL & GOBERNANZA DE DATOS

> **Documento:** Registro Integral de Requerimientos y Especificaciones Funcionales  
> **Ubicación:** `C:\Users\User\Desktop\Manual Pedagógico ETL para Power Query & Excel\README_PROMPT_MAESTRO.md`  
> **Fecha:** 2026-10-20  
> **Autor/Arquitecto:** Ing. Juancito Peña  
> **Objetivo:** Recopilar y formalizar en un único prompt maestro de ingeniería todos los requerimientos pedagógicos, técnicos, analíticos y de diseño solicitados para la plataforma web interactiva.

---

## 🏛️ 1. VISIÓN Y NARRATIVA ESTRATÉGICA

Construir una plataforma educativa y analítica empresarial de nivel directivo (Light Mode puro, ancho maestro del 85%, responsive, sin modo oscuro) orientada a la capacitación ejecutiva y universitaria en **Ingeniería ETL, Power Query, Microsoft Excel 365, Power BI y Gobernanza de Datos**.

### 1.1. Fundamentos y Roles del Dato
La plataforma debe explicar con máxima claridad pedagógica los 5 roles clave del ciclo de vida del dato moderno:
1. **Procesamiento de Datos:** Ingestión transaccional, captura masiva y almacenamiento crudo (OLTP).
2. **Curador de Datos:** Custodio de la calidad del dato, desinfección de texto, deduplicación y metadatos.
3. **Análisis de Datos (BI):** Creación de KPIs, modelos dimensionales en estrella, Tablas Dinámicas y Dashboards directivos.
4. **Ingeniería de Datos:** Pipelines masivos, Data Warehousing, orquestación y gobernanza a escala.
5. **Ciencia de Datos:** Modelos predictivos, Machine Learning, clustering y pronósticos estadísticos.

### 1.2. La Paradoja de los Sistemas de Información (ERPs y CRMs vs Excel/BI)
- Exponer el choque entre la teoría y la realidad corporativa: Las empresas gastan millones de dólares en **SAP, Microsoft Dynamics 365, Salesforce, Odoo o Macola** para gestionar finanzas, contabilidad, RRHH, compras, ventas y producción.
- **La cruda realidad:** Los ERPs gestionan la transacción pero son rígidos e inflexibles para el análisis ágil directivo. El botón más cliqueado en cualquier sistema del mundo es **"Exportar a Excel"**.
- El infierno de la calidad de datos en los formularios CRUD: usuarios que introducen tabuladores invisibles, saltos de línea, dobles espacios, errores tipográficos/leetspeak, fechas fusionadas con texto de horarios y valores nulos (`null`).
- **El Conector de Carpeta (Folder Connector) & el Botón Mágico:** Demostrar cómo con Power Query se conectan carpetas locales de red para procesar automáticamente 12 archivos mensuales con el atajo **`Ctrl + Alt + F5` (Actualizar Todo / Refresh All)** sin repetir tareas manuales.
- **Tabla Comparativa de Tiempos:** Demostrar un ahorro de tiempo superior al 99% (de 6-8 horas manuales mensuales a menos de 3 segundos con Power Query).

---

## 🎨 2. ESTÁNDARES DE DISEÑO UI/UX & MULTIMEDIA

1. **100% Light Mode Ejecutivo:** Prohibido el uso de modo oscuro. Fondos en blanco y slate ultra claro (`#f8fafc`), textos en alto contraste (`#0f172a`), bordes sutiles y sombras de elevación suaves.
2. **Ancho Maestro del 85%:** Toda la aplicación (barra superior, navbar, contenido y footer) debe estar contenida en `width: 85% !important; margin: 0 auto;`.
3. **Tipografía Aumentada para Videos y Clases:** Textos en 16px base, interlineado cómodo (1.7), títulos jerárquicos grandes (H1 hasta 36px) para grabaciones de pantalla y proyecciones docentes.
4. **Menú de Navegación Fijo en Una Sola Fila (Sticky Top):**
   - Logotipo y nombre del sistema a la izquierda.
   - Selector global de caso de empresa en el centro.
   - 5 botones de navegación con iconos FontAwesome en fila horizontal compacta.
   - Botón de descarga directa a Excel a la derecha.
5. **Carrusel de Sistemas Transaccionales (Auto-Play + Manual):**
   - Presentación de los 4 grandes sistemas: SAP S/4HANA, Dynamics 365, Salesforce CRM y Odoo/Macola.
   - Imágenes de interfaz, tarjetas descriptivas de módulos y la justificación de por qué requieren extracción a Excel.
6. **Footer Corporativo de 4 Columnas:**
   - Columna 1: Identidad y Gobernanza.
   - Columna 2: Ecosistema Tecnológico (Excel, Power Query, Power BI, Python).
   - Columna 3: Atajos de Oro de Teclado (`Ctrl + Alt + F5`, `Alt + F12`, etc.).
   - Columna 4: Garantías de Privacidad y Ejecución 100% Client-Side.

---

## 📊 3. RIGOR ANALÍTICO: 5 ESQUEMAS DE DATOS INDEPENDIENTES Y EXCLUSIVOS

**REGLA CRÍTICA:** Queda estrictamente prohibido compartir una estructura de datos genérica entre las industrias. Cada sector debe poseer sus propios campos, columnas, métricas, tasas impositivas y lógica operativa:

### Caso 1: Supermercado & Retail Masivo (Comercio Minorista)
- **Campos Específicos:** `NUM_FACTURA`, `FECHA_DOCUMENTO`, `REGION`, `CLIENTE_ID`, `CLIENTE_NOMBRE`, `VENDEDOR`, `CATEGORIA_PRODUCTO`, `PRODUCTO_SKU`, `CANAL_VENTA` (Sucursal, App Móvil, Preventa Ruta), `CONDICION_PAGO`, `CANTIDAD_UNIDADES`, `PRECIO_VENTA`, `SUBTOTAL`, `ITBIS_18`, `TOTAL_VENTA`, `COSTO_UNITARIO`, `COSTO_TOTAL`, `MARGEN_BRUTO`, `ESTATUS_FACTURA`.
- **KPIs del Dashboard:** Facturación Bruta, Ingreso Real Efectivo, Margen Bruto RD$, Rentabilidad Margen %, Cumplimiento de Meta Comercial, Tasa de Cancelación.
- **Gráficos:** Ventas vs Costos por Territorio (Columnas 2D), Mix por Familia de Producto (Anillos), Tendencia Cronológica Bruta vs Neta (Líneas con Marcadores), Ranking Top 8 Vendedores (Barras 2D).

### Caso 2: Logística, Transporte & Fletes (Cadena de Suministro)
- **Campos Específicos:** `NUM_MANIFIESTO`, `FECHA_DESPACHO`, `RUTA_ORIGEN_DESTINO`, `EMPRESA_CLIENTE`, `CONDUCTOR_FLOTA`, `TIPO_VEHICULO_PLACA`, `TIPO_CARGA` (Seca, Refrigerada, Granel, Peligrosa), `MODALIDAD_FLETE` (Contenedor Completo, Consolidado LTL), `CONDICION_FLETE`, `TONELADAS_CARGA`, `TARIFA_POR_TONELADA`, `SUBTOTAL_FLETE`, `PEAJES_COMBUSTIBLE`, `TOTAL_FLETE_RD`, `COSTO_OPERATIVO`, `MARGEN_FLETE`, `ESTATUS_DESPACHO` (Completado, En Tránsito, Demorado, Cancelado).
- **KPIs del Dashboard:** Total Facturación Fletes, Flete Efectivo Cobrado, Costo Combustible/Peajes, Margen Operativo %, Cumplimiento de Entregas a Tiempo (OTIF), Tasa de Despachos Anulados.
- **Gráficos:** Fletes por Territorio (Columnas 2D), Mix de Carga Transportada (Anillos), Evolución Mensual de Toneladas (Líneas), Ranking Top Conductores de Flota (Barras 2D).

### Caso 3: Finanzas, Tesorería & Cuentas por Cobrar (CxC / Cartera de Crédito)
- **Campos Específicos:** `NUM_PAGARE_FACTURA`, `FECHA_EMISION`, `FECHA_VENCIMIENTO`, `DIAS_CREDITO_OTORGADO`, `RNC_DEUDOR`, `NOMBRE_DEUDOR`, `OFICIAL_CREDITO`, `LINEA_CREDITO_INSTRUMENTO`, `CANAL_PAGO`, `TRAMO_VENCIMIENTO` (0-30 días Corriente, 31-60 días Vencido, 61-90 días Mora Alta, +90 días Castigo), `MONTO_PRINCIPAL_RD`, `TASA_INTERES_ANUAL`, `INTERES_MORA_GENERADO`, `SALDO_TOTAL_EXIGIBLE`, `ABONO_RECUPERADO`, `SALDO_PENDIENTE`, `DIAS_MORA_REALES`, `ESTATUS_CARTERA` (Al Día, Parcialmente Pagado, En Cobranza Legal, Incobrable).
- **KPIs del Dashboard:** Cartera Total Otorgada, Recaudo Efectivo de Cartera, Intereses de Mora Generados, Tasa de Recuperación %, Índice de Morosidad %, Cartera Castigada.
- **Gráficos:** Cartera Vigente vs Vencida por Región (Columnas 2D), Distribución por Tramo de Mora (Anillos), Flujo Mensual de Cobranza (Líneas), Ranking de Oficiales por Recaudo (Barras 2D).

### Caso 4: Recursos Humanos & Nómina Corporativa (Planilla Multisucursal)
- **Campos Específicos:** `COD_EMPLEADO`, `FECHA_INGRESO`, `SEDE_PLANTA`, `NOMBRE_COLABORADOR`, `SUPERVISOR_TURNO`, `DEPARTAMENTO_AREA`, `CARGO_POSICION`, `TIPO_CONTRATO`, `MODALIDAD_PAGO` (ACH Nómina, Cheque), `SUELDO_BRUTO_BASE`, `HORAS_EXTRAS_VALOR`, `RETENCION_AFP_287`, `RETENCION_SFS_304`, `RETENCION_ISR`, `TOTAL_DESCUENTOS_LEY`, `SUELDO_NETO_PAGADO`, `APORTE_PATRONAL_TSS`, `ESTATUS_LABORAL` (Activo, Licencia Médica, Suspendido, Desvinculado).
- **KPIs del Dashboard:** Masa Salarial Bruta, Salarios Netos Transferidos, Total Retenciones de Ley (TSS/ISR), Carga Impositiva Laboral %, Promedio de Horas Extras por Turno, Tasa de Rotación / Bajas.
- **Gráficos:** Costo Laboral por Sede (Columnas 2D), Masa Salarial por Departamento (Anillos), Evolución Quincenal de Nómina (Líneas), Ranking de Productividad por Supervisor (Barras 2D).

### Caso 5: Salud, Clínicas & Coberturas ARS (Facturación Médica)
- **Campos Específicos:** `NUM_AUTORIZACION_MEDICA`, `FECHA_ATENCION`, `SEDE_HOSPITALARIA`, `EXPEDIENTE_PACIENTE`, `MEDICO_TRATANTE`, `ESPECIALIDAD_MEDICA`, `SERVICIO_PROCEDIMIENTO` (Cirugía, Hospitalización, Consulta, Imágenes, Laboratorio), `ASEGURADORA_ARS`, `PLAN_SEGURO`, `MONTO_FACTURADO_TOTAL`, `COBERTURA_ARS_MONTO`, `COPAGO_PACIENTE_MONTO`, `COSTO_INSUMOS_MEDICOS`, `MARGEN_PRESTACION_CLINICA`, `ESTATUS_RECLAMACION` (Liquidada, Glosada en Revisión, En Espera de Pago, Rechazada Definitiva).
- **KPIs del Dashboard:** Facturación Clínica Bruta, Cobro Efectivo ARS, Copago Cobrado en Caja, Margen Operativo Médico, % de Reclamaciones Glosadas, Tasa de Rechazo de Aseguradoras.
- **Gráficos:** Facturación vs Copagos por Región (Columnas 2D), Participación por Especialidad Médica (Anillos), Reclamaciones Mensuales Presentadas vs Aprobadas (Líneas), Ranking de Médicos por Rendimiento (Barras 2D).

---

## 🛠️ 4. MANUAL MAESTRO DE TRANSFORMACIÓN ETL (LENGUAJE M & DAX)

El manual debe redactarse sin pantallas divididas (100% de ancho en bloques verticales completos) cubriendo 10 pasos fundamentales:
- **Paso 1:** Depuración de espacios, caracteres no imprimibles y dobles espacios (`Text.Trim`, `Text.Clean`).
- **Paso 2:** Separación de llave primaria (ID) y corrección de tipografía leetspeak (`Table.SplitColumn`, `Table.ReplaceValue`).
- **Paso 3:** Desacoplamiento de fechas y horarios para Inteligencia de Tiempo (`Table.TransformColumnTypes` con `type date`).
- **Paso 4:** Erradicación estricta de nulos (`null`), celdas vacías y tipado decimal regional en inglés EE.UU. para evitar errores de coma/punto.
- **Paso 5:** Lógica condicional de negocio para aislar transacciones canceladas o rechazadas (`Table.AddColumn` condicional).
- **Paso 6:** Cierre y carga eficiente en el **Modelo de Datos de Power Pivot (xVelocity Engine)** mediante *Crear únicamente la conexión*.
- **Paso 7 (Simulación 3D):** Emulación visual del **Panel de Campos de Tabla Dinámica de Excel** con sus 4 cuadrantes (*Filtros, Columnas, Filas y Valores*).
- **Paso 8 (Medidas DAX):** Creación de medidas analíticas explícitas utilizando `DIVIDE`, `CALCULATE` y `SUM`.
- **Paso 9 (Segmentadores):** Inserción y configuración de Slicers multiobjeto con la opción *Conexiones de Informes*.
- **Paso 10 (Storytelling):** Pautas para comunicar hallazgos, márgenes territoriales y quiebres operativos a la Junta Directiva.

---

## ⚡ 5. EXPERIENCIA REACTIVA BIDIRECCIONAL EN VIVO

1. **Sincronización Total de Selectores:** Cualquier cambio de empresa desde el Header Navbar, el Generador o el Sidebar del Dashboard debe:
   - Sincronizar el valor de todos los selectores.
   - Regenerar el dataset propio de esa industria.
   - Refrescar la tabla de muestra del generador con las columnas y datos de esa industria.
   - Refrescar la tabla de muestra en vivo del dashboard con las columnas y datos de esa industria.
   - Actualizar los 6 KPIs con sus nombres y valores reales.
   - Redibujar los 4 gráficos Chart.js con los títulos, categorías y métricas de esa industria.
   - Recrear los botones de los segmentadores (Slicers) adaptados a esa industria.
   - Actualizar la Tabla Dinámica (Pivot Table).
2. **Descargas Multi-Hoja:**
   - Libro Excel (`.xlsx`): Hoja 1 con datos crudos completos del sector activo y Hoja 2 con la receta ETL paso a paso.
   - Archivo CSV: Formateado en UTF-8 con BOM (`\uFEFF`) para compatibilidad nativa con Excel en Windows y Mac.
   - Archivo JSON estructurado.
