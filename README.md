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


             
