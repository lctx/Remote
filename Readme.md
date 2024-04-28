# RemoteBD
Este proyecto pasa por la necesidad de exponer una base de datos local a internet sin la necesidad de tener una dirección ip pública.
En conjunto, RemoteBD se compone de 3 partes diferentes:
 1 *RemoteBD: es la aplicacion local que se conecta con la base de datos
 2 RemoteBDHub: es una aplicación web que implemente un hub de signalR que sirve de medio entre la BD y el cliente
 3 RemoteBDClient: es una aplicación que se conecta a una RemoteBD
# Funciones
Esta aplicación debe poder conectarse a cualquier base de datos utilizando un orm, de preferencia EntityFramework, con las entidades mapeadas, estas deben poder serializarse y enviarse en formato json/grpc a travez de signalR. 
La sección de SignalR es lo mas importante, debe exponer absolutamente todo el esquema de la base de datos mapeada con el ORM dependiendo de los roles del usuario que solicita la información.