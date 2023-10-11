# Ejercicio CiberKillChain - Defensa

## Alumno

ALUMNO: Carutti, Gabriel Augusto


## Resolución

DEFENSA
=======

ACTIONS & OBJECTIVES
====================

Escenario: Máquina virtual de criptominería corriendo como un servicio en la máquina infectada.

Contramedidas: 

Recuperación - Backup

Desde la plataforma se suspende momentáneamente la cuenta del cliente y se recupera la información desde el backup diario con fecha del día anterior al evento conocido del ataque, de forma preventiva. Se asesora al cliente para que realice una recuperación desde una imagen de su sistema con fecha previa al evento de descarga e instalación del malware.

COMMAND & CONTROL
=================

Escenario: No hay actividad ni control remotos.

Contramedidas: 

-

INSTALLATION
============

Escenario: El cliente instala el archivo pensando que se trata de un parche de seguridad.

Contramedidas: 

Detectivo/Preventivo - IDS/IPS

Se suministra una aplicación a los clientes que detecte y prevenga el tráfico de datos sospechoso relacionado a la criptominería.

EXPLOITATION
============

Escenario: El cliente intenta descargar el archivo pensando que se trata de un parche de seguridad.

Contramedidas: 

Preventivo - Configuración

Se les instruye a los clientes para que tengan la opción AutoStart deshabilitada en el archivo de configuración VBoxVmService.

DELIVERY
========

Escenario: El cliente recibe el correo electrónico con la configuración maliciosa.

Contramedidas: 

Preventivo - Advertencias

Se emite un dossier preventivo de advertencias para los clientes donde se les informa que de ninguna forma la empresa intentará que sus clientes descarguen ni ingresen a un enlace por correo electrónico como tampoco enviarles actualizaciones por ese medio.

WEAPONIZATION
=============

Escenario: El atacante arma un enlace malicioso para ser utilizado con tácticas de ingeniería social.

Contramedidas: 

Disuasivo - Políticas

Se expone en las políticas de la plataforma una advertencia que diga que quienes intenten perjudicar las cuentas de los clientes, ejecutar cualquier ataque hacia los mismos o la plataforma serán llevados a la justicia en la juridiscción de la plataforma.

RECONNAISSANCE
==============

Escenario: El atacante busca recopilar direcciones de correo electrónico de los clientes expuestos en la plataforma y desde las web de las empresas de los clientes.

Contramedidas: 

Preventivo - Advertencias

En el contrato a los clientes se les recomienda fuertemente que no publiquen ni suministren las direcciones de correo electrónico que utilizan de enlace con la plataforma.

