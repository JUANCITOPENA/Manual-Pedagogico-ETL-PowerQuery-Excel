# 📊 Manual Pedagógico ETL para Power Query & Microsoft Excel 365
## 🏆 Sistema Empresarial de Curaduría de Datos, Arquitectura Analítica & Gobernanza Corporativa
**Versión Actual:** `v5.0-PRO (Master Enterprise Release)`  
**Autor & Arquitecto:** Ing. Juancito Peña Vizcaíno  
**Ubicación del Proyecto:** `C:\Users\User\Desktop\Manual Pedagógico ETL para Power Query & Excel\`  
**Estado General:** `🟢 100% FUNCIONAL | ESTABLE | BLINDADO | PRODUCCIÓN LISTA`

---

## 📌 1. Resumen Ejecutivo y Estatus del Sistema

Este proyecto es una plataforma interactiva de alto impacto pedagógico y profesional, diseñada para la enseñanza, consultoría y capacitación gerencial en **Ingeniería de Datos, Curaduría, Limpieza ETL con Power Query y Visualización Analítica en Microsoft Excel 365**.

Resuelve de raíz la **"Paradoja del ERP/CRM"**: cómo las corporaciones invierten millones en sistemas transaccionales (SAP S/4HANA, Microsoft Dynamics 365, Salesforce, Odoo), pero los directores y analistas siempre deben exportar a Excel para responder preguntas de rentabilidad cruzada, enfrentándose a datos corruptos, faltas ortográficas (leetspeak), espacios fantasma, campos nulos y discrepancias impositivas.

---

## 🎯 2. Matriz de Estatus por Módulos y Funcionalidades

| Módulo / Funcionalidad | Descripción Técnica | Estatus |
| :--- | :--- | :---: |
| **Menú Superior Sticky Fijo** | Barra de navegación en una sola fila compacta, con logo SVG, selector global de industria sincronizado y accesos directos a las 5 secciones. | `🟢 100% OPERATIVO` |
| **1. Arquitectura & La Paradoja ERP** | Narrativa empresarial profunda sobre los roles de datos (Procesamiento, Análisis, Curador, Data Scientist, Data Engineer) y comparativa de tiempos de curaduría. | `🟢 100% OPERATIVO` |
| **Carrusel Corporativo de ERPs** | Carrusel interactivo automático (cada 5s) y manual con fichas técnicas, logos y capturas de SAP S/4HANA, Dynamics 365, Salesforce y Odoo/Macola. | `🟢 100% OPERATIVO` |
| **2. Manual ETL Paso a Paso** | 10 fases completas de transformación en Power Query explicadas a detalle, con código M nativo, alertas de mejores prácticas y botones interactivos. | `🟢 100% OPERATIVO` |
| **Simulador 3D de Tabla Dinámica** | Emulación visual de la lista de campos de Excel, sus 4 cuadrantes (Filtros, Columnas, Filas, Valores) y medidas DAX esenciales. | `🟢 100% OPERATIVO` |
| **3. Generador de Datos Multidisciplinario** | Motor estocástico con inyección opcional de impurezas (leetspeak `@/4/3/0`, dobles espacios, nulos, ventanas horarias compuestas). | `🟢 100% OPERATIVO` |
| **5 Esquemas Relacionales Independientes** | 5 estructuras de datos desacopladas (Retail, Logística, Finanzas, RRHH, Salud) con columnas, cálculos y lógicas exclusivas. | `🟢 100% OPERATIVO` |
| **Tabla de Previsualización (Tab 3)** | Encabezados (`<thead>`) y celdas (`<tbody>`) dinámicos según el esquema activo, con insignias de estatus e iconos de advertencia en impurezas. | `🟢 100% OPERATIVO` |
| **4. Dashboard Ejecutivo Reactivo** | Panel con Sidebar izquierdo de Slicers y área principal con 6 KPIs y 4 gráficos homólogos de Excel 365 con Chart.js. | `🟢 100% OPERATIVO` |
| **Muestra de Datos en Vivo del Dashboard** | Tabla integrada en la parte inferior del Dashboard que muestra las 9 columnas críticas del sector y reacciona a los segmentadores en tiempo real. | `🟢 100% OPERATIVO` |
| **Segmentadores (Slicers) de Excel 365** | 3 slicers con títulos dinámicos adaptados a cada industria (Rutas, Sucursales, Plantas, ARS, Tramos de Mora) y botones interactivos. | `🟢 100% OPERATIVO` |
| **5. Tabla Dinámica Analítica (Tab 5)** | Motor de agregación multidimensional al vuelo que permite cambiar la dimensión de corte y totaliza con pie corporativo. | `🟢 100% OPERATIVO` |
| **Exportaciones Nativas** | Generación de `.xlsx` (2 hojas: Datos crudos + Receta M), `.csv` (UTF-8 con BOM `\uFEFF`) y `.json` sanitizado sin campos internos. | `🟢 100% OPERATIVO` |
| **Diseño UI/UX Light Mode** | Cumplimiento estricto del 85% de ancho maestro (`master-wrapper`), colores Excel verde esmeralda (`#107c41`), slate y azul institucional. Cero modo dark. | `🟢 100% OPERATIVO` |

