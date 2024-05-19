# Financial-Fraud-Detection

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/e2154d67-760c-4b6e-b973-12b155e1ab96)


* La urgencia por detectar fraudes en transacciones móviles de dinero ha llevado a una empresa del segmento Fintech a buscar soluciones innovadoras. Como científicos de datos hemos sido convocados para desarrollar un modelo de machine learning que pueda distinguir de manera precisa entre transacciones legítimas y fraudulentas.

* Presentamos un conjunto de datos sintéticos generado utilizando el simulador llamado PaySim como una aproximación a dicho problema. PaySim utiliza datos agregados del conjunto de datos privados para generar un conjunto de datos sintético que se asemeja al funcionamiento normal de las transacciones e inyecta comportamientos maliciosos para evaluar posteriormente el rendimiento de los métodos de detección de fraude.

* Los datos originales son de kaggle y tienen alrededor de 6 millones de registros, por lo que hemos utilizado una biblioteca de python llamada POLARS para mejorar nuestro análisis de preprocesamiento de los datos.

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/0e8542d0-0907-4418-ab86-86cbae61cde2)
Link Polars: https://docs.pola.rs/

             https://docs.pola.rs/docs/python/version/0.18/reference/dataframe/api/polars.DataFrame.to_dummies.html


![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/2dc2de2c-8993-46b4-8bc0-f9e8ed403f1d)
Link Kaggle: https://www.kaggle.com/datasets/ealaxi/paysim1

# IMPORTANDO LIBRERIAS Y DATASET

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/a8f97791-cedb-4b98-bdca-b141b16a3bb9)

# PREPROCESAMIENTO DE DATOS

* En este paso vamos a realizar el análisis del dataset y realizar el preprocesamiento de datos. Para esto verificaremos la presencia de datos nulos y/o faltantes, asicomo presencia de datos duplicados.

* Analizaremos que columnas son importantes para nuestros posteriores análisis y cuales descartaremos. Adicionalmente se evaluará el tratamiento de variables categóricas con el método de One-Hot encoding y creación de nuevas variables utilizando el Feature Engineering de las variables.

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/f8b99eaf-7af2-4f08-b72c-c375d5f269b2)

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/c4a76b95-e774-49d7-a600-26892e78ff83)

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/e780f06c-d35b-473d-8256-2a4e919c7e09)

* Mostramos el Nuevo Dataset:

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/bc00feea-a92d-4d92-b563-3047787e6405)

* Eliminamos Variables no Relevantes y convertimos a variables Dummies:

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/db3b0d20-7070-4e8a-93de-e8e4ff86de5a)

# ANÁLISIS EXPLORATORIO DE DATOS

* Analizando la variable Objetivo:

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/03d7ce5a-c186-4d46-ade6-552584a568ee)

* También se analizan multiples variables

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/2f23b90e-d3c3-4281-9beb-b99a386203d0)

* Se realiza el Análisis Bivariado y Multivariado para sacar conclusiones

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/68bbc1ff-7b8a-464d-85f8-36c9fb1fc576)

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/97408721-0c3a-45d2-bd86-c114d1a63102)

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/105bc9c0-161c-4240-a668-0630f1aaeefd)

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/80c7949d-c55f-49ad-b9f3-58f15d74f388)

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/ea1e7f18-5ef3-43a0-9fd9-0348472d07a6)

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/8caee353-c582-478b-9b3e-b295cc1ee90d)

* Analizando los datos solo Fraudulentos

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/cce1f088-f0b1-4ff4-96e3-6670aa08df40)

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/5e58b4fd-a285-43c5-a629-fe1c2ff60385)

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/d9589c48-d0c0-46c6-a8e0-c6bf3a6aae69)

* Matriz de Correlación

Después de analizar las variables en el Heatmap, decidimos eliminar algunas variables que consideramos que no aportaban valor y generaban multicolinealidad. Asimismo, decidimos mantener algunas que consideramos importantes por más que quizás nos aporten correlación.

De esta manera, el nuevo Heatmap resultante es el siguiente:

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/d0e32a93-dae6-4c7e-8005-4d87f61a33fd)

* Realizamos Balanceo de Datos debido a que la variable objetivo, se encuentra muy desbalanceada

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/d199e822-ff0a-46e5-ae25-debd7e51111e)

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/6fa3fe52-3703-4264-8e58-60e3ff749c26)

Despues del balanceo mejoró la correlación de variables con la variable objetivo

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/0126f03d-ccef-40e8-a95f-793fda55e996)

