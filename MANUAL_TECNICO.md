# MANUAL_TÉCNICO — Manual Interno IA: RGPD y AI Act Art. 50

**Repositorio:** `migueljerico/manual-ia-rgpd-ai-act`  
**Versión del manual:** 1.0  
**Fecha de actualización:** 10 de agosto de 2026  
**Estado:** Completado

---

## 1. Descripción general

El proyecto **Manual Interno IA — RGPD y AI Act Art. 50** es un repositorio de documentación que sirve como índice y punto de acceso a un manual de cumplimiento normativo elaborado para la empresa ficticia **AM Associates**. El manual, de 2 páginas, está diseñado para empleados administrativos y establece pautas obligatorias para el uso de herramientas de IA generativa (Microsoft Copilot y ChatGPT) conforme al Reglamento General de Protección de Datos (RGPD) y al Artículo 50 del AI Act de la Unión Europea (Reglamento UE 2024/1689), cuya obligación de marcado es efectiva desde agosto de 2026.

El repositorio no contiene código fuente de aplicación, sino que está compuesto por un archivo `README.md` (documentación principal) y un archivo `LICENSE` (licencia MIT). El manual completo está alojado externamente en Google Docs y se accede mediante un enlace desde el `README.md`.

---

## 2. Arquitectura general

El proyecto sigue una estructura de **documentación informativa** en lugar de una aplicación de software. La arquitectura se representa en tres capas conceptuales:

```
┌─────────────────────────────────────────────────────────────┐
│                  CAPA DE PRESENTACIÓN                       │
│  README.md (documentación en GitHub)                        │
│  Enlace externo → Documento Google Docs (manual completo)   │
└─────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                    CAPA DE LÓGICA                           │
│  Contenido normativo:                                       │
│  • Obligaciones RGPD                                        │
│  • Obligaciones AI Act Art. 50                              │
│  • Prompt CO-STAR                                           │
│  • Flujo de trabajo (antes/durante/después)                 │
└─────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                     CAPA DE DATOS / API                     │
│  No se consume ninguna API externa.                         │
│  Datos de referencia: Reglamentos UE, AEPD, M365 tenant     │
│  (origen: documentación oficial, no automatizada)           │
└─────────────────────────────────────────────────────────────┘
```

No existe interacción con servicios web, bases de datos ni endpoints. El flujo es unidireccional: el usuario lee el repositorio, accede al documento externo y aplica las directrices en su entorno de trabajo.

---

## 3. Módulos y componentes

El repositorio contiene dos archivos raíz, cada uno con una responsabilidad específica:

### 3.1 `README.md`

| Campo | Detalle |
|---|---|
| **Responsabilidad** | Documento principal del repositorio. Presenta el proyecto, resume el marco normativo, describe el flujo de trabajo y proporciona el enlace al manual completo. |
| **Estructura interna** | Secciones: badges de estado, acceso al documento, descripción, marco normativo (RGPD y AI Act), flujo de trabajo, prompt CO-STAR, cláusula de marcado. |
| **Elementos clave** | Tabla de principios RGPD, tabla de obligaciones de marcado AI Act, tabla de flujo de trabajo, prompt CO-STAR en formato Markdown. |
| **Enlace externo** | URL de Google Docs: `https://docs.google.com/document/d/1Xw2HOFEUWyGn7wxkvXeXEs0AWgNf5zlm4mDL-GEh8_I/edit` |

### 3.2 `LICENSE`

| Campo | Detalle |
|---|---|
| **Responsabilidad** | Define los términos de uso y distribución del contenido del repositorio. |
| **Tipo de licencia** | MIT License. |
| **Titular** | Miguel Jericó (migueljerico). |
| **Año** | Copyright (c) 2025 (original), aplicable a 2026 en adelante. |
| **Permisos** | Uso comercial, modificación, distribución y uso privado, con condición de incluir el aviso de copyright y la licencia. |

No hay otros módulos de código, scripts ni archivos de configuración.

---

## 4. APIs y endpoints

No aplica. El proyecto no expone ni consume APIs. La única integración externa es el enlace directo a Google Docs, que no constituye una API documentada en este repositorio.

---

## 5. Variables de entorno

No aplica. No se detectan variables de entorno, archivos `.env`, configuraciones de entorno ni parámetros de ejecución. El proyecto es puramente documental.

---

## 6. Guía de despliegue