---

## 🏢 3. Detalle de los 5 Esquemas Relacionales Independientes

### 🛒 1. Supermercado & Retail Masivo (`retail`)
- **Campos:** `NUM_FACTURA`, `FECHA_VENTA`, `REGION`, `CLIENTE`, `VENDEDOR`, `CATEGORIA`, `PRODUCTO`, `CANAL_VENTA`, `CONDICION_PAGO`, `CANTIDAD`, `PRECIO_VENTA`, `SUBTOTAL`, `ITBIS_18`, `TOTAL_FACTURA`, `COSTO_TOTAL`, `MARGEN_BRUTO`, `ESTATUS_FACTURA`.
- **Slicers:** Región Geográfica, Estatus de Factura, Canal de Venta.
- **KPIs:** Ventas Brutas, Ingreso Real Efectivo, Margen Bruto, Margen %, % Meta Comercial, Tasa Cancelaciones.
- **Gráficos:** Ventas vs Costos por Región, Mix por Categoría, Tendencia Mensual, Top 8 Vendedores.

### 🚚 2. Logística, Fletes & Cadena de Suministro (`logistica`)
- **Campos:** `NUM_MANIFIESTO`, `FECHA_DESPACHO`, `RUTA_ORIGEN_DESTINO`, `EMPRESA_CLIENTE`, `CHOFER_FLOTA`, `VEHICULO_PLACA`, `TIPO_CARGA`, `MODALIDAD_FLETE`, `CONDICION_FLETE`, `TONELADAS_CARGA`, `TARIFA_POR_TON`, `SUBTOTAL_FLETE`, `PEAJES_COMBUSTIBLE`, `TOTAL_FLETE_RD`, `COSTO_OPERATIVO`, `MARGEN_FLETE`, `ESTATUS_DESPACHO`.
- **Slicers:** Ruta de Despacho, Estatus de Despacho, Tipo de Carga.
- **KPIs:** Fletes Brutos Totales, Flete Efectivo Cobrado, Margen Operativo, Rentabilidad %, Toneladas Transportadas, Tasa Despachos Anulados.
- **Gráficos:** Fletes vs Costos Operativos por Ruta, Mix por Tipo de Carga, Toneladas Mensuales, Top 8 Choferes de Flota.

### 💳 3. Finanzas Corporativas & Cuentas por Cobrar (`finanzas`)
- **Campos:** `NUM_PAGARE`, `FECHA_EMISION`, `FECHA_VENCIMIENTO`, `SUCURSAL_CARTERA`, `RNC_DEUDOR`, `NOMBRE_DEUDOR`, `OFICIAL_CREDITO`, `LINEA_CREDITO`, `CANAL_PAGO`, `TRAMO_MORA`, `MONTO_PRINCIPAL`, `TASA_INTERES_ANUAL`, `INTERES_MORA`, `SALDO_TOTAL_EXIGIBLE`, `ABONO_RECUPERADO`, `SALDO_PENDIENTE`, `DIAS_MORA`, `ESTATUS_CARTERA`.
- **Slicers:** Sucursal Cartera, Tramo de Mora (0-30d, 31-60d, 61-90d, +90d), Canal de Recaudo.
- **KPIs:** Cartera Total Exigible, Abonos Recuperados, Saldo Pendiente, Tasa de Recuperación %, Días Mora Promedio, Tasa Incobrables.
- **Gráficos:** Cartera Exigible vs Abonos por Sucursal, Mix por Línea Financiera, Recaudo Mensual, Top 8 Oficiales de Crédito.

