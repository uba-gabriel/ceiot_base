# Ejercicio CiberKillChain - Ataque

## Alumno

ALUMNO: Carutti, Gabriel Augusto


DESCRIPCIÓN DEL TRABAJO FINAL: Módulo compatible con una plataforma de desarrollo IoT similar a Node-RED o Arduino, para almacenamiento, procesamiento y accesibilidad a sus datos en la nube.
Consiste en la suscripción desde un servidor a los mensajes MQTT generados desde la plataforma y la inserción de la información en una base de datos en la nube. Incluye un panel de control web disponible para los clientes que permite la visualización ordenada de la información almacenada. 
Entre los detalles que interesan para el ataque se destaca que la identificación de los clientes de la plataforma es a través de un correo electrónico.

OBJETIVO DEL ATAQUE
===================
Minar Bitcoin's desde los servidores de los clientes de la plataforma. 

ATAQUE
======

(Mediante el catálogo de Mitre ATT&CK - Técnicas para empresas)

RECONNAISSANCE
==============

T1589	 - Reúna información de identidad de la víctima.	

.002	- [Correos electrónicos](https://attack.mitre.org/techniques/T1589/002/)

T1087	 - Descubrimiento de cuenta.

.003	- [Cuenta de correo electrónico](https://attack.mitre.org/techniques/T1087/003/)

Se buscará recopilar direcciones de correo electrónico de los clientes expuestos en la plataforma y desde las web de las empresas de los clientes que también se puedan identificar en la plataforma.

WEAPONIZATION
=============

T1204 - Ejecución de usuario sometidos a ingeniería social.
Formas de phishing.
 
.002	- [Archivo malicioso](https://attack.mitre.org/techniques/T1204/002/)

Preparo un archivo malware de tipo "trojano" que al ejecutarse configure en segundo plano un servicio de maquina virtual de criptominería programada para trabajar en horarios nocturnos.

.003	- [Crear o modificar servicio del sistema](https://attack.mitre.org/techniques/T1543/003/)

Sistema de ataque similar a Loudminer.
LoudMiner inicia automáticamente una máquina virtual Linux como un servicio al inicio si la opción AutoStart está habilitada en el archivo de configuración VBoxVmService.

Preparo un correo electrónico que en el lugar de "reply" lleve el correo de la plataforma, y en "subject" un mensaje corto y conciso simulando ser la empresa proveedora que requiere una actualización de seguridad. En el "body" envío una imagen de la empresa proveedora y un enlace a una descarga del archivo para actualizar la seguridad del sistema con las instrucciones y la firma de los titulares de la empresa proveedora.

DELIVERY
========

Envío el correo electrónico a los clientes con la configuración descripta en el paso anterior.

EXPLOITATION
============

El archivo se descarga por el cliente, permitiendo que pase a través de las medidas de seguridad del sistema pensando que se trata de un parche de seguridad.

INSTALLATION
============

El archivo se instala por el cliente con privilegios de administrador pensando que se trata de un parche de seguridad.

COMMAND & CONTROL
=================

No corresponde ya que queda corriendo en segundo plano de forma predeterminada y no se controla.

ACTIONS & OBJECTIVES
====================

T1569 - Servicios del sistema.

.002	- [Ejecución del servicio](https://attack.mitre.org/techniques/T1569/002/)

Se inicia una máquina virtual de criptominería como un servicio en la máquina infectada.

Se vuelcan los procesos de minería de Bitcoin's en memoria desde la maquina virtual corriendo como un servicio en el servidor del cliente.
Al lanzarse los ataques desde segundo plano y programados para impactar en horarios nocturnos predefinidos, se espera que no sean detectados facilmente por los clientes.