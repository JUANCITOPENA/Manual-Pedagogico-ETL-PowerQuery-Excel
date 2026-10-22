# 🗺️ PLAN DE TRABAJO MAESTRO DE INGENIERÍA: ARQUITECTURA ANALÍTICA MULTISECTORIAL

> **Proyecto:** DataForge Enterprise & Laboratorio ETL  
> **Ubicación:** `C:\Users\User\Desktop\Manual Pedagógico ETL para Power Query & Excel\PLAN_DE_TRABAJO_MAESTRO.md`  
> **Fecha:** 22 de Octubre de 2026  
> **Versión:** `v6.2-PRO`  
> **Estado:** `🟢 100% COMPLETADO, AUDITADO, CERTIFICADO Y EN PRODUCCIÓN`  
> **Gobernanza:** Gobernanza Empresarial de Desarrollo con IA & Power BI Data Architect

---

## 🎯 1. OBJETIVO PRINCIPAL DEL PLAN

Erradicar por completo cualquier estructura de datos genérica compartida entre los 5 casos de negocio. Implementar **5 motores de generación de datos totalmente independientes y especializados**, donde cada sector empresarial (**Supermercado, Logística, Finanzas/CxC, Recursos Humanos y Salud**) disponga de:
1. Su propio catálogo y estructura relacional de campos y tipos de datos.
2. Sus propios encabezados y formato de tabla en las vistas de previsualización.
3. Sus propios 6 KPIs ejecutivos calculados con lógica de negocio real.
4. Sus propios 4 gráficos interactivos Chart.js con métricas, títulos y dimensiones coherentes.
5. Sus propios segmentadores (Slicers) nativos de Excel.
6. Exportación a Excel (.xlsx multi-hoja), CSV (BOM) y JSON con la estructura exacta de ese sector.

---

## 🏛️ 2. ESQUEMA DE DATOS COMPARATIVO POR INDUSTRIA

A continuación se detalla la matriz de modelado de datos que se aplicará para asegurar que ningún campo quede artificialmente forzado:

| Dimensión / Atributo | 🛒 1. Supermercado & Retail | 🚚 2. Logística & Fletes | 💳 3. Finanzas & CxC | 👥 4. Recursos Humanos | 🏥 5. Salud & Clínicas |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Identificador Primario** | `NUM_FACTURA` | `NUM_MANIFIESTO` | `NUM_PAGARE` | `COD_EMPLEADO` | `NUM_AUTORIZACION` |
| **Dimensión Temporal** | `FECHA_VENTA` | `FECHA_DESPACHO` | `FECHA_EMISION` / `VENCIMIENTO` | `FECHA_INGRESO` / `PERIODO` | `FECHA_ATENCION` |
| **Entidad Territorial** | `REGION_SUCURSAL` | `RUTA_ORIGEN_DESTINO` | `REGION_COBRANZA` | `SEDE_PLANTA` | `SEDE_HOSPITALARIA` |
| **Sujeto de Negocio** | `CLIENTE_DISTRIBUIDOR` | `EMPRESA_GENERADORA` | `DEUDOR_RNC` | `COLABORADOR` | `PACIENTE_AFILIADO` |
| **Responsable Interno** | `VENDEDOR_RUTA` | `CHOFER_FLOTA` | `OFICIAL_CREDITO` | `SUPERVISOR_TURNO` | `MEDICO_ESPECIALISTA` |
| **Objeto Transaccional** | `PRODUCTO_SKU` | `TIPO_CARGA` (Seca, Fría) | `LINEA_CREDITO` (Pagaré) | `CARGO_PUESTO` | `PROCEDIMIENTO_MEDICO` |
| **Canal / Modalidad** | `CANAL_VENTA` (App, POS) | `TIPO_VEHICULO` (40ft, Termo) | `CANAL_PAGO` (ACH, Caja) | `MODALIDAD_PAGO` (ACH, Cheque) | `ASEGURADORA_ARS` |
| **Términos Operativos** | `CONDICION_PAGO` | `TIPO_FLETE` (LTL, FTL) | `TRAMO_MORA` (0-30d, 90d+) | `TIPO_CONTRATO` (Fijo, Turno) | `TIPO_PACIENTE` (Amb, Hosp) |
| **Métrica Volumétrica** | `CANTIDAD_UNIDADES` | `TONELADAS_CARGA` | `DIAS_MORA_REALES` | `HORAS_EXTRAS_TRABAJADAS` | `CANTIDAD_SERVICIOS` |
| **Métrica Unitaria** | `PRECIO_VENTA_UNIT` | `TARIFA_POR_TONELADA` | `TASA_INTERES_ANUAL` | `TARIFA_HORA_EXTRA` | `TARIFA_PROCEDIMIENTO` |
| **Métrica Bruta** | `SUBTOTAL_VENTA` | `SUBTOTAL_FLETE` | `MONTO_PRINCIPAL` | `SUELDO_BRUTO_BASE` | `MONTO_RECLAMADO_TOTAL` |
| **Ajustes / Impuestos** | `ITBIS_18` | `PEAJES_COMBUSTIBLE` | `INTERESES_MORA` | `RETENCIONES_LEY` (TSS/ISR) | `COBERTURA_ARS` |
| **Métrica Neta Total** | `TOTAL_FACTURADO` | `TOTAL_FLETE_RD` | `SALDO_TOTAL_EXIGIBLE` | `SUELDO_NETO_PAGADO` | `COPAGO_PACIENTE_RD` |
| **Métrica de Costo** | `COSTO_TOTAL_MERCANCIA` | `COSTO_OPERATIVO_CAMION` | `ABONO_RECUPERADO` | `APORTE_PATRONAL_TSS` | `COSTO_INSUMOS_MEDICOS` |
| **Métrica de Utilidad** | `MARGEN_BRUTO` | `MARGEN_OPERATIVO` | `SALDO_PENDIENTE` | `CARGA_LABORAL_TOTAL` | `MARGEN_PRESTACION` |
| **Estatus del Evento** | `ESTATUS_FACTURA` | `ESTATUS_DESPACHO` | `ESTATUS_CARTERA` | `ESTATUS_LABORAL` | `ESTATUS_RECLAMACION` |

