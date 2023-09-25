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

El atacante buscará recopilar direcciones de correo electrónico de los clientes expuestos en la plataforma y desde las web de las empresas de los clientes.

Disuasivo - Contrato

Se realiza un contrato con los clientes donde se obliga a los mismos a no publicar ni suministrar bajo ningún caso las direcciones de correo electrónico que utilizan para conectarse a la plataforma.

WEAPONIZATION
=============

El atacante buscará armar un enlace malicioso en forma de phishing.

Disuasivo - Contrato

En el mismo contrato con los clientes también se les informa que de ninguna forma la plataforma intentará contactarlos por correo electrónico ni tampoco enviarles ninguna actualización ni archivo que deban ejecutar por cualquier motivo.

DELIVERY
========

El atacante envía el correo electrónico a los clientes con la configuración maliciosa.

Disuasivo - Políticas

Se expone en las políticas de la plataforma una advertencia que diga que quienes intenten perjudicar la información provista por los clientes o ejecuten cualquier ataque hacia los mismos o la plataforma serán demandados y llevados a la justicia en la juridiscción de la plataforma.

EXPLOITATION
============

El cliente intenta descargar el archivo pensando que se trata de un parche de seguridad.

Preventivo - Antivirus

Se suministra a los clientes un programa Antivirus que detecte la descarga de archivos ejecutables potencialmente maliciosos.

INSTALLATION
============

El cliente instala el archivo pensando que se trata de un parche de seguridad.

Preventivo - Antivirus

Se suministra a los clientes un programa Antivirus que detecte la instalación de archivos que intenten abrir un shell para ejecutar scripts en segundo plano. 

COMMAND & CONTROL
=================

El cliente ejecuta el archivo y este abre un shell para correr en segundo plano.

Detectivo/Preventivo - IDS/IPS

Se suministra una aplicación a los clientes que detecte y prevenga el tráfico de datos sospechoso relacionado al protolo MQTT que no lleve las firmas adecuadas.

ACTIONS & OBJECTIVES
====================

Comienzan los ataques en segundo plano y se envían datos erróneos en mensajes MQTT, logrando que los reportes diarios sean inservibles.

Recovery - Backup

Desde la plataforma se suspende momentáneamente la cuenta del cliente y se recupera la información desde el backup diario con fecha del día anterior al evento del ataque. Se asesora al cliente para que realice una recuperación desde una imagen de su sistema con fecha previa al evento de descarga e instalación.