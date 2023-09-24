# Ejercicio CiberKillChain - Defensa

## Alumno

ALUMNO: Carutti, Gabriel Augusto

## Enunciado

Desarrollar la defensa en función del ataque planteado en orden inverso. No es una respuesta a un incidente, hay que detectar el ataque independientemente de la etapa.

Para cada etapa elegir una sola defensa, la más importante, considerar recursos limitados.

## Resolución

DEFENSA
=======


RECONNAISSANCE
==============

T1589	 - Reúna información de identidad de la víctima	

.002	- Correos electrónicos

T1087	 - Descubrimiento de cuenta

.003	Cuenta de correo electrónico

Se buscará recopilar direcciones de correo electrónico de los clientes expuestos en la plataforma y desde las web de las empresas de los clientes.

WEAPONIZATION
=============

T1204 - Ejecución de usuario sometidos a ingeniería social.
Formas de phishing.
 
.001	- Enlace malicioso

Preparo un archivo que al ejecutarse se replique y corra en segundo plano preparando múltiples tareas a correr simultáneas en horarios nocturnos.

Preparo un correo electrónico que en el lugar de "reply" lleve el correo de la plataforma, y en "subject" un mensaje corto y conciso simulando ser la empresa proveedora que requiere una actualización de seguridad. En el "body" envío una imagen de la empresa proveedora y un enlace a una descarga del archivo para actualizar la seguridad del sistema con las instrucciones y la firma de los titulares de la empresa proveedora.

DELIVERY
========

Envío el correo electrónico a los clientes con la configuración descripta en el paso anterior.

EXPLOITATION
============

El archivo se descarga por el usuario destino permitiendo que pase a través de las medidas de seguridad del sistema pensando que se trata de un parche de seguridad.

INSTALLATION
============

El archivo se instala por el usuario pasando por el Firewall y  con privilegios de administrador pensando que se trata de un parche de seguridad.

COMMAND & CONTROL
=================

Se ejecuta en segundo plano como si fuese una actualización de seguridad.

ACTIONS & OBJECTIVES
====================

T1491 - Desfiguración	
Enviar mensajes, intimidación y reclamación de crédito mediante Desfiguración causando incomodidad al usuario.

Al lanzarse los ataques desde segundo plano en los momentos predefinidos, se comienzan a enviar datos erróneos en mensajes MQTT volcando en la base de datos información basura de sus sensores, logrando que los reportes diarios sean inservibles.
Al corromper la información provista por los dispositivos se pueden provocar pérdidas financieras en los clientes por lo que se espera tener éxito en el corto plazo con la demanda de Bitcoin's.