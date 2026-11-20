# Paso 2: Búsqueda Sistemática y Registro de Resultados

Este documento sintetiza la estrategia de búsqueda bibliográfica, los resultados cuantitativos obtenidos en las bases de datos consultadas y los resultados del [archivo Excel](./Cribado.xlsx) utilizado para la gestión y cribado de los artículos.

---

## 1. Cadenas de Búsqueda

A continuación se detallan las cadenas de búsqueda sintácticamente adaptadas para cada base de datos:

### Base de Datos 1: `IEEE Xplore`
```text
("resistance training" OR "weightlifting" OR "upper body" OR "upper limb" OR "strength training") 
AND 
("exercise classification" OR "activity recognition" OR "gesture recognition") 
AND 
("wearable" OR "smartwatch" OR "IMU" OR "inertial sensor" OR "microcontroller" OR "MCU") 
AND 
("Convolutional Neural Network" OR "CNN" OR "Edge AI" OR "embedded machine learning" OR "TinyML" OR "on-device" OR "edge computing") 
NOT 
("camera" OR "vision-based" OR "rehabilitation" OR "clinical" OR "patients")
```

### Base de Datos 2: `Scopus`
```text
("resistance training" OR "gym" OR "strength training" OR "fitness" OR "weightlifting") 
AND 
("exercise classification" OR "workout tracking" OR "rep counting" OR "movement analysis") 
AND 
("wearable" OR "smartwatch" OR "wristband" OR "smart band" OR "IMU") 
AND 
("Convolutional Neural Network" OR "CNN" OR "deep learning" OR "machine learning") 
NOT 
("camera" OR "vision-based" OR "rehabilitation" OR "clinical" OR "patients")
```

---

## 2. Resultados Obtenidos

Resumen cuantitativo de los artículos obtenidos en la fase de extracción inicial:

|  Base de Datos  | Fecha de Búsqueda |             Filtros Aplicados             | N.º de Resultados |
| :-------------: | :---------------: | :---------------------------------------: | :---------------: |
| **IEEE Xplore** |  `[13/11/2026]`   | `2018-2024, Artículos de revista, Inglés` |       `24`        |
|   **Scopus**    |  `[13/11/2026]`   | `2018-2024, Artículos de revista, Inglés` |       `26`        |
|    **TOTAL**    |         —         |                     —                     |     **`50`**      |

---

## 3. Explicación del Archivo de Seguimiento ([Excel](./Cribado.xlsx))

El archivo de hoja de cálculo asociado (`Cribado.xlsx`) actúa como la matriz de sistematización para la selección y descarte de literatura según los PICOS obtenidos en el [`Paso 1`](../Paso%201/). Su estructura está diseñada para garantizar la trazabilidad y la transparencia del proceso.

### Estructura y Contenido del Excel:

Reúne la información esencial de cada artículo recuperado (Título, Autores, Año de publicación, Decisión (`Inclusión`/`Exclusión`) y Motivo de exclusión).

### Resultados Cribado (PICOS y PRISMA)

![Matriz General de Registros en Excel](./Resultados%20Cribado.png)
*Figura 1: Balance General de Cribado y Motivos de Exclusión (Códigos PRIMSMA Principal).*

![Resumen y Estadísticas en Excel](./Distribución%20de%20Exclusiones%20por%20PRISMA.png)
*Figura 2: Distribución de Exclusiones por Código PRISMA para los 42 artículos excluidos.*

---

Finalmente, los $8$ artículos seleccionados se pueden encontrar en formato PDF en [`Papers`](./Papers/).