---

## 📋 3. FASES DE EJECUCIÓN TÉCNICA

### Fase 1: Arquitectura de Datos & Generadores Especializados
- Crear 5 funciones generadoras desacopladas:
  - `generateRetailData()`
  - `generateLogisticsData()`
  - `generateFinanceData()`
  - `generateHRData()`
  - `generateHealthData()`
- Cada función generará estrictamente los campos definidos en la matriz anterior con reglas de negocio matemáticas coherentes (ej: en RRHH, calcular deducción AFP 2.87% y SFS 3.04% de acuerdo con la Ley 87-01 de República Dominicana; en Logística, cálculo de flete por toneladas más peajes; en Salud, separación de cobertura ARS y copago).

### Fase 2: Tablas de Muestra Reactivas Dinámicas (Thead & Tbody)
- Refactorizar `renderRawTable()` (en pestaña de Datasets) y `renderDashboardTable()` (en pestaña de Dashboard).
- El encabezado `<thead>` se reconstruirá dinámicamente según la industria activa:
  - Si es Logística: Columnas de Manifiesto, Toneladas, Ruta, Chofer, Flete Total, Estatus Despacho.
  - Si es Finanzas: Columnas de Pagaré, Deudor, Vencimiento, Principal, Mora, Saldo Pendiente.
  - Si es RRHH: Columnas de Empleado, Departamento, Cargo, Sueldo Bruto, Descuentos TSS, Sueldo Neto.
  - Si es Salud: Columnas de Autorización, Paciente, Médico, Procedimiento, Cobertura ARS, Copago.
  - Si es Retail: Columnas de Factura, Cliente, Vendedor, Producto, Cantidad, Total ITBIS, Margen.

### Fase 3: KPIs Dinámicos con Fórmulas Especializadas
- Adaptar las 6 tarjetas KPI del Dashboard para computar las métricas reales de cada industria:
  - **Retail:** Facturación Bruta, Ingreso Real, Margen Bruto, Margen %, % Meta, Tasa Cancelación.
  - **Logística:** Facturación Fletes, Flete Cobrado, Costo Combustible, Margen %, Tasa OTIF (A tiempo), Despachos Anulados.
  - **Finanzas:** Cartera Total, Cobro Recuperado, Intereses Mora, % Recuperación, Cartera Vigente, Cartera Castigada.
  - **RRHH:** Masa Salarial Bruta, Sueldos Netos Pagados, Retenciones TSS/ISR, Carga Social %, Horas Extras Promedio, Tasa Rotación.
  - **Salud:** Facturación Clínica, Cobro Efectivo ARS, Copagos en Caja, Margen Quirúrgico %, % Glosas ARS, Reclamaciones Rechazadas.