# CONSTRUCCIÓN DE MODELOS 

* Se evaluaron 4 modelos de clasificación
  
  > Regresión Logística
  
  > Árbol de Decisión
  
  > Random Forest
  
  > Naive Bayes

### REGRESIÓN LOGÍSTICA

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/6ea3547a-3d69-4eba-a02b-d9722abc311c)

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/81d84a69-c95f-4158-a9d4-3c801b9b4a13)

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/4c913a81-5583-4f1d-8f9d-145a39c10514)

### ÁRBOL DE DECISIÓN

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/f779d21c-f9f9-4b40-a85c-1c1b8376c320)

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/a09b8454-3b7c-4db2-9d0b-1b658d9fc16d)

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/7a2e3c35-c6dc-4a67-8318-bd23cac90446)

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/3806cbac-c256-40ee-b6ee-d018d1a7c243)

### RANDOM FOREST

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/82207228-4d0e-46c7-87e9-e5aa66e79574)

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/9ff07269-6f62-4d25-a243-0f4e51cbc4a4)

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/3804202d-ba3c-4e76-8ac7-9d2333aaebec)

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/add674c1-c337-4c22-99f9-3c7ecbe60066)

### NAIVE BAYES

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/a6fa489b-fec5-4e86-b270-1b05742b79ca)

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/aa3a0df3-5f3c-4659-a3e0-f4e59d385e76)

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/f4a2d894-0088-4882-ae34-bd8d64886239)

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/4e6dd9fa-80c0-4440-bccd-ee10a59c90a8)

# SELECCIÓN DEL MODELO

* Comparativo de las métricas de todos los modelos analizados

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/52897a85-b571-4dee-afae-78d277f19084)

![image](https://github.com/davidcarrillo10288/Financial-Fraud-Detection/assets/104275645/3a7e2fd4-aaef-4660-8e07-e89803f65865)

# CONCLUSIONES

1. <ins>Regresión Logística:</ins>
* Tiene un rendimiento moderado en términos de precisión, recall y F1-Score, con valores alrededor del 85%.
* El valor de AUC es razonablemente bueno, alrededor del 93%, lo que indica una capacidad aceptable del modelo para distinguir entre las clases.

2. <ins>Árbol de Decisión:</ins>
* Muestra un rendimiento sólido en todas las métricas, con valores alrededor del 93-98%.
* Su precisión, recall y F1-Score son bastante buenos, lo que indica una clasificación eficaz de las clases.
* El valor de AUC es alto, cercano al 98.5%, lo que sugiere una excelente capacidad de discriminación entre las clases.

3. <ins>Random Forest:</ins>
* Exhibe un rendimiento mucho mejor que el Árbol de Decisión en términos de precisión, recall y F1-Score, con valores alrededor del 95-99%.
* Su AUC es ligeramente superior al del Árbol de Decisión, indicando una mejor capacidad para distinguir entre las clases.
* Es una opción sólida y estable debido a la naturaleza de ensemble del modelo.

4. <ins>Naive Bayes:</ins>
* Tiene un rendimiento aceptable en términos de recall y AUC, con valores del 100% y alrededor del 93%, respectivamente.
* Sin embargo, su precisión y F1-Score son más bajos en comparación con los otros modelos, lo que indica una menor capacidad para clasificar correctamente las clases.

> **En conclusión, El Random forest muestra un rendimiento superior al Árbol de Decisión. Sin embargo, se puede concluir que ambos modelos muestran en términos generales un rendimiento sólido y estable, dependerá de los requerimientos que tengamos.**

> **La Regresión Logística, aunque tiene un rendimiento moderado, sigue siendo una opción viable, especialmente si se valora la interpretabilidad del modelo.**

> **El Naive Bayes muestra un rendimiento aceptable en algunas métricas, pero su precisión y F1-Score son más bajos en comparación con otros modelos.**

> **La elección entre estos modelos puede depender de las necesidades específicas del problema, como la interpretación del modelo, el tiempo de ejecución y la estabilidad del rendimiento.**

> **Es así, que los modelos Random Forest y Árbol de Decisión resultaron ser excelentes, Si bien nos decantamos por el modelo Random Forest por sus excelente métricas obtenidas y por que es un modelo estable y robusto, no podríamos descartar al Árbol de decisión, porque nos dió unas métricas aceptables, y si requerimos de mayor rapidez y tenemos menos poder de computo podría ser una opción a considerar.**





