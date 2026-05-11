# Plan de Gestión de Configuración (SCM) - ISW 4K4

- **Asignatura:** Ingeniería y Calidad de Software
- **Año:** 2026
- **Curso:** 4K4
- **Grupo:** 10
- **Integrantes:**
  - **Carranza Duobaitis**, Candelaria (402600)
  - **Cavina Pellis**, Manuel (95648)
  - **Llabot**, Ignacio Martín (403083)
  - **Maldonado**, Franco Gabriel (92123)
  - **Marti**, Eliazar Alexis (403419)
  - **Martínez Agliozzo**, Luz María (94415)
  - **Nobile**, Bruno Nicolas (92098)
  - **Palomeque Galindo**, Matías Ezequiel (94482)
  - **Salvatico**, Francisco (403815)
  - **Sana**, Fabrizzio (98161)
  - **Schurrer**, Gabriel Nicolas (95046)

---

## 1. Propósito

El propósito de este repositorio es establecer la Gestión de Configuración de Software (SCM) para todos los artefactos generados durante el cursado de la materia, asegurando la integridad, trazabilidad y recuperación de la información en todo momento.

## 2. Alcance

Este plan abarca la administración y control de versiones de documentos teóricos, guías prácticas, bibliografía, resoluciones de Trabajos Prácticos (TPs) evaluables, el Trabajo Práctico Integrador (TPI) y el código fuente asociado al producto de software desarrollado.

## 3. Herramientas Utilizadas

- **Control de Versiones:** Git
- **Alojamiento del Repositorio:** GitHub (Repositorio Público)

---

## 4. Estructura del Repositorio

La organización física de los Ítems de Configuración (IC) se distribuye en los siguientes directorios:

```
/
├── CodigoFuente/           # Archivos fuente del producto de software (TPI)
├── TPs/                    # Consignas y resoluciones de Trabajos Prácticos evaluables
├── TPigs/                  # Documentación e incrementos del Trabajo Práctico Integrador
├── Material/
│   ├── teorico/            # Apuntes y presentaciones de clases teóricas
│   ├── practico/           # Guías y ejercicios de clases prácticas
│   └── bibliografia/       # Libros, papers y referencias obligatorias/optativas
└── Parciales/
    └── Parcial_N/          # Material agrupado por parcial (N = 1, 2, etc.)
        ├── teorico/
        ├── practico/
        └── resumenes/
```

---

## 5. Identificación de Ítems de Configuración y Reglas de Nombrado

Todos los archivos deben respetar el siguiente formato general:

**`[PREFIJO]_[Nombre-Descriptivo]_v[X.X].[ext]`**

- `[PREFIJO]`: Siglas de 2 a 3 letras según el tipo de ítem (ver tabla).
- `[Nombre-Descriptivo]`: Descripción breve del contenido, en CamelCase, sin espacios.
- `v[X.X]`: Número de versión (ej: v1.0, v1.1, v2.0).
- `[ext]`: Extensión fija del archivo según el tipo de ítem. Si un ítem puede existir en más de un formato (editable + entrega), se indica `Editable` en el nombre para distinguirlo.

### Listado de Ítems de Configuración

| Ítem de Configuración | Prefijo | Regla de Nombrado | Ubicación | Extensión |
|---|---|---|---|---|
| Plan de Gestión SCM | `SCM` | `SCM_PlanGestion_v<X.X>.pdf` | `/TPs/` | `.pdf` (no editable) |
| Consigna de TP | `TP` | `TP_Consigna-<NombreTP>_v<X.X>.pdf` | `/TPs/` | `.pdf` (no editable) |
| Resolución de TP (editable) | `TP` | `TP_Resolucion-<NombreTP>_Editable_v<X.X>.docx` | `/TPs/` | `.docx` |
| Resolución de TP (entrega) | `TP` | `TP_Resolucion-<NombreTP>_v<X.X>.pdf` | `/TPs/` | `.pdf` |
| Cronograma | `CRON` | `CRON_Cronograma_v<X.X>.xlsx` | `/Material/` | `.xlsx` (no editable en otro formato) |
| Documentación TPI | `TPI` | `TPI_<Nombre-Descriptivo>_v<X.X>.pdf` | `/TPigs/` | `.pdf` |
| Documentación TPI (editable) | `TPI` | `TPI_<Nombre-Descriptivo>_Editable_v<X.X>.docx` | `/TPigs/` | `.docx` |
| Material Teórico | `TEO` | `TEO_<Nombre-Descriptivo>_v<X.X>.pdf` | `/Material/teorico/` | `.pdf` (no editable) |
| Material Práctico / Guías | `PRA` | `PRA_<Nombre-Descriptivo>_v<X.X>.pdf` | `/Material/practico/` | `.pdf` (no editable) |
| Bibliografía | `BIB` | `BIB_<Nombre-Descriptivo>_v<X.X>.pdf` | `/Material/bibliografia/` | `.pdf` (no editable) |
| Código Fuente | `SRC` | `SRC_<Nombre-Descriptivo>_v<X.X>.<ext>` | `/CodigoFuente/` | Varía según lenguaje (.java, .kt, .py, etc.) |
| Resúmenes de Parcial | `PAR` | `PAR_<Nombre-Descriptivo>_v<X.X>.pdf` | `/Parciales/Parcial_N/resumenes/` | `.pdf` |

