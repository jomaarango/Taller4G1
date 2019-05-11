# Taller 4 Seguridad Base de Datos   


**Integrantes**  
Arango Garcia Jorge Mario   
Chacon Prieto Jose Alberto   
Gamez Ramirez Juan Carlos   
Sierra Nieto Joaquin   
  
**Docente**   
César Iván Rodríguez Sánchez   
  
UNIVERSIDAD PILOTO DE COLOMBIA   
FACULTAD DE INGENIERÍA DE SISTEMAS   
POSTGRADOS   
BOGOTÁ   
MAYO 10 DE 2019  
  
  
## ACTIVIDADES

* Instalar splunk en la maquina virtual.  
* Realizar busqueda de los navegadores utilizados por la ip 74.53.23.135 
  
    
Se ejecuta la consulta que especifica que la la dirección IP 74.53.23.135 que muestra los navegadores utilizados por este cliente, generamos diferentes modelos de la consulta para permitir un mayor entendimientos de los resultados que Splunk puede llegar a generar a nivel de entendimiento de los eventos.  

![Image of Yaktocat](https://github.com/jomaarango/Taller4G1/blob/Borradortaller4/Imagenes/Navegdoresutilizados2.JPG?raw=true) 

Tambien es posible visualizar los eventos con lineas de tendencia  

![Image of Yaktocat](https://github.com/jomaarango/Taller4G1/blob/Borradortaller4/Imagenes/busquedanavegadores.JPG) 

Adicionalmente se creo un dashboard para ver la cantidad de eventos por el dia de ocurrencia  

![Image of Yaktocat](https://github.com/jomaarango/Taller4G1/blob/Borradortaller4/Imagenes/dashboard.JPG) 

* Configure la BD mysql en la maquina virtual.  
    
![Image of Yaktocat](https://github.com/jomaarango/Taller4G1/blob/Borradortaller4/Imagenes/Confmysql.JPG)

Activar log MySQL de forma permanente

Para activar el log de MySQL de manera que siga activado tras reiniciar el servidor, debemos hacerlo editando el fichero de configuración de la MySQL

![Image of Yaktocat](https://github.com/jomaarango/Taller4G1/blob/Borradortaller4/Imagenes/Impormysql1.JPG)  

se reinician el servico para que se activen los logs
![Image of Yaktocat](https://github.com/jomaarango/Taller4G1/blob/Borradortaller4/Imagenes/Impormysql2.JPG)  

![Image of Yaktocat](https://github.com/jomaarango/Taller4G1/blob/Borradortaller4/Imagenes/creacionUsuarioMysql.PNG)  

![Image of Yaktocat](https://github.com/jomaarango/Taller4G1/blob/Borradortaller4/Imagenes/privilegiosUsuarioSplunk.PNG)  







![Image of Yaktocat](https://github.com/jomaarango/Taller4G1/blob/Borradortaller4/Imagenes/crear%20identidad.PNG)  

![Image of Yaktocat](https://github.com/jomaarango/Taller4G1/blob/Borradortaller4/Imagenes/identidadsplunk.PNG)  

Se crea consulta para Sourcetype employees7  

![Image of Yaktocat](https://github.com/jomaarango/Taller4G1/blob/Borradortaller4/Imagenes/consultaEventos7.PNG)  


![Image of Yaktocat](https://github.com/jomaarango/Taller4G1/blob/Borradortaller4/Imagenes/DatSumary.PNG)  


* Seleccione 2 riesgos que considere críticos detectarlos y que se puedan detectar en un SIEM.  

**Riesgo 1**  
**Modificación de Tablas horarios no permitidos**  
Dentro del escenario tomado como riesgo para la base de datos modelos se considera que un empleado realice modificaciones sobre las bases de datos en horarios no laborales, para este caso se escoge que un sabado no es comun que se realice modifcioaciones sobre las bases de datos, evidenciamos los cambios y como splunk muestra los logs realcionados a este tipo de querys especificos:  

![Image of Yaktocat](https://github.com/jomaarango/Taller4G1/blob/Borradortaller4/Imagenes/1_creacionUsuarioMysql.PNG)   

![Image of Yaktocat](https://github.com/jomaarango/Taller4G1/blob/Borradortaller4/Imagenes/2_ConsultaTabla.PNG)  

![Image of Yaktocat](https://github.com/jomaarango/Taller4G1/blob/Borradortaller4/Imagenes/3_cambiotabla.PNG)  

![Image of Yaktocat](https://github.com/jomaarango/Taller4G1/blob/Borradortaller4/Imagenes/4_cambioVerificado.PNG)  

Query configurado en Splunk para detectar los comportamientos asociados al riesgo descrito: sourcetype="mysql:generalQueryLog" Command=Query Argument="update*"  


**Riesgo 2**  
**Intentos de conexión Fallidos**  
Se considera un riesgo la evidencia de intento de conexión a la base de datos fallidos, superiores a 10 intentos fallidos consecutivos, por lo tanto se evidenciará con Splunk como se verifica el intento de conexiones fallidas sobre nuestra base de datos:  



* Configure splunk para detectar esos 2 riesgos.  
* Pruebe que splunk puede detectar esos 2 riesgos.  
* Cree un repositorio en GitHub para colocar todas las evidencias y resultados del taller.  


