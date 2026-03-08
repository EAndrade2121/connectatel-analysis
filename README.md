# connectatel-analysis

## Objetivo
identificar patrones de uso, detectar comportamientos atípicos y comprender qué segmentos de clientes muestran necesidades diferenciadas, con el fin de optimizar la oferta comercial y mejorar la experiencia del usuario.

## Datasets
- `plans.csv`: los planes actuales (precio, minutos incluidos, GB incluidos, costo por extra).
- `users_latam.csv`: información de clientes: edad, ciudad, fecha de registro, plan contratado.
- `usage.csv`: el detalle de uso real: llamadas (duración) y mensajes (longitud).

## Etapas
### 1. Cargar y explorar
- En esta etapa se importaron las librerías de pandas, seaborn y matplotlib.pyplot
- Se cargaron los 3 datasets
- Se inspeccionó cada dataset con .info()

### 2. Identificar problemas de calidad de datos
- Se identificaron valores nulos, sentinels
- Se estandarizaron formatos de columnas de fechas

### 3. Limpieza de datos
- Se limpiaron datos irreales como edades con valor de -999 y se reemplazo por la median, ciudades con nombre `?` y se reemplazo por NA y fechas fueras de rango que aun no han pasado por NA.
- Se utilizaron funciones para si en un futuro hay nuevos datos que limpiar, sea mas sencillo de realizarlo y no se tenga que escribir mucho mas código

### 4. Summary statistics de uso por usuario
- Se agruparon valores de cantidad de llamadas y cantidad de mensajes de texto por usuario
- Se unieron los datasets de usuarios y uso (agrupado) para crear un solo dataset llamado user_profile

### 5. Visualización de distribuciones y outliers
- Se generaron histogramas de edades, cantidad de llamadas y cantidad de mensajes por plan para ver si existe una relación entre el tipo de plan contratado y el sesgo de la distribución
- Se identificaron outliers con boxplots para revisar si esos valores afectarían el análisis

### 6. Segmentación de clientes
- Se crearon grupos de clientes basados en su uso por llamadas y mensajes y por edad para así ver la distribución de esos grupos y ver de manera mas sencilla a que grupo se les tomará mayor importancia en la generación de estrategias

### 7. Resumen ejecutivo
- Al final se genero un informe ejecutivo con el resumen de lo realiado con los dataset, los hallazgos y las recomendaciones

## Ejecutar notebook
Para ejecutar el notebook es importante tener descargado el archivo S7 Version -Estudiante-Project-ConnectaTel.ipynb, adjunto en este repositorio, y abrirlo en  jupyter notebook, visual studio code o google colab. 

Una vez abierto, es necesario ejecutar celda por celda con el botón de play o presionar `ctrl` + `enter`