### Ejemplos de aplicación

| Ítem | Nombre del archivo |
|---|---|
| Plan SCM (este documento) | `SCM_PlanGestion_v1.0.pdf` |
| Consigna del TP4 | `TP_Consigna-SCM_v1.0.pdf` |
| Resolución del TP4 (editable) | `TP_Resolucion-SCM_Editable_v1.0.docx` |
| Resolución del TP4 (entrega) | `TP_Resolucion-SCM_v1.0.pdf` |
| Cronograma de la materia | `CRON_Cronograma_v1.0.xlsx` |
| Apunte teórico Unidad 3 | `TEO_Unidad3-SCM_v1.0.pdf` |
| Guía práctica Unidad 2 | `PRA_GuiaEjerciciosU2_v1.0.pdf` |

---

## 6. Criterio de Nombrado de Commits

El equipo utiliza la convención *Conventional Commits*:

**`<acción>: <descripción breve>`**

| Acción | Uso |
|---|---|
| `feat:` | Agregar un nuevo archivo, directorio, resolución o código |
| `fix:` | Corregir un error en un documento o archivo |
| `docs:` | Crear o modificar documentación (README, glosario, etc.) |
| `refactor:` | Reorganizar carpetas o estructura sin cambiar contenido |
| `chore:` | Mantenimiento general del repositorio |

**Ejemplos:**
- `feat: agrega resolución TP4 SCM v1.0`
- `fix: corrige tabla de ítems de configuración en README`
- `docs: actualiza criterio de línea base`

---
## 7. Criterio de Línea Base
 
Se establece una Línea Base formal cada vez que un Trabajo Práctico o entrega del TPI sea **entregado** a la cátedra, independientemente de su resultado de evaluación.
 
Este criterio garantiza que siempre quede registrado el estado del repositorio en el momento exacto de cada entrega, asegurando la trazabilidad del trabajo del grupo.
 
**Ítems que deben estar presentes en cada Línea Base:**
- Plan SCM actualizado (`SCM_PlanGestion_vX.X.pdf`)
- Resolución del TP entregado
- Consigna correspondiente al TP entregado
- Material disponible hasta la fecha de entrega
---
 
## 8. Nomenclatura de Línea Base
 
```
ISW_G10_LINEA_BASE_<VERSIONxx>_<NombreLB>
```
 
- **`ISW_G10_LINEA_BASE`**: Prefijo obligatorio.
- **`<VERSIONxx>`**: Número de versión con dos dígitos (ej: `01`, `02`).
- **`<NombreLB>`**: Nombre descriptivo en PascalCase, sin espacios ni tildes.
### Comandos Git para crear una Línea Base
 
```bash
git tag -a ISW_G10_LINEA_BASE_01_EntregaTP1 -m "Línea base 1 - Entrega TP1"
git push origin ISW_G10_LINEA_BASE_01_EntregaTP1
```
 
### Registro de Líneas Base
 
| Versión | Tag | Descripción | Ítems incluidos |
|---|---|---|---|
| 01 | `ISW_G10_LINEA_BASE_01_EntregaTP1` | Estado del repositorio al momento de entrega del TP1 | Plan SCM, TP1 |
| 02 | `ISW_G10_LINEA_BASE_02_EntregaTP2` | Estado del repositorio al momento de entrega del TP2 | Plan SCM, TP1, TP2 |
| 03 | `ISW_G10_LINEA_BASE_03_EntregaTP3` | Estado del repositorio al momento de entrega del TP3 | Plan SCM, TP1, TP2, TP3 |
| 04 | `ISW_G10_LINEA_BASE_04_EntregaTP4` | Estado del repositorio al momento de entrega del TP4 | Plan SCM, TP1, TP2, TP3, TP4 |
 
> **Nota:** la columna "Ítems incluidos" se actualiza en cada entrega con los artefactos presentes en el repositorio al momento de crear el tag.
 
---

## 9. Glosario

- **IC:** Ítem de Configuración
- **ISW:** Ingeniería y Calidad de Software
- **LB:** Línea Base
- **SCM:** Software Configuration Management (Gestión de Configuración de Software)
- **TPI:** Trabajo Práctico Integrador
- **G10:** Grupo 10
- **4K4:** Comisión del cursado