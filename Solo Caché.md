# Cómo configurar un Solo Caché.

En está página web, se realizará una configuración sobre la máquina UbuntuServer 16.04.5, para configurar y comprobar el funcionamiento de un servidor DNS De Solo Caché utilizando el servicio Webmin.

En esta práctica, tiene como objetivo enseñar al alumnado la configuración de un servidor DNS de Solo Caché y diferenciar los distintos tipos de servidores DNS.

## Configuración DNS.

1.- Vamos a Webmin y entramos en la página de configuración de BIND9.
![]()

2.- Una vez dentro de la página, vamos a "**Forwarding and Transfers**".
![]()
3.- Dónde dice "**Server to forward queries to**", borramos todas las IP que aparezcan y le daremos a "**Save**.
![]()

4.- Ahora, vamos a la página de configuración de Bind9 y escogeremos ""**Edit Config File**".
![]()

5.- A continuación, nos situamos un poco a la derecha de dónde dice "**Edit Config File**", ya que, podremos desplegar una lista, pues, escogeremos <**/etc/bind/named.conf.options**>.
![]()

6.- Vamos al final de ese fichero, y escribiremos debajo de <**dnssec-validation auto;**>:

   listen-on-v6 { any; };
    
   recursion yes;
    
   allow-recursion {localnets;};
    
   allow-transfer {none;};
   
  De tal forma, que quede así:
  ![]()
  
  Y daremos en **"Save**".
  
  7.- Por último paso, reiniciamos el servicio de Bind9 para comprobar que todo funcione y se apliquen los cambios realizados.
  []()
  
  ## Comprobar funcionamiento del DNS Solo Caché.
