# Plan de Gestión de Configuración (SCM) - ISW 4k4

* **Grupo:** 10
* **Asignatura:** Ingeniería y Calidad de Software
* **Año:** 2026
* **Curso:** 4K4

---

## 1. Propósito
El propósito de este repositorio es establecer la Gestión de Configuración de Software (SCM) para todos los artefactos generados durante el cursado de la materia, asegurando la integridad, trazabilidad y recuperación de la información en todo momento.

## 2. Alcance
Este plan abarca la administración y control de versiones de documentos teóricos, guías prácticas, bibliografía, resoluciones de Trabajos Prácticos (TPs) evaluables, el Trabajo Práctico Integrador (TPI) y el código fuente asociado al producto de software desarrollado.

## 3. Herramientas Utilizadas
* **Control de Versiones:** Git
* **Alojamiento del Repositorio:** GitHub (Repositorio Público)

---

## 4. Estructura del Repositorio
La organización física de los Ítems de Configuración (IC) se distribuye en los siguientes directorios principales:

```text
/
├── CodigoFuente/      # Archivos fuente del producto de software (TPI)
├── TPs/                # Consignas y resoluciones de Trabajos Prácticos evaluables
├── TPigs/              # Documentación e incrementos del Trabajo Práctico Integrador
├── Material/
│   ├── teorico/        # Apuntes y presentaciones de clases teóricas
│   ├── practico/       # Guías y ejercicios de clases prácticas
│   └── bibliografia/   # Libros, papers y referencias obligatorias/optativas
└── Parciales/
    └── Parcial_N/      # Material de estudio agrupado por parcial (N = 1, 2, etc.)
        ├── teorico/    # Material de estudio teórico del parcial
        ├── practico/   # Ejercicios de práctica para el parcial
        └── resumenes/  # Resúmenes propios elaborados por el grupo        
```

## 5. Identificación de Ítems de Configuración y Reglas de Nombrado

Para mantener la consistencia y la trazabilidad de las versiones, todos los archivos deben respetar la siguiente convención de nombrado general:

**Formato General:** `[PREFIJO]_[Nombre-Descriptivo]_v[X.X].[ext]`
* `[PREFIJO]`: Indicador de 2 a 3 letras según el tipo de Ítem de Configuración.
* `[Nombre-Descriptivo]`: Breve descripción del contenido (usando CamelCase o guiones, sin espacios).
* `v[X.X]`: Número de versión del documento (ej: v1.0, v1.1, v2.0).
* `[ext]`: Extensión del archivo (.pdf, .md, .java, etc.).

| Ítem de Configuración | Regla de Nombrado | Ubicación en el Repo | Ejemplo de Aplicación |
| :--- | :--- | :--- | :--- |
| **Trabajos Prácticos** | `TP_<Nombre-Descriptivo>_v<X.X>.<ext>` | `/TPs/` | `TP_TrabajoPractico4-SCM_v1.0.pdf` |
| **Trabajo Integrador** | `TPI_<Nombre-Descriptivo>_v<X.X>.<ext>` | `/TPigs/` | `TPI_DocumentoArquitectura_v1.2.md` |
| **Material Teórico** | `TEO_<Nombre-Descriptivo>_v<X.X>.<ext>` | `/Material/teorico/` | `TEO_Unidad3-SCM_v1.0.pdf` |
| **Material Práctico** | `PRA_<Nombre-Descriptivo>_v<X.X>.<ext>` | `/Material/practico/` | `PRA_GuiaEjerciciosU2_v1.0.pdf` |
| **Bibliografía** | `BIB_<Nombre-Descriptivo>_v<X.X>.<ext>` | `/Material/bibliografia/` | `BIB_Paper-NoSilverBullet_v1.0.pdf` |
| **Código Fuente** | `SRC_<Nombre-Descriptivo>_v<X.X>.<ext>` | `/CodigoFuente/` | `SRC_App_Backend_v1.0.java` |
| **Parciales / Resúmenes** | `PAR_<Nombre-Descriptivo>_v<X.X>.<ext>` | `/Parciales/Parcial_N/resumenes/` | `PAR_Resumen1erParcial_v1.0.pdf` |

---

## 6. Criterio de nombramiento de commits

Para llevar un control formal y estandarizado de los cambios, el equipo utiliza la convención *Conventional Commits*. El mensaje de cada commit debe estructurarse de la siguiente manera:

`<Acción>: <Descripción breve de los cambios>`

### Acciones recomendadas
* `feat:` Para agregar un nuevo archivo, directorio, resolución de TP o código fuente. (Ej: `feat: agrega resolución completa del TP4`)
* `fix:` Para corregir un error, un bug o un problema de redacción en un documento. (Ej: `fix: corrige error de tipeo en diagrama de clases`)
* `docs:` Para crear o modificar archivos de documentación, como el README o glosarios. (Ej: `docs: actualiza convención de ramas en README`)
* `refactor:` Para reorganizar o mejorar estructuras, carpetas o código sin cambiar su funcionalidad. (Ej: `refactor: reestructura carpetas principales del proyecto`)
* `chore:` Para tareas de mantenimiento rutinario o limpieza, como la gestión del repositorio. (Ej: `chore: agrega archivos .gitkeep para inicializar carpetas vacías`)

---

## 7. Criterio de Línea Base
Se establecerá una Línea Base formal en el repositorio, utilizando etiquetas (Tags) de Git, exclusivamente bajo el siguiente criterio:
Cada vez que un Trabajo Práctico o entrega del TPI sea evaluado y APROBADO por la cátedra.

--- 

## 8. Nomenclatura de Línea Base
 
La nomenclatura de la línea base debe respetar el siguiente formato:
 
```
ISW_G10_LINEA_BASE_<VERSIONxx>_<NombreLB>
```
 
* **`ISW_G10_LINEA_BASE`**: Prefijo obligatorio para todas las líneas base del proyecto.
* **`<VERSIONxx>`**: Número de versión con dos dígitos (ej: `01`, `02`, `03`).
* **`<NombreLB>`**: Nombre descriptivo en PascalCase, sin espacios ni tildes (ej: `AprobacionTP3`).
 
### Ejemplos de etiquetas
 
| Versión | Tag | Descripción |
| :--- | :--- | :--- |
| 01 | `ISW_G10_LINEA_BASE_01_AprobacionTP1` | TP1 aprobado |
| 02 | `ISW_G10_LINEA_BASE_02_AprobacionTP2` | TP2 aprobado |
| 03 | `ISW_G10_LINEA_BASE_03_AprobacionTP3` | TP3 aprobado |
 
### Comandos Git
 
Para crear y publicar una línea base:
 
```bash
git tag -a ISW_G10_LINEA_BASE_01_AprobacionTP1 -m "Línea base 1 - Aprobación TP1"
git push origin ISW_G10_LINEA_BASE_01_AprobacionTP1
```
 
> **Importante:** Toda línea base debe ser comunicada al equipo y la etiqueta generada debe quedar registrada en la documentación del proyecto, asegurando su trazabilidad.

---

## 9. Glosario
* **ISW:** Ingeniería y Calidad de Software
* **G10:** Grupo 10, el grupo correspondiente a la materia
* **4K4:** Comisión correspondiente
