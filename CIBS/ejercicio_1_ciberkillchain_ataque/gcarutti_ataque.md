ALUMNO: Carutti, Gabriel Augusto


DESCRIPCIÓN DEL TRABAJO FINAL: Módulo compatible con una plataforma de desarrollo IoT similar a Node-RED, para almacenamiento, procesamiento y accesibilidad a sus datos en la nube.
Consiste en la suscripción desde un servidor a los mensajes MQTT generados desde la plataforma y la inserción de la información en una base de datos en la nube. Incluye un sitio web disponible para los clientes que permite la visualización ordenada de la información almacenada. 
Entre los detalles que interesan para el ataque se destaca que la identificación de los dispositivos de la plataforma es a través de un correo electrónico por cada cliente.

OBJETIVO DEL ATAQUE
===================
Obtener Bitcoin's

ATAQUE
======

(Mediante el catálogo de Mitre ATT&CK - Técnicas para empresas)

RECONNAISSANCE
==============

T1589	 - Reúna información de identidad de la víctima	

.002	- Correos electrónicos

T1087	 - Descubrimiento de cuenta

.003	Cuenta de correo electrónico

Se recopilan direcciones de correo electrónico de los clientes que pueden estar expuestos de la plataforma y desde las web de las empresas de los clientes.

WEAPONIZATION
=============

T1204 - Ejecución de usuario sometidos a ingeniería social.
Formas de phishing.
 
.001	- Enlace malicioso

Preparo un archivo que al ejecutarse se replique y corra en segundo plano preparando múltiples tareas a correr simultáneas en horarios nocturnos.

DELIVERY
========

Envío el correo electrónico a los clientes colocando en el lugar de "reply" el correo de la plataforma, y en "subject" un mensaje corto y conciso simulando ser la empresa proveedora que requiere una actualización de seguridad. En el "body" envío una imagen de la empresa y un enlace a una descarga del archivo para actualizar la seguridad del sistema con las instrucciones y la firma de los titulares de la empresa.

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
Se solicitan Bitcoin's para proveer una solución.
Al corromper la información provista por los dispositivos se pueden provocar pérdidas financieras en los clientes por lo que se espera tener éxito en el corto plazo.