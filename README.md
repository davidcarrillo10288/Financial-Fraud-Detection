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









             