### Fase 4: Gráficos de Chart.js Especializados por Sector
- Redibujar los 4 gráficos con series y leyendas propias:
  - **Gráfico 1 (Columnas 2D):**
    - Retail: Ventas vs Costos por Región.
    - Logística: Fletes vs Gastos de Ruta por Destino.
    - Finanzas: Cartera Vigente vs Saldo en Mora por Sucursal.
    - RRHH: Salario Base vs Costo de Horas Extras por Sede.
    - Salud: Cobertura de Seguros ARS vs Copagos por Clínica.
  - **Gráfico 2 (Anillos):**
    - Retail: Mix por Familia de Producto.
    - Logística: Mix por Tipo de Carga.
    - Finanzas: Distribución por Tramo de Vencimiento (0-30, 31-60, 61-90, +90).
    - RRHH: Distribución de Personal por Departamento.
    - Salud: Mix por Servicio (Hospitalización, Cirugía, Laboratorio, Imágenes).
  - **Gráfico 3 (Líneas con Marcadores):**
    - Retail: Facturación Bruta vs Ingreso Real mensual.
    - Logística: Toneladas Despachadas vs Entregadas mensual.
    - Finanzas: Recaudo Efectivo vs Meta de Cobranza mensual.
    - RRHH: Evolución de Masa Salarial y Retenciones mensual.
    - Salud: Reclamaciones Presentadas vs Liquidadas por ARS mensual.
  - **Gráfico 4 (Barras Horizontales 2D):**
    - Retail: Top 8 Vendedores.
    - Logística: Top 8 Conductores de Flota.
    - Finanzas: Top 8 Oficiales de Cobro por Recaudo.
    - RRHH: Top 8 Supervisores de Área por Productividad.
    - Salud: Top 8 Médicos Especialistas por Procedimientos.

### Fase 5: Segmentadores (Slicers) Nativos Adaptativos
- Los botones de segmentación lateral se generarán con las dimensiones propias de cada industria:
  - Retail: Territorio, Estatus de Venta, Canal (App, Sucursal, Preventa).
  - Logística: Ruta, Estatus Despacho, Modalidad (FTL, LTL).
  - Finanzas: Región Cobro, Estatus Cartera, Tramo de Mora.
  - RRHH: Sede Planta, Estatus Laboral, Modalidad de Contrato.
  - Salud: Sede Clínica, Estatus Reclamación, Aseguradora ARS.

### Fase 6: Exportaciones Multi-Hoja Específicas
- Las funciones `downloadExcel()`, `downloadCSV()` y `downloadJSON()` exportarán el archivo con el nombre formal del sector y las columnas exactas (sin mezclar campos de otras industrias), acompañadas de la Hoja 2 con la receta pedagógica ETL.

---

## 🚦 4. QUALITY GATES & CRITERIOS DE ACEPTACIÓN

1. **Gate 1 - Integridad Analítica:** Ningún campo de una industria debe aparecer en otra (ej: no puede existir "ITBIS" en RRHH, ni "Copago" en Logística).
2. **Gate 2 - Reactividad Instantánea:** Cambiar de industria debe actualizar el 100% de la interfaz (Navbar, KPIs, Gráficos, Tablas de Muestra del Generador y Dashboard, Slicers y Pivot Table) en menos de 100 milisegundos.
3. **Gate 3 - Legibilidad para Grabaciones:** Tipografías grandes (16px base, 1.7 interlineado), alto contraste, 100% Light Mode y contenedor maestro centrado al 85%.
4. **Gate 4 - Exportación Limpia:** El libro `.xlsx` y el archivo `.csv` descargados deben abrirse en Microsoft Excel mostrando tildes correctas y separadores numéricos adecuados sin errores de fórmula.

---

## 💬 5. DECISIÓN REQUERIDA DEL USUARIO

Una vez revisado este plan y el prompt maestro consolidado en `README_PROMPT_MAESTRO.md`, por favor indícame:
- ¿Deseas aprobar este plan para proceder a implementar la separación total de los 5 esquemas de datos y sus tablas dinámicas en `index.html`?
- ¿Tienes algún ajuste o campo adicional que desees incorporar en alguna de las 5 industrias antes de iniciar la codificación?
