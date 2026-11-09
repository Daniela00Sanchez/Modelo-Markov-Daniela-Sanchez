# Simulación de congestión en una bodega mediante un Modelo Oculto de Markov

**Estudiante:** Daniela María Sánchez Sánchez  
**Asignatura:** Simulación  
**Lenguaje:** Python  
**Herramienta:** Google Colab

## Descripción del proyecto

En esta actividad trabajé con un Modelo Oculto de Markov (HMM) para simular cómo puede cambiar la congestión en una bodega de logística.

El objetivo fue analizar cómo las condiciones operativas pueden influir en los tiempos de registro de mercancías, utilizando probabilidades y simulaciones.

Para desarrollar el ejercicio trabajé con datos simulados, no con información real de una empresa.

## Funcionamiento del modelo

Definí dos estados ocultos:

- Operación fluida.
- Operación congestionada.

También establecí tres observaciones relacionadas con los tiempos de registro: rápido, normal y lento.

Utilicé una matriz de transición, una matriz de emisión y probabilidades iniciales para representar el funcionamiento del modelo.

## Simulaciones realizadas

Comparé tres escenarios: operación habitual, mayor congestión y menor congestión.

Para cada escenario realicé 50 repeticiones de 1.000 horas simuladas.

Los porcentajes promedio de registros lentos fueron:

| Escenario | Promedio |
|---|---:|
| Operación habitual | 23,46 % |
| Mayor congestión | 49,09 % |
| Menor congestión | 9,25 % |

Estos resultados muestran cómo cambia la frecuencia de registros lentos cuando se modifican las probabilidades de transición.

## Algoritmos utilizados

**Viterbi:** lo utilicé para estimar los estados ocultos. En una simulación de 30 horas obtuve una coincidencia del 83,33 % con los estados generados.

**Forward:** lo utilicé para calcular la probabilidad de las secuencias observadas y estudiar los cambios en las condiciones del modelo.

**Baum-Welch:** lo estudié en el marco teórico como una alternativa para estimar las matrices de probabilidad a partir de observaciones.

## Herramientas utilizadas

- Python 3.13.18
- NumPy 2.4.6
- Pandas 2.2.3
- Matplotlib 3.10.0
- Google Colab

Utilicé la semilla aleatoria 2026 para facilitar la reproducción de los experimentos.

## Cómo ejecutar el programa

1. Descargar el archivo `Sanchez_Daniela_Modelo_Markov.ipynb`.
2. Abrir Google Colab.
3. Seleccionar **Archivo → Subir cuaderno**.
4. Cargar el archivo descargado.
5. Seleccionar **Entorno de ejecución → Ejecutar todas**.
6. Revisar las tablas, las gráficas y los resultados.

## Archivos del proyecto

- `Sanchez_Daniela_Modelo_Markov.ipynb`: código de la simulación.
- `01_Frecuencia_Registros_Markov.png`: gráfica de la primera simulación.
- `02_Comparacion_Escenarios_Markov.png`: comparación de los tres escenarios.
- `03_Repeticiones_Markov.csv`: resultados de las repeticiones.
- `04_Resumen_Estadistico_Markov.csv`: resumen estadístico.
- Documento Word: explicación académica del proyecto.

## Conclusiones

Con esta actividad pude comprender mejor cómo funcionan los Modelos Ocultos de Markov y cómo se pueden utilizar para representar procesos que cambian con el tiempo.

Los resultados mostraron que, al modificar las probabilidades de congestión, también cambia la frecuencia de registros lentos.

El modelo fue desarrollado como un ejercicio académico. Para utilizarlo en una empresa real sería necesario trabajar con datos históricos y validar sus resultados.
