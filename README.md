# Coronary Heart Disease
 Clasificador acerca de potenciales pacientes portadores de una enfermedad coronaria.
# Objetivo:
	Predecir si un paciente no está en riesgo de padecer una enfermedad coronaria a 10 años.
# Variables del DataSet utilizado: 
	Demográfico: 
•	Male: masculino= 1, Femenino= 0
•	Age: edad del paciente
	Conductual:
•	Current Smoker: actualmente fuma= 1, actualmente no fuma= 0
•	Cigs Per Day: cantidad de cigarrillos que la persona fuma por día
•	BP Meds: paciente toma medicación para la presión arterial= 1, de los contrario= 0
•	Prevalent Stroke: el paciente tuvo previamente un ACV= 1, de los contrario= 0
•	Prevalent HyP: el paciente es hipertenso= 1, no es hipertenso= 0
•	Diabetes: el paciente tiene diabetes= 1, no tiene diabetes= 0
	Médico:
•	Tot Chol: nivel de colesterol total
•	Sys BP: presión arterial sistólica 
•	Dia BP: presión arterial diastólica
•	IMC: índice de masa corporal
•	Heart Rate: frecuencia cardíaca
•	Glucosa: nivel de glucosa
•	Variable a Predecir
10 year risk of coronary heart disease CHD: Si= 1, No= 0
# Estrategia utilizada para llegar al objetivo 
1° Exploración de los Datos
2° Análisis descriptivo 
3° Implementación de modelos de clasificación
# Detalles: 
De la exploración de los datos pudimos observar que:
-	Las variables no tienen outliers
-	Las clases del dataset no están balanceadas
-	La media de hombres con riesgo a contraer una enfermedad cardiovascular es mayor a la media de mujeres
-	Si el paciente tuvo anteriormente un ACV, es hipertenso o tiene diabetes es más probable que padezca una enfermedad cardiovascular en 10 años
-	Al contrario de lo que se pensaría, según el dataset, las probabilidades de contraer la enfermedad entre personas que fuman y no fuman es muy similar
# ¿Cómo se construyó el modelo?
•	Variables features:
	- Male
	- Current Smoker
	- Bpmeds
	- Prevalent Stroke
	- Prevalent HyP
	- Diabetes
•	Variable Target:
	- Ten Year CHD
•	Entrenamos el modelo con el 40% de los datos
# Conclusiones:
•	Al balancear el modelo observamos que el Accuracy en los modelos de regresión logística y Naive Bayes disminuyó. Aún así se observa que las métricas de precisión, recall y F1 mejoraron.
•	El modelo que mejoró notablemente y tuvo la mejor performance de todos los testeados fue el KNN con datos balanceados. Este modelo es el que logró una mejor precisión y sensibilidad al momento de clasificar datos positivos, como datos negativos.
•	Los hombres parecerían ser más susceptibles a padecer enfermedades cardíacas que las mujeres. 
•	Aumentando la edad, cantidad de cigarrillos fumados por día y la presión sistólica aumentaría también la probabilidad de padecer enfermedades cardíacas.
•	Se eligió el modelo KNN Balanceado para predecir ya que el accuracy es de 89%.
•	El modelo es más específico que sensitivo.
•	Todos los modelos podrían mejorar con más datos.
