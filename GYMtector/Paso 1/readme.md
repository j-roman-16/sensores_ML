# Paso 1: Definición del Protocolo y Estrategia de Investigación

Este documento establece las bases metodológicas iniciales para la revisión sistemática de la literatura, delimitando el objeto de estudio, la estructura PICOS, la estrategia de búsqueda bibliográfica inicial y la justificación teórica y práctica del tema.

## 1. Pregunta de Investigación Principal

Formulada bajo el marco estructural **PICO / PICOS**:

> **¿Cuál es la precisión y viabilidad técnica del uso de un sensor IMU ubicado en la muñeca izquierda y procesado mediante una red convolucional con inferencia *offline* (Edge AI) para detectar y clasificar ejercicios de tren superior en adultos jóvenes ($18-35$ años) durante el entrenamiento en gimnasio para su seguimiento y feedback, en comparación con algoritmos clásicos y otras ubicaciones del sensor?**


## 2. Tabla PICOS Completa

| Criterio PICOS | Criterios de Inclusión | Criterios de Exclusión |
| :--- | :--- | :--- |
| **P – Población (Population)** | Adultos sanos (18-35 años) en contexto de *fitness*/rendimiento deportivo, realizando un set cerrado de ejercicios de tren superior en plataformas fijas (poleas, palancas o peso libre). | El estudio se centra en entornos clínicos, pacientes en rehabilitación, actividades ajenas al entrenamiento de fuerza o edades fuera del rango definido. |
| **I – Intervención (Intervention)** | Uso de sensor IMU (acelerómetro y/o giroscopio) en dispositivo *wearable* (muñeca, pecho o brazo) con cualquier modelo de clasificación (redes convolucionales, algoritmos clásicos u otras arquitecturas), tanto con inferencia *offline* embebida (Edge AI) como externa (PC, *smartphone* o nube). | Usa exclusivamente tecnologías excluidas (ej. cámaras/visión artificial u otros sensores no inerciales sin IMU *wearable*). |
| **C – Comparador (Comparator)** | Compara frente a un *baseline* o aporta resultados comparables en al menos uno de los tres ejes: algorítmico (CNN frente a modelos clásicos u otras redes), arquitectura de inferencia (embebida/Edge AI frente a nube/dispositivos externos) o ubicación física (muñeca frente a pecho o brazo). | El *paper* solo reporta resultados aislados sin compararlos ni permitir comparación con otros modelos, arquitecturas de inferencia o ubicaciones del sensor. |
| **O – Resultados (Outcomes)** | Reporta métricas cuantitativas estándar (Precisión, Recall, F1 o *Accuracy*) derivadas de una división rigurosa de *train/test* o validación cruzada sin filtración. Las métricas secundarias (consumo energético y tamaño en *flash*) se extraen cuando estén disponibles. | Solo aporta evaluaciones cualitativas ("funciona bien"), utiliza métricas *ad hoc* no estándar en la literatura o no detalla el protocolo de evaluación. |

---

## 3. Lista de 10 Términos Clave en Inglés para la Búsqueda

A continuación se listan los 10 términos descriptores primarios (incluyendo términos MeSH/DeCS equivalentes en inglés) seleccionados para configurar las ecuaciones de búsqueda en bases de datos como PubMed, Scopus y Web of Science:

1. **`Wearable sensor`**
2. **`Inertial Measurement Unit (IMU)`**
3. **`Convolutional Neural Network (CNN)`**
4. **`Edge AI / Embedded Machine Learning`**
5. **`Exercise classification / Activity recognition`**
6. **`Upper body / Upper limb`**
7. **`Resistance training / Weightlifting`**
8. **`Smartwatch / Wristband`**
9. **`Machine learning`**
10. **`Fitness tracking / Workout feedback`**

### Ejemplo de Algoritmo de Búsqueda Sugerido (Cadena Booleana):
```text
("resistance training" OR "weightlifting" OR "upper body" OR "fitness") 
AND ("exercise classification" OR "activity recognition" OR "workout tracking") 
AND ("wearable" OR "smartwatch" OR "wristband" OR "IMU" OR "inertial sensor" OR "accelerometer" OR "gyroscope") 
AND ("Convolutional Neural Network" OR "CNN" OR "Edge AI" OR "embedded machine learning") 
NOT ("camera" OR "vision-based" OR "rehabilitation" OR "clinical")
```

## 4. Justificación de la Relevancia del Tema

La monitorización automatizada del entrenamiento de fuerza es fundamental para que los usuarios de gimnasio puedan llevar un registro y recibir feedback de sus rutinas. El uso de pulseras inteligentes (IMUs en la muñeca) es la solución menos invasiva y más habitual comercialmente. Sin embargo, procesar estas señales cinemáticas localmente mediante redes convolucionales embebidas (Edge AI) supone un reto de ingeniería crítico. Resolver esta limitación permite clasificar ejercicios complejos eliminando la latencia de transmisión, reduciendo el consumo energético y garantizando la privacidad del usuario, superando las dependencias del procesamiento clásico en la nube.
