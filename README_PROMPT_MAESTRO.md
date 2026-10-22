# 📜 PROMPT MAESTRO CONSOLIDADO: PLATAFORMA PEDAGÓGICA ETL, POWER QUERY, EXCEL & GOBERNANZA DE DATOS

> **Documento:** Registro Integral de Requerimientos y Especificaciones Funcionales  
> **Ubicación:** `C:\Users\User\Desktop\Manual Pedagógico ETL para Power Query & Excel\README_PROMPT_MAESTRO.md`  
> **Versión:** `v6.2-PRO`  
> **Fecha:** 22 de Octubre de 2026  
> **Autor/Arquitecto:** Ing. Juancito Peña Vizcaíno  
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
3. **Tipografía Aumentada en un 5%:** Todos los textos, párrafos, tablas, títulos (H1-H6), subtítulos, selectores, KPIs y observaciones con incremento matemático del 5% (`font-size: 105%` base) para máxima legibilidad docente y proyecciones.
4. **Bordes Animados Corporativos:** Efecto animado `@keyframes borderGlowLoop` aplicado en todas las cards y secciones con gradiente armónico verde Excel, Power Query, azul Microsoft y esmeralda fresco.
5. **Menú de Navegación Fijo en Una Sola Fila (Sticky Top):**
   - Logotipo y nombre del sistema a la izquierda.
   - Selector global de caso de empresa en el centro.
   - 5 botones de navegación con iconos FontAwesome en fila horizontal compacta.
   - Botón de descarga directa a Excel a la derecha.
6. **Carrusel de Sistemas Transaccionales (Auto-Play + Manual):**
   - Presentación de los 4 grandes sistemas: SAP S/4HANA, Dynamics 365, Salesforce CRM y Odoo/Macola.
7. **Visor Modal Lightbox al 95% de la Pantalla:**
   - Para infografías y diagramas técnicos (`img1.png`, `img2.png`, `img3.png`, `img4.png`).
   - Botón de cierre (`X`) visible, navegación con flechas y tecla `Escape`.

---

## 👥 3. MATRIZ DE SENIORITY, ROLES & REMUNERACIÓN GLOBAL

Previo a la tabla comparativa de tiempos de consolidación, incorporar una sección con:
- **6 Niveles de Especialización:** Data Entry, Técnico Soporte, Curador ETL, Analista BI, Científico de Datos y Arquitecto IA/MCP.
- **Tabla Comparativa Salarial:** Desglose anual en USD por rol con y sin habilidades en IA/MCP, prima salarial porcentual y rangos geográficos (RD/LATAM, USA, Europa).
- **Fuentes de Remuneración:** Glassdoor, LinkedIn Workforce, Michael Page y CompTIA.
- **Gráficos Chart.js:** Brecha Salarial de Tecnologías y Crecimiento de Demanda de Perfiles.
- **Infografía de Cierre:** Integración de `img/img1.png` con apertura a pantalla completa.

---

## 🖼️ 4. GALERÍA MASTER ETL (TAB 2)

Dentro de la sección de Power Query, incorporar un Card Group al 100% de ancho con las 3 fases del pipeline:
- Tarjeta 1: Conexión & Orígenes de Datos (`img/img2.png`).
- Tarjeta 2: Desinfección & Purificación M (`img/img3.png`).
- Tarjeta 3: Cálculos Financieros & Columnas Personalizadas (`img/img4.png`).
- Al hacer clic sobre cualquier imagen, se expande al **95% del total de la pantalla** en el visor modal interactivo.

---

## 🧊 5. MANUAL ILUSTRADO 3D DE TABLAS DINÁMICAS (TUTSPLUS - TAB 5)

En la pestaña 5, implementar un manual pedagógico completo basado en la metodología de *Envato TutsPlus (CMS-28571)* adaptado 100% al set de datos de **Supermercado & Retail Masivo**:
- **Modelado 3D Isométrico:** Representación en 3 capas en relieve con visualización de los 4 cuadrantes (Filtros, Columnas, Filas, Valores).
- **8 Fases de Aprendizaje:** Higiene, inserción con atajos (`Alt + N + V`), anatomía del panel, construcción de vista de retail, configuración de valores (Suma, Promedio, RD$), agrupación cronológica, formato tabular clásico y segmentadores (Slicers).
- **Eliminación del Simulador Secundario:** Exclusión de tablas redundantes de simulación para enfocar la experiencia pedagógica en el manual ilustrado 3D.

---

## 📊 6. RIGOR ANALÍTICO: 5 ESQUEMAS DE DATOS INDEPENDIENTES Y EXCLUSIVOS

**REGLA CRÍTICA:** Queda estrictamente prohibido compartir una estructura de datos genérica entre las industrias. Cada sector debe poseer sus propios campos, columnas, métricas, tasas impositivas y lógica operativa:

### Caso 1: Supermercado & Retail Masivo (Comercio Minorista)
- **Campos Específicos:** `NUM_FACTURA`, `FECHA_DOCUMENTO`, `REGION`, `CLIENTE_ID`, `CLIENTE_NOMBRE`, `VENDEDOR`, `CATEGORIA_PRODUCTO`, `PRODUCTO_SKU`, `CANAL_VENTA` (Sucursal, App Móvil, Preventa Ruta), `CONDICION_PAGO`, `CANTIDAD_UNIDADES`, `PRECIO_VENTA`, `SUBTOTAL`, `ITBIS_18`, `TOTAL_VENTA`, `COSTO_UNITARIO`, `COSTO_TOTAL`, `MARGEN_BRUTO`, `ESTATUS_FACTURA`.
- **KPIs del Dashboard:** Facturación Bruta, Ingreso Real Efectivo, Margen Bruto RD$, Rentabilidad Margen %, Cumplimiento de Meta Comercial, Tasa de Cancelación.

### Caso 2: Logística, Transporte & Fletes (Cadena de Suministro)
- **Campos Específicos:** `NUM_MANIFIESTO`, `FECHA_DESPACHO`, `RUTA_ORIGEN_DESTINO`, `EMPRESA_CLIENTE`, `CONDUCTOR_FLOTA`, `TIPO_VEHICULO_PLACA`, `TIPO_CARGA`, `MODALIDAD_FLETE`, `CONDICION_FLETE`, `TONELADAS_CARGA`, `TARIFA_POR_TONELADA`, `SUBTOTAL_FLETE`, `PEAJES_COMBUSTIBLE`, `TOTAL_FLETE_RD`, `COSTO_OPERATIVO`, `MARGEN_FLETE`, `ESTATUS_DESPACHO`.

### Caso 3: Finanzas, Tesorería & Cuentas por Cobrar (CxC / Cartera de Crédito)
- **Campos Específicos:** `NUM_PAGARE_FACTURA`, `FECHA_EMISION`, `FECHA_VENCIMIENTO`, `DIAS_CREDITO_OTORGADO`, `RNC_DEUDOR`, `NOMBRE_DEUDOR`, `OFICIAL_CREDITO`, `LINEA_CREDITO_INSTRUMENTO`, `CANAL_PAGO`, `TRAMO_VENCIMIENTO`, `MONTO_PRINCIPAL_RD`, `TASA_INTERES_ANUAL`, `INTERES_MORA_GENERADO`, `SALDO_TOTAL_EXIGIBLE`, `ABONO_RECUPERADO`, `SALDO_PENDIENTE`, `DIAS_MORA_REALES`, `ESTATUS_CARTERA`.

### Caso 4: Recursos Humanos & Nómina Corporativa (Planilla Multisucursal)
- **Campos Específicos:** `COD_EMPLEADO`, `FECHA_INGRESO`, `SEDE_PLANTA`, `NOMBRE_COLABORADOR`, `SUPERVISOR_TURNO`, `DEPARTAMENTO_AREA`, `CARGO_POSICION`, `TIPO_CONTRATO`, `MODALIDAD_PAGO`, `SUELDO_BRUTO_BASE`, `HORAS_EXTRAS_VALOR`, `RETENCION_AFP_287`, `RETENCION_SFS_304`, `RETENCION_ISR`, `TOTAL_DESCUENTOS_LEY`, `SUELDO_NETO_PAGADO`, `APORTE_PATRONAL_TSS`, `ESTATUS_LABORAL`.

### Caso 5: Salud, Clínicas & Coberturas ARS (Facturación Médica)
- **Campos Específicos:** `NUM_AUTORIZACION_MEDICA`, `FECHA_ATENCION`, `SEDE_HOSPITALARIA`, `EXPEDIENTE_PACIENTE`, `MEDICO_TRATANTE`, `ESPECIALIDAD_MEDICA`, `SERVICIO_PROCEDIMIENTO`, `ASEGURADORA_ARS`, `PLAN_SEGURO`, `MONTO_FACTURADO_TOTAL`, `COBERTURA_ARS_MONTO`, `COPAGO_PACIENTE_MONTO`, `COSTO_INSUMOS_MEDICOS`, `MARGEN_PRESTACION_CLINICA`, `ESTATUS_RECLAMACION`.

---

## ⚡ 7. EXPERIENCIA REACTIVA BIDIRECCIONAL EN VIVO

1. **Sincronización Total de Selectores:** Cualquier cambio de empresa desde el Header Navbar, el Generador o el Sidebar del Dashboard debe sincronizar todos los componentes, gráficos y segmentadores al unísono.
2. **Navegación Blindada:** La función `switchTab` debe estar protegida con manejo defensivo de errores para garantizar transiciones fluidas e instantáneas.
3. **Descargas Multi-Hoja:** Generación de archivos `.xlsx` (datos crudos + receta M), `.csv` (UTF-8 con BOM) y `.json` sanitizado.

---
*Consolidado y mantenido por el Ing. Juancito Peña Vizcaíno.*
