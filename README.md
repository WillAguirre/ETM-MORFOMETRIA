# 🧠 Sistema Automatizado para Medición Morfométrica en Cultivos Celulares 3D

Este proyecto presenta el desarrollo de un sistema computacional automatizado para la obtención de características morfométricas en esferoides tumorales multicelulares (ETM), utilizando técnicas de procesamiento digital de imágenes.

## 📌 Objetivo

Desarrollar un método automatizado y objetivo que permita medir características morfométricas como el área y el diámetro en imágenes de cultivos celulares 3D, específicamente ETM, reduciendo la subjetividad del analista y mejorando la precisión y eficiencia del análisis.

## 🧪 Contexto

Los ETM son modelos celulares en 3D utilizados para estudios preclínicos de fármacos y terapias. Sin embargo, la evaluación manual de su morfometría puede generar sesgos. Este sistema busca ofrecer una alternativa automática, basada en visión computacional, para estandarizar estas mediciones.

## 🛠️ Tecnologías utilizadas

- **Lenguaje:** Python  
- **Librerías:**  
  - OpenCV (procesamiento de imágenes)  
  - NumPy (manipulación de matrices y cálculos)  

## 🖼️ Flujo del algoritmo

1. **Carga de imagen** (.TIF, resolución 2560x1920, 10x)
2. **Preprocesamiento:** Filtro de mediana para reducir ruido
3. **Umbralización:** Separación del fondo
4. **Detección de bordes:** Algoritmo de Canny
5. **Operaciones morfológicas:** Dilatación y cierre
6. **Extracción de contornos:** `findContours`
7. **Cálculo de centro de masa y radios**
8. **Cálculo de área y diámetro**
9. **Validación con software ImageJ**

## 📊 Resultados

- Alta correlación con mediciones de ImageJ, especialmente en los primeros días de cultivo.
- La variabilidad en las mediciones aumenta con el tiempo, pero se mantiene en rangos aceptables.
- Reducción significativa del tiempo de análisis.

| Día | Área (Software) | Área (ImageJ) | Diámetro (Software) | Diámetro (ImageJ) |
|-----|------------------|----------------|----------------------|--------------------|
| 3   | 1108,76 µm²      | 1103,94 µm²    | 628,33 µm            | 557,08 µm          |
| 7   | 929,45 µm²       | 1103,94 µm²    | 592,99 µm            | 608,33 µm          |
| 14  | 904,32 µm²       | 985,64 µm²     | 544,35 µm            | 525,44 µm          |
| 21  | 916,28 µm²       | 978,11 µm²     | 516,52 µm            | 527,80 µm          |

## 📈 Futuras mejoras

- Mejorar la detección precisa de bordes y la eliminación de ruido
- Incluir nuevas métricas como:
  - Área del centro oscuro
  - Solidez
  - Textura

## 👨‍💻 Autores

- Wilson Stiven Aguirre Mahecha  
  Semillero de Bioinformática y Biología Computacional  
  Grupo GI2B - ITM, Medellín, Colombia  
  [Correo institucional](mailto:wilsonaguirre309506@correo.itm.edu.co)

- JA Lopera-Rodríguez  
  Investigador GI2B - ITM  

## 📚 Referencias

1. Bradski G. & Kaehler A. *Learning OpenCV*, O’Reilly, 2008.  
2. Guide to NumPy. [Ver PDF](https://ecs.wgtn.ac.nz/foswiki/pub/Support/ManualPagesAndDocumentation/numpybook.pdf)  
3. Collins TJ. *ImageJ for Microscopy*, BioTechniques, 2007. DOI: [10.2144/000112517](https://doi.org/10.2144/000112517)
