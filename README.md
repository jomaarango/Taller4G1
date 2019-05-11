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
MAYO 11 DE 2019   


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

![Image of Yaktocat](https://github.com/jomaarango/Taller4G1/blob/Borradortaller4/Imagenes/Impormysql2.JPG)  

![Image of Yaktocat](https://github.com/jomaarango/Taller4G1/blob/Borradortaller4/Imagenes/creacionUsuarioMysql.PNG)  

**Se genera un Dashboard para la visualizacion de los eventos fallidos en tiempo real**  
