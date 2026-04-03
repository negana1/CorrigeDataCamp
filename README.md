# CorrigeDataCamp

Este proyecto consiste en un script en R para la corrección automática de entregas de tareas de DataCamp.
Extrae la puntuación de cada alumno a partir de los ficheros entregados y la combina con el listado de alumnos matriculados, generando un informe final en Excel.

El proceso está automatizado y funciona independientemente del número de entregas recibidas.

---

## Descripción del proyecto

Cuando los alumnos entregan una tarea de DataCamp, se genera un fichero comprimido con la siguiente estructura por alumno:

- Un fichero `puntos.txt` con la puntuación obtenida
- Un justificante en PDF del curso completado

Este script procesa todas las entregas automáticamente, extrae la información relevante, detecta posibles errores o entregas incompletas y genera dos ficheros Excel con los resultados.

---

## Requisitos e instalación

**R** con los siguientes paquetes instalados:
```r
install.packages(c("stringr", "readxl", "writexl", "dplyr"))
```

**Ficheros necesarios** en el directorio de trabajo:

- `entregas.zip` — fichero comprimido con todas las entregas de Moodle
- `AlumnosTD25_26.xlsx` — listado de alumnos matriculados

---

## Estructura de ficheros
```
CorrigeDataCamp/
│
├── CorrigeDataCamp.Rmd       # Script principal
├── entregas.zip              # Entregas descargadas de Moodle
├── AlumnosTD25_26.xlsx       # Listado de alumnos matriculados
│
├── entregas/                 # Carpeta generada al descomprimir
│   ├── Apellidos, Nombre_ID_assignsubmission_file/
│   │   ├── puntos.txt
│   │   └── justificante.pdf
│   └── ...                   # un directorio por cada alumno
│
├── NotasRIntermedio.xlsx     # Generado: puntuaciones por alumno
└── AlumnosNotas.xlsx         # Generado: resultado final combinado
```

---


