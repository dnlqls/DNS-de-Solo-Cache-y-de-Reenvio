# Servidores de Solo Caché y de Reenvío.

En esta página aprenderás a cómo diferenciar y configurar un servidor DNS de Solo Caché y un servidor de Reenvío utilizando el servicio Webmin.

## Diferencias entre un servidor DNS de Solo Caché y uno de Reenvio.

### Reenvío.

Un servidor DNS de Reenvío, es un servidor "falso", ya que, no contiene ningúna zona maestra/esclava para que podamos configurar los registros como se hizo en la anterior actividad de "Instalar y configurar un servidor DNS", lo que hace este peculiar servidor es reenviar (de ahí el nombre) una solicitud DNS a otro servidor DNS y que este nos de la respuesta a la solicitud.

Como podemos apreciar en la imagen, el PC1 quiere entrar a Youtube.com pero no sabe su IP, entonces le manda la solicitud al servidor DNS, pero como es de reenvio, no tiene caché, ni zonas configuradas que se lo resuelvan, así que, se lo manda a Internet, es decir, a otro servidor DNS.

Si vemos la imagen, el otro servidor DNS, proveniente del DNS, ya sabe la IP de la solicitud de youtube.com que se la mandará a nuestro servidor DNS, para que luego, este la mande al PC1.
