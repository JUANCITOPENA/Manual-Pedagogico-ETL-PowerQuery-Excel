# 🚀 SUBAGENTE DEVOPS & GITHUB DEPLOYER (`SUB-OPS-05`)
## Sistema Multi-Agente de Curaduría de Datos, Power Query & Microsoft Excel
**Arquitecto:** Ing. Juancito Peña Vizcaíno  
**Ubicación:** `agents/SUBAGENTE_DEVOPS_GITHUB_DEPLOYER.md`  
**Clasificación:** Subagente Especializado en Control de Versiones y Despliegue Cloud

---

## 🎯 1. Misión y Responsabilidad

Gestionar el ciclo de vida del código fuente, el control de versiones con Git, la sincronización con el repositorio oficial en GitHub y la publicación continua y automatizada en **GitHub Pages**. Asegura que la aplicación sea 100% accesible en la web pública para la comunidad pedagógica y profesional sin dependencias de servidores propietarios.

---

## 🌐 2. Especificaciones de Despliegue en GitHub Pages

1. **Arquitectura Serverless / Static Web:**
   - La plataforma está compuesta por un único artefacto HTML autónomo (`index.html`) con librerías externas entregadas por CDNs de alta velocidad (Cloudflare, cdnjs, jsDelivr).
   - Cero requerimientos de Node.js, Python o PHP en tiempo de ejecución de producción.
2. **Repositorio Oficial:**
   - **URL del Repositorio:** `https://github.com/JUANCITOPENA/Manual-Pedagogico-ETL-PowerQuery-Excel`
   - **URL de Producción (GitHub Pages):** `https://juancitopena.github.io/Manual-Pedagogico-ETL-PowerQuery-Excel/`
3. **Flujo de Publicación Automatizado:**
   - Rama maestra: `main` (o `master`).
   - GitHub Pages configurado para servir directamente desde la raíz (`/`) de la rama principal.
   - Cada *commit* y *push* sincroniza instantáneamente las actualizaciones pedagógicas y analíticas.
4. **Respaldo Local Preventivo:**
   - Todo cambio crítico genera previamente un archivo de respaldo en `.backup/` para garantizar la resiliencia y recuperación inmediata ante cualquier eventualidad.