### 👥 4. Recursos Humanos & Planilla Multisucursal (`rrhh`)
- **Campos:** `COD_EMPLEADO`, `FECHA_INGRESO`, `SEDE_PLANTA`, `NOMBRE_COLABORADOR`, `SUPERVISOR_TURNO`, `DEPARTAMENTO`, `CARGO_PUESTO`, `TIPO_CONTRATO`, `MODALIDAD_PAGO`, `SUELDO_BRUTO`, `HORAS_EXTRAS_VALOR`, `RETENCION_AFP_287`, `RETENCION_SFS_304`, `RETENCION_ISR`, `TOTAL_DESCUENTOS`, `SUELDO_NETO_PAGADO`, `APORTE_PATRONAL_TSS`, `ESTATUS_LABORAL`.
- **Slicers:** Sede / Planta, Estatus Laboral, Departamento.
- **KPIs:** Masa Salarial Bruta, Nómina Neta Pagada, Retenciones TSS & ISR, Aporte Patronal TSS (14.19%), Horas Extras Totales, Tasa Bajas / Salidas.
- **Gráficos:** Masa Salarial vs Retenciones por Planta, Distribución por Departamento, Evolución Mensual, Top 8 Supervisores de Turno.

### 🏥 5. Salud, Clínicas & Coberturas ARS (`salud`)
- **Campos:** `NUM_AUTORIZACION`, `FECHA_ATENCION`, `SEDE_CLINICA`, `EXPEDIENTE_PACIENTE`, `MEDICO_TRATANTE`, `ESPECIALIDAD_MEDICA`, `SERVICIO_PROCEDIMIENTO`, `ASEGURADORA_ARS`, `PLAN_SEGURO`, `MONTO_TOTAL_FACTURADO`, `COBERTURA_ARS`, `COPAGO_PACIENTE`, `COSTO_INSUMOS`, `MARGEN_CLINICA`, `ESTATUS_RECLAMACION`.
- **Slicers:** Sede Clínica, Estatus Reclamación, Aseguradora ARS.
- **KPIs:** Facturación Médica Total, Cobertura ARS Liquidada, Copagos Paciente, Margen Prestación, Tasa Aprobación ARS %, Tasa Glosas / Rechazos.
- **Gráficos:** Facturación vs Cobertura por Clínica, Mix por Especialidad Médica, Flujo Mensual de Reclamaciones, Top 8 Médicos Tratantes.

---

## 🚀 4. Guía de Ejecución y Visualización

1. **Abrir en Navegador Web:**
   Hacer doble clic directamente en el archivo:
   `C:\Users\User\Desktop\Manual Pedagógico ETL para Power Query & Excel\index.html`
   o abrirlo desde Chrome, Edge, Firefox, Brave u Opera.
2. **Cambiar de Caso de Empresa:**
   Utilizar el selector global ubicado en la barra de navegación superior o en el sidebar lateral izquierdo. Todo el ecosistema (tablas, gráficos, segmentadores, KPIs, tabla dinámica y descargas) se transforma inmediatamente.
3. **Descargar Archivos de Práctica:**
   - Clic en **Descargar Excel (.xlsx)** para obtener un libro con hoja de datos crudos y hoja con la receta de Power Query en código M.
   - Clic en **Descargar CSV (.csv)** para importar en Power BI o Python con codificación UTF-8 y BOM para evitar problemas con tildes y caracteres especiales.
   - Clic en **Descargar JSON (.json)** para APIs o microservicios.

---

## 🔒 5. Gobernanza y Control de Calidad
- **Sintaxis de JavaScript:** Verificada y validada mediante compilador Node.js (`0 errores`).
- **Aislamiento de Entorno:** Trabajo acotado estrictamente a la carpeta local del proyecto.
- **Compatibilidad:** 100% responsive (desde 320px hasta pantallas UltraWide 4K), 100% Light Theme corporativo.

---
*Manual y Sistema desarrollado con los más altos estándares de Gobernanza de Software y Analítica de Datos.*