Al ser un proyecto de documentación estática, el "despliegue" consiste en publicar el repositorio en GitHub y acceder al contenido externo. Pasos:

### 6.1 Requisitos previos

- Cuenta en GitHub con permisos para crear o clonar repositorios.
- Conexión a internet para acceder al repositorio y al documento de Google Docs.
- (Opcional) Git instalado en el equipo local para clonar.

### 6.2 Publicación del repositorio (si se parte desde cero)

1. Crear un nuevo repositorio en GitHub con el nombre `manual-ia-rgpd-ai-act`.
2. Subir los archivos `README.md` y `LICENSE` al repositorio.
3. Verificar que el enlace de Google Docs del `README.md` sea accesible públicamente (o con permisos de la organización AM Associates).

### 6.3 Clonación y visualización local

```bash
git clone https://github.com/migueljerico/manual-ia-rgpd-ai-act.git
cd manual-ia-rgpd-ai-act
```

Abrir el archivo `README.md` en cualquier editor de Markdown o visualizarlo directamente en GitHub.

### 6.4 Acceso al manual completo

- Hacer clic en el enlace del `README.md` (botón "Ver Manual Completo").
- Si el documento de Google Docs requiere permisos, solicitar acceso al propietario.
- Una vez abierto, el manual puede imprimirse, exportarse a PDF o compartirse internamente.

### 6.5 Verificación de funcionamiento

- Confirmar que el enlace no devuelve error 404.
- Comprobar que los badges del `README.md` se renderizan correctamente (dependen de servicios externos de shields.io).

---

## 7. Limitaciones conocidas y mejoras futuras

### 7.1 Limitaciones

| Limitación | Descripción |
|---|---|
| **Contenido externo** | El manual real está alojado en Google Docs, no en el repositorio. Si el enlace externo se rompe o cambia los permisos, el repositorio queda sin contenido útil. |
| **Dependencia de servicios externos** | Los badges de estado dependen de shields.io y de la disponibilidad de internet. |
| **Sin control de versiones del contenido** | El documento de Google Docs no tiene un historial de versiones integrado con el repositorio, lo que dificulta el seguimiento de cambios normativos. |
| **Alcance limitado** | Solo cubre los requisitos básicos de RGPD y AI Act Art. 50; no incluye normativas sectoriales (salud, educación, etc.) ni otros artículos del AI Act. |
| **Formato no automatizable** | No hay scripts ni plantillas reutilizables para generar documentos similares. |

### 7.2 Mejoras propuestas

1. **Incluir el manual en el repositorio** en formato Markdown o PDF, además del enlace externo, para garantizar redundancia.
2. **Automatizar la verificación de enlaces** con GitHub Actions para detectar roturas del enlace de Google Docs.
3. **Añadir ejemplos de registros internos** (plantillas de prompt, tabla de registro de contenido sintético) directamente en el repositorio.
4. **Ampliar la cobertura normativa** con otros artículos del AI Act (sistemas de alto riesgo, transparencia, etc.) y guías específicas por sector.
5. **Crear una plantilla de prompt reutilizable** en formato `.txt` o `.md` descargable.
6. **Incluir un historial de cambios** (CHANGELOG) para reflejar las actualizaciones del manual.

---

## 8. Referencias normativas

- **RGPD** — Reglamento (UE) 2016/679, de 27 de abril de 2016, relativo a la protección de las personas físicas en lo que respecta al tratamiento de datos personales.
- **AI Act** — Reglamento (UE) 2024/1689, de 13 de junio de 2024, por el que se establecen normas armonizadas en materia de inteligencia artificial. El Artículo 50 (obligaciones de transparencia y marcado) es de aplicación obligatoria desde agosto de 2026.
- **AEPD** — Agencia Española de Protección de Datos, autoridad de control de referencia en el manual.

---

## 9. Licencia

El contenido de este repositorio está bajo la licencia **MIT**. Se permite su uso, copia, modificación y distribución siempre que se incluya el aviso de copyright original:

```
Copyright (c) 2025 Miguel Jericó (migueljerico)
```

**Nota:** La fecha de copyright corresponde al año de creación original del repositorio. El presente manual técnico se actualiza en agosto de 2026 conforme al estado vigente del proyecto.

<p align="center">Creado por <a href="https://github.com/migueljerico">@migueljerico</a> y documentado por QwenCloud (deepseek-v4-flash-0731) desde la App Asistente de IA · 2026</p>